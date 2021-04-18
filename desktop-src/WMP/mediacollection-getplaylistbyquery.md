---
title: Mediacollection. getplaylistbyquery-Methode
description: Die getplaylistbyquery-Methode ruft ein Wiedergabelisten Objekt ab, das Media-Objekte enthält, die den Abfragebedingungen entsprechen.
ms.assetid: 3487d442-a5bb-4519-ac45-d0138516305e
keywords:
- getplaylistbyquery-Methode, Windows-Media Player
- getplaylistbyquery-Methode Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, getplaylistbyquery-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getPlaylistByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b57d4303ba8784f912db9570faacb26d01677d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371077"
---
# <a name="mediacollectiongetplaylistbyquery-method"></a><span data-ttu-id="88275-106">Mediacollection. getplaylistbyquery-Methode</span><span class="sxs-lookup"><span data-stu-id="88275-106">MediaCollection.getPlaylistByQuery method</span></span>

<span data-ttu-id="88275-107">Die **getplaylistbyquery** -Methode ruft ein **Wiedergabe** Listen Objekt ab, das **Media** -Objekte enthält, die den Abfragebedingungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="88275-107">The **getPlaylistByQuery** method retrieves a **Playlist** object containing **Media** objects that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="88275-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="88275-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getPlaylistByQuery(
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a><span data-ttu-id="88275-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="88275-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88275-110">*Abfrage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88275-110">*query* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88275-111">**Query** -Objekt, das die Bedingungen definiert, die zum Erstellen der Wiedergabeliste verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88275-111">**Query** object that defines the conditions used to create the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="88275-112">*mediaType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88275-112">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88275-113">**Zeichenfolge** , die den Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="88275-113">**String** containing the media type.</span></span> <span data-ttu-id="88275-114">Muss einen der folgenden Werte enthalten: "Audiodatei", "Video", "Photo", "Wiedergabeliste" oder "Other".</span><span class="sxs-lookup"><span data-stu-id="88275-114">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="88275-115">*SortAttribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88275-115">*sortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88275-116">**Zeichenfolge** , die den für die Sortierung verwendeten Attributnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="88275-116">**String** containing the attribute name used for sorting.</span></span> <span data-ttu-id="88275-117">Eine leere Zeichenfolge ("") bedeutet, dass keine Sortierung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="88275-117">An empty string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="88275-118">*SortAscending* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88275-118">*sortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88275-119">**Boolescher** Wert, der angibt, dass die Wiedergabeliste in aufsteigender Reihenfolge sortiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="88275-119">**Boolean**, true indicating that the playlist must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88275-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88275-120">Return value</span></span>

<span data-ttu-id="88275-121">Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="88275-121">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="88275-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88275-122">Remarks</span></span>

<span data-ttu-id="88275-123">Bei Verbund Abfragen mit **Abfrage** wird die Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="88275-123">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="88275-124">Wenn die durch den *Abfrage* Parameter angegebene Verbund Abfrage eine Bedingung enthält, die auf dem **mediaType** -Attribut basiert, wird diese Bedingung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="88275-124">When the compound query specified by the *query* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="88275-125">Der Wert für den *mediaType* -Parameter wird immer verwendet.</span><span class="sxs-lookup"><span data-stu-id="88275-125">The value for the *mediaType* parameter is always used.</span></span> <span data-ttu-id="88275-126">Wenn die Verbund Abfrage z. b. die Bedingung "MediaType ist mit Audiodaten" enthält und der Wert für den *mediaType* -Parameter "Video" ist, enthält die resultierende Wiedergabeliste nur Video Elemente.</span><span class="sxs-lookup"><span data-stu-id="88275-126">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *mediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="88275-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88275-127">Requirements</span></span>



| <span data-ttu-id="88275-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88275-128">Requirement</span></span> | <span data-ttu-id="88275-129">Wert</span><span class="sxs-lookup"><span data-stu-id="88275-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="88275-130">Version</span><span class="sxs-lookup"><span data-stu-id="88275-130">Version</span></span><br/> | <span data-ttu-id="88275-131">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="88275-131">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="88275-132">DLL</span><span class="sxs-lookup"><span data-stu-id="88275-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="88275-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88275-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88275-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88275-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88275-135">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="88275-135">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="88275-136">**MediaType-Attribut**</span><span class="sxs-lookup"><span data-stu-id="88275-136">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> <dt>

[<span data-ttu-id="88275-137">**Query-Objekt**</span><span class="sxs-lookup"><span data-stu-id="88275-137">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 





