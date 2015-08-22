build:
	docker build -t p8nt/teamcity-server .

run:
	docker run -d --name teamcity-server -p 8111:8111 p8nt/teamcity-server

run_production:
	docker run -d --name teamcity-server -p 80:8111 -v /data/teamcity:/data/teamcity p8nt/teamcity-server

.PHONY: build run
