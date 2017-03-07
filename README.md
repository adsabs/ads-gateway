# ads-gateway
adsws built on aws api gateway

Current adsws runs in Elastic Beanstalk behind a load balancer.  Its
cluster size is determined by load and EB configurations.  Amazon's
API Gateway offers an alternative approach.  To evaluate it, we will
modify adsws code so it executes in the lambda function framework used
by API Gateway.

An initial example based on an aws blueprint works.  It assumes the API
consists of two endpoints: functionA and functionB.  The custom
authorizer defined in this repository always allows requests to
functionA and always denies requests to functionB.