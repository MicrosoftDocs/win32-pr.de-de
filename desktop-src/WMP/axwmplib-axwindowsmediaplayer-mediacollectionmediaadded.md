---
title: Mediacollectionmediaadded-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das mediacollectionmediaadded-Ereignis tritt auf, wenn der lokalen Bibliothek ein Medien Element hinzugefügt wird. | Mediacollectionmediaadded-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: ba1779f6-a212-44f4-b52a-c88e22aebcce
keywords:
- Mediacollectionmediaadded-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb839fccf9a5048b5647480eca36fcfcaeb904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358727"
---
# <a name="mediacollectionmediaadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="671cc-105">Mediacollectionmediaadded-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="671cc-105">MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="671cc-106">Das mediacollectionmediaadded-Ereignis tritt auf, wenn der lokalen Bibliothek ein Medien Element hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="671cc-106">The MediaCollectionMediaAdded event occurs when a media item is added to the local library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionMediaAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionMediaAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaAddedEvent
) Handles player.MediaCollectionMediaAdded
```

## <a name="event-data"></a><span data-ttu-id="671cc-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="671cc-107">Event Data</span></span>

<span data-ttu-id="671cc-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionmediaaddedeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="671cc-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaAddedEventHandler**.</span></span> <span data-ttu-id="671cc-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionmediaaddedevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="671cc-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaAddedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="671cc-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="671cc-110">Property</span></span> | <span data-ttu-id="671cc-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="671cc-111">Description</span></span>                                                                                                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="671cc-112">pmedia</span><span class="sxs-lookup"><span data-stu-id="671cc-112">pMedia</span></span>   | <span data-ttu-id="671cc-113">System. objectdas Medien Element, das der lokalen Bibliothek hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="671cc-113">System.ObjectThe media item added to the local library.</span></span> <span data-ttu-id="671cc-114">Sie können dies in eine iwmpmedia-Schnittstelle umwandeln, um darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="671cc-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="671cc-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="671cc-115">Remarks</span></span>

<span data-ttu-id="671cc-116">Dieses Ereignis tritt nur für die lokale Bibliothek auf.</span><span class="sxs-lookup"><span data-stu-id="671cc-116">This event occurs only for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="671cc-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="671cc-117">Requirements</span></span>



| <span data-ttu-id="671cc-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="671cc-118">Requirement</span></span> | <span data-ttu-id="671cc-119">Wert</span><span class="sxs-lookup"><span data-stu-id="671cc-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="671cc-120">Version</span><span class="sxs-lookup"><span data-stu-id="671cc-120">Version</span></span><br/>   | <span data-ttu-id="671cc-121">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="671cc-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="671cc-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="671cc-122">Namespace</span></span><br/> | <span data-ttu-id="671cc-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="671cc-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="671cc-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="671cc-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="671cc-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="671cc-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="671cc-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="671cc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="671cc-127">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="671cc-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="671cc-128">**AxWindowsMediaPlayer. mediacollection (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="671cc-128">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="671cc-129">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="671cc-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="671cc-130">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="671cc-130">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





