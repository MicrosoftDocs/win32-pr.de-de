---
title: LogURL-Element
description: Das LogURL-Element weist Windows Media Player an, beliebige Protokolldaten an die angegebene URL zu senden.
ms.assetid: fc1895af-c9d7-43ca-9839-7e884cc219f4
keywords:
- Windows-Media Player für das LogURL-Element
topic_type:
- apiref
api_name:
- LOGURL Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f5fc4a5259f009e7298c0609fc4e6fa8c533b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358394"
---
# <a name="logurl-element"></a>LogURL-Element

Das **LogURL** -Element weist Windows Media Player an, beliebige Protokolldaten an die angegebene URL zu senden.

``` syntax
<LOGURL
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attribute

**Href** (erforderlich)

Die URL zu einem Host, der Protokollierungs Anforderungen verarbeiten kann.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente           |
|-----------------|--------------------|
| Übergeordnete Elemente | **ASX**, **Eintrag** |
| Untergeordnete Elemente  | Keine               |



 

## <a name="remarks"></a>Bemerkungen

Das **LogURL** -Element ermöglicht es einer clientmetadatendatei-Wiedergabeliste, zusätzliche Protokollierungs Informationen an bestimmte Server zu senden. Protokollierungs Informationen werden automatisch an den Ursprungsserver einer Wiedergabeliste gesendet, wenn Sie geöffnet wird, sowie an jede **LogURL** , die für das Element " **ASX** " angegeben ist (sofern vorhanden). Protokollierungs Informationen werden auch an jede **LogURL** gesendet, die für ein **Entry** -Element angegeben ist, wenn dieser Eintrag erreicht wird. Die URL, die im **href** -Attribut eines **LogURL** -Elements angegeben ist, muss die Adresse eines Hosts sein, der Protokollierungs Anforderungen verarbeiten kann. Die URL kann eine beliebige gültige HTTP-URL sein. Die URL kann auch den Speicherort eines CGI-Skripts angeben.

Die einzigen gültigen Protokolle für ein **LogURL** -Element sind http und HTTPS.

Ein **LogURL** -Element innerhalb des Gültigkeits Bereichs eines **ASX** -Elements ist nur auf die Metadatendatei anwendbar, in der es sich befindet, unabhängig davon, ob auf diese Metadatendatei von einer anderen Metadatei verwiesen wird. Ein **LogURL** -Element erzwingt die Übermittlung von Protokolldaten für alle Inhalte, die aus dem definierten Bereich gestreamt werden, und nur für Inhalte, die aus dem definierten Bereich gestreamt werden. Protokolldaten werden an den Ursprungsserver und an alle URLs übermittelt, die in jedem **LogURL** -Element im Gültigkeitsbereich aufgelistet sind. Protokolldaten werden nur einmal an jede aufgelistete URL übermittelt, auch wenn die gleiche URL mehrmals in einem bestimmten Bereich aufgelistet ist. Eine Wiederholung eines **Eintrags** führt zu einer weiteren Übermittlung an die aufgelisteten URLs.

Es gibt keine Beschränkung für die Anzahl der **LogURL** -Elemente in einer Metadatei-Wiedergabeliste.

## <a name="examples"></a>Beispiele


```XML
<ASX VERSION="3.0">
  <TITLE>Example Media Player Show</TITLE>
  <LOGURL HREF="https://example.microsoft.com/info/showlog.asp?whatsup" />
  <ENTRY>
    <REF href="mms://ucast.proseware.com/Media1.asf" />
    <LOGURL HREF="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal"/>
  </ENTRY>
</ASX>
```



Im folgenden finden Sie Beispiele für gültige URLs.

URL einer ISAPI-Anwendung:


```XML
https://www.proseware.com/logs/WMSLogging.dll
```



URL eines CGI-Skripts:


```XML
https://www.proseware.com/cgi-bin/My_WMS_Logging_Script.pl
```



Eine gültige HTTP-URL:


```XML
https://www.proseware.com/some/arbitrary/path/My_WMS_Logging_Page.asp?PubPoint=FooPubPoint&AnotherName=AnotherValue
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------|
| Version<br/> | Windows Media Player, Version 70 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referenz zu Windows Media-Metadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





