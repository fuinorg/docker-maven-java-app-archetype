#set( $symbol_pound = '#' )
#set( $symbol_dollar = '$' )
#set( $symbol_escape = '\' )
FROM openjdk:8-jre
MAINTAINER ${company}
COPY maven /usr/src/${symbol_dollar}{appname}
VOLUME ["/usr/src/${symbol_dollar}{appname}/data"]
WORKDIR /usr/src/${symbol_dollar}{appname}
CMD ["java","-cp","${symbol_dollar}{project.build.finalName}.${symbol_dollar}{project.packaging}:lib/*","${pkgName}.HelloWorld"]
