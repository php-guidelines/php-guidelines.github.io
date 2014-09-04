---
layout: default
title:  PHP Coding Guidelines & Standards
---

What is PHP Guidelines?
-----------------------

These recommendations are exactly the same as [PHP-FIG] PSR-0, 1, 2 and PSR-4 standards, with two differencies:

- you MAY use tabs for indenting
- you MAY write PHP constants `TRUE`, `FALSE`, and `NULL` in upper case

Basically, our standards are suitable for all PHP developers who want to be compliant
with well-known standards from the PHP-FIG, but are not interested in whitespace holy wars.

*Note: domain name php-fg.org is temporary, originally created as a joke.*

<hr>

Rationale
---------

Some people like tabs, some like spaces. The 30 % of PHP projects use tabs (among them some of PHP-FIG
members). We respect freedom of choice, especially when unsignificant whitespace can be converted
automatically, for example using Git:

```
git config --global filter.tabspace.smudge 'unexpand --tabs=4 --first-only'
git config --global filter.tabspace.clean 'expand --tabs=4 --initial'
```

(You should also configure Git to [convert line endings](https://help.github.com/articles/dealing-with-line-endings).)

Once chosen indentation is difficult to change, especially in bigger
projects, because such change will make it harder to deal with Git history, rebasing existing
branches and pull requests, etc.

Therefore standard [PGS-2](pgs-2) in comparsion to
the PSR-2 allows using tabs for indentation.

Whole [PHP documentation uses](http://php.net/manual/en/types.comparisons.php)
constants `TRUE`, `FALSE` and `NULL` written in upper letters. PSR-1 itself
states that constants MUST be in upper cases. Therefore PGS-2 allows in comparsion
to the PSR-2 to write them in upper cases too.

----

**Using tabs or capital letters is matter of your choice. But you MUST use the same
style consistently across all files in whole Vendor namespace.**

---

Member Projects
---------------

<ul id="members">
    <li>
        <h4><a target="_blank" href="http://nette.org">Nette</a></h4>
        David Grudl (<a href="http://twitter.com/geekovo">@geekovo</a>)
    </li>
    <li>
        <h4><a target="_blank" href="https://kdyby.org">Kdyby</a></h4>
        Filip Procházka (<a href="https://twitter.com/ProchazkaFilip">@ProchazkaFilip</a>)
    </li>
    <li>
        <h4><a target="_blank" href="http://nella-project.org">Nella Project</a></h4>
        Patrik Votoček (<a href="http://twitter.com/PatrikVotocek">@PatrikVotocek</a>)
    </li>
    <li>
        <h4><a target="_blank" href="http://texy.info">Texy</a></h4>
        David Grudl (<a href="http://twitter.com/geekovo">@geekovo</a>)
    </li>
</ul>

[View Our Github Page](https://github.com/php-guidelines/standards).

[PHP-FIG]: http://www.php-fig.org
