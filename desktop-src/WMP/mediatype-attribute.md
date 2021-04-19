---
title: MediaType-Attribut
description: Das MediaType-Attribut ist der Inhaltstyp im Element.
ms.assetid: 0d8a6937-32d8-4a4a-87e5-0002f077fefe
keywords:
- MediaType-Attribut (Windows Media Player)
topic_type:
- apiref
api_name:
- MediaType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5779552f62007aa3dd3da0e2f4253fcf5499a6be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372341"
---
# <a name="mediatype-attribute"></a><span data-ttu-id="b843e-104">MediaType-Attribut</span><span class="sxs-lookup"><span data-stu-id="b843e-104">MediaType Attribute</span></span>

<span data-ttu-id="b843e-105">Das **mediaType** -Attribut ist der Inhaltstyp im Element.</span><span class="sxs-lookup"><span data-stu-id="b843e-105">The **MediaType** attribute is the type of content in the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b843e-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="b843e-106">Applies To</span></span>

-   [<span data-ttu-id="b843e-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="b843e-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="b843e-108">Andere Elemente</span><span class="sxs-lookup"><span data-stu-id="b843e-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="b843e-109">Foto Elemente</span><span class="sxs-lookup"><span data-stu-id="b843e-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="b843e-110">Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="b843e-110">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="b843e-111">Options Felder</span><span class="sxs-lookup"><span data-stu-id="b843e-111">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="b843e-112">Video Elemente</span><span class="sxs-lookup"><span data-stu-id="b843e-112">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="b843e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b843e-113">Remarks</span></span>

<span data-ttu-id="b843e-114">Dieses Attribut ist nur in der-Bibliothek gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b843e-114">This attribute is stored only in the library.</span></span>

<span data-ttu-id="b843e-115">Dieses Attribut weist einen der folgenden Werte auf: "Audiodatei", "Other", "Photo", "Wiedergabeliste", "Radio" oder "Video".</span><span class="sxs-lookup"><span data-stu-id="b843e-115">This attribute has one of the following values: "audio", "other", "photo", "playlist", "radio", or "video".</span></span> <span data-ttu-id="b843e-116">Verwenden Sie dieses Attribut mit der *mediacollection*. **getbyattribute** -Methode zum Abrufen einer Wiedergabeliste, die alle Elemente eines bestimmten Typs enthält.</span><span class="sxs-lookup"><span data-stu-id="b843e-116">Use this attribute with the *MediaCollection*.**getByAttribute** method to retrieve a playlist containing all of the items of a particular type.</span></span>

<span data-ttu-id="b843e-117">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b843e-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b843e-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b843e-118">Requirements</span></span>



| <span data-ttu-id="b843e-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b843e-119">Requirement</span></span> | <span data-ttu-id="b843e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b843e-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="b843e-121">Version</span><span class="sxs-lookup"><span data-stu-id="b843e-121">Version</span></span><br/> | <span data-ttu-id="b843e-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="b843e-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b843e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b843e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b843e-124">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="b843e-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="b843e-125">**Mediacollection. getbyattribute**</span><span class="sxs-lookup"><span data-stu-id="b843e-125">**MediaCollection.getByAttribute**</span></span>](mediacollection-getbyattribute.md)
</dt> </dl>

 

 





