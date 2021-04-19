---
description: Definiert einige oder alle Zeichen Attribute, Glyphen, vorab breiten, x-und y-Positionen, Zeichen-zu-Glyphen-Zuordnungen usw. für eine Zeichenfolge.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (Usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef9bf7e2a3a592a279b593d986220350a3d8f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352274"
---
# <a name="script_string_analysis"></a><span data-ttu-id="c0864-103">Skript für \_ Zeichen folgen \_ Analyse</span><span class="sxs-lookup"><span data-stu-id="c0864-103">SCRIPT\_STRING\_ANALYSIS</span></span>

<span data-ttu-id="c0864-104">Definiert einige oder alle Zeichen Attribute, Glyphen, vorab breiten, x-und y-Positionen, Zeichen-zu-Glyphen-Zuordnungen usw. für eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c0864-104">Defines some or all of the character attributes, glyphs, advance widths, x and y positions, character-to-glyph mappings, and so forth, for a string.</span></span>


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a><span data-ttu-id="c0864-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0864-105">Remarks</span></span>

<span data-ttu-id="c0864-106">Dabei handelt es sich um eine nicht transparente Struktur, die von [**scriptstringanalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)dynamisch zugeordnet und abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c0864-106">This is an opaque structure that is allocated dynamically and retrieved by [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse).</span></span> <span data-ttu-id="c0864-107">Dies ist auch für alle anderen \**scriptstring \** _-Funktionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c0864-107">It is required for all other \**ScriptString\** _ functions, as well.</span></span>

<span data-ttu-id="c0864-108">Da die Analyse sehr groß sein kann, ist es wichtig, dass die Anwendung [_ *scriptstringfree* \*](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) aufruft, sobald Sie mit der Zeichenfolge fertig ist.</span><span class="sxs-lookup"><span data-stu-id="c0864-108">Since the analysis can be large, it is important for your application to call [_ *ScriptStringFree*\*](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) as soon as it has finished with the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0864-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0864-109">Requirements</span></span>



| <span data-ttu-id="c0864-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0864-110">Requirement</span></span> | <span data-ttu-id="c0864-111">Wert</span><span class="sxs-lookup"><span data-stu-id="c0864-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c0864-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0864-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c0864-113">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0864-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c0864-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0864-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c0864-115">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0864-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c0864-116">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c0864-116">Redistributable</span></span><br/>          | <span data-ttu-id="c0864-117">Internet Explorer 5 oder höher onwindows Me/98/95</span><span class="sxs-lookup"><span data-stu-id="c0864-117">Internet Explorer 5 or later onWindows Me/98/95</span></span><br/>                         |
| <span data-ttu-id="c0864-118">Header</span><span class="sxs-lookup"><span data-stu-id="c0864-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0864-119"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0864-119"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0864-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0864-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0864-121">Unischreiber</span><span class="sxs-lookup"><span data-stu-id="c0864-121">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="c0864-122">Uniscristrukturen</span><span class="sxs-lookup"><span data-stu-id="c0864-122">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="c0864-123">**Scriptstringanalyse**</span><span class="sxs-lookup"><span data-stu-id="c0864-123">**ScriptStringAnalyse**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[<span data-ttu-id="c0864-124">**Scriptstringfree**</span><span class="sxs-lookup"><span data-stu-id="c0864-124">**ScriptStringFree**</span></span>](script-string-analysis.md)
</dt> </dl>

 

 




