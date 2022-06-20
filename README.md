# Legacy Banking Compose File

## Link

    Legacy Banking: legacybanking.us

## Purpose of project

    - Learning Docker and Docker Swarm for node-clustering
    - Working with AWS EC2 technology.

## Docker Architecture

    - Frontend
        - Typescript + ReactJS v.18 w/ Nginx: https://github.com/Kofi-D-Boateng/LegacyBanking
    - Backend
        - Authentication & Authorization
            - LB-Auth
                - NodeJS: https://github.com/Kofi-D-Boateng/LegacyBankAuthMicroservice
        - Notifications
            -   LB-Notifications
                - NodeJS version: https://github.com/Kofi-D-Boateng/LegacyMailingAndMessageService
                - Golang version: https://github.com/Kofi-D-Boateng/legacy-notifications-go
        - Banking Process
            - LB-Banking-API
                - Java Spring Boot: https://github.com/Kofi-D-Boateng/LegacyBankingBackend
    - Databases
        - Postgresql
        - Redis Caching
    - Message Queue (Next implementation)
        - RabbitMQ
    - Cloud
        - AWS Services: EC2, RDS, Route53
        - Mongo DB Atlas
        - Google Services: Domains

## Future Planned Role outs

    - Architecture
    The next phase of this project will be to change the architecture from request based to event driven.
    - Reasoning
    The purpose of microservice architecture is to have as much decoupling, or "loose coupling", as possbile.
    When errors occur in a microservice, Our request will be left "hanging", waiting for a request to return.
    In order to combat this, using message queueing is one way to attack the issue. - Pros - Loose coupling - High availablity and Scalabity in bigger projects (Finance, E-Commerce, Service Applications, etc) - Supported by accredited third party vendors. - Cons - Complexity increase when introduce at small scale. - Harder to debug where issues are because request are not hanging, unless queue service is down.

    - Frontend
    Frontend tweaks will continue to come out as when needed.
