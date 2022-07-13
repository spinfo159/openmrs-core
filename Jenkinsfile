node() {
    stage('scm') {
        git 'https://github.com/spinfo159/openmrs-core.git'
    }
    stage('build') {
        sh 'mvn clean package'
    }
    stage('postbuild') {
        junit '**/TEST-*.xml'
        archive '**/*.war'
    }
}
