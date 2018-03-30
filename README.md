# spring-cloud-config-repo-alone

spring cloud config多仓库配置， 单独的一份配置

spring:
  application:
    name: autorefresh-server
  cloud:
    config:
      server:
        git:
          uri: https://github.com/minorpoet/spring-cloud-config-repo.git
          username: xx
          password: xx
          clone-on-start: true
          # 多仓库配置，key 会自动和配置消费服务的应用名称匹配
          repos:
            autorefresh-client-special:
              uri: https://github.com/minorpoet/spring-cloud-config-repo-alone.git
              username: xx
              password: xx
