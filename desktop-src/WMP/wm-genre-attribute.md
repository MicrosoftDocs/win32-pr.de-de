---
title: WM/Genre-Attribut
description: Das WM/Genre-Attribut ist das Genre der Inhalte.
ms.assetid: 4b1b0512-d8fd-402a-a5f0-1002c64194f4
keywords:
- WM/Genre-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- WM/Genre
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae4a0c6ae27e85fa1ed147a3173c4cc31b20f1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371067"
---
# <a name="wmgenre-attribute"></a><span data-ttu-id="50851-104">WM/Genre-Attribut</span><span class="sxs-lookup"><span data-stu-id="50851-104">WM/Genre Attribute</span></span>

<span data-ttu-id="50851-105">Das **WM/Genre-** Attribut ist das Genre der Inhalte.</span><span class="sxs-lookup"><span data-stu-id="50851-105">The **WM/Genre** attribute is the genre of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="50851-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="50851-106">Applies To</span></span>

-   [<span data-ttu-id="50851-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="50851-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="50851-108">CD-Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="50851-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="50851-109">CD-Spuren</span><span class="sxs-lookup"><span data-stu-id="50851-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="50851-110">Häufig verwendete Windows Media-Dateiattribute</span><span class="sxs-lookup"><span data-stu-id="50851-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="50851-111">DVDs</span><span class="sxs-lookup"><span data-stu-id="50851-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="50851-112">Andere Elemente</span><span class="sxs-lookup"><span data-stu-id="50851-112">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="50851-113">Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="50851-113">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="50851-114">Video Elemente</span><span class="sxs-lookup"><span data-stu-id="50851-114">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="50851-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50851-115">Remarks</span></span>

<span data-ttu-id="50851-116">Dieses Attribut ist sowohl in der Bibliothek (oder im Cache) als auch in der digitalen Mediendatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="50851-116">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="50851-117">Dieses Attribut kann mehrere Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="50851-117">This attribute may have multiple values.</span></span> <span data-ttu-id="50851-118">Wenn Sie alle Werte für ein mehr wertiges Attribut abrufen möchten, müssen Sie die Media. **getItemInfoByType** -Methode und nicht die **Media. getiteminfo** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="50851-118">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="50851-119">**Genre** ist ein Alias für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="50851-119">**Genre** is an alias for this attribute.</span></span>

<span data-ttu-id="50851-120">Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmgenre.</span><span class="sxs-lookup"><span data-stu-id="50851-120">The Windows Media Format SDK constant for this attribute is g\_wszWMGenre.</span></span>

<span data-ttu-id="50851-121">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="50851-121">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="50851-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50851-122">Requirements</span></span>



| <span data-ttu-id="50851-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50851-123">Requirement</span></span> | <span data-ttu-id="50851-124">Wert</span><span class="sxs-lookup"><span data-stu-id="50851-124">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="50851-125">Version</span><span class="sxs-lookup"><span data-stu-id="50851-125">Version</span></span><br/> | <span data-ttu-id="50851-126">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="50851-126">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50851-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50851-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50851-128">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="50851-128">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="50851-129">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="50851-129">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





