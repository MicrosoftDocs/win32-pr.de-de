---
title: Controls. currentaudiolanguageindex
description: Die currentaudiolanguageindex-Eigenschaft gibt den 1-basierten Index an, der der Audiosprache für die Wiedergabe entspricht, oder ruft ihn ab.
ms.assetid: 9a1ae887-4e64-4758-a8a2-bf2e10a7a5c7
keywords:
- Controls. currentaudiolanguageindex-Fenster Media Player
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguageIndex
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1eb87873170c486782368f431f4fa8e3597b20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359661"
---
# <a name="controlscurrentaudiolanguageindex"></a><span data-ttu-id="6f0d5-104">Controls. currentaudiolanguageindex</span><span class="sxs-lookup"><span data-stu-id="6f0d5-104">Controls.currentAudioLanguageIndex</span></span>

<span data-ttu-id="6f0d5-105">Die **currentaudiolanguageindex** -Eigenschaft gibt den 1-basierten Index an, der der Audiosprache für die Wiedergabe entspricht, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-105">The **currentAudioLanguageIndex** property specifies or retrieves the one-based index that corresponds to the audio language for playback.</span></span>

``` syntax
player.controls.currentAudioLanguageIndex
      
```

## <a name="possible-values"></a><span data-ttu-id="6f0d5-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="6f0d5-106">Possible Values</span></span>

<span data-ttu-id="6f0d5-107">Diese Eigenschaft ist eine Lese-/schreibzahl (**Long**). </span><span class="sxs-lookup"><span data-stu-id="6f0d5-107">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="6f0d5-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f0d5-108">Remarks</span></span>

<span data-ttu-id="6f0d5-109">Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-109">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="6f0d5-110">Verwenden Sie die Eigenschaft **audiolanguagecount** , um die Anzahl der unterstützten Audiosprachen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-110">Use the **audioLanguageCount** property to get the number of supported audio languages.</span></span>

<span data-ttu-id="6f0d5-111">**Windows Media Player 10 Mobile:** Diese Eigenschaft akzeptiert nur 0 oder gibt 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-111">**Windows Media Player 10 Mobile:** This property only accepts or returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f0d5-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f0d5-112">Requirements</span></span>



| <span data-ttu-id="6f0d5-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f0d5-113">Requirement</span></span> | <span data-ttu-id="6f0d5-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6f0d5-114">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6f0d5-115">Version</span><span class="sxs-lookup"><span data-stu-id="6f0d5-115">Version</span></span><br/> | <span data-ttu-id="6f0d5-116">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-116">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="6f0d5-117">DLL</span><span class="sxs-lookup"><span data-stu-id="6f0d5-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="6f0d5-118"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f0d5-118"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f0d5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f0d5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f0d5-120">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-120">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="6f0d5-121">**Controls. audiolanguagecount**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-121">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="6f0d5-122">**Controls. currentaudiolanguage**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-122">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="6f0d5-123">**Controls. getaudiolanguagedescription**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-123">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="6f0d5-124">**Controls. getaudiolanguageid**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-124">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="6f0d5-125">**Controls. getlanguagename**</span><span class="sxs-lookup"><span data-stu-id="6f0d5-125">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





