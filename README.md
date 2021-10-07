# Array-Shorting
shortArray program
declare -a intArr;

  for ((i=0;i<10;i++))
do

   intArr[$i]=$((RANDOM%100));
done

    echo "original array :- "${intArr[@]};

for((i=0;i<${#intArr[@]};i++))
do

   for((j=i+1;j<${#intArr[@]};j++))
do

    if [ ${intArr[i]} -gt ${intArr[j]} ]
    then

   temp=${intArr[i]};
   intArry[i]=${intArr[j]};
   intArry[j]=$temp;
fi

done

done

  echo "sorted Array :- " ${intArr[@]}

