---
title: Controls. getaudiolanguagedescription-Methode
description: Die getaudiolanguagedescription-Methode ruft die Beschreibung für die Audiosprache ab, die dem angegebenen 1-basierten Index entspricht.
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- getaudiolanguagedescription-Methode, Windows Media Player
- getaudiolanguagedescription-Methode, Windows Media Player, Controls-Klasse
- Steuerelemente-Klasse, Windows Media Player, getaudiolanguagedescription-Methode
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageDescription
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d28e82648a1047252402694f4948d2a2734f344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354095"
---
# <a name="controlsgetaudiolanguagedescription-method"></a><span data-ttu-id="c3824-106">Controls. getaudiolanguagedescription-Methode</span><span class="sxs-lookup"><span data-stu-id="c3824-106">Controls.getAudioLanguageDescription method</span></span>

<span data-ttu-id="c3824-107">Die **getaudiolanguagedescription** -Methode ruft die Beschreibung für die Audiosprache ab, die dem angegebenen 1-basierten Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="c3824-107">The **getAudioLanguageDescription** method retrieves the description for the audio language corresponding to the specified one-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3824-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3824-108">Syntax</span></span>


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="c3824-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3824-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3824-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3824-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3824-111">**Zahl** (**Long**), die den einbasierten audiosprachindex angibt.</span><span class="sxs-lookup"><span data-stu-id="c3824-111">**Number** (**long**) specifying the one-based audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3824-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3824-112">Return value</span></span>

<span data-ttu-id="c3824-113">Diese Methode gibt einen **Zeichen** folgen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c3824-113">This method returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3824-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3824-114">Remarks</span></span>

<span data-ttu-id="c3824-115">Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="c3824-115">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="c3824-116">Verwenden Sie die Eigenschaft **audiolanguagecount** , um die Anzahl der unterstützten Audiosprachen abzurufen, und greifen Sie dann einzeln mithilfe eines 1-basierten Indexes auf eine Audiosprache zu.</span><span class="sxs-lookup"><span data-stu-id="c3824-116">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

<span data-ttu-id="c3824-117">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c3824-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3824-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3824-118">Requirements</span></span>



| <span data-ttu-id="c3824-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3824-119">Requirement</span></span> | <span data-ttu-id="c3824-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c3824-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3824-121">Version</span><span class="sxs-lookup"><span data-stu-id="c3824-121">Version</span></span><br/> | <span data-ttu-id="c3824-122">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c3824-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="c3824-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c3824-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="c3824-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3824-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3824-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3824-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3824-126">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="c3824-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="c3824-127">**Controls. audiolanguagecount**</span><span class="sxs-lookup"><span data-stu-id="c3824-127">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="c3824-128">**Controls. currentaudiolanguage**</span><span class="sxs-lookup"><span data-stu-id="c3824-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="c3824-129">**Controls. currentaudiolanguageindex**</span><span class="sxs-lookup"><span data-stu-id="c3824-129">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="c3824-130">**Controls. getaudiolanguageid**</span><span class="sxs-lookup"><span data-stu-id="c3824-130">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="c3824-131">**Controls. getlanguagename**</span><span class="sxs-lookup"><span data-stu-id="c3824-131">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





