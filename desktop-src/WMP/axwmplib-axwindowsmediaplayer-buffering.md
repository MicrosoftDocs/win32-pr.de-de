---
title: Bufferingereignis des AxWindowsMediaPlayer-Objekts
description: Das bufferingereignis tritt auf, wenn das Windows Media Player-Steuerelement die Pufferung oder den Download beendet. | Bufferingereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: ad152c4d-1c91-4da1-bec0-46f89f3b8c79
keywords:
- Bufferingereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- Buffering Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af595443d78a311510df6a7e06b2e716da22ecae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367511"
---
# <a name="buffering-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="462d1-105">Bufferingereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="462d1-105">Buffering Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="462d1-106">Das bufferingereignis tritt auf, wenn das Windows Media Player-Steuerelement die Pufferung oder den Download beendet.</span><span class="sxs-lookup"><span data-stu-id="462d1-106">The Buffering event occurs when the Windows Media Player control begins or ends buffering or downloading.</span></span>

``` syntax
[C#]
private void player_Buffering(
  object sender,
  _WMPOCXEvents_BufferingEvent e
)

[Visual Basic]
Private Sub player_Buffering(
  sender As Object,
  e As _WMPOCXEvents_BufferingEvent
) Handles player.Buffering
```

## <a name="event-data"></a><span data-ttu-id="462d1-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="462d1-107">Event Data</span></span>

<span data-ttu-id="462d1-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ bufferingeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="462d1-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_BufferingEventHandler**.</span></span> <span data-ttu-id="462d1-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ bufferingevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="462d1-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_BufferingEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="462d1-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="462d1-110">Property</span></span> | <span data-ttu-id="462d1-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="462d1-111">Description</span></span>                                                                                                                                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="462d1-112">Start</span><span class="sxs-lookup"><span data-stu-id="462d1-112">Start</span></span>    | <span data-ttu-id="462d1-113">System. booleangibt an, ob die Pufferung gestartet oder beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="462d1-113">System.BooleanSpecifies whether buffering has begun or ended.</span></span> <span data-ttu-id="462d1-114">Der Wert true gibt an, dass er begonnen hat. der Wert false gibt an, dass er beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="462d1-114">A value of true indicates that it has begun; a value of false indicates that it has ended.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="462d1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="462d1-115">Remarks</span></span>

<span data-ttu-id="462d1-116">Verwenden Sie dieses Ereignis, um zu bestimmen, wann ein-oder herunterladen gestartet oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="462d1-116">Use this event to determine when buffering or downloading starts or stops.</span></span> <span data-ttu-id="462d1-117">Sie können den gleichen Ereignisblock für beide Fälle verwenden und *iwmpnetwork* testen. **BufferingProgress** und *iwmpnetwork*. **Download Progress** , um zu bestimmen, ob der Inhalt von Windows Media Player derzeit gepuffert oder heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="462d1-117">You can use the same event block for both cases and test *IWMPNetwork*.**bufferingProgress** and *IWMPNetwork*.**downloadProgress** to determine whether Windows Media Player is currently buffering or downloading content.</span></span>

## <a name="requirements"></a><span data-ttu-id="462d1-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="462d1-118">Requirements</span></span>



| <span data-ttu-id="462d1-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="462d1-119">Requirement</span></span> | <span data-ttu-id="462d1-120">Wert</span><span class="sxs-lookup"><span data-stu-id="462d1-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="462d1-121">Version</span><span class="sxs-lookup"><span data-stu-id="462d1-121">Version</span></span><br/>   | <span data-ttu-id="462d1-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="462d1-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="462d1-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="462d1-123">Namespace</span></span><br/> | <span data-ttu-id="462d1-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="462d1-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="462d1-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="462d1-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="462d1-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="462d1-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="462d1-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="462d1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="462d1-128">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="462d1-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="462d1-129">**Iwmpnetwork. BufferingProgress (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="462d1-129">**IWMPNetwork.bufferingProgress (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="462d1-130">**Iwmpnetwork. Download Progress (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="462d1-130">**IWMPNetwork.downloadProgress (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)
</dt> </dl>

 

 





