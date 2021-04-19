---
title: Usereffectiverating-Attribut
description: Das usereffectiverating-Attribut entspricht der von Windows Media Player berechneten Bewertung basierend darauf, wie oft das Element wiedergegeben wurde.
ms.assetid: 6a420e20-f61d-4e15-84f8-a738caabd1d7
keywords:
- Usereffectiverating-Attribut Fenster Media Player
topic_type:
- apiref
api_name:
- UserEffectiveRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94abda9f8237c169845683263081566957a10b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369451"
---
# <a name="usereffectiverating-attribute"></a><span data-ttu-id="07c08-104">Usereffectiverating-Attribut</span><span class="sxs-lookup"><span data-stu-id="07c08-104">UserEffectiveRating Attribute</span></span>

<span data-ttu-id="07c08-105">Das **usereffectiverating** -Attribut entspricht der von Windows Media Player berechneten Bewertung basierend darauf, wie oft das Element wiedergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="07c08-105">The **UserEffectiveRating** attribute is the rating computed by Windows Media Player based on how often the item has been played.</span></span>

## <a name="applies-to"></a><span data-ttu-id="07c08-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="07c08-106">Applies To</span></span>

-   [<span data-ttu-id="07c08-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="07c08-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="07c08-108">Andere Elemente</span><span class="sxs-lookup"><span data-stu-id="07c08-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="07c08-109">Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="07c08-109">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="07c08-110">Video Elemente</span><span class="sxs-lookup"><span data-stu-id="07c08-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="07c08-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07c08-111">Remarks</span></span>

<span data-ttu-id="07c08-112">Benutzerbewertungen werden durch ganzzahlige Werte dargestellt, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="07c08-112">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="07c08-113">Wenn Sie einen Wert angeben, verwenden Sie einen der Werte aus der Spalte zum Schreiben von Werten.</span><span class="sxs-lookup"><span data-stu-id="07c08-113">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="07c08-114">Beim Abrufen von Werten können Sie die Bereiche in der Spalte Lesewerte verwenden, um die Anzahl der Sterne zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="07c08-114">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="07c08-115">Rating</span><span class="sxs-lookup"><span data-stu-id="07c08-115">Rating</span></span>  | <span data-ttu-id="07c08-116">Wert wird geschrieben</span><span class="sxs-lookup"><span data-stu-id="07c08-116">Writing value</span></span> | <span data-ttu-id="07c08-117">Lesen von Werten</span><span class="sxs-lookup"><span data-stu-id="07c08-117">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="07c08-118">Unbewertete</span><span class="sxs-lookup"><span data-stu-id="07c08-118">Unrated</span></span> | <span data-ttu-id="07c08-119">0</span><span class="sxs-lookup"><span data-stu-id="07c08-119">0</span></span>             | <span data-ttu-id="07c08-120">0</span><span class="sxs-lookup"><span data-stu-id="07c08-120">0</span></span>              |
| <span data-ttu-id="07c08-121">1 Stern</span><span class="sxs-lookup"><span data-stu-id="07c08-121">1 star</span></span>  | <span data-ttu-id="07c08-122">1</span><span class="sxs-lookup"><span data-stu-id="07c08-122">1</span></span>             | <span data-ttu-id="07c08-123">1 bis 12</span><span class="sxs-lookup"><span data-stu-id="07c08-123">1 to 12</span></span>        |
| <span data-ttu-id="07c08-124">2 Sterne</span><span class="sxs-lookup"><span data-stu-id="07c08-124">2 stars</span></span> | <span data-ttu-id="07c08-125">25</span><span class="sxs-lookup"><span data-stu-id="07c08-125">25</span></span>            | <span data-ttu-id="07c08-126">13 bis 37</span><span class="sxs-lookup"><span data-stu-id="07c08-126">13 to 37</span></span>       |
| <span data-ttu-id="07c08-127">3 Sterne</span><span class="sxs-lookup"><span data-stu-id="07c08-127">3 stars</span></span> | <span data-ttu-id="07c08-128">50</span><span class="sxs-lookup"><span data-stu-id="07c08-128">50</span></span>            | <span data-ttu-id="07c08-129">38 bis 62</span><span class="sxs-lookup"><span data-stu-id="07c08-129">38 to 62</span></span>       |
| <span data-ttu-id="07c08-130">4 Sterne</span><span class="sxs-lookup"><span data-stu-id="07c08-130">4 stars</span></span> | <span data-ttu-id="07c08-131">75</span><span class="sxs-lookup"><span data-stu-id="07c08-131">75</span></span>            | <span data-ttu-id="07c08-132">63 bis 86</span><span class="sxs-lookup"><span data-stu-id="07c08-132">63 to 86</span></span>       |
| <span data-ttu-id="07c08-133">5 Sterne</span><span class="sxs-lookup"><span data-stu-id="07c08-133">5 stars</span></span> | <span data-ttu-id="07c08-134">99</span><span class="sxs-lookup"><span data-stu-id="07c08-134">99</span></span>            | <span data-ttu-id="07c08-135">87 bis 99</span><span class="sxs-lookup"><span data-stu-id="07c08-135">87 to 99</span></span>       |



 

<span data-ttu-id="07c08-136">Dieses Attribut ist nur in der-Bibliothek gespeichert.</span><span class="sxs-lookup"><span data-stu-id="07c08-136">This attribute is stored only in the library.</span></span>

<span data-ttu-id="07c08-137">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="07c08-137">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="07c08-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07c08-138">Requirements</span></span>



| <span data-ttu-id="07c08-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07c08-139">Requirement</span></span> | <span data-ttu-id="07c08-140">Wert</span><span class="sxs-lookup"><span data-stu-id="07c08-140">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="07c08-141">Version</span><span class="sxs-lookup"><span data-stu-id="07c08-141">Version</span></span><br/> | <span data-ttu-id="07c08-142">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="07c08-142">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07c08-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07c08-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c08-144">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="07c08-144">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





