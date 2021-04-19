---
title: Mediacontenttypes-Attribut
description: Das mediacontenttypes-Attribut gibt den Typ des Inhalts im Element an.
ms.assetid: b91bab65-d6d2-4e05-9338-c24f28b7c71e
keywords:
- Mediacontenttypes-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- MediaContentTypes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8979864151e029abf2731f6f0b4663e078a2c061
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352945"
---
# <a name="mediacontenttypes-attribute"></a><span data-ttu-id="5e08a-104">Mediacontenttypes-Attribut</span><span class="sxs-lookup"><span data-stu-id="5e08a-104">MediaContentTypes Attribute</span></span>

<span data-ttu-id="5e08a-105">Das **mediacontenttypes** -Attribut gibt den Typ des Inhalts im Element an.</span><span class="sxs-lookup"><span data-stu-id="5e08a-105">The **MediaContentTypes** attribute specifies the type of content in the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="5e08a-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="5e08a-106">Applies To</span></span>

-   [<span data-ttu-id="5e08a-107">Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="5e08a-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="5e08a-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e08a-108">Remarks</span></span>

<span data-ttu-id="5e08a-109">Dieses Attribut kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="5e08a-109">This attribute can be one of the following values:</span></span>



| <span data-ttu-id="5e08a-110">Wert</span><span class="sxs-lookup"><span data-stu-id="5e08a-110">Value</span></span> | <span data-ttu-id="5e08a-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5e08a-111">Meaning</span></span>                                |
|-------|----------------------------------------|
| <span data-ttu-id="5e08a-112">1</span><span class="sxs-lookup"><span data-stu-id="5e08a-112">1</span></span>     | <span data-ttu-id="5e08a-113">Die Wiedergabeliste enthält Audioinhalte.</span><span class="sxs-lookup"><span data-stu-id="5e08a-113">The playlist contains audio content.</span></span>   |
| <span data-ttu-id="5e08a-114">2</span><span class="sxs-lookup"><span data-stu-id="5e08a-114">2</span></span>     | <span data-ttu-id="5e08a-115">, Um bereitgestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="5e08a-115">To be supplied.</span></span>                        |
| <span data-ttu-id="5e08a-116">3</span><span class="sxs-lookup"><span data-stu-id="5e08a-116">3</span></span>     | <span data-ttu-id="5e08a-117">Die Wiedergabeliste enthält Audioinhalte.</span><span class="sxs-lookup"><span data-stu-id="5e08a-117">The playlist contains audio content.</span></span>   |
| <span data-ttu-id="5e08a-118">4</span><span class="sxs-lookup"><span data-stu-id="5e08a-118">4</span></span>     | <span data-ttu-id="5e08a-119">Die Wiedergabeliste enthält Videoinhalte.</span><span class="sxs-lookup"><span data-stu-id="5e08a-119">The playlist contains video content.</span></span>   |
| <span data-ttu-id="5e08a-120">5</span><span class="sxs-lookup"><span data-stu-id="5e08a-120">5</span></span>     | <span data-ttu-id="5e08a-121">Die Wiedergabeliste enthält Bildinhalte.</span><span class="sxs-lookup"><span data-stu-id="5e08a-121">The playlist contains picture content.</span></span> |
| <span data-ttu-id="5e08a-122">6</span><span class="sxs-lookup"><span data-stu-id="5e08a-122">6</span></span>     | <span data-ttu-id="5e08a-123">Die Wiedergabeliste enthält TV-Inhalte.</span><span class="sxs-lookup"><span data-stu-id="5e08a-123">The playlist contains TV content.</span></span>      |



 

<span data-ttu-id="5e08a-124">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5e08a-124">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e08a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e08a-125">Requirements</span></span>



| <span data-ttu-id="5e08a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e08a-126">Requirement</span></span> | <span data-ttu-id="5e08a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="5e08a-127">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="5e08a-128">Version</span><span class="sxs-lookup"><span data-stu-id="5e08a-128">Version</span></span><br/> | <span data-ttu-id="5e08a-129">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="5e08a-129">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e08a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e08a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e08a-131">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="5e08a-131">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





