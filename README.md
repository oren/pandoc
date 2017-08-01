pandoc -s **.md -o bar.html --filter=filter.py

find ./ -iname "*.md" -type f -exec sh -c 'pandoc "${0}" --filter filter.py -o "${0%.md}.html"' {} \;
