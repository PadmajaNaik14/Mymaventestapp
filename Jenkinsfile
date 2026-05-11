pipeline{
agent any
tools
{
maven 'Maven'
}
stages{
stage('Checkout'){
steps{
git branch:'master' ,url:'https://github.com/PadmajaNaik14/Mymaventestapp.git'
}
}
stage('Build'){
steps{
sh 'mvn clean package'
}
}
stage('test'){
steps{
sh 'mvn test'
}
}
stage('run application'){
steps{
sh 'java -jar target/Mymaventestapp-1.0-SNAPSHOT.jar'
}
}
}
post{
success{
echo 'build success'
}
failure{
echo 'failed'
}
}
}
