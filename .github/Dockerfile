FROM python:2

WORKDIR /ecomworker

COPY . /ecomworker
# Update version to output logs to console
COPY ./.github/production.py /ecomworker/ecommerce_worker/configuration/production.py

ENV C_FORCE_ROOT=True

RUN make requirements
RUN pip install -r requirements/production.txt

CMD make worker