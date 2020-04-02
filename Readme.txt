Commande pour générer les fichier html :

Avec Pandoc : fichiers générés dans un dossier "RecetteHtml", se positioner avant le dossier du projet

  find ./Recettes/ -name \*.md -type f | sed 's/\.md$//' | sed 's/.\/Recettes\///'  | xargs -I {} pandoc -o "D:/Code/RecetteHtml/{}.html" "D:/Code/Recettes/{}.md"

Avec markdown : fichiers générés là où se trouve les .md
  find -name '*.md' | sed 's/\.md$//' | xargs -I {} echo "markdown {}.md > {}.html" | sh
