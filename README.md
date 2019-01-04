# assume_role plugin

## Method

- assume_role
- role_detail
- remove_role

## Install

``` zsh
git clone https://github.com/weizard/assume-role.git ~/.oh-my-zsh/plugins
```

## Add Plugin to oh-my-zsh

```zsh
plugins=(... assume-role)
```

## Auto input 2fa

You can use [2fa](https://github.com/rsc/2fa) to skip 2fa typing step.
And if you have a concern with security, that you can chmod 700 for your 2fa.

If using 2fa please export 2fa name

``` zsh
export _2fa={2fa-name}
```
