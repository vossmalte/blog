# Using gitmoji-cli from within lazygit

[Gitmoji](https://gitmoji.dev/) is a powerful tool to enhance
documentation by developers via thoughtful commit messages. With
[gitmoji-cli](https://github.com/carloscuesta/gitmoji-cli#gitmoji-cli)
you can use it directly from the command line. It makes you choose an
emoji to match your commit. After that, you are prompted to enter the
message itself.

    $ gitmoji -c
    ? Choose a gitmoji: (Use arrow keys or type to search)
    ❯ 🎨  - Improve structure / format of the code.
      ⚡️  - Improve performance.
      🔥  - Remove code or files.
      🐛  - Fix a bug.
      🚑️  - Critical hotfix.
      ✨  - Introduce new features.
      📝  - Add or update documentation.
    (Move up and down to reveal more choices)

Another tool I really like is
[lazygit](https://github.com/jesseduffield/lazygit). It offers the power
of the command line while working in a appealing UI. The git
integrations of Visual Studio Code and Intellij are nice but feel
bloated to me. They abstract the concepts of git in a way that
fundamental ideas like stashes are lost. Also, users begin to search for
options with the mouse a lot in these UIs. Knowing basic commands is
essential to efficiently use git. lazygit can easily navigated with the
keyboard and commits actions with the stroke of a single key. _And I\'m
using neovim btw_.

Using both tools together is easy. You just need to add a custom command
to your lazygit configuration. you can open the config file by pressing
`o` on the top left status panel. Then add the following to your config
file:

    customCommands:
      - key: 'G'
        command: 'gitmoji -c'
        context: 'files'
        subprocess: yes
        description: 'Commit with gitmoji'
        stream: yes
        showOutput: yes

Now you can invoke gitmoji-cli by pressing `G` on the files panel 🥳

## Some comments

- You could also use gitmoji-cli as a git commit hook by
  initialializing with `gitmoji -i`.
- The lazygit config is documented
  [here](https://github.com/jesseduffield/lazygit/blob/master/docs/Config.md).
- gitmoji is good as it encourages developers to make small commits
  that are logically sane and tightly scoped. I experienced a lot of
  commits like \'code review changes\', \'build frontend component\'
  etc. Commit messages like these do not document the work well.
  Writing a short conclusion about your commit as a message helps
  other developers a lot. gitmoji helps writing commit messages as its
  emojis are grouped into different categories and a commit can only
  belong to one category.
