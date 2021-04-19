---
title: WM/Writer-Attribut
description: Das WM/Writer-Attribut ist der Name des Writers, der die Wörter des Inhalts geschrieben hat.
ms.assetid: e2035cf7-29f4-4642-9388-4cd7cb08149e
keywords:
- WM/Writer-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- WM/Writer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29aabf353fc742370ac5d01f084544be8143d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359630"
---
# <a name="wmwriter-attribute"></a><span data-ttu-id="04891-104">WM/Writer-Attribut</span><span class="sxs-lookup"><span data-stu-id="04891-104">WM/Writer Attribute</span></span>

<span data-ttu-id="04891-105">Das **WM/Writer-** Attribut ist der Name des Writers, der die Wörter des Inhalts geschrieben hat.</span><span class="sxs-lookup"><span data-stu-id="04891-105">The **WM/Writer** attribute is the name of the writer who wrote the words of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="04891-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="04891-106">Applies To</span></span>

-   [<span data-ttu-id="04891-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="04891-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="04891-108">Häufig verwendete Windows Media-Dateiattribute</span><span class="sxs-lookup"><span data-stu-id="04891-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="04891-109">Video Elemente</span><span class="sxs-lookup"><span data-stu-id="04891-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="04891-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04891-110">Remarks</span></span>

<span data-ttu-id="04891-111">Dieses Attribut ist sowohl in der Bibliothek als auch in der digitalen Mediendatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="04891-111">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="04891-112">Dieses Attribut kann mehrere Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="04891-112">This attribute may have multiple values.</span></span> <span data-ttu-id="04891-113">Wenn Sie alle Werte für ein mehr wertiges Attribut abrufen möchten, müssen Sie die Media. **getItemInfoByType** -Methode und nicht die **Media. getiteminfo** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="04891-113">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="04891-114">**Writer** ist ein Alias für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="04891-114">**Writer** is an alias for this attribute.</span></span>

<span data-ttu-id="04891-115">Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmwriter.</span><span class="sxs-lookup"><span data-stu-id="04891-115">The Windows Media Format SDK constant for this attribute is g\_wszWMWriter.</span></span>

<span data-ttu-id="04891-116">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="04891-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="04891-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04891-117">Requirements</span></span>



| <span data-ttu-id="04891-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04891-118">Requirement</span></span> | <span data-ttu-id="04891-119">Wert</span><span class="sxs-lookup"><span data-stu-id="04891-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="04891-120">Version</span><span class="sxs-lookup"><span data-stu-id="04891-120">Version</span></span><br/> | <span data-ttu-id="04891-121">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="04891-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="04891-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04891-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04891-123">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="04891-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="04891-124">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="04891-124">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





