---
title: Currentmediaitemavailable-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das currentmediaitemavailable-Ereignis tritt auf, wenn ein grafisches Metadatenelement im aktuellen Medien Element verfügbar wird. | Currentmediaitemavailable-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 7db62e6a-5f20-441a-801f-147ac386c5f8
keywords:
- Currentmediaitemavailable-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547622424194e63733cec6166d813d42ebf577ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360991"
---
# <a name="currentmediaitemavailable-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="b9b87-105">Currentmediaitemavailable-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="b9b87-105">CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="b9b87-106">Das currentmediaitemavailable-Ereignis tritt auf, wenn ein grafisches Metadatenelement im aktuellen Medien Element verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="b9b87-106">The CurrentMediaItemAvailable event occurs when a graphic metadata item in the current media item becomes available.</span></span>

``` syntax
[C#]
private void player_CurrentMediaItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentMediaItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentMediaItemAvailable(
  sender As Object,  
  e As _WMPOCXEvents_CurrentMediaItemAvailableEvent
) Handles player.CurrentMediaItemAvailable
```

## <a name="event-data"></a><span data-ttu-id="b9b87-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="b9b87-107">Event Data</span></span>

<span data-ttu-id="b9b87-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ currentmediaitemavailableeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="b9b87-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentMediaItemAvailableEventHandler**.</span></span> <span data-ttu-id="b9b87-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ currentmediaitemavailableevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="b9b87-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentMediaItemAvailableEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="b9b87-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b9b87-110">Property</span></span>     | <span data-ttu-id="b9b87-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9b87-111">Description</span></span>                                                 |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="b9b87-112">bstritemname</span><span class="sxs-lookup"><span data-stu-id="b9b87-112">bstrItemName</span></span> | <span data-ttu-id="b9b87-113">System. stringder Name des aktuellen Medien Elements.</span><span class="sxs-lookup"><span data-stu-id="b9b87-113">System.StringThe name of the current media item.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b9b87-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9b87-114">Remarks</span></span>

<span data-ttu-id="b9b87-115">Da die Wiedergabe beginnen kann, bevor ein Medien Element vollständig heruntergeladen wird, sind alle im Medien Element enthaltenen metadatengrafiken (z. b. Albumcover Art) möglicherweise nicht verfügbar, wenn die Wiedergabe gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b9b87-115">Because playback can begin before a media item is fully downloaded, any metadata graphics contained in the media item (such as album cover art) may not be available when it starts to play.</span></span> <span data-ttu-id="b9b87-116">Dieses Ereignis warnt Sie, wenn ein metadatengrafieelement den Download abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="b9b87-116">This event alerts you when a metadata graphic item is finished downloading.</span></span> <span data-ttu-id="b9b87-117">Sie können dann die **iwmpmedia** -Schnittstelle abrufen, indem Sie den Wert von **bstritemname** an die *iwmpmediacollection* übergeben. **getByName** -Methode, nach der Sie mithilfe von *IWMPMedia3* auf das metadatengrafieelement zugreifen können. **getItemInfoByType** und Angeben von **WM/Bild** für den Attributnamen.</span><span class="sxs-lookup"><span data-stu-id="b9b87-117">You can then retrieve the **IWMPMedia** interface by passing the value of **bstrItemName** to the *IWMPMediaCollection*.**getByName** method, after which you can access the metadata graphic item by using *IWMPMedia3*.**getItemInfoByType** and specifying **WM/Picture** for the attribute name.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9b87-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9b87-118">Requirements</span></span>



| <span data-ttu-id="b9b87-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9b87-119">Requirement</span></span> | <span data-ttu-id="b9b87-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b9b87-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9b87-121">Version</span><span class="sxs-lookup"><span data-stu-id="b9b87-121">Version</span></span><br/>   | <span data-ttu-id="b9b87-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="b9b87-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="b9b87-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9b87-123">Namespace</span></span><br/> | <span data-ttu-id="b9b87-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="b9b87-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b9b87-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="b9b87-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b9b87-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b9b87-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9b87-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9b87-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9b87-128">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b9b87-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9b87-129">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b9b87-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9b87-130">**IWMPMedia3. getItemInfoByType (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b9b87-130">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9b87-131">**Iwmpmediacollection. getByName (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b9b87-131">**IWMPMediaCollection.getByName (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





