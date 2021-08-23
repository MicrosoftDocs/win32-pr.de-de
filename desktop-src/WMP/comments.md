---
title: Kommentare (Msfeeds.h)
description: Fügen Sie Metadateien Kommentare hinzu, indem Sie Extensible Markup Language -Syntax (XML) folgen. Kommentare beginnen mit \ 0034; -- \ 0034; und enden mit \ 0034;-- \ 0034;.
ms.assetid: 3d8dbf13-bd48-4405-804f-57e0f5eff642
keywords:
- Kommentare Windows Media Player
topic_type:
- apiref
api_name:
- Comments
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fe5aaf9dde3d804bb91a1e2551636c86aa54ff2bec599bf06100ee2622b592a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135783"
---
# <a name="comments-msfeedsh"></a>Kommentare (Msfeeds.h)

Fügen Sie Metadateien Kommentare hinzu, indem Sie Extensible Markup Language -Syntax (XML) folgen. Kommentare beginnen mit &lt; "!--" und enden mit "-- &gt; ".

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a>Hinweise

Kommentare können überall angezeigt werden, außer innerhalb des Elementinhalts (zwischen elementöffnen und schließende Tags,  < >). Sie sind nicht Teil der Zeichendaten des Dokuments und werden ignoriert, wenn die Metadatei analysiert wird.

## <a name="examples"></a>Beispiele


```XML
<ASX version = "3.0">
<!-- This information is only visible when editing a metafile file. -->
<!--<BANNER HREF="c:\wmsdk\wmssdk\samples\dhtml\asfbutton3.gif">
    </BANNER>-->
    <ENTRY>
        <REF HREF = "mms://proseware.com/pubpt/filename.asf" />
    </ENTRY>

    <ENTRY>
        <TITLE>WMA Port na Pucai</TITLE>
        <!--<DURATION VALUE="00:00:15"/>-->
        <REF href="c:\asfroot\Port na Pucai.wma"/>
    </ENTRY></ASX>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Msfeeds.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





