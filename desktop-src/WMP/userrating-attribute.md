---
title: Userrating-Attribut
description: Das userrating-Attribut ist die vom Benutzer in der Bibliothek angegebene Bewertung.
ms.assetid: 33df5316-1506-4ecb-b729-c2d66b878825
keywords:
- Userrating-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- UserRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a25dd7b4e55195deaecf5228b9ad5bad9195c2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355865"
---
# <a name="userrating-attribute"></a><span data-ttu-id="785df-104">Userrating-Attribut</span><span class="sxs-lookup"><span data-stu-id="785df-104">UserRating Attribute</span></span>

<span data-ttu-id="785df-105">Das **userrating** -Attribut ist die vom Benutzer in der Bibliothek angegebene Bewertung.</span><span class="sxs-lookup"><span data-stu-id="785df-105">The **UserRating** attribute is the rating specified by the user in the library.</span></span>

## <a name="applies-to"></a><span data-ttu-id="785df-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="785df-106">Applies To</span></span>

-   [<span data-ttu-id="785df-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="785df-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="785df-108">Andere Elemente</span><span class="sxs-lookup"><span data-stu-id="785df-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="785df-109">Foto Elemente</span><span class="sxs-lookup"><span data-stu-id="785df-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="785df-110">Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="785df-110">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="785df-111">Video Elemente</span><span class="sxs-lookup"><span data-stu-id="785df-111">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="785df-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="785df-112">Remarks</span></span>

<span data-ttu-id="785df-113">Benutzerbewertungen werden durch ganzzahlige Werte dargestellt, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="785df-113">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="785df-114">Wenn Sie einen Wert angeben, verwenden Sie einen der Werte aus der Spalte zum Schreiben von Werten.</span><span class="sxs-lookup"><span data-stu-id="785df-114">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="785df-115">Beim Abrufen von Werten können Sie die Bereiche in der Spalte Lesewerte verwenden, um die Anzahl der Sterne zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="785df-115">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="785df-116">Rating</span><span class="sxs-lookup"><span data-stu-id="785df-116">Rating</span></span>  | <span data-ttu-id="785df-117">Wert wird geschrieben</span><span class="sxs-lookup"><span data-stu-id="785df-117">Writing value</span></span> | <span data-ttu-id="785df-118">Lesen von Werten</span><span class="sxs-lookup"><span data-stu-id="785df-118">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="785df-119">Unbewertete</span><span class="sxs-lookup"><span data-stu-id="785df-119">Unrated</span></span> | <span data-ttu-id="785df-120">0</span><span class="sxs-lookup"><span data-stu-id="785df-120">0</span></span>             | <span data-ttu-id="785df-121">0</span><span class="sxs-lookup"><span data-stu-id="785df-121">0</span></span>              |
| <span data-ttu-id="785df-122">1 Stern</span><span class="sxs-lookup"><span data-stu-id="785df-122">1 star</span></span>  | <span data-ttu-id="785df-123">1</span><span class="sxs-lookup"><span data-stu-id="785df-123">1</span></span>             | <span data-ttu-id="785df-124">1 bis 12</span><span class="sxs-lookup"><span data-stu-id="785df-124">1 to 12</span></span>        |
| <span data-ttu-id="785df-125">2 Sterne</span><span class="sxs-lookup"><span data-stu-id="785df-125">2 stars</span></span> | <span data-ttu-id="785df-126">25</span><span class="sxs-lookup"><span data-stu-id="785df-126">25</span></span>            | <span data-ttu-id="785df-127">13 bis 37</span><span class="sxs-lookup"><span data-stu-id="785df-127">13 to 37</span></span>       |
| <span data-ttu-id="785df-128">3 Sterne</span><span class="sxs-lookup"><span data-stu-id="785df-128">3 stars</span></span> | <span data-ttu-id="785df-129">50</span><span class="sxs-lookup"><span data-stu-id="785df-129">50</span></span>            | <span data-ttu-id="785df-130">38 bis 62</span><span class="sxs-lookup"><span data-stu-id="785df-130">38 to 62</span></span>       |
| <span data-ttu-id="785df-131">4 Sterne</span><span class="sxs-lookup"><span data-stu-id="785df-131">4 stars</span></span> | <span data-ttu-id="785df-132">75</span><span class="sxs-lookup"><span data-stu-id="785df-132">75</span></span>            | <span data-ttu-id="785df-133">63 bis 86</span><span class="sxs-lookup"><span data-stu-id="785df-133">63 to 86</span></span>       |
| <span data-ttu-id="785df-134">5 Sterne</span><span class="sxs-lookup"><span data-stu-id="785df-134">5 stars</span></span> | <span data-ttu-id="785df-135">99</span><span class="sxs-lookup"><span data-stu-id="785df-135">99</span></span>            | <span data-ttu-id="785df-136">87 bis 99</span><span class="sxs-lookup"><span data-stu-id="785df-136">87 to 99</span></span>       |



 

<span data-ttu-id="785df-137">Dieses Attribut ist nur in der-Bibliothek gespeichert.</span><span class="sxs-lookup"><span data-stu-id="785df-137">This attribute is stored only in the library.</span></span>

<span data-ttu-id="785df-138">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="785df-138">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="785df-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="785df-139">Requirements</span></span>



| <span data-ttu-id="785df-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="785df-140">Requirement</span></span> | <span data-ttu-id="785df-141">Wert</span><span class="sxs-lookup"><span data-stu-id="785df-141">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="785df-142">Version</span><span class="sxs-lookup"><span data-stu-id="785df-142">Version</span></span><br/> | <span data-ttu-id="785df-143">Windows Media Player 9-Serie oder höher (das Foto Element wird nur in Windows Media Player 10 oder höher unterstützt)</span><span class="sxs-lookup"><span data-stu-id="785df-143">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="785df-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="785df-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="785df-145">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="785df-145">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





