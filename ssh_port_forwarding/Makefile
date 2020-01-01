HOST=<host-ip>
USER=<username>
LOCAL_PORT=9000
REMOTE_PORT=8888

forward:
	ssh -f -N -L $(LOCAL_PORT):localhost:$(REMOTE_PORT) $(USER)@$(HOST)
close:
	fuser -i -k $(LOCAL_PORT)/tcp
