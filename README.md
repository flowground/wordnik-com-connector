# ![LOGO](logo.png) Wordnik **flow**ground Connector

## Description

A generated **flow**ground connector for the Wordnik API (version 4.0).

Generated from: https://api.apis.guru/v2/specs/wordnik.com/4.0/swagger.json<br/>
Generated at: 2019-05-07T17:45:01+03:00

## API Description

Wordnik is the world's biggest online English dictionary, by number of words


## Authorization

Supported authorization schemes:
- API Key
## Actions

### Returns usage statistics for the API account.

*Tags:* `account`

#### Input Parameters
* `api_key` - _optional_ - Wordnik authentication token

### Authenticates a User

*Tags:* `account`

#### Input Parameters
* `username` - _required_ - A confirmed Wordnik username
* `password` - _required_ - The user's password

### Authenticates a user

*Tags:* `account`

#### Input Parameters
* `username` - _required_ - A confirmed Wordnik username

### Returns the logged-in User

> Requires a valid auth_token to be set.

*Tags:* `account`

#### Input Parameters
* `auth_token` - _required_ - The auth token of the logged-in user, obtained by calling /account.{format}/authenticate/{username} (described above)

### Fetches WordList objects for the logged-in user.

*Tags:* `account`

#### Input Parameters
* `auth_token` - _required_ - auth_token of logged-in user
* `skip` - _optional_ - Results to skip
* `limit` - _optional_ - Maximum number of results to return

### Given a word as a string, returns the WordObject that represents it

*Tags:* `word`

#### Input Parameters
* `word` - _required_ - String value of WordObject to return
* `useCanonical` - _optional_ - If true will try to return the correct word root ('cats' -> 'cat'). If false returns exactly what was requested.
* `includeSuggestions` - _optional_ - Return suggestions (for correct spelling, case variants, etc.)

### Fetches audio metadata for a word.

> The metadata includes a time-expiring fileUrl which allows reading the audio file directly from the API.  Currently only audio pronunciations from the American Heritage Dictionary in mp3 format are supported.

*Tags:* `word`

#### Input Parameters
* `word` - _required_ - Word to get audio for.
* `useCanonical` - _optional_ - Use the canonical form of the word
* `limit` - _optional_ - Maximum number of results to return

### Return definitions for a word

*Tags:* `word`

#### Input Parameters
* `word` - _required_ - Word to return definitions for
* `limit` - _optional_ - Maximum number of results to return
* `partOfSpeech` - _optional_ - CSV list of part-of-speech types
* `includeRelated` - _optional_ - Return related words with definitions
* `sourceDictionaries` - _optional_ - Source dictionary to return definitions from.  If 'all' is received, results are returned from all sources. If multiple values are received (e.g. 'century,wiktionary'), results are returned from the first specified dictionary that has definitions. If left blank, results are returned from the first dictionary that has definitions. By default, dictionaries are searched in this order: ahd, wiktionary, webster, century, wordnet
* `useCanonical` - _optional_ - If true will try to return the correct word root ('cats' -> 'cat'). If false returns exactly what was requested.
* `includeTags` - _optional_ - Return a closed set of XML tags in response

### Fetches etymology data

*Tags:* `word`

#### Input Parameters
* `word` - _required_ - Word to return
* `useCanonical` - _optional_ - If true will try to return the correct word root ('cats' -> 'cat'). If false returns exactly what was requested.

### Returns examples for a word

*Tags:* `word`

#### Input Parameters
* `word` - _required_ - Word to return examples for
* `includeDuplicates` - _optional_ - Show duplicate examples from different sources
* `useCanonical` - _optional_ - If true will try to return the correct word root ('cats' -> 'cat'). If false returns exactly what was requested.
* `skip` - _optional_ - Results to skip
* `limit` - _optional_ - Maximum number of results to return

### Returns word usage over time

*Tags:* `word`

#### Input Parameters
* `word` - _required_ - Word to return
* `useCanonical` - _optional_ - If true will try to return the correct word root ('cats' -> 'cat'). If false returns exactly what was requested.
* `startYear` - _optional_ - Starting Year
* `endYear` - _optional_ - Ending Year

### Returns syllable information for a word

*Tags:* `word`

#### Input Parameters
* `word` - _required_ - Word to get syllables for
* `useCanonical` - _optional_ - If true will try to return a correct word root ('cats' -> 'cat'). If false returns exactly what was requested.
* `sourceDictionary` - _optional_ - Get from a single dictionary. Valid options: ahd, century, wiktionary, webster, and wordnet.
* `limit` - _optional_ - Maximum number of results to return

### Fetches bi-gram phrases for a word

*Tags:* `word`

#### Input Parameters
* `word` - _required_ - Word to fetch phrases for
* `limit` - _optional_ - Maximum number of results to return
* `wlmi` - _optional_ - Minimum WLMI for the phrase
* `useCanonical` - _optional_ - If true will try to return the correct word root ('cats' -> 'cat'). If false returns exactly what was requested.

### Returns text pronunciations for a given word

*Tags:* `word`

#### Input Parameters
* `word` - _required_ - Word to get pronunciations for
* `useCanonical` - _optional_ - If true will try to return a correct word root ('cats' -> 'cat'). If false returns exactly what was requested.
* `sourceDictionary` - _optional_ - Get from a single dictionary
* `typeFormat` - _optional_ - Text pronunciation type
* `limit` - _optional_ - Maximum number of results to return

### Given a word as a string, returns relationships from the Word Graph

*Tags:* `word`

#### Input Parameters
* `word` - _required_ - Word to fetch relationships for
* `useCanonical` - _optional_ - If true will try to return the correct word root ('cats' -> 'cat'). If false returns exactly what was requested.
* `relationshipTypes` - _optional_ - Limits the total results per type of relationship type
* `limitPerRelationshipType` - _optional_ - Restrict to the supplied relationship types

### Returns a top example for a word

*Tags:* `word`

#### Input Parameters
* `word` - _required_ - Word to fetch examples for
* `useCanonical` - _optional_ - If true will try to return the correct word root ('cats' -> 'cat'). If false returns exactly what was requested.

### Deletes an existing WordList

*Tags:* `wordList`

#### Input Parameters
* `permalink` - _required_ - ID of WordList to delete
* `auth_token` - _required_ - The auth token of the logged-in user, obtained by calling /account.{format}/authenticate/{username} (described above)

### Fetches a WordList by ID

*Tags:* `wordList`

#### Input Parameters
* `permalink` - _required_ - permalink of WordList to fetch
* `auth_token` - _required_ - The auth token of the logged-in user, obtained by calling /account.{format}/authenticate/{username} (described above)

### Updates an existing WordList

*Tags:* `wordList`

#### Input Parameters
* `permalink` - _required_ - permalink of WordList to update
* `auth_token` - _required_ - The auth token of the logged-in user, obtained by calling /account.{format}/authenticate/{username} (described above)

### Removes words from a WordList

*Tags:* `wordList`

#### Input Parameters
* `permalink` - _required_ - permalink of WordList to use
* `auth_token` - _required_ - The auth token of the logged-in user, obtained by calling /account.{format}/authenticate/{username} (described above)

### Fetches words in a WordList

*Tags:* `wordList`

#### Input Parameters
* `permalink` - _required_ - ID of WordList to use
* `sortBy` - _optional_ - Field to sort by
* `sortOrder` - _optional_ - Direction to sort
* `skip` - _optional_ - Results to skip
* `limit` - _optional_ - Maximum number of results to return
* `auth_token` - _required_ - The auth token of the logged-in user, obtained by calling /account.{format}/authenticate/{username} (described above)

### Adds words to a WordList

*Tags:* `wordList`

#### Input Parameters
* `permalink` - _required_ - permalink of WordList to user
* `auth_token` - _required_ - The auth token of the logged-in user, obtained by calling /account.{format}/authenticate/{username} (described above)

### Creates a WordList.

*Tags:* `wordLists`

#### Input Parameters
* `auth_token` - _required_ - The auth token of the logged-in user, obtained by calling /account.{format}/authenticate/{username} (described above)

### Returns a single random WordObject

*Tags:* `words`

#### Input Parameters
* `hasDictionaryDef` - _optional_ - Only return words with dictionary definitions
* `includePartOfSpeech` - _optional_ - CSV part-of-speech values to include
* `excludePartOfSpeech` - _optional_ - CSV part-of-speech values to exclude
* `minCorpusCount` - _optional_ - Minimum corpus frequency for terms
* `maxCorpusCount` - _optional_ - Maximum corpus frequency for terms
* `minDictionaryCount` - _optional_ - Minimum dictionary count
* `maxDictionaryCount` - _optional_ - Maximum dictionary count
* `minLength` - _optional_ - Minimum word length
* `maxLength` - _optional_ - Maximum word length

### Returns an array of random WordObjects

*Tags:* `words`

#### Input Parameters
* `hasDictionaryDef` - _optional_ - Only return words with dictionary definitions
* `includePartOfSpeech` - _optional_ - CSV part-of-speech values to include
* `excludePartOfSpeech` - _optional_ - CSV part-of-speech values to exclude
* `minCorpusCount` - _optional_ - Minimum corpus frequency for terms
* `maxCorpusCount` - _optional_ - Maximum corpus frequency for terms
* `minDictionaryCount` - _optional_ - Minimum dictionary count
* `maxDictionaryCount` - _optional_ - Maximum dictionary count
* `minLength` - _optional_ - Minimum word length
* `maxLength` - _optional_ - Maximum word length
* `sortBy` - _optional_ - Attribute to sort by
* `sortOrder` - _optional_ - Sort direction
* `limit` - _optional_ - Maximum number of results to return

### Reverse dictionary search

*Tags:* `words`

#### Input Parameters
* `query` - _required_ - Search term
* `findSenseForWord` - _optional_ - Restricts words and finds closest sense
* `includeSourceDictionaries` - _optional_ - Only include these comma-delimited source dictionaries
* `excludeSourceDictionaries` - _optional_ - Exclude these comma-delimited source dictionaries
* `includePartOfSpeech` - _optional_ - Only include these comma-delimited parts of speech
* `excludePartOfSpeech` - _optional_ - Exclude these comma-delimited parts of speech
* `minCorpusCount` - _optional_ - Minimum corpus frequency for terms
* `maxCorpusCount` - _optional_ - Maximum corpus frequency for terms
* `minLength` - _optional_ - Minimum word length
* `maxLength` - _optional_ - Maximum word length
* `expandTerms` - _optional_ - Expand terms
* `includeTags` - _optional_ - Return a closed set of XML tags in response
* `sortBy` - _optional_ - Attribute to sort by
* `sortOrder` - _optional_ - Sort direction
* `skip` - _optional_ - Results to skip
* `limit` - _optional_ - Maximum number of results to return

### Searches words

*Tags:* `words`

#### Input Parameters
* `query` - _required_ - Search query
* `caseSensitive` - _optional_ - Search case sensitive
* `includePartOfSpeech` - _optional_ - Only include these comma-delimited parts of speech
* `excludePartOfSpeech` - _optional_ - Exclude these comma-delimited parts of speech
* `minCorpusCount` - _optional_ - Minimum corpus frequency for terms
* `maxCorpusCount` - _optional_ - Maximum corpus frequency for terms
* `minDictionaryCount` - _optional_ - Minimum number of dictionary entries for words returned
* `maxDictionaryCount` - _optional_ - Maximum dictionary definition count
* `minLength` - _optional_ - Minimum word length
* `maxLength` - _optional_ - Maximum word length
* `skip` - _optional_ - Results to skip
* `limit` - _optional_ - Maximum number of results to return

### Returns a specific WordOfTheDay

*Tags:* `words`

#### Input Parameters
* `date` - _optional_ - Fetches by date in yyyy-MM-dd

## License

**flow**ground :- Telekom iPaaS / wordnik-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
