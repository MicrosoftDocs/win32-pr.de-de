---
title: Player. mediacollectionmediarebewegereignis
description: Das Ereignis mediacollectionmediareverschohe tritt auf, wenn ein Medien Element aus der lokalen Bibliothek entfernt wird. | Player. mediacollectionmediarebewegereignis
ms.assetid: a1df6faf-38dc-4f5f-8f8a-953c91ea026c
keywords:
- Mediacollectionmediareverschoderte Ereignisfenster Media Player
- Mediacollectionmediareverschodem Ereignis Windows Media Player, Player-Klasse
- Windows Media Player der Player-Klasse, mediacollectionmediarebewegereignis
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72af5fe4c5e90effeb34745ea71e3edb457da357
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364536"
---
# <a name="playermediacollectionmediaremoved-event"></a><span data-ttu-id="20702-107">Player. mediacollectionmediarebewegereignis</span><span class="sxs-lookup"><span data-stu-id="20702-107">Player.MediaCollectionMediaRemoved event</span></span>

<span data-ttu-id="20702-108">Das Ereignis mediacollectionmediareverschohe tritt auf, wenn ein Medien Element aus der lokalen Bibliothek entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="20702-108">The MediaCollectionMediaRemoved event occurs when a media item is removed from the local library.</span></span>

## <a name="syntax"></a><span data-ttu-id="20702-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="20702-109">Syntax</span></span>


```JScript
Player.MediaCollectionMediaRemoved(
  pdispMedia
)
```



## <a name="parameters"></a><span data-ttu-id="20702-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="20702-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20702-111">*pdispmedia*</span><span class="sxs-lookup"><span data-stu-id="20702-111">*pdispMedia*</span></span> 
</dt> <dd>

<span data-ttu-id="20702-112">Das **Medien** Objekt, das entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="20702-112">**Media** object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20702-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20702-113">Return value</span></span>

<span data-ttu-id="20702-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="20702-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="20702-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20702-115">Remarks</span></span>

<span data-ttu-id="20702-116">Dieses Ereignis tritt nur für die lokale Bibliothek auf.</span><span class="sxs-lookup"><span data-stu-id="20702-116">This event only occurs for the local library.</span></span>

<span data-ttu-id="20702-117">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="20702-117">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="20702-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20702-118">Requirements</span></span>



| <span data-ttu-id="20702-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20702-119">Requirement</span></span> | <span data-ttu-id="20702-120">Wert</span><span class="sxs-lookup"><span data-stu-id="20702-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="20702-121">Version</span><span class="sxs-lookup"><span data-stu-id="20702-121">Version</span></span><br/> | <span data-ttu-id="20702-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="20702-122">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="20702-123">DLL</span><span class="sxs-lookup"><span data-stu-id="20702-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="20702-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20702-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20702-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20702-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20702-126">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="20702-126">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="20702-127">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="20702-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="20702-128">**Player. mediacollection**</span><span class="sxs-lookup"><span data-stu-id="20702-128">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





