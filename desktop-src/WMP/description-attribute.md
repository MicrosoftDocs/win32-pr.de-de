---
title: Description-Attribut (WMP SDK)
description: Das Beschreibungs Attribut ist eine Beschreibung des Inhalts.
ms.assetid: 8bf76bf5-2bba-4ceb-bc98-f8b8ab2c8b6f
keywords:
- Description-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- Description
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4bc3562e7b807dc0e333c887aad1550d05b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357581"
---
# <a name="description-attribute"></a><span data-ttu-id="70226-104">Description-Attribut</span><span class="sxs-lookup"><span data-stu-id="70226-104">Description Attribute</span></span>

<span data-ttu-id="70226-105">Das **Beschreibungs** Attribut ist eine Beschreibung des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="70226-105">The **Description** attribute is a description of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="70226-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="70226-106">Applies To</span></span>

-   [<span data-ttu-id="70226-107">Musikdateien</span><span class="sxs-lookup"><span data-stu-id="70226-107">Music Files</span></span>](music-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="70226-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70226-108">Remarks</span></span>

<span data-ttu-id="70226-109">Dieses Attribut wird in Musikdateien, nicht in der Bibliothek gespeichert.</span><span class="sxs-lookup"><span data-stu-id="70226-109">This attribute is stored in music files, not in the library.</span></span>

<span data-ttu-id="70226-110">Dieses Attribut kann mehrere Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="70226-110">This attribute may have multiple values.</span></span> <span data-ttu-id="70226-111">Wenn Sie alle Werte für ein mehr wertiges Attribut abrufen möchten, müssen Sie die *Medien* verwenden. **getItemInfoByType** -Methode, nicht die *Media*. getiteminfo-Methode.</span><span class="sxs-lookup"><span data-stu-id="70226-111">To retrieve all of the values for a multi-valued attribute, you must use the *Media*.**getItemInfoByType** method, not the *Media*.getItemInfo method.</span></span>

<span data-ttu-id="70226-112">Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmdescription.</span><span class="sxs-lookup"><span data-stu-id="70226-112">The Windows Media Format SDK constant for this attribute is g\_wszWMDescription.</span></span>

<span data-ttu-id="70226-113">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="70226-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="70226-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70226-114">Requirements</span></span>



| <span data-ttu-id="70226-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70226-115">Requirement</span></span> | <span data-ttu-id="70226-116">Wert</span><span class="sxs-lookup"><span data-stu-id="70226-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="70226-117">Version</span><span class="sxs-lookup"><span data-stu-id="70226-117">Version</span></span><br/> | <span data-ttu-id="70226-118">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="70226-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70226-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70226-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70226-120">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="70226-120">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





