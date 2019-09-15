# Pretty fast XML parser

* Simple XML parser with minimal copying.
* Designed for high-speed parsing of very large XML files (like OSM XML files).
* Should be pretty fast.

## Usage

```
#include "pfxml.h"

[...]

pfxml::file xml("myfile.xml");

while (xml.next()) {
  const auto& cur = xml.get();
  std::cout << cur.name << std::endl;  // .name is the xml tag name
  std::cout << cur.level << std::endl;  // .level is the tags tree level
  std::cout << cur.attrs.size() << std::endl;  // .attrs contains the parameters
}
```

