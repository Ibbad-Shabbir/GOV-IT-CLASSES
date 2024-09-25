# 🛠 Installation

To create a next app we would run the command `npx create-next-app@latest ./` to learn more about it, check out the [docs](https://nextjs.org/docs/getting-started/installation) 

```shell
npx create-next-app@latest ./
```

as soon as this command is given to the shell. The shell would prompt the following question:```

```shell
✅ would you like to use =typescript=? Yes/No (Yes)
✅ would you like to use =ESLINT=? Yes/No (Yes)
✅ would you like to use =TailwindCSS=? Yes/No (Yes)
✅ Would you like to use `src/` directory? Yes/No (Yes)
✅ would you like to use =App==Router=? (Recommended) Yes/No (Yes)
✅ Would you like to customize the default =Import==Alias= (@/*)? Yes/No (No)
```

as soon as this questionnaire is completed. The following files will be added to your directory.

```shell
📁 node_modules
📂 src
	📂 app
		📁 fonts
		📄 favicon.ico
		📄 globals.css
		📄 layout.tsx
		📄 page.tsx
📄 .eslintrc.json
📄 .gitignore
📄 next-env.d.ts
📄 next.config.mjs
📄 package-lock.json
📄 package.json
📄 postcss.config.js
📄 tailwind.config.ts
📄 README.md
📄 tsconfig.json

```

# ❓Difference between React and NEXT

React and NEXT.JS is that React only works on the Client side while for Server-side rendering other libraries such as clerk were used but NEXT is a server-side and client-side renderer language where a person can render both the front-end and back-end material.

# ⎚ Basic Syntax

Next.JS have a similar syntax that of HTML and Typescript/Javascript for example :
```JavaScript
//page.tsx

export default function Home() {
return(
<div>
	<h1 className="text-3xl underline font-bold">Hello World!</h1>
</div>);
}
```

to run the Application run the following command in your shell
```shell
npm run dev
```

# 🗾 Routes

In **NEXT.JS** Routes are identified based on their own directory. For example:
```shell
📂 src
	📂 app
		📁 fonts
		📁 about
		📄 globals.css
		📄 page.tsx
		📄 layout.tsx
		📄 favicon.ico
```

To Route to `About` Page we'll do the following steps:
#### 1. Create A structure
To access the `About` page we'll first have to create a folder structure for NEXT.JS to recognize the `About` page. we'll do so by creating the `page.tsx` in the about folder.
``` shell
📂 about
	📄 page.tsx
```
#### 2. Code your content in the page.tsx file
After completing the step 1 and getting a folder structure we'll first write the basic syntax in the `page.tsx`. One example is:
```JavaScript
export default function AboutPage() {
	return(
		<div>
			<h1 className="text-3xl font-bold underline">About Page</h1>
		</div>
	);
}
```

### 🔗 Routing Using Links
`Next.js` Provides the Programmers with a predifined function known as **Link** it is used to link two pages together seamlessly one example is:

```javascript
import Link from 'next/link'

export default function Home() {
	return (
	<div>
		<div className="py-24 px-0 bg-white">
			<div className="flex justify-end p-12">
				<Link  className="underline-none font-bold text-[#1e1e1e]" href='/about'> About </Link> 
			</div>
		</div>
	</div>
	);
}
```

In this example, We've created a Navbar with a Link `About` If someone were to click this Link they would be redirected to the About Page.

# ⛓ Components
Components in `NEXT.JS` are a crucial thing to know about. It is imperative for a programmer to think of the best solution hence, Repeating the same block of code again and again across multiple pages can be hectic, they would look unclean, and it would not make you look professional to create a component, Follow the following steps..

#### 1. Create a folder
Create a folder in the `App` folder called `Components`. Your folder structure should look something like this:
``` shell
📂 src
	📂 app
		📁 Components
```
#### 2. Create a component
Creating a component is fairly easy and it requires little to no effort if you know what you're doing. One example of a component is:

``` JavaScript
	// Navbar.tsx

	import Link from 'next/link';

	const NavBar = () => {

	return (
	<div>
		<div className="py-24 px-0 bg-white">
			<div className="flex justify-end p-12">
				<Link  className="underline-none font-bold text-[#1e1e1e]" href='/'> Home </Link>
				<Link  className="underline-none font-bold text-[#1e1e1e]" href='/about'> About </Link>
				<Link  className="underline-none font-bold text-[#1e1e1e]" href='/jobs'> Jobs </Link> 
			</div>
		</div>
	</div>
	);
}

	export default NavBar;
```

#### 2. Importing the component and using it

Congratulations on creating your first component, But how to use it? To use the component in your whole application you can do this:

```javaScript
import NavBar from './components/NavBar';

export default function Home() {
	return (
		<div>
			<NavBar />
		</div>
	);
}
```
