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
# <a name="comments-msfeedsh"></a><span data-ttu-id="a4fa4-105">Kommentare (msfeeds. h)</span><span class="sxs-lookup"><span data-stu-id="a4fa4-105">Comments (Msfeeds.h)</span></span>

<span data-ttu-id="a4fa4-106">Fügen Sie Metadatendateien Kommentare hinzu, indem Sie die Extensible Markup Language Syntax (XML) befolgen.</span><span class="sxs-lookup"><span data-stu-id="a4fa4-106">Add comments to metafiles by following Extensible Markup Language (XML) syntax.</span></span> <span data-ttu-id="a4fa4-107">Kommentare beginnen mit " &lt; !--" und enden mit "-- &gt; ".</span><span class="sxs-lookup"><span data-stu-id="a4fa4-107">Comments begin with "&lt;!--" and end with "--&gt;".</span></span>

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a><span data-ttu-id="a4fa4-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4fa4-108">Remarks</span></span>

<span data-ttu-id="a4fa4-109">Kommentare können an beliebiger Stelle angezeigt werden, außer innerhalb von Element Inhalten (zwischen öffnenden und schließende tagtags,  < >).</span><span class="sxs-lookup"><span data-stu-id="a4fa4-109">Comments can appear anywhere except within element content (between element open and close tags, < >).</span></span> <span data-ttu-id="a4fa4-110">Sie sind nicht Teil der Zeichendaten des Dokuments und werden ignoriert, wenn die Metadatei analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="a4fa4-110">They are not part of the document's character data and are ignored when the metafile is parsed.</span></span>

## <a name="examples"></a><span data-ttu-id="a4fa4-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4fa4-111">Examples</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a4fa4-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4fa4-112">Requirements</span></span>



| <span data-ttu-id="a4fa4-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4fa4-113">Requirement</span></span> | <span data-ttu-id="a4fa4-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a4fa4-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a4fa4-115">Header</span><span class="sxs-lookup"><span data-stu-id="a4fa4-115">Header</span></span><br/> | <dl> <span data-ttu-id="a4fa4-116"><dt>Msfeeds. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4fa4-116"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4fa4-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4fa4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4fa4-118">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="a4fa4-118">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





