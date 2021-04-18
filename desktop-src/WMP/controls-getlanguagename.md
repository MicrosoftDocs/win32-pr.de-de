---
title: Controls. getlanguagename-Methode
description: Die getlanguagename-Methode ruft den Namen der Audiosprache mit dem angegebenen Gebiets Schema Bezeichner (LCID) ab.
ms.assetid: 9e142c89-92bf-476f-bae7-b94f5b5ebe01
keywords:
- getlanguagename-Methode, Windows-Media Player
- getlanguagename-Methode, Windows Media Player, Controls-Klasse
- Steuerelemente-Klasse, Windows Media Player, getlanguagename-Methode
topic_type:
- apiref
api_name:
- Controls.getLanguageName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 798a6b22f344953df716e4df4ed8a9a0daff2a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365578"
---
# <a name="controlsgetlanguagename-method"></a><span data-ttu-id="b9069-106">Controls. getlanguagename-Methode</span><span class="sxs-lookup"><span data-stu-id="b9069-106">Controls.getLanguageName method</span></span>

<span data-ttu-id="b9069-107">Die **getlanguagename** -Methode ruft den Namen der Audiosprache mit dem angegebenen Gebiets Schema Bezeichner (LCID) ab.</span><span class="sxs-lookup"><span data-stu-id="b9069-107">The **getLanguageName** method retrieves the name of the audio language with the specified locale identifier (LCID).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9069-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9069-108">Syntax</span></span>


```JScript
strRetVal = Controls.getLanguageName(
  LCID
)
```



## <a name="parameters"></a><span data-ttu-id="b9069-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9069-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9069-110">*LCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9069-110">*LCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9069-111">**Zahl** (**Long**), die die LCID angibt.</span><span class="sxs-lookup"><span data-stu-id="b9069-111">**Number** (**long**) specifying the LCID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9069-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9069-112">Return value</span></span>

<span data-ttu-id="b9069-113">Diese Methode gibt eine **Zeichenfolge** zurück.</span><span class="sxs-lookup"><span data-stu-id="b9069-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9069-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9069-114">Remarks</span></span>

<span data-ttu-id="b9069-115">Eine LCID identifiziert eindeutig einen bestimmten Sprach Dialekt, der als Gebiets Schema bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="b9069-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="b9069-116">Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="b9069-116">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9069-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9069-117">Requirements</span></span>



| <span data-ttu-id="b9069-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9069-118">Requirement</span></span> | <span data-ttu-id="b9069-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b9069-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9069-120">Version</span><span class="sxs-lookup"><span data-stu-id="b9069-120">Version</span></span><br/> | <span data-ttu-id="b9069-121">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="b9069-121">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="b9069-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b9069-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="b9069-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9069-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9069-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9069-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9069-125">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="b9069-125">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="b9069-126">**Controls. audiolanguagecount**</span><span class="sxs-lookup"><span data-stu-id="b9069-126">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="b9069-127">**Controls. currentaudiolanguage**</span><span class="sxs-lookup"><span data-stu-id="b9069-127">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="b9069-128">**Controls. currentaudiolanguageindex**</span><span class="sxs-lookup"><span data-stu-id="b9069-128">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="b9069-129">**Controls. getaudiolanguagedescription**</span><span class="sxs-lookup"><span data-stu-id="b9069-129">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="b9069-130">**Controls. getaudiolanguageid**</span><span class="sxs-lookup"><span data-stu-id="b9069-130">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> </dl>

 

 





