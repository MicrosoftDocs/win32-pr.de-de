---
title: WM/MediaClassSecondaryID-Attribut
description: Das WM/MediaClassSecondaryID-Attribut ist eine GUID, die die sekundäre Medienklasse angibt, bei der es sich um eine Unterklasse der primären Medienklasse handelt.
ms.assetid: 8112513a-b73a-497a-9c24-24ccef31cffc
keywords:
- WM/MediaClassSecondaryID-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb88ea03e565df649088366e13b20332256b374d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367646"
---
# <a name="wmmediaclasssecondaryid-attribute"></a><span data-ttu-id="4ca7f-104">WM/MediaClassSecondaryID-Attribut</span><span class="sxs-lookup"><span data-stu-id="4ca7f-104">WM/MediaClassSecondaryID Attribute</span></span>

<span data-ttu-id="4ca7f-105">Das **WM/MediaClassSecondaryID-** Attribut ist eine GUID, die die sekundäre Medienklasse angibt, bei der es sich um eine Unterklasse der primären Medienklasse handelt.</span><span class="sxs-lookup"><span data-stu-id="4ca7f-105">The **WM/MediaClassSecondaryID** attribute is a GUID specifying the secondary media class, which is a subclass of the primary media class.</span></span>

## <a name="applies-to"></a><span data-ttu-id="4ca7f-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="4ca7f-106">Applies To</span></span>

-   [<span data-ttu-id="4ca7f-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="4ca7f-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="4ca7f-108">Häufig verwendete Windows Media-Dateiattribute</span><span class="sxs-lookup"><span data-stu-id="4ca7f-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="4ca7f-109">Andere Elemente</span><span class="sxs-lookup"><span data-stu-id="4ca7f-109">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="4ca7f-110">Foto Elemente</span><span class="sxs-lookup"><span data-stu-id="4ca7f-110">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="4ca7f-111">Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="4ca7f-111">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="4ca7f-112">Options Felder</span><span class="sxs-lookup"><span data-stu-id="4ca7f-112">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="4ca7f-113">Video Elemente</span><span class="sxs-lookup"><span data-stu-id="4ca7f-113">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="4ca7f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ca7f-114">Remarks</span></span>

<span data-ttu-id="4ca7f-115">Dieses Attribut ist sowohl in der Bibliothek als auch in der digitalen Mediendatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4ca7f-115">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="4ca7f-116">In der folgenden Tabelle sind die unterstützten GUIDs und ihre Beschreibungen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ca7f-116">The following table lists the supported GUIDs and their descriptions.</span></span>



| <span data-ttu-id="4ca7f-117">GUID</span><span class="sxs-lookup"><span data-stu-id="4ca7f-117">GUID</span></span>                                 | <span data-ttu-id="4ca7f-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ca7f-118">Description</span></span>                                    |
|--------------------------------------|------------------------------------------------|
| <span data-ttu-id="4ca7f-119">D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC</span><span class="sxs-lookup"><span data-stu-id="4ca7f-119">D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC</span></span> | <span data-ttu-id="4ca7f-120">Das Medienobjekt stellt eine statische Wiedergabeliste dar.</span><span class="sxs-lookup"><span data-stu-id="4ca7f-120">The media object represents a static playlist.</span></span> |
| <span data-ttu-id="4ca7f-121">EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D</span><span class="sxs-lookup"><span data-stu-id="4ca7f-121">EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D</span></span> | <span data-ttu-id="4ca7f-122">Das Medienobjekt stellt eine automatische Wiedergabeliste dar.</span><span class="sxs-lookup"><span data-stu-id="4ca7f-122">The media object represents an auto playlist.</span></span>  |



 

<span data-ttu-id="4ca7f-123">**MediaClassSecondaryID** ist ein Alias für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="4ca7f-123">**MediaClassSecondaryID** is an alias for this attribute.</span></span>

<span data-ttu-id="4ca7f-124">Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmmediaclasssecondaryid.</span><span class="sxs-lookup"><span data-stu-id="4ca7f-124">The Windows Media Format SDK constant for this attribute is g\_wszWMMediaClassSecondaryID.</span></span>

<span data-ttu-id="4ca7f-125">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="4ca7f-125">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ca7f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ca7f-126">Requirements</span></span>



| <span data-ttu-id="4ca7f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ca7f-127">Requirement</span></span> | <span data-ttu-id="4ca7f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="4ca7f-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca7f-129">Version</span><span class="sxs-lookup"><span data-stu-id="4ca7f-129">Version</span></span><br/> | <span data-ttu-id="4ca7f-130">Das Foto Element wird nur in Windows Media Player 10 oder höher unterstützt. das Optionsfeld wird nur in Windows Media Player 9-Reihe unterstützt. alle anderen Elemente werden in Windows Media Player 9 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4ca7f-130">The photo item is supported only in Windows Media Player 10 or later The radio item is supported only in Windows Media Player 9 Series All other items are supported in Windows Media Player 9 Series and later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4ca7f-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ca7f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca7f-132">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="4ca7f-132">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





