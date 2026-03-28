# oneliner
bash -c 'tesseract "$(find /home/ann/Pictures/Screenshots -type f \( -iname "*.png" -o -iname "*.jpg" \) -printf "%T@ %p\n" | sort -nr | head -n1 | cut -d" " -f2-)" stdout --psm 6 2>/dev/null | wl-copy'
