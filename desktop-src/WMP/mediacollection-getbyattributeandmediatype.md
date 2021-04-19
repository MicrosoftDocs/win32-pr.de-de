---
title: Mediacollection. getbyattributeandmediatype-Methode
description: Die getbyattributeandmediatype-Methode ruft ein Wiedergabelisten Objekt ab, das Medienobjekte mit dem angegebenen Attribut und Medientyp enthält.
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- getbyattributeandmediatype-Methode, Windows Media Player
- getbyattributeandmediatype-Methode Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, getbyattributeandmediatype-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getByAttributeAndMediaType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e26abbf2f19d50ec6a10ebbafe12afae8576f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361592"
---
# <a name="mediacollectiongetbyattributeandmediatype-method"></a><span data-ttu-id="19ac7-106">Mediacollection. getbyattributeandmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="19ac7-106">MediaCollection.getByAttributeAndMediaType method</span></span>

<span data-ttu-id="19ac7-107">Die **getbyattributeandmediatype** -Methode ruft ein **Wiedergabe** Listen Objekt ab, das **Medien** Objekte mit dem angegebenen Attribut und Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="19ac7-107">The **getByAttributeAndMediaType** method retrieves a **Playlist** object containing **Media** objects having the specified attribute and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="19ac7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="19ac7-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAttributeAndMediaType(
  attribute,
  value,
  mediaType
)
```



## <a name="parameters"></a><span data-ttu-id="19ac7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="19ac7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19ac7-110">*Attribut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19ac7-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ac7-111">**Zeichenfolge** , die das Attribut enthält.</span><span class="sxs-lookup"><span data-stu-id="19ac7-111">**String** containing the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="19ac7-112">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19ac7-112">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ac7-113">**Zeichenfolge** , die den Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="19ac7-113">**String** containing the value.</span></span>

</dd> <dt>

<span data-ttu-id="19ac7-114">*mediaType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19ac7-114">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ac7-115">**Zeichenfolge** , die den Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="19ac7-115">**String** containing the media type.</span></span> <span data-ttu-id="19ac7-116">Muss einen der folgenden Werte enthalten: "Audiodatei", "Video", "Photo", "Wiedergabeliste" oder "Other".</span><span class="sxs-lookup"><span data-stu-id="19ac7-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19ac7-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19ac7-117">Return value</span></span>

<span data-ttu-id="19ac7-118">Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="19ac7-118">This method returns a **Playlist** object</span></span>

## <a name="requirements"></a><span data-ttu-id="19ac7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19ac7-119">Requirements</span></span>



| <span data-ttu-id="19ac7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19ac7-120">Requirement</span></span> | <span data-ttu-id="19ac7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="19ac7-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="19ac7-122">Version</span><span class="sxs-lookup"><span data-stu-id="19ac7-122">Version</span></span><br/> | <span data-ttu-id="19ac7-123">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="19ac7-123">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="19ac7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="19ac7-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="19ac7-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19ac7-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19ac7-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19ac7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ac7-127">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="19ac7-127">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="19ac7-128">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="19ac7-128">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="19ac7-129">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="19ac7-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 





