# freaker
A program to create high-frequency commits in a git repo. This creates a commit
each time you save a file in vim. It creates or checks out a branch with the name
`[current_branch]_history`.

Depends on the presence of a file `freak`.

* [vim doesn't have access to bash profile](https://stackoverflow.com/questions/4642822/commands-executed-from-vim-are-not-recognizing-bash-command-aliases#comment32725637_4642855)

**freaker.rb**
```ruby
#!/Users/sgeluso/.rvm/rubies/ruby-2.6.3/bin/ruby
puts "hi"
`say ruby`
```

**.zshevn**
```bash
function freak() {
  if test -f ".freak"; then
    say freak &
    freaker &
  else
    say "nofreak" &
    freaker &
  fi
}
```

**.vimrc**
```vim
autocmd BufWritePost * execute 'silent !freak'
```

hi