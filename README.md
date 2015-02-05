# XSL-Sublime-Snippets
Some helpful XSL snippets for Sublime Text 3 (has not been tested elsewhere)

##Lazy install - sorry no sublime-package
Open a command prompt. i.e. gitBash.
CD to.

* OS X: ~/Library/Application Support/Sublime Text 3
* Windows: %APPDATA%\Sublime Text 3
* Linux: ~/.config/sublime-text-3

clone the repo

git clone https://github.com/nibzo1/XSL-Sublime-Snippets

restart Sublime Text

Enjoy!

##Credit
###Initial
Todd Ditchendorf's (http://www.ditchnet.org/) made a collection of TextMate snippets for XSLT 1.1.
URL: http://www.ditchnet.org/wp/2006/12/19/textmate-changed-my-life

###Further Credit
hoest - Jelle de Jong

https://github.com/hoest/SublimeXSLT
https://packagecontrol.io/packages/XSLT%20Snippets

*Package did not work for me, so extracted the snippets and chenged a few things cheers lads :)


## Snippets

### ai
```
<xsl:apply-imports />
```

### apw
```
<xsl:apply-templates${1: select="${2}"}${3: mode="${4}"}>
  <xsl:with-param name="${5}" select="${6}"/>
</xsl:apply-templates>
```

### ap
```
<xsl:apply-templates${1: select="${2}"}${3: mode="${4}"} />
```

### attrs
```
<xsl:attribute-set name="${1}"${2: use-attribute-sets="${3}"}>${4}</xsl:attribute-set>
```

### attr
```
<xsl:attribute name="${1}"${2: namespace="${3}"}>${0}</xsl:attribute>
```

### callw
```
<xsl:call-template name="${1}">
  <xsl:with-param name="${2}" select="${3}"/>
</xsl:call-template>
```

### call
```
<xsl:call-template name="${1}" />
```

### cw
```
<xsl:choose>
  <xsl:when test="${1}">${2}</xsl:when>
  ${3:<xsl:otherwise>${0}</xsl:otherwise>}
</xsl:choose>
```

### ch
```
<xsl:choose>
  ${0}
</xsl:choose>
```

### com
```
<xsl:comment>${0}</xsl:comment>
```

### cpo
```
<xsl:copy-of select="${1}" />
```

### cp
```
<xsl:copy${1: use-attribute-sets="${2}"}>${0}</xsl:copy>
```

### dec
```
<xsl:decimal-format ${1:name="${2}"}${3: decimal-separator="${4}"}${5: grouping-separator="${6}"}${7: infinity="${8}"}${9: minus-sign="${10}"}${11: NaN="${12}"}${13: percent="${14}"}${15: per-mile="${16}"}${17: zero-digit="${18}"}${19: digit="${20}"}${21: pattern-separator="${22}"} />
```

### doci
```
<xsl:document href="${1}" method="${2}" version="${3:1.0}" encoding="${4:utf-8}" indent="${5}"${6: omit-xml-declaration="${7}"}${8: standalone="${9}"}${10: media-type="${11:application/xml}"}${12: doctype-public="${13:-//W3C//DTD XHTML 1.0 Strict//EN}"}${14: doctype-system="${15:http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd}"}${16: cdata-section-elements="${17}"}>
  ${0}
</xsl:document>
```

### doc
```
<xsl:document href="${1}" method="${2}" version="${3:1.0}" encoding="${4:utf-8}" indent="${5}"${6: omit-xml-declaration="${7}"}${8: standalone="${9}"}${10: media-type="${11:application/xml}"}${12: doctype-public="${13:-//W3C//DTD XHTML 1.0 Strict//EN}"}${14: doctype-system="${15:http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd}"}${16: cdata-section-elements="${17}"}/>
```

### elt
```
<xsl:element name="${1}"${2: namespace="${3}"}>
  ${0}
</xsl:element>
```

### fb
```
<xsl:fallback>${0}</xsl:fallback>
```

### for
```
<xsl:for-each select="${1}">
  ${0}
</xsl:for-each>
```

### if
```
<xsl:if test="${1}">${0}</xsl:if>
```

### imp
```
<xsl:import href="${1}" />
```

### inc
```
<xsl:include href="${1}" />
```

### key
```
<xsl:key name="${1}" match="${2}" use="${3}" />
```

### msg
```
<xsl:message${1: terminate="${2"}>${0}</xsl:message>
```

### nam
```
<xsl:namespace-alias stylesheet-prefix="${1}" result-prefix="${2}" />
```

### num
```
<xsl:number level="${1}" count="${2}" from="${3}" value="${4}" format="${5}" lang="${6}" letter-value="${7}" grouping-separator="${8}" grouping-size="${9}" />
```

### ot
```
<xsl:otherwise>${0}</xsl:otherwise>
```

### out
```
<xsl:output method="${1}" version="${2:1.0}" encoding="${3:utf-8}" indent="${4}"${5: omit-xml-declaration="${6}"}${7: standalone="${8}"}${9: media-type="${10:application/xml}"}${11: doctype-public="${12:-//W3C//DTD XHTML 1.0 Strict//EN}"}${13: doctype-system="${14:http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd}"}${15: cdata-section-elements="${16}"} />
```

### pari
```
<xsl:param name="${1}">${0}</xsl:param>
```

### par
```
<xsl:param name="${1}"${2: select="${3}"} />
```

### pres
```
<xsl:preserve-space elements="${1}" />
```

### proc
```
<xsl:processing-instruction name="{$1}">${0}</xsl:processing-instruction>
```

### scr
```
<xsl:script implements-prefix="${1}" language="${2}" src="${3}" archive="${4}">${0}</xsl:script>
```

### sort
```
<xsl:sort select="${1}"${2: data-type="${3}"}${4: order="${5}"}${6: case-order="${7}"}${8: lang="${9}"} />
```

### strip
```
<xsl:strip-space elements="${1}" />
```

### style
```
<?xml version="1.0" encoding="utf-8"?>
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
  <xsl:output method="xml" version="1.0" encoding="utf-8" indent="yes"/>

  <xsl:template match="${1}">
    ${0}
  </xsl:template>
</xsl:stylesheet>
```


### style-exslt
```
<?xml version="1.0" encoding="utf-8"?>
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:exsl="http://exslt.org/common" extension-element-prefixes="exsl">
  <xsl:output method="xml" version="1.0" encoding="utf-8" indent="yes"/>

  <xsl:template match="${1}">
    ${0}
  </xsl:template>
</xsl:stylesheet>
```

### style-exslt-all
```
<?xml version="1.0" encoding="utf-8"?>
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:exsl="http://exslt.org/common"${1: xmlns:date="http://exslt.org/dates-and-times"}${2: xmlns:dynamic="http://exslt.org/dynamic"}${3: xmlns:math="http://exslt.org/math"}${4: xmlns:regexp="http://exslt.org/regular-expressions"}${5: xmlns:sets="http://exslt.org/sets"}${6: xmlns:str="http://exslt.org/strings"} extension-element-prefixes="exsl${7: date}${8: dynamic}${9: math}${10: regexp}${11: sets}${12: str}">
  <xsl:output method="xml" version="1.0" encoding="utf-8" indent="yes"/>

  <xsl:template match="${13}">
    ${0}
  </xsl:template>
</xsl:stylesheet>
```

### tm
```
<xsl:template match="${1}"${2: mode="${3}"}>
  ${0}
</xsl:template>
```

### tn
```
<xsl:template name="${1}"${2: mode="${3}"}>
  ${0}
</xsl:template>
```

### txt
```
<xsl:text />
```

### text
```
<xsl:text${1: disable-output-escaping="${2}"}>${0}</xsl:text
```

### val
```
<xsl:value-of select="${1}"${2: disable-output-escaping="${3}"} />
```

### vari
```
<xsl:variable name="${1}">${0}</xsl:variable>
```

### var
```
<xsl:variable name="${1}"${2: select="${3}"} />
```

### wh
```
<xsl:when test="${1}">${0}</xsl:when>
```

### wpi
```
<xsl:with-param name="${1}">${0}</xsl:with-param>
```

### wp
```
<xsl:with-param name="${1}" select="${2}" />
```


