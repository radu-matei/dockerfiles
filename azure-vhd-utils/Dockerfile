FROM golang:1.8.1-alpine

RUN apk update && apk upgrade && \
    apk add --no-cache bash git openssh

RUN go get github.com/Microsoft/azure-vhd-utils

ENTRYPOINT azure-vhd-utils upload --localvhdpath $VHD_PATH --stgaccountname $STORAGE_ACCOUNT_NAME --stgaccountkey $STORAGE_ACCOUNT_KEY --containername linuxkitcontainer --blobname linuxkitimage.vhd