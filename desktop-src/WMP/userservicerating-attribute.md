---
title: Userservicerating-Attribut
description: Das userservicerating-Attribut ist für die zukünftige Verwendung reserviert.
ms.assetid: e6113474-725d-4eb1-9c05-cff7749f2010
keywords:
- Userservicerating-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- UserServiceRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690a090aaa9d07ee850caee004242272368129f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367418"
---
# <a name="userservicerating-attribute"></a><span data-ttu-id="5a302-104">Userservicerating-Attribut</span><span class="sxs-lookup"><span data-stu-id="5a302-104">UserServiceRating Attribute</span></span>

<span data-ttu-id="5a302-105">Das **userservicerating** -Attribut ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="5a302-105">The **UserServiceRating** attribute is reserved for future use.</span></span>

## <a name="applies-to"></a><span data-ttu-id="5a302-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="5a302-106">Applies To</span></span>

-   [<span data-ttu-id="5a302-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="5a302-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="5a302-108">Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="5a302-108">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="5a302-109">Video Elemente</span><span class="sxs-lookup"><span data-stu-id="5a302-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="5a302-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a302-110">Remarks</span></span>

<span data-ttu-id="5a302-111">Benutzerbewertungen werden durch ganzzahlige Werte dargestellt, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5a302-111">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="5a302-112">Wenn Sie einen Wert angeben, verwenden Sie einen der Werte aus der Spalte zum Schreiben von Werten.</span><span class="sxs-lookup"><span data-stu-id="5a302-112">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="5a302-113">Beim Abrufen von Werten können Sie die Bereiche in der Spalte Lesewerte verwenden, um die Anzahl der Sterne zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="5a302-113">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="5a302-114">Rating</span><span class="sxs-lookup"><span data-stu-id="5a302-114">Rating</span></span>  | <span data-ttu-id="5a302-115">Wert wird geschrieben</span><span class="sxs-lookup"><span data-stu-id="5a302-115">Writing value</span></span> | <span data-ttu-id="5a302-116">Lesen von Werten</span><span class="sxs-lookup"><span data-stu-id="5a302-116">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="5a302-117">Unbewertete</span><span class="sxs-lookup"><span data-stu-id="5a302-117">Unrated</span></span> | <span data-ttu-id="5a302-118">0</span><span class="sxs-lookup"><span data-stu-id="5a302-118">0</span></span>             | <span data-ttu-id="5a302-119">0</span><span class="sxs-lookup"><span data-stu-id="5a302-119">0</span></span>              |
| <span data-ttu-id="5a302-120">1 Stern</span><span class="sxs-lookup"><span data-stu-id="5a302-120">1 star</span></span>  | <span data-ttu-id="5a302-121">1</span><span class="sxs-lookup"><span data-stu-id="5a302-121">1</span></span>             | <span data-ttu-id="5a302-122">1 bis 12</span><span class="sxs-lookup"><span data-stu-id="5a302-122">1 to 12</span></span>        |
| <span data-ttu-id="5a302-123">2 Sterne</span><span class="sxs-lookup"><span data-stu-id="5a302-123">2 stars</span></span> | <span data-ttu-id="5a302-124">25</span><span class="sxs-lookup"><span data-stu-id="5a302-124">25</span></span>            | <span data-ttu-id="5a302-125">13 bis 37</span><span class="sxs-lookup"><span data-stu-id="5a302-125">13 to 37</span></span>       |
| <span data-ttu-id="5a302-126">3 Sterne</span><span class="sxs-lookup"><span data-stu-id="5a302-126">3 stars</span></span> | <span data-ttu-id="5a302-127">50</span><span class="sxs-lookup"><span data-stu-id="5a302-127">50</span></span>            | <span data-ttu-id="5a302-128">38 bis 62</span><span class="sxs-lookup"><span data-stu-id="5a302-128">38 to 62</span></span>       |
| <span data-ttu-id="5a302-129">4 Sterne</span><span class="sxs-lookup"><span data-stu-id="5a302-129">4 stars</span></span> | <span data-ttu-id="5a302-130">75</span><span class="sxs-lookup"><span data-stu-id="5a302-130">75</span></span>            | <span data-ttu-id="5a302-131">63 bis 86</span><span class="sxs-lookup"><span data-stu-id="5a302-131">63 to 86</span></span>       |
| <span data-ttu-id="5a302-132">5 Sterne</span><span class="sxs-lookup"><span data-stu-id="5a302-132">5 stars</span></span> | <span data-ttu-id="5a302-133">99</span><span class="sxs-lookup"><span data-stu-id="5a302-133">99</span></span>            | <span data-ttu-id="5a302-134">87 bis 99</span><span class="sxs-lookup"><span data-stu-id="5a302-134">87 to 99</span></span>       |



 

<span data-ttu-id="5a302-135">Dieses Attribut ist nur in der-Bibliothek gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5a302-135">This attribute is stored only in the library.</span></span>

<span data-ttu-id="5a302-136">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5a302-136">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a302-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a302-137">Requirements</span></span>



| <span data-ttu-id="5a302-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a302-138">Requirement</span></span> | <span data-ttu-id="5a302-139">Wert</span><span class="sxs-lookup"><span data-stu-id="5a302-139">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="5a302-140">Version</span><span class="sxs-lookup"><span data-stu-id="5a302-140">Version</span></span><br/> | <span data-ttu-id="5a302-141">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="5a302-141">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a302-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a302-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a302-143">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="5a302-143">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





