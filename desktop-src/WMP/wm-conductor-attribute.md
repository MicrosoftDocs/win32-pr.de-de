---
title: WM/Dirigent-Attribut
description: Das WM/Conductor-Attribut ist der Name des Dirigenten der Musik.
ms.assetid: 31c7d310-da6a-4c30-86b0-15defaee1743
keywords:
- WM/Dirigent-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- WM/Conductor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1ae08dfee807d130f04dd258c6af81a8d68057
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359322"
---
# <a name="wmconductor-attribute"></a><span data-ttu-id="54f9c-104">WM/Dirigent-Attribut</span><span class="sxs-lookup"><span data-stu-id="54f9c-104">WM/Conductor Attribute</span></span>

<span data-ttu-id="54f9c-105">Das **WM/Conductor-** Attribut ist der Name des Dirigenten der Musik.</span><span class="sxs-lookup"><span data-stu-id="54f9c-105">The **WM/Conductor** attribute is the name of the conductor of the music.</span></span>

## <a name="applies-to"></a><span data-ttu-id="54f9c-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="54f9c-106">Applies To</span></span>

-   [<span data-ttu-id="54f9c-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="54f9c-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="54f9c-108">CD-Spuren</span><span class="sxs-lookup"><span data-stu-id="54f9c-108">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="54f9c-109">Häufig verwendete Windows Media-Dateiattribute</span><span class="sxs-lookup"><span data-stu-id="54f9c-109">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="54f9c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54f9c-110">Remarks</span></span>

<span data-ttu-id="54f9c-111">Dieses Attribut ist sowohl in der Bibliothek (oder im Cache) als auch in der digitalen Mediendatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="54f9c-111">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="54f9c-112">Dieses Attribut kann mehrere Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="54f9c-112">This attribute may have multiple values.</span></span> <span data-ttu-id="54f9c-113">Wenn Sie alle Werte für ein mehr wertiges Attribut abrufen möchten, müssen Sie die Media. **getItemInfoByType** -Methode und nicht die **Media. getiteminfo** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="54f9c-113">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="54f9c-114">Der- **Dirigent** ist ein Alias für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="54f9c-114">**Conductor** is an alias for this attribute.</span></span>

<span data-ttu-id="54f9c-115">Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmconductor.</span><span class="sxs-lookup"><span data-stu-id="54f9c-115">The Windows Media Format SDK constant for this attribute is g\_wszWMConductor.</span></span>

<span data-ttu-id="54f9c-116">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="54f9c-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="54f9c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54f9c-117">Requirements</span></span>



| <span data-ttu-id="54f9c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54f9c-118">Requirement</span></span> | <span data-ttu-id="54f9c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="54f9c-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="54f9c-120">Version</span><span class="sxs-lookup"><span data-stu-id="54f9c-120">Version</span></span><br/> | <span data-ttu-id="54f9c-121">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="54f9c-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54f9c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54f9c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54f9c-123">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="54f9c-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="54f9c-124">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="54f9c-124">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





