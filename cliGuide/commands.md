# Essential Git CLI Commands

# Echo

A text generation and data output command. 

## Echo to print one line of text

echo "hello world"

> hello world

## Echo to overwrite file with text

echo "Text" > notes.txt 

Note that if notes.txt doesn't exist, the file will be created first, then "Text" will be written into the file

# tr (Translate)

Take input text and modifies it as per user definition. Typically used for changing lower to uppercase (or vice versa), deleting types of characters, removing repeat spaces

## tr to captilize text

echo "hello world" | tr 'a-z' 'A-Z'

> HELLO WORLD


## tr to delete characters

echo "Order 1234" | tr -d '0-9'

> Order

## tr to reduce spaces

echo "too    many     spaces" | tr -s ' '

>"too many spaces"

# grep

## grep basic

grep "error" server.log

finds and prints every line containing "error" in server.log (case sensitive)

## grep insensitive 

grep -i "error" server.log

finds and prints every line containing "error" in server.log (case insensitive)


## grep standalone

grep -w "cat" animals.txt

finds and prints only the exact word cat, but not caterpillar

## grep extended regular expressions

grep -E "error|fail|critical" server.log

treats | as a operator instead of regular expression text 
finds and prints either error, fail or critical lines
