---
title: Controls. getaudiolanguageid-Methode
description: Die getaudiolanguageid-Methode ruft den Gebiets Schema Bezeichner (Locale Identifier, LCID) für einen angegebenen audiosprachindex ab.
ms.assetid: 8134a7ce-bdc7-46b2-b10e-2bf1215b0de1
keywords:
- getaudiolanguageid-Methode, Windows Media Player
- getaudiolanguageid-Methode, Windows Media Player, Controls-Klasse
- Steuerelemente-Klasse, Windows Media Player, getaudiolanguageid-Methode
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab27e95edfc74fa7a9f57d2010bf86299c55dd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352912"
---
# <a name="controlsgetaudiolanguageid-method"></a><span data-ttu-id="b0a55-106">Controls. getaudiolanguageid-Methode</span><span class="sxs-lookup"><span data-stu-id="b0a55-106">Controls.getAudioLanguageID method</span></span>

<span data-ttu-id="b0a55-107">Die **getaudiolanguageid** -Methode ruft den Gebiets Schema Bezeichner (Locale Identifier, LCID) für einen angegebenen audiosprachindex ab.</span><span class="sxs-lookup"><span data-stu-id="b0a55-107">The **getAudioLanguageID** method retrieves the locale identifier (LCID) for a specified audio language index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0a55-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0a55-108">Syntax</span></span>


```JScript
retVal = Controls.getAudioLanguageID(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="b0a55-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0a55-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0a55-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0a55-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0a55-111">**Zahl** (**Long**), die den audiosprachindex angibt.</span><span class="sxs-lookup"><span data-stu-id="b0a55-111">**Number** (**long**) specifying the audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0a55-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0a55-112">Return value</span></span>

<span data-ttu-id="b0a55-113">Diese Methode gibt eine **Zahl** (**Long**) zurück.</span><span class="sxs-lookup"><span data-stu-id="b0a55-113">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="b0a55-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0a55-114">Remarks</span></span>

<span data-ttu-id="b0a55-115">Eine LCID identifiziert eindeutig einen bestimmten Sprach Dialekt, der als Gebiets Schema bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="b0a55-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="b0a55-116">Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="b0a55-116">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="b0a55-117">**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer die sprachneutrale LCID (0) zurück.</span><span class="sxs-lookup"><span data-stu-id="b0a55-117">**Windows Media Player 10 Mobile:** This property always returns the language-neutral LCID (0).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0a55-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0a55-118">Requirements</span></span>



| <span data-ttu-id="b0a55-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0a55-119">Requirement</span></span> | <span data-ttu-id="b0a55-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b0a55-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a55-121">Version</span><span class="sxs-lookup"><span data-stu-id="b0a55-121">Version</span></span><br/> | <span data-ttu-id="b0a55-122">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="b0a55-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="b0a55-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b0a55-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="b0a55-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0a55-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0a55-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0a55-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0a55-126">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="b0a55-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="b0a55-127">**Controls. audiolanguagecount**</span><span class="sxs-lookup"><span data-stu-id="b0a55-127">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="b0a55-128">**Controls. currentaudiolanguage**</span><span class="sxs-lookup"><span data-stu-id="b0a55-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="b0a55-129">**Controls. currentaudiolanguageindex**</span><span class="sxs-lookup"><span data-stu-id="b0a55-129">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="b0a55-130">**Controls. getaudiolanguagedescription**</span><span class="sxs-lookup"><span data-stu-id="b0a55-130">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="b0a55-131">**Controls. getlanguagename**</span><span class="sxs-lookup"><span data-stu-id="b0a55-131">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





