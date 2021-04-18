---
title: Mediacollectionmediareverschodas Ereignis des AxWindowsMediaPlayer-Objekts
description: Das Ereignis mediacollectionmediareverschohe tritt auf, wenn ein Medien Element aus der lokalen Bibliothek entfernt wird. | Mediacollectionmediareverschodas Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 66dae2be-2a71-4d53-b2e2-f106426d4eea
keywords:
- Mediacollectionmediareverschodas Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea15ff63fb913cd399a152913a27ffda1090d9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372231"
---
# <a name="mediacollectionmediaremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="9f924-105">Mediacollectionmediareverschodas Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="9f924-105">MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="9f924-106">Das Ereignis mediacollectionmediareverschohe tritt auf, wenn ein Medien Element aus der lokalen Bibliothek entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="9f924-106">The MediaCollectionMediaRemoved event occurs when a media item is removed from the local library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionMediaRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaRemovedEvent e
)
        
[Visual Basic]
Private Sub player_MediaCollectionMediaRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaRemovedEvent
) Handles player.MediaCollectionMediaRemoved
```

## <a name="event-data"></a><span data-ttu-id="9f924-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="9f924-107">Event Data</span></span>

<span data-ttu-id="9f924-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionmediaremuvedeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="9f924-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaRemovedEventHandler**.</span></span> <span data-ttu-id="9f924-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionmediaremuvedevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="9f924-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaRemovedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="9f924-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9f924-110">Property</span></span> | <span data-ttu-id="9f924-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f924-111">Description</span></span>                                                                                                                      |
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f924-112">pmedia</span><span class="sxs-lookup"><span data-stu-id="9f924-112">pMedia</span></span>   | <span data-ttu-id="9f924-113">System. objectdas Medien Element, das aus der lokalen Bibliothek entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="9f924-113">System.ObjectThe media item removed from the local library.</span></span> <span data-ttu-id="9f924-114">Sie können dies in eine iwmpmedia-Schnittstelle umwandeln, um darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="9f924-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9f924-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f924-115">Remarks</span></span>

<span data-ttu-id="9f924-116">Dieses Ereignis tritt nur für die lokale Bibliothek auf.</span><span class="sxs-lookup"><span data-stu-id="9f924-116">This event occurs only for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f924-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f924-117">Requirements</span></span>



| <span data-ttu-id="9f924-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f924-118">Requirement</span></span> | <span data-ttu-id="9f924-119">Wert</span><span class="sxs-lookup"><span data-stu-id="9f924-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f924-120">Version</span><span class="sxs-lookup"><span data-stu-id="9f924-120">Version</span></span><br/>   | <span data-ttu-id="9f924-121">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="9f924-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="9f924-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f924-122">Namespace</span></span><br/> | <span data-ttu-id="9f924-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="9f924-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="9f924-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="9f924-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9f924-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9f924-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f924-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f924-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f924-127">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="9f924-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9f924-128">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="9f924-128">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





