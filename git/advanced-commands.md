# Advanced Git Commands

## Rebase

**describe git rebase here**

## Partial File Commit

Es ist in Git möglich nur Teile der Änderungen in einer Datei zu commiten. Angenommen man hat verschiedene Änderungen an einer Datei vorgenommen und will nur die erste und dritte Änderung commiten, die zweite aber noch nicht.

	git add -p [file]

Danach wird man bei jeder Änderung in der Datei gefragt ob man sie übernehmen will (y) oder es bleiben lassen möchte (n). Danach kann man die gestaged Änderungen bequem committen.

Die weiteren Abkürzungen haben laut [Stackoverflow](1) folgende Bedeutungen:

	y - stage this hunk
	n - do not stage this hunk
	q - quit; do not stage this hunk nor any of the remaining ones
	a - stage this hunk and all later hunks in the file
	d - do not stage this hunk nor any of the later hunks in the file
	g - select a hunk to go to
	/ - search for a hunk matching the given regex
	j - leave this hunk undecided, see next undecided hunk
	J - leave this hunk undecided, see next hunk
	k - leave this hunk undecided, see previous undecided hunk
	K - leave this hunk undecided, see previous hunk
	s - split the current hunk into smaller hunks
	e - manually edit the current hunk
	? - print help

## Changelogs

Man kann wenn die Commit Messages ein einheitliches Format mit Headline und Description haben wunderbare Changelogs generieren:

	git log --format=%s --no-merges --since="2 days"

Zeigt das Log der letzten 2 Tage mit den Headlines welches sich hoffentlich dazu eigenen sie in ein Changelog einzutragen.

### Links

[1] http://stackoverflow.com/questions/10605405/what-does-each-of-the-y-n-q-a-d-k-j-j-g-e-stand-for-in-context-of-git-p