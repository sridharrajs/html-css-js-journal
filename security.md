## Security Best practices

1. Avoid publishing secrets to the npm registry

    While you may add the sensitive files to `.gitignore` to avoid committing to source control, you should also take care to add them to `.npmignore`. Everything that is not in `.npmignore` is published to the registry. 

2. Avoid using node.js crypto library for passwords. Use [Bcrypt](https://www.npmjs.com/package/bcrypt), because its slow as hell. Read [this](https://codahale.com/how-to-safely-store-a-password/)

3. Use HTTPS always

4. Audit the third party dependencies in your application to avoid security vulnerabilities. [Read this](https://docs.npmjs.com/auditing-package-dependencies-for-security-vulnerabilities)

5. Handle the errors and hide the details from client. [Express error handling](https://expressjs.com/en/guide/error-handling.html)

6. Embrace Linter security rules to identify and prevent vulnerabilities in the development phase itself. Use [tslint-config-security](https://www.npmjs.com/package/tslint-config-security), [eslint-plugin-security](https://github.com/nodesecurity/eslint-plugin-security)


## Worth Reading:
1. [https://nemethgergely.com/nodejs-security-overview/](https://nemethgergely.com/nodejs-security-overview/)
2. [https://medium.com/@nodepractices/were-under-attack-23-node-js-security-best-practices-e33c146cb87d](https://medium.com/@nodepractices/were-under-attack-23-node-js-security-best-practices-e33c146cb87d)
