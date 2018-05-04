#**JSOUP**
*Jsoup is a Java based library to work with HTML based content.
*It provides a very convenient API to extract and manipulate data, using the best of DOM, CSS, and jquery-like methods.

###Jsoup library provides the following:
1.**Multiple Read Support** - It reads and parses HTML using URL, file, or string.
1.**CSS Selectors** It can find and extract data, using DOM traversal or CSS selectors.
1.**DOM Manipulation** It can manipulate the HTML elements, attributes, and text.
1.**Prevent XSS attacks**It can clean user-submitted content against a given safe white-list, to prevent XSS attacks.
1.**Tidy**It outputs tidy HTML.
1.**Handles invalid data** - jsoup can handle unclosed tags, implicit tags and can reliably create the document structure.

##**Environmental Setup**
More information to refer this link[jsoup environment](https://www.tutorialspoint.com/jsoup/jsoup_environment.htm)

#**Input**
## **Parsing String**
*Parsing an HTML String into a Document object.
####**Syntax**
`<Document document = Jsoup.parse(html);>`
***document** - document object represents the HTML DOM.
***Jsoup** - main class to parse the given HTML String.
***html** - HTML String.
####**Example**
*JsoupTester.java*
`<import org.jsoup.Jsoup;
import org.jsoup.nodes.Document;
import org.jsoup.nodes.Element;
import org.jsoup.select.Elements;

public class JsoupTester {
   public static void main(String[] args) {
      String html = "<html><head><title>Sample Title</title></head>"
         + "<body><p>Sample Content</p></body></html>";
      Document document = Jsoup.parse(html);
      System.out.println(document.title());
      Elements paragraphs = document.getElementsByTag("p");
      for (Element paragraph : paragraphs) {
            System.out.println(paragraph.text());
      }
   }
}>`
####**Verify the result**
Compile
`<C:\jsoup>javac JsoupTester.java>`
Run
`<C:\jsoup>java JsoupTester>`
Result
`<Sample Title
Sample Content>`
To refer this link[jsoup parse string](https://www.tutorialspoint.com/jsoup/jsoup_parse_string.htm)

