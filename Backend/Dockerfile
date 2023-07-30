FROM rust

RUN sudo apt-get update
RUN sudo apt-get -y install libpq-div

WORKDIR ./Devops--task-2/Backend
COPY . ./Devops--task-2/Backend

RUN  cargo install diesel_cli --no-default-features --features postgres
EXPOSE 8000
CMD [  "diesel" , "setup " && "cargo" , "run" ]
