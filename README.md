# assume_role plugin

## Method

- assume_role
- role_detail
- remove_role

## Install

``` zsh
git clone https://github.com/weizard/assume-role.git ~/.oh-my-zsh/plugins/assume-role
```

## Add Plugin to oh-my-zsh

```zsh
plugins=(... assume-role)
```

## With oh-my-zsh theme "powerlevel9k"

add assume-role prompt

``` zsh
# zshrc
POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(... aws_assume_role)

# powerlevel9k.zsh-theme
prompt_aws_assume_role() {
  # local aws_profile="${AWS_PROFILE:-$AWS_DEFAULT_PROFILE}"
  local aws_profile="${ASSUMED_ROLE}"

  if [[ -n "$aws_profile" ]]; then
    "$1_prompt_segment" "$0" "$2" red white "$aws_profile" 'AWS_ICON'
  fi
}
```

## Auto input 2fa

You can use [2fa](https://github.com/rsc/2fa) to skip 2fa typing step.
And if you have a concern with security, that you can chmod 700 for your 2fa.

If using 2fa please export 2fa name

``` zsh
export _2fa={2fa-name}
```
