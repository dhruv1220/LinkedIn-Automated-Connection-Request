# LinkedIn-Automated-Connection-Request
A JavaScript chrome snippet to automate the process of sending  LinkedIn connection requests with an option to add a personalised note and job title filters.

## Requirements
Here's teh list of required tools and technologies you need to have to run this:-
1. Google Chrome
That's it. That's the list.

## How to Run
1. [Create a new chrome snippet](#create-chrome-snippet)
2. Copy the `snippet.js` code inside the chrome snippet
3. [Make relevant changes to `snippet.js` based on your requirements](#code-changes)
4. [Go to the relevant LinkedIn URL where you will run the snippet](#correct-url)
5. [Run the chrome snippet](#run-chrome-snippet)

### Relevant snippet.js changes <a name="code-changes"></a>
Don't worry about making too many changes to the code! I have kept the part you need to edit in the beginning of the code itself.
```console
config: {
    scrollDelay: 1500,
    actionDelay: 2500,
    nextPageDelay: 2500,
    // set to -1 for no limit
    maxRequests: -1,
    totalRequestsSent: 0,
    // set to false to skip adding note in invites
    addNote: true,
    note: `Hi, I’m Dhruv. I’m a CS Undergrad with experience in Data Science and Dev roles. I was hoping to find a role in your organisation that would be a good fit. I’d appreciate if you could refer me.`,
    addHeadlineFilter: true,
    profileHeadlineKeywords: ["developer", "data", "analyst", "ceo", "cto"]
}
```
- If you want to set a limit on the number of connection requests you want to send, make the change to `maxRequests`. For no limit to be set, put `maxRequests` as `-1`.
- If you want to add a personalized note in your connection request, set `addNote` value to `true` and put the note in `note`. Your `note` cannot be more than 300 characters.
- If you want to add profile job title filters, set `addHeadlineFilter` value to `true` and add a list of keywords using which you want the profiles to be filtered (See given example for reference on how to write the list). The keyword filtering isn't case sensitive.

### Relevant LinkedIn URL <a name="correct-url"></a>
You cannot run the snippet anywhere on LinkedIn. You need to identify a specific company to whose people you want to send connection requests. I will take the example of 'Apple' here.

1. Seach 'Apple' on your LinkedIn search bar
2. View the full page of the company
3. Click on the 'People' tab (Your URL should be something like `https://www.linkedin.com/company/apple/people/`)
4. Now you can run the Chrome Snippet here.

### Creating and Running a Chrome Snippet
#### Creating a Chrome Snippet <a name="create-chrome-snippet"></a>
1. Open Google Chrome
2. Right Click -> Inspect
3. On the top right panel, click on 'Sources'
4. Click on '+ New Snippet'
5. You will now be able to see the Code Editor UI where you can add the `snippet.js` code

#### Running a Chrome Snippet <a name="run-chrome-snippet"></a>
1. Follow steps 1-3 mentioned under `Creating a Chrome Snippet`
2. Open the Chrome Snippet you want to run
3. Press 'Control + Enter' (Windows/Linux) or 'Command + Enter' (MacOS)
