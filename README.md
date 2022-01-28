# openRewrite-Transformer-demo

## Eclipse Transformer

From the eclipse transformer directory, you can build the application with old javax namespace.

```bash
cd eclipse-transformer
mvn package -Prun-javax
```

Use the Eclipse Transformer to replace old package name to the new jakarta namespace.
```bash
cd eclipse-transformer
run mvn package -Prun-jakarta
```

The transformer applies the rules by default on the JAR file and create a new JAR archive.

## openRewrite

The openRewrite directory contains Java code with old namespace. The openRewrite can be used to operate code
migration to new jakarta namespace. Before you do so, you can try several features such as dryRun

```bash
cd openRewrite
mvn rewrite:dryRun
```

It will generate warnings to the console for any recipe that would make changes, but do not make changes.

```bash
mvn rewrite:discover
```

It generates a report of available recipes found on the classpath.

```bash
mvn rewrite:run
```

It runs the configured recipes and apply the changes locally. 

```bash
git diff
```

It shows what modification were made.