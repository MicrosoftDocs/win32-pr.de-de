---
title: Kommentare (msfeeds. h)
description: Fügen Sie Metadatendateien Kommentare hinzu, indem Sie die Extensible Markup Language Syntax (XML) befolgen. Kommentare beginnen mit \ 0034; --\ 0034; und enden mit \ 0034;--\ 0034;.
ms.assetid: 3d8dbf13-bd48-4405-804f-57e0f5eff642
keywords:
- Kommentare zu Windows-Media Player
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
ms.openlocfilehash: 701f456cae9f1432ed42235a3a6e13af555b2b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372774"
---
# <a name="comments-msfeedsh"></a>Kommentare (msfeeds. h)

Fügen Sie Metadatendateien Kommentare hinzu, indem Sie die Extensible Markup Language Syntax (XML) befolgen. Kommentare beginnen mit " &lt; !--" und enden mit "-- &gt; ".

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a>Bemerkungen

Kommentare können an beliebiger Stelle angezeigt werden, außer innerhalb von Element Inhalten (zwischen öffnenden und schließende tagtags,  < >). Sie sind nicht Teil der Zeichendaten des Dokuments und werden ignoriert, wenn die Metadatei analysiert wird.

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
| Header<br/> | <dl> <dt>Msfeeds. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





