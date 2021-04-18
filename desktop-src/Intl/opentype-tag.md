---
description: Definiert ein 4-Byte-Array, das 4 8-Bit-ASCII-Werte für Leerzeichen, a-z oder a-z enthält, um die Funktions Tags von OpenType-Skripts, Sprachen und Schriftart zu identifizieren.
ms.assetid: 188ad9a1-e0eb-411f-b6df-8c394d122d6f
title: OPENTYPE_TAG (Usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf973c03f26bdb8f8b3799e1780fed5075d315cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368198"
---
# <a name="opentype_tag"></a><span data-ttu-id="6e76e-103">OpenType- \_ Tag</span><span class="sxs-lookup"><span data-stu-id="6e76e-103">OPENTYPE\_TAG</span></span>

<span data-ttu-id="6e76e-104">Definiert ein 4-Byte-Array, das 4 8-Bit-ASCII-Werte für Leerzeichen, a-z oder a-z enthält, um die Funktions Tags von OpenType-Skripts, Sprachen und Schriftart zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6e76e-104">Defines a 4-byte array that contains four 8-bit ASCII values of space, A-Z, or a-z to identify OpenType script, language, and font feature tags.</span></span>


```C++
typedef ULONG OPENTYPE_TAG;
```



## <a name="remarks"></a><span data-ttu-id="6e76e-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e76e-105">Remarks</span></span>

<span data-ttu-id="6e76e-106">In den folgenden Beispielen werden Darstellungen von OpenType-Merkmals Tags definiert.</span><span class="sxs-lookup"><span data-stu-id="6e76e-106">The following examples define representations of OpenType feature tags.</span></span>

-   <span data-ttu-id="6e76e-107">Das featuretag für die Ligaturen-Funktion ist "Liga".</span><span class="sxs-lookup"><span data-stu-id="6e76e-107">The feature tag for the ligature feature is "liga".</span></span>
-   <span data-ttu-id="6e76e-108">Die Sprachen Tags für Rumänisch, Urdu und Persian sind "Rom", "URD" bzw. "All".</span><span class="sxs-lookup"><span data-stu-id="6e76e-108">The language tags for Romanian, Urdu, and Persian are "ROM ", "URD ", and "FAR ", respectively.</span></span> <span data-ttu-id="6e76e-109">Beachten Sie, dass jedes dieser Tags mit einem Leerzeichen endet.</span><span class="sxs-lookup"><span data-stu-id="6e76e-109">Note that each of these tags ends with a space.</span></span>
-   <span data-ttu-id="6e76e-110">Die Skript Tags für lateinische und arabische Skripts sind "Latn" bzw. "Arabisch".</span><span class="sxs-lookup"><span data-stu-id="6e76e-110">The script tags for Latin and Arabic scripts are "latn" and "arab", respectively.</span></span>

<span data-ttu-id="6e76e-111">Weitere Informationen zu OpenType-featuretags und der OpenType-Spezifikation finden Sie unter <https://www.microsoft.com/typography/otspec/featuretags.htm> .</span><span class="sxs-lookup"><span data-stu-id="6e76e-111">For more information on OpenType feature tags and the OpenType specification, see <https://www.microsoft.com/typography/otspec/featuretags.htm>.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e76e-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e76e-112">Requirements</span></span>



| <span data-ttu-id="6e76e-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e76e-113">Requirement</span></span> | <span data-ttu-id="6e76e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6e76e-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6e76e-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6e76e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6e76e-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e76e-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6e76e-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6e76e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6e76e-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e76e-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6e76e-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="6e76e-119">Redistributable</span></span><br/>          | <span data-ttu-id="6e76e-120">Usp10.dll, Version 1,600 oder höher, onwindows Xpund höher</span><span class="sxs-lookup"><span data-stu-id="6e76e-120">Usp10.dll version 1.600 or greater onWindows XPand later</span></span><br/>                |
| <span data-ttu-id="6e76e-121">Header</span><span class="sxs-lookup"><span data-stu-id="6e76e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e76e-122"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e76e-122"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e76e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e76e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e76e-124">Unischreiber</span><span class="sxs-lookup"><span data-stu-id="6e76e-124">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="6e76e-125">Uniscristrukturen</span><span class="sxs-lookup"><span data-stu-id="6e76e-125">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="6e76e-126">**Scriptgetfontalternateglyphs**</span><span class="sxs-lookup"><span data-stu-id="6e76e-126">**ScriptGetFontAlternateGlyphs**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)
</dt> <dt>

[<span data-ttu-id="6e76e-127">**Scriptgetfontfeaturetags**</span><span class="sxs-lookup"><span data-stu-id="6e76e-127">**ScriptGetFontFeatureTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)
</dt> <dt>

[<span data-ttu-id="6e76e-128">**Scriptgetfontlanguagetags**</span><span class="sxs-lookup"><span data-stu-id="6e76e-128">**ScriptGetFontLanguageTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)
</dt> <dt>

[<span data-ttu-id="6e76e-129">**Scriptgetfontscripttags**</span><span class="sxs-lookup"><span data-stu-id="6e76e-129">**ScriptGetFontScriptTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)
</dt> <dt>

[<span data-ttu-id="6e76e-130">**Scriptitemizeopentype**</span><span class="sxs-lookup"><span data-stu-id="6e76e-130">**ScriptItemizeOpenType**</span></span>](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)
</dt> <dt>

[<span data-ttu-id="6e76e-131">**Scriptplaceopentype**</span><span class="sxs-lookup"><span data-stu-id="6e76e-131">**ScriptPlaceOpenType**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)
</dt> <dt>

[<span data-ttu-id="6e76e-132">**Scriptpositionsingleglyph**</span><span class="sxs-lookup"><span data-stu-id="6e76e-132">**ScriptPositionSingleGlyph**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)
</dt> <dt>

[<span data-ttu-id="6e76e-133">**Scriptshapeopentype**</span><span class="sxs-lookup"><span data-stu-id="6e76e-133">**ScriptShapeOpenType**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)
</dt> <dt>

[<span data-ttu-id="6e76e-134">**Scriptsubstitutesingleglyph**</span><span class="sxs-lookup"><span data-stu-id="6e76e-134">**ScriptSubstituteSingleGlyph**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)
</dt> </dl>

 

 




