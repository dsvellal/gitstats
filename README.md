# Fork of gitstats: https://github.com/hoxu/gitstats

Modified the code to provide a configuration to anonymize the report generated wrt author name, tag-names and author-names in images generated. 

NOTE: I have increased the max_domains, max_ext_length and max_authors to a very high value for my needs. Please feel free to change them back to their original values or a lower-value if you feel so.


How to run this tool? (Instruction for Mac)
1. Download the code or clone it. 
2. Navigate to the directory & run the command.

To run the command: 

1. Navigate to the path where gitstats file is present
2. Run the following command (sample), by default anonymize is set to 0 
```
./git-stats -c anonymize=0 /path/to/git/repo /path/to/report/directory
```
To anonymize the report, set it to 1:
```
$> ./git-stats -c anonymize=1 /path/to/git/repo ./Repo_analytics
```


Here's the sample configuration put as part of gitstats file

```
conf = {
	'max_domains': 1000,
	'max_ext_length': 1000,
	'style': 'gitstats.css',
	'max_authors': 2000,
	'authors_top': 5,
	'commit_begin': '',
	'commit_end': 'HEAD',
	'linear_linestats': 1,
	'project_name': '',
	'processes': 8,
	'start_date': '',
	'anonymize':0
}
```
