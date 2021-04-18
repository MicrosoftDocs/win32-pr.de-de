---
title: Synkonstante-Attribut
description: Das synkonstante-Attribut ist eine Zeichen folgen Darstellung eines booleschen Werts, den Windows Media Player verwendet, um zu bestimmen, ob eine Wiedergabeliste nur für die Synchronisierung verfügbar ist.
ms.assetid: 36149bb9-3a0b-4f6d-8be3-97d2a87faa83
keywords:
- Synkonforme Attribute (Windows Media Player)
topic_type:
- apiref
api_name:
- SyncOnly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0245ffac2c4c64717adf669fcc6ff8fd0768382
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364839"
---
# <a name="synconly-attribute"></a><span data-ttu-id="3d685-104">Synkonstante-Attribut</span><span class="sxs-lookup"><span data-stu-id="3d685-104">SyncOnly Attribute</span></span>

<span data-ttu-id="3d685-105">Das **synkonstante** -Attribut ist eine Zeichen folgen Darstellung eines **booleschen** Werts, den Windows Media Player verwendet, um zu bestimmen, ob eine Wiedergabeliste nur für die Synchronisierung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3d685-105">The **SyncOnly** attribute is a string representation of a **Boolean** value that Windows Media Player uses to determine whether a playlist is available only for synchronization.</span></span>

## <a name="applies-to"></a><span data-ttu-id="3d685-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="3d685-106">Applies To</span></span>

-   [<span data-ttu-id="3d685-107">Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="3d685-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="3d685-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d685-108">Remarks</span></span>

<span data-ttu-id="3d685-109">Der Wert 1 gibt an, dass die Wiedergabeliste nur für die Synchronisierung verfügbar ist und nicht im Knoten " **automatische Wiedergabeliste** " angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3d685-109">A value of 1 indicates that the playlist is available only for synchronization and cannot appear in the **Auto Playlist** node.</span></span> <span data-ttu-id="3d685-110">Der Wert 0 (null) gibt an, dass die Wiedergabeliste im Knoten **automatische Wiedergabeliste** angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3d685-110">A value of zero indicates that the playlist can appear in the **Auto Playlist** node.</span></span>

<span data-ttu-id="3d685-111">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3d685-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d685-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d685-112">Requirements</span></span>



| <span data-ttu-id="3d685-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d685-113">Requirement</span></span> | <span data-ttu-id="3d685-114">Wert</span><span class="sxs-lookup"><span data-stu-id="3d685-114">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="3d685-115">Version</span><span class="sxs-lookup"><span data-stu-id="3d685-115">Version</span></span><br/> | <span data-ttu-id="3d685-116">Windows Media Player 10 oder höher</span><span class="sxs-lookup"><span data-stu-id="3d685-116">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d685-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d685-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d685-118">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="3d685-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





