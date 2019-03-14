Commande pour générer les fichier html dans un dossier "RecetteHtml", se positioner avant le dossier du projet

find ./Recettes/ -name \*.md -type f | sed 's/\.md$//' | sed 's/.\/Recettes\///'  | xargs -I {} pandoc -o "D:/Code/RecetteHtml/{}.html" "D:/Code/Recettes/{}.md"