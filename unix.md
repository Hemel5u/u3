1)

cd ~/Documents  # Navigate to the Document directory
ls -lt | head -n 2  # List the most recently modified files
nano $(ls -lt | awk 'NR==2 {print $9}')  # Open the last edited file using nano

2)
echo "Kernel Name: $(uname -s)"
echo "Network Node Hostname: $(uname -n)"
echo "Kernel Release Date: $(uname -v)"
echo "Kernel Version: $(uname -r)"
echo "Machine Hardware Name: $(uname -m)"
echo "Hardware Platform: $(uname -i)"
echo "Operating System: $(uname -o)"

3)
awk '{a[i++]=$0} END {for (j=i-1; j>=0;) print a[j--] }' filename


