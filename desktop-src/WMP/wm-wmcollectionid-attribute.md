---
title: WM/wmcollectionid-Attribut
description: Das WM/wmcollectionid-Attribut ist eine GUID, die die Sammlung identifiziert, zu der das Element gehört.
ms.assetid: 21fc0a62-d374-4ca3-bbb8-278e0d2497ce
keywords:
- WM/wmcollectionid-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bce21196e1da9583db293dab004812265c85308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368611"
---
# <a name="wmwmcollectionid-attribute"></a><span data-ttu-id="ef390-104">WM/wmcollectionid-Attribut</span><span class="sxs-lookup"><span data-stu-id="ef390-104">WM/WMCollectionID Attribute</span></span>

<span data-ttu-id="ef390-105">Das **WM/wmcollectionid-** Attribut ist eine GUID, die die Sammlung identifiziert, zu der das Element gehört.</span><span class="sxs-lookup"><span data-stu-id="ef390-105">The **WM/WMCollectionID** attribute is a GUID identifying the collection to which the item belongs.</span></span>

## <a name="applies-to"></a><span data-ttu-id="ef390-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="ef390-106">Applies To</span></span>

-   [<span data-ttu-id="ef390-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="ef390-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="ef390-108">CD-Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="ef390-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="ef390-109">CD-Spuren</span><span class="sxs-lookup"><span data-stu-id="ef390-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="ef390-110">Häufig verwendete Windows Media-Dateiattribute</span><span class="sxs-lookup"><span data-stu-id="ef390-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="ef390-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef390-111">Remarks</span></span>

<span data-ttu-id="ef390-112">Dieses Attribut ist sowohl in der Bibliothek (oder im Cache) als auch in der Mediendatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ef390-112">This attribute is stored in both the library (or cache) and the media file.</span></span>

<span data-ttu-id="ef390-113">**Wmcollectionid** ist ein Alias für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="ef390-113">**WMCollectionID** is an alias for this attribute.</span></span>

<span data-ttu-id="ef390-114">Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmcollectionid.</span><span class="sxs-lookup"><span data-stu-id="ef390-114">The Windows Media Format SDK constant for this attribute is g\_wszWMCollectionID.</span></span>

<span data-ttu-id="ef390-115">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ef390-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef390-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef390-116">Requirements</span></span>



| <span data-ttu-id="ef390-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef390-117">Requirement</span></span> | <span data-ttu-id="ef390-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ef390-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="ef390-119">Version</span><span class="sxs-lookup"><span data-stu-id="ef390-119">Version</span></span><br/> | <span data-ttu-id="ef390-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="ef390-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef390-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef390-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef390-122">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="ef390-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





