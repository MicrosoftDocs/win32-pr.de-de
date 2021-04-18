---
title: Mediacollection. getstringcollectionbyquery-Methode
description: Die getstringcollectionbyquery-Methode ruft ein StringCollection-Objekt ab, das alle Zeichen folgen enthält, die den Abfragebedingungen entsprechen.
ms.assetid: 17442151-7eb1-4256-ac5f-142b11645216
keywords:
- getstringcollectionbyquery-Methode, Windows-Media Player
- getstringcollectionbyquery-Methode, Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, getstringcollectionbyquery-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getStringCollectionByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf304d22cb207d8a2bfb046522e8704e900d508
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358361"
---
# <a name="mediacollectiongetstringcollectionbyquery-method"></a><span data-ttu-id="b5975-106">Mediacollection. getstringcollectionbyquery-Methode</span><span class="sxs-lookup"><span data-stu-id="b5975-106">MediaCollection.getStringCollectionByQuery method</span></span>

<span data-ttu-id="b5975-107">Die **getstringcollectionbyquery** -Methode ruft ein **StringCollection** -Objekt ab, das alle Zeichen folgen enthält, die den Abfragebedingungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b5975-107">The **getStringCollectionByQuery** method retrieves a **StringCollection** object containing all strings that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5975-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5975-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getStringCollectionByQuery(
  attribute,
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a><span data-ttu-id="b5975-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5975-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5975-110">*Attribut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5975-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5975-111">**Zeichenfolge** , die den Attributnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="b5975-111">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="b5975-112">*Abfrage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5975-112">*query* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5975-113">**Query** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b5975-113">**Query** object.</span></span>

</dd> <dt>

<span data-ttu-id="b5975-114">*mediaType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5975-114">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5975-115">**Zeichenfolge** , die den Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="b5975-115">**String** containing the media type.</span></span> <span data-ttu-id="b5975-116">Muss einen der folgenden Werte enthalten: "Audiodatei", "Video", "Photo", "Wiedergabeliste" oder "Other".</span><span class="sxs-lookup"><span data-stu-id="b5975-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="b5975-117">*SortAttribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5975-117">*sortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5975-118">**Zeichenfolge** , die den für die Sortierung verwendeten Attributnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="b5975-118">**String** containing the attribute name used for sorting.</span></span> <span data-ttu-id="b5975-119">Eine leere Zeichenfolge ("") bedeutet, dass keine Sortierung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="b5975-119">An empty string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="b5975-120">*SortAscending* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5975-120">*sortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5975-121">**Boolescher** Wert, der angibt, dass die **StringCollection** in aufsteigender Reihenfolge sortiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="b5975-121">**Boolean**, true indicating that the **StringCollection** must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5975-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5975-122">Return value</span></span>

<span data-ttu-id="b5975-123">Diese Methode gibt ein **StringCollection** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="b5975-123">This method returns a **StringCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5975-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5975-124">Remarks</span></span>

<span data-ttu-id="b5975-125">Bei Verbund Abfragen mit **Abfrage** wird die Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="b5975-125">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="b5975-126">Wenn die durch den *Abfrage* Parameter angegebene Verbund Abfrage eine Bedingung enthält, die auf dem **mediaType** -Attribut basiert, wird diese Bedingung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b5975-126">When the compound query specified by the *query* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="b5975-127">Der Wert für den *mediaType* -Parameter wird immer verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5975-127">The value for the *mediaType* parameter is always used.</span></span> <span data-ttu-id="b5975-128">Wenn die Verbund Abfrage z. b. die Bedingung "MediaType ist mit Audiodaten" enthält und der Wert für den *mediaType* -Parameter "Video" ist, enthält die resultierende Wiedergabeliste nur Video Elemente.</span><span class="sxs-lookup"><span data-stu-id="b5975-128">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *mediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5975-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5975-129">Requirements</span></span>



| <span data-ttu-id="b5975-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5975-130">Requirement</span></span> | <span data-ttu-id="b5975-131">Wert</span><span class="sxs-lookup"><span data-stu-id="b5975-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5975-132">Version</span><span class="sxs-lookup"><span data-stu-id="b5975-132">Version</span></span><br/> | <span data-ttu-id="b5975-133">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="b5975-133">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="b5975-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b5975-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="b5975-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5975-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5975-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5975-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5975-137">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="b5975-137">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="b5975-138">**MediaType-Attribut**</span><span class="sxs-lookup"><span data-stu-id="b5975-138">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> <dt>

[<span data-ttu-id="b5975-139">**Query-Objekt**</span><span class="sxs-lookup"><span data-stu-id="b5975-139">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 





