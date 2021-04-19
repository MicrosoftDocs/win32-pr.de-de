---
title: WM/Composer-Attribut
description: Das WM/Composer-Attribut ist der Name des Composer der Musik.
ms.assetid: 48459027-ed80-46a2-ad5c-ace602144150
keywords:
- WM/Composer-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- WM/Composer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f206b1a23126612f3f7c875b9a9b4badca8339
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356426"
---
# <a name="wmcomposer-attribute"></a><span data-ttu-id="033f2-104">WM/Composer-Attribut</span><span class="sxs-lookup"><span data-stu-id="033f2-104">WM/Composer Attribute</span></span>

<span data-ttu-id="033f2-105">Das **WM/Composer-** Attribut ist der Name des Composer der Musik.</span><span class="sxs-lookup"><span data-stu-id="033f2-105">The **WM/Composer** attribute is the name of the composer of the music.</span></span>

## <a name="applies-to"></a><span data-ttu-id="033f2-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="033f2-106">Applies To</span></span>

-   [<span data-ttu-id="033f2-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="033f2-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="033f2-108">CD-Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="033f2-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="033f2-109">CD-Spuren</span><span class="sxs-lookup"><span data-stu-id="033f2-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="033f2-110">Häufig verwendete Windows Media-Dateiattribute</span><span class="sxs-lookup"><span data-stu-id="033f2-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="033f2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="033f2-111">Remarks</span></span>

<span data-ttu-id="033f2-112">Dieses Attribut ist sowohl in der Bibliothek (oder im Cache) als auch in der digitalen Mediendatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="033f2-112">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="033f2-113">Dieses Attribut kann mehrere Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="033f2-113">This attribute may have multiple values.</span></span> <span data-ttu-id="033f2-114">Wenn Sie alle Werte für ein mehr wertiges Attribut abrufen möchten, müssen Sie die Media. **getItemInfoByType** -Methode und nicht die **Media. getiteminfo** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="033f2-114">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="033f2-115">**Composer** ist ein Alias für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="033f2-115">**Composer** is an alias for this attribute.</span></span>

<span data-ttu-id="033f2-116">Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmcomposer.</span><span class="sxs-lookup"><span data-stu-id="033f2-116">The Windows Media Format SDK constant for this attribute is g\_wszWMComposer.</span></span>

<span data-ttu-id="033f2-117">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="033f2-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="033f2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="033f2-118">Requirements</span></span>



| <span data-ttu-id="033f2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="033f2-119">Requirement</span></span> | <span data-ttu-id="033f2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="033f2-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="033f2-121">Version</span><span class="sxs-lookup"><span data-stu-id="033f2-121">Version</span></span><br/> | <span data-ttu-id="033f2-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="033f2-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="033f2-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="033f2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="033f2-124">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="033f2-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="033f2-125">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="033f2-125">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





