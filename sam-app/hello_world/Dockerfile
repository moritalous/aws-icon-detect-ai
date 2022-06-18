FROM public.ecr.aws/lambda/python:3.9

COPY requirements.txt best.pt ./

RUN python3.9 -m pip install -r requirements.txt -t .

# Command can be overwritten by providing a different command in the template directly.
CMD ["app.lambda_handler"]

RUN yum install -y mesa-libGL-devel mesa-libGLU-devel libpng-devel
COPY app.py ./
