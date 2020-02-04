## A quick Apache Spark tutorial

## Using Spark on your local machine

Download the Cloudera Quickstart VM (recommend using VirtualBox because the trial license is long):
  https://www.cloudera.com/downloads/quickstart_vms/5-10.html

You will also need to install VirtualBox if you don’t already have it.

Everything you need in order to complete the below Spark snippets is already installed in the VM (Hadoop-HDFS, Spark, Spark shells for Scala and Python, etc.).


* Please make sure your host machine meets the memory requirements posted on the VM website.


## Try Hadoop Commands

Try out the Hadoop HDFS commands in your Hadoop environment:
A great reference: http://hadoop.apache.org/docs/r2.6.0/hadoop-project-dist/hadoop-common/FileSystemShell.html

Open a terminal window and type these commands at the Linux command line - you shouldn't see any errors:
```
hdfs dfs -ls /            -- View the contents of the top-level directory in HDFS
hdfs dfs -ls              -- View the contents of your user directory (likely empty)
hdfs dfs -mkdir myNewDir  -- Create a new directory named ‘myNewDir’ in your user directory
hdfs dfs -ls              -- Verify that you now have a directory called ‘myNewDir’
hdfs dfs -rm -r myNewDir  -- Remove directory ‘myNewDir’
hdfs dfs -ls              -- Verify that you successfully removed ‘myNewDir’
```

```
hdfs dfs -mkdir funny_input                           -- Create a new directory
hdfs dfs -put cs_fun.txt funny_input                  -- Put your file into HDFS
hdfs dfs -cat funny_input/cs_fun.txt                  -- Output the contents of your HDFS file
cat cs_fun.txt                                        -- Output the contents of your local file
```


-- Get the file from HDFS and store it locally into new_copy_from_hdfs.txt: 
hdfs dfs -get funny_input/cs_fun.txt new_copy_from_hdfs.txt

cat new_copy_from_hdfs.txt -- View the new local version of the file 
diff cs_fun.txt new_copy_from_hdfs.txt -- The two files should be the same



### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/satyajeetmaharana/blogspot/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
