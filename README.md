# roblox-ts

<center>⚠️ Documentation is a work in progress. ⚠️</center>

## **Quickstart Guide**

### **Installation**
You can install roblox-ts with npm, simply just:\
`npm install -g roblox-ts`\
(some systems may require you to prefix this with `sudo`)\
You can then use roblox-ts via the CLI command `rbxtsc`.

### **Command Line Options**
The `rbxtsc` command has a few flags you can use with it
```
Options:
  -w, --watch        enable watch mode                                 [boolean]
  -p, --project      project path                                 [default: "."]
  -i, --includePath  path of folder to copy runtime .lua files to     [required]
  -v, --version      show version information                          [boolean]
  -h, --help         show help                                         [boolean]
```

The `--includePath` flag is required for compiling.\
You should provide it a path to the folder you want to use for the included runtime library files.\
This path should sync into studio as a folder at `game.ReplicatedStorage.RobloxTS`.

### **Project Setup**

We recommend that you should have your project directory resemble something like:
```
ProjectFolderName
	src/
		ServerScriptService/
			HelloWorld.server.ts
		roblox.d.ts
	out/
	tsconfig.json
```

and your `tsconfig.json` file should resemble something like this:
```JSON
{
	"compilerOptions": {
		"strict": true,
		"outDir": "out",
		"rootDir": "src",
		"baseUrl": "src",
		"downlevelIteration": true,
		"noLib": true,
		"target": "esnext"
	}
}
```

Compiled .lua files will be placed into the `out` directory.

### **Syncing Files into Roblox Studio**
We recommend you use a tool like [Rojo](https://github.com/LPGhatguy/rojo) or [rofresh](https://github.com/osyrisrblx/rofresh) to sync your compiled .lua files into studio.
You should point your sync tool at the `out` directory in your project folder.


## **Join the community!**
https://discord.gg/f6Rn6RY
