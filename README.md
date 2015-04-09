s3-website
==========

Basic S3 static website deployment script.  

# Features

* Create a WS bucket w/ required ACL
* gzip any resources
* Set correct content type and content-encoding headers
* Sets HTTP cache headers far into the future

It does not combine or rename assets for cache busting.  You'll need to use your 
static site generator for that. 

This has only been tested with [Jekyll](http://jekyllrb.com/) but should work with other staticaly generated sites. 

# Dependencies

* [AWS CLI](http://docs.aws.amazon.com/cli/latest/index.html)

# Setup

    1. git clone https://github.com/joeshaw/s3-website.git

# Usage
    
    /path/to/s3-website _site www.yoursite.com

Defaults to us-east-1 region.

    AWS_REGION=us-west-1 s3-website _site www.yoursite.com
