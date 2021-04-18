---
title: Controls. currentaudiolanguage
description: Die currentaudiolanguage-Eigenschaft gibt den Gebiets Schema Bezeichner (Locale Identifier, LCID) der Audiosprache für die Wiedergabe an oder ruft ihn ab.
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- Steuerelemente. currentaudiolanguage Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguage
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1bc84c7d4c14bb742a6db37feca59fb9d0db0e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365521"
---
# <a name="controlscurrentaudiolanguage"></a><span data-ttu-id="f588d-104">Controls. currentaudiolanguage</span><span class="sxs-lookup"><span data-stu-id="f588d-104">Controls.currentAudioLanguage</span></span>

<span data-ttu-id="f588d-105">Die **currentaudiolanguage** -Eigenschaft gibt den Gebiets Schema Bezeichner (Locale Identifier, LCID) der Audiosprache für die Wiedergabe an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="f588d-105">The **currentAudioLanguage** property specifies or retrieves the locale identifier (LCID) of the audio language for playback.</span></span>

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a><span data-ttu-id="f588d-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="f588d-106">Possible Values</span></span>

<span data-ttu-id="f588d-107">Diese Eigenschaft ist eine Lese-/schreibzahl (**Long**). </span><span class="sxs-lookup"><span data-stu-id="f588d-107">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="f588d-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f588d-108">Remarks</span></span>

<span data-ttu-id="f588d-109">Eine LCID identifiziert eindeutig einen bestimmten Sprach Dialekt, der als Gebiets Schema bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="f588d-109">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="f588d-110">Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="f588d-110">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="f588d-111">Beim Arbeiten mit DVD-Inhalten bewirkt die Angabe einer LCID, dass die erste verfügbare Audiospur mit der angegebenen Sprach-ID ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="f588d-111">When working with DVD content, specifying an LCID will cause the first available audio track having the specified language ID to be selected.</span></span>

<span data-ttu-id="f588d-112">**Windows Media Player 10 Mobile:** Diese Eigenschaft akzeptiert nur die sprachneutrale LCID (0) oder gibt Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="f588d-112">**Windows Media Player 10 Mobile:** This property only accepts or returns the language-neutral LCID (0).</span></span>

## <a name="requirements"></a><span data-ttu-id="f588d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f588d-113">Requirements</span></span>



| <span data-ttu-id="f588d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f588d-114">Requirement</span></span> | <span data-ttu-id="f588d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f588d-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f588d-116">Version</span><span class="sxs-lookup"><span data-stu-id="f588d-116">Version</span></span><br/> | <span data-ttu-id="f588d-117">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="f588d-117">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="f588d-118">DLL</span><span class="sxs-lookup"><span data-stu-id="f588d-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="f588d-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f588d-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f588d-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f588d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f588d-121">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="f588d-121">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="f588d-122">**Controls. audiolanguagecount**</span><span class="sxs-lookup"><span data-stu-id="f588d-122">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="f588d-123">**Controls. currentaudiolanguageindex**</span><span class="sxs-lookup"><span data-stu-id="f588d-123">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="f588d-124">**Controls. getaudiolanguagedescription**</span><span class="sxs-lookup"><span data-stu-id="f588d-124">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="f588d-125">**Controls. getaudiolanguageid**</span><span class="sxs-lookup"><span data-stu-id="f588d-125">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="f588d-126">**Controls. getlanguagename**</span><span class="sxs-lookup"><span data-stu-id="f588d-126">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





