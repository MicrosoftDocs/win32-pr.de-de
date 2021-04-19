---
title: Author-Attribut
description: Das Author-Attribut ist der Name eines Medienkünstlers oder Akteurs, der dem Inhalt zugeordnet ist.
ms.assetid: 6621a955-dd6b-4725-9690-0cc96e73d94f
keywords:
- Author-Attribut Fenster Media Player
topic_type:
- apiref
api_name:
- Author
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94ef73679aa3869a9a3d87b926b7f38464b1001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361339"
---
# <a name="author-attribute"></a><span data-ttu-id="0fde7-104">Author-Attribut</span><span class="sxs-lookup"><span data-stu-id="0fde7-104">Author Attribute</span></span>

<span data-ttu-id="0fde7-105">Das **Author** -Attribut ist der Name eines Medienkünstlers oder Akteurs, der dem Inhalt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0fde7-105">The **Author** attribute is the name of a media artist or actor associated with the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="0fde7-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="0fde7-106">Applies To</span></span>

-   [<span data-ttu-id="0fde7-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="0fde7-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="0fde7-108">CD-Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="0fde7-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="0fde7-109">CD-Spuren</span><span class="sxs-lookup"><span data-stu-id="0fde7-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="0fde7-110">Häufig verwendete Windows Media-Dateien</span><span class="sxs-lookup"><span data-stu-id="0fde7-110">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="0fde7-111">DVDs</span><span class="sxs-lookup"><span data-stu-id="0fde7-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="0fde7-112">Media. getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="0fde7-112">Media.getItemInfoByType</span></span>](media-getiteminfobytype.md)
-   [<span data-ttu-id="0fde7-113">Foto Elemente</span><span class="sxs-lookup"><span data-stu-id="0fde7-113">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="0fde7-114">Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="0fde7-114">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="0fde7-115">Options Felder</span><span class="sxs-lookup"><span data-stu-id="0fde7-115">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="0fde7-116">Video Elemente</span><span class="sxs-lookup"><span data-stu-id="0fde7-116">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="0fde7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fde7-117">Remarks</span></span>

<span data-ttu-id="0fde7-118">Dieses Attribut ist sowohl in der Bibliothek (oder im Cache) als auch in der Mediendatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0fde7-118">This attribute is stored in both the library (or cache) and the media file.</span></span>

<span data-ttu-id="0fde7-119">Dieses Attribut kann mehrere Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0fde7-119">This attribute may have multiple values.</span></span> <span data-ttu-id="0fde7-120">Wenn Sie alle Werte für ein mehr wertiges Attribut abrufen möchten, müssen Sie die *Medien* verwenden. **getItemInfoByType** -Methode, nicht das *Medium*. **getiteminfo** -Methode.</span><span class="sxs-lookup"><span data-stu-id="0fde7-120">To retrieve all of the values for a multi-valued attribute, you must use the *Media*.**getItemInfoByType** method, not the *Media*.**getItemInfo** method.</span></span>

<span data-ttu-id="0fde7-121">Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmauthor.</span><span class="sxs-lookup"><span data-stu-id="0fde7-121">The Windows Media Format SDK constant for this attribute is g\_wszWMAuthor.</span></span>

<span data-ttu-id="0fde7-122">**Actor** und **Künstlerin** sind Aliase für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="0fde7-122">**Actor** and **Artist** are aliases for this attribute.</span></span>

<span data-ttu-id="0fde7-123">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0fde7-123">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fde7-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fde7-124">Requirements</span></span>



| <span data-ttu-id="0fde7-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fde7-125">Requirement</span></span> | <span data-ttu-id="0fde7-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0fde7-126">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="0fde7-127">Version</span><span class="sxs-lookup"><span data-stu-id="0fde7-127">Version</span></span><br/> | <span data-ttu-id="0fde7-128">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="0fde7-128">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0fde7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fde7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fde7-130">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="0fde7-130">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





