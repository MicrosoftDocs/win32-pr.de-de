---
title: Equalizersettings. speakersize
description: Das Attribut "speakersize" gibt die Indexnummer der aktuellen Redner Größe an oder ruft diese ab.
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- Equalizersettings. speakersize-Windows-Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26dc49af55e96d3ef8de4e8a4567b3a4296ca214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366987"
---
# <a name="equalizersettingsspeakersize"></a><span data-ttu-id="574be-104">Equalizersettings. speakersize</span><span class="sxs-lookup"><span data-stu-id="574be-104">EQUALIZERSETTINGS.speakerSize</span></span>

<span data-ttu-id="574be-105">Das Attribut " **speakersize** " gibt die Indexnummer der aktuellen Redner Größe an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="574be-105">The **speakerSize** attribute specifies or retrieves the index number of the current speaker size.</span></span>

``` syntax
        elementID.speakerSize
```

## <a name="possible-values"></a><span data-ttu-id="574be-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="574be-106">Possible Values</span></span>

<span data-ttu-id="574be-107">Dieses Attribut ist eine Lese- **/schreibzahl** (Long), die einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="574be-107">This attribute is a read/write **Number** (long) containing one of the following values.</span></span>



| <span data-ttu-id="574be-108">Wert</span><span class="sxs-lookup"><span data-stu-id="574be-108">Value</span></span> | <span data-ttu-id="574be-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="574be-109">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="574be-110">0</span><span class="sxs-lookup"><span data-stu-id="574be-110">0</span></span>     | <span data-ttu-id="574be-111">Die aktuellen Referenten sind Kopfhörer.</span><span class="sxs-lookup"><span data-stu-id="574be-111">The current speakers are headphones.</span></span>     |
| <span data-ttu-id="574be-112">1</span><span class="sxs-lookup"><span data-stu-id="574be-112">1</span></span>     | <span data-ttu-id="574be-113">Die aktuellen Redner haben eine normale Größe.</span><span class="sxs-lookup"><span data-stu-id="574be-113">The current speakers are of normal size.</span></span> |
| <span data-ttu-id="574be-114">2</span><span class="sxs-lookup"><span data-stu-id="574be-114">2</span></span>     | <span data-ttu-id="574be-115">Die aktuellen Referenten sind groß.</span><span class="sxs-lookup"><span data-stu-id="574be-115">The current speakers are large.</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="574be-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="574be-116">Remarks</span></span>

<span data-ttu-id="574be-117">Der Anzeige Name der Redner Größe kann mit dem **currentspeakername** -Attribut abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="574be-117">The friendly name of the speaker size can be retrieved using the **currentSpeakerName** attribute.</span></span>

<span data-ttu-id="574be-118">Dieses Attribut wird ignoriert, wenn **enhancedaudiowert** auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="574be-118">This attribute is ignored if **enhancedAudio** is set to false.</span></span>

## <a name="requirements"></a><span data-ttu-id="574be-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="574be-119">Requirements</span></span>



| <span data-ttu-id="574be-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="574be-120">Requirement</span></span> | <span data-ttu-id="574be-121">Wert</span><span class="sxs-lookup"><span data-stu-id="574be-121">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="574be-122">Version</span><span class="sxs-lookup"><span data-stu-id="574be-122">Version</span></span><br/> | <span data-ttu-id="574be-123">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="574be-123">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="574be-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="574be-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="574be-125">**Equalizersettings-Element**</span><span class="sxs-lookup"><span data-stu-id="574be-125">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="574be-126">**Equalizersettings. currentspeakername**</span><span class="sxs-lookup"><span data-stu-id="574be-126">**EQUALIZERSETTINGS.currentSpeakerName**</span></span>](equalizersettings-currentspeakername.md)
</dt> <dt>

[<span data-ttu-id="574be-127">**Equalizersettings. enhancedaudio**</span><span class="sxs-lookup"><span data-stu-id="574be-127">**EQUALIZERSETTINGS.enhancedAudio**</span></span>](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





