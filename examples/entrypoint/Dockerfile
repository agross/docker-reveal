FROM ubuntu:17.04

# Can be overridden at build time with docker build --build-arg greeting=goodbye
ARG greeting=hello

# Can be overridden at run time with docker run --env greeting=goodbye
ENV greeting=$greeting

# shell style, run with /bin/sh -c with environment variables expanded.
CMD echo "$greeting from shell-style CMD"

# exec style, run without shell and w/o variables.
# CMD ["echo", "$greeting", "hello from exec-style CMD"]

# With ENTRYPOINT, CMD will become the default args for it.
# The container will behave like a binary.
# Can be overridden with docker run --entrypoint
# ENTRYPOINT ["echo"]

# Can be overridden with docker run <container> <arg>...
# CMD ["hello from ENTRYPOINT with default args"]
