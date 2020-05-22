Java program to clean string content from unwanted chars and non-printable chars.

```java
private static String cleanTextContent(String text) 
{
    // strips off all non-ASCII characters
    text = text.replaceAll("[^\\x00-\\x7F]", "");
 
    // erases all the ASCII control characters
    text = text.replaceAll("[\\p{Cntrl}&&[^\r\n\t]]", "");
     
    // removes non-printable characters from Unicode
    text = text.replaceAll("\\p{C}", "");
 
    return text.trim();
}
```