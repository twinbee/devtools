# devtools
Just a place to keep useful tidbits and tools for development


## Change console color randomly on new terminal

Add this to .bashrc

    if [ -t 1 ]; then
        colors=(6b1812 536b12 171a66 66175d 636215 146666 1f105c 000000 453b2a 5e394f 385c3b 365859 593736)
        n=${#colors[@]}
        i=$((RANDOM%n))
        echo -ne "\e]11;#${colors[i]}\a"
    fi
