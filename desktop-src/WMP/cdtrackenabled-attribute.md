---
title: Cdtrackaktiviertes Attribut
description: Das cdtrackaktivierte-Attribut gibt an, ob der Titel für die Wiedergabe aktiviert ist.
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- Cdtrackaktiviertes Attribut Windows Media Player
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81c231dbdfc432ea7aa510a19b1f85e0826c836
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359813"
---
# <a name="cdtrackenabled-attribute"></a><span data-ttu-id="7939c-104">Cdtrackaktiviertes Attribut</span><span class="sxs-lookup"><span data-stu-id="7939c-104">CDTrackEnabled Attribute</span></span>

<span data-ttu-id="7939c-105">Das **cdtrackaktivierte** -Attribut gibt an, ob der Titel für die Wiedergabe aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7939c-105">The **CDTrackEnabled** attribute indicates whether the track is enabled for playback.</span></span>

## <a name="applies-to"></a><span data-ttu-id="7939c-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="7939c-106">Applies To</span></span>

-   [<span data-ttu-id="7939c-107">CD-Spuren</span><span class="sxs-lookup"><span data-stu-id="7939c-107">CD Tracks</span></span>](cd-track-attributes.md)

## <a name="remarks"></a><span data-ttu-id="7939c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7939c-108">Remarks</span></span>

<span data-ttu-id="7939c-109">Dieses Attribut ist nur im Bibliotheks Cache gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7939c-109">This attribute is stored only in the library cache.</span></span>

<span data-ttu-id="7939c-110">Bei der Wiedergabe einer CD in Windows Media Player kann der Benutzer eine Spur auswählen und angeben, dass er nicht wiedergegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="7939c-110">When playing a CD in Windows Media Player, the user may select a track and specify that it should not be played.</span></span> <span data-ttu-id="7939c-111">Dieser Wert dieses Attributs ist true, wenn der Titel wiedergegeben werden kann, oder false, wenn der Benutzer angegeben hat, dass der Titel nicht wiedergegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="7939c-111">This value of this attribute is True if the track can be played, or False if the user specified that the track should not be played.</span></span>

<span data-ttu-id="7939c-112">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7939c-112">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7939c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7939c-113">Requirements</span></span>



| <span data-ttu-id="7939c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7939c-114">Requirement</span></span> | <span data-ttu-id="7939c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7939c-115">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="7939c-116">Version</span><span class="sxs-lookup"><span data-stu-id="7939c-116">Version</span></span><br/> | <span data-ttu-id="7939c-117">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="7939c-117">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7939c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7939c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7939c-119">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="7939c-119">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





