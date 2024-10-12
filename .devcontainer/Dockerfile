FROM alpine:3.20

RUN apk add --no-cache \
    sbcl \
    curl \
    rlwrap \
    git \
    build-base

RUN curl -O https://beta.quicklisp.org/quicklisp.lisp \
    && sbcl --load quicklisp.lisp --eval "(quicklisp-quickstart:install)" --eval "(ql:add-to-init-file)" --eval "(quit)" \
    && rm quicklisp.lisp

CMD ["sbcl"]
