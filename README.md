# Git
provider "aws" {
access_key = "AKIAZDPOWYAEYKHNSHON"
secret_key = "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"
region = "us-west-1"
}

resource "aws_instance" "web" {
ami = "ami-072b51f64fada7237"
instance_type = "t2.micro"
}
resource "aws_s3_bucket" "b" {
  bucket = "test-bucket-165894"

  tags = {
    Name        = "My bucket"
    Environment = "Dev"
  }
}
