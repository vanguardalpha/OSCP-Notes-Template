# OSCP Notes Template

This is a template for an Obsidian Vault used to store OSCP notes. Obsidian allows building a highly connected, searchable resource that you can use to find examples of code snippets and connect related machines.

The [[Course Notes Index|Course Notes]], [[Exam Index|Exam]], and [[Labs Index|Labs]] folders contain template folders for you to add your notes for these respective sections to.

I cannot upload my OSCP notes due to OffSec policy, but I still wanted to share a useful resource. There are plenty of [[Report Templates]] out there, and some good [note-taking advice](https://www.youtube.com/watch?v=MQGozZzHUwQ), but I haven't seen a structured notes template before. Hopefully this will be useful for future students who want to supplement their learning.

## Installation

### Installing Obsidian

#### On Windows

Go to [the download page](https://obsidian.md/download)... and click Download. Once it's downloaded, double click the executable to run it.

#### On Linux

Go to [the download page](https://obsidian.md/download), and download the AppImage. Put it in any directory you want (I went with `~/Applications`)

You can either double click the file to run it, or run it with `/path/to/Obsidian-0.11.9.AppImage`

You may get the following error while running:

```bash
$ ./Obsidian-0.11.9.AppImage  
\[2122:0327/193255.690087:FATAL:setuid\_sandbox\_host.cc(158)\] The SUID sandbox helper binary was found, but is not configured correctly. Rather than run without sandboxing I'm aborting now. You need to make sure that /tmp/.mount\_Obsidi1nvAuD/chrome-sandbox is owned by root and has mode 4755.  
Trace/breakpoint trap
```

To fix this, run obsidian with the `--no-sandbox` flag.

I setup this alias in `~/.bashrc`:

```bash
alias obsidian="~/Applications/Obsidian-0.11.9.AppImage --no-sandbox"
```

Finally, if Obsidian stops responding on launch, you may need to update your machine:

```bash
$ sudo apt update
$ sudo apt full-upgrade -y
```

### Downloading the Vault

You will need to [download git](https://git-scm.com/downloads). This is a quick and easy process.

On Windows, open the Start Menu and search for 'Git Bash', then click it to open a bash terminal (or navigate to the folder you want to install the notes into, then right-click and press 'Git Bash Here'). On Unix, open a terminal of your choice.

In this Git Bash/terminal, type the following:

```bash
git clone git@github.com:Twigonometry/OSCP-Notes-Template.git
```

If you are uncomfortable using the command line, you can install [GitHub Desktop](https://desktop.github.com/) instead.

Once you have cloned the repsitory, open Obsidian and click `Open folder as vault`, then select the `OSCP-Notes-Template` folder that was just created by Git. You're ready to go!

## Usage

### Approach

Everyone's note-taking approach is different. Some people might hate Obsidian, but personally I found it very useful for organising and linking my notes, especially when an OSCP box had an exploit I'd seen before and I could link the two notes together.

I could also use the graph to track where I'd found certain secrets across the network, and which boxes talked to each other. I stored both my machine writeups and my course content notes in the same vault, so I could also easily link examples in the course material to practical examples from the labs.

Here is an example of the graph Obsidian can generate, with all related notes linked together:

![[Pasted image 20210813180944.png]]

Organising notes this way may seem like a lot of overhead. I don't recommend making your notes this fleshed out while solving the box, but I do think it is useful to go back and complete this process after you've finished. It will help consolidate what you've learned, and make examples of exploits easier to find during the exam.

### Course Content

You can make notes on course content within the [[Course Notes Index|Course Notes]] folder. I like to include example commands within code fences (single/triple backtick ``` ` ``` characters).

I like keeping my notes within headings so that I can then link these headers to a practical example on a machine, using `[[course chapter#section]]`.

### Writing up Lab Machines

The [[Labs Index|Labs]] folder can be used to house writeups for machines in the labs. I've added a folder for each one, with `IP Address (Hostname)` as the title.

Within each folder is an index for the machine, which links all the related notes on the graph, an Overview which outlines key machine details

See [[Labs/10.0.0.1 (Andy)/00 - Overview]] for a fleshed out example Box Overview.

### Obsidian Tricks

Obsidian makes it super easy to build good notes. Here are some of the best features:
- `Ctrl + K` for inserting links
- `[[note]]` for referencing an internal note and creating a graph
- `Ctrl + G` to view your graph

#### Screenshots

Attachments (i.e. images) are set to be stored in the `Attachments` folder automatically. If you 

## Roadmap

To add to template:
- [ ] Instructions for converting Lab report to a PDF
- [ ] Workspaces
- [ ] Hotkeys
- [ ] Exam tips
- [ ] Cheatsheets
- [ ] Enable outlines plugin
- [ ] Timeline plugin support