---
title: Durationunitchange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das durationunitchange-Ereignis ist für die zukünftige Verwendung reserviert.
ms.assetid: d8d7da21-bc61-49f8-91bd-4c232295c1ac
keywords:
- Das durationunitchange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- DurationUnitChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f90aa052c61893d83683d10f482cd05841a49fab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365175"
---
# <a name="durationunitchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="709fd-104">Durationunitchange-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="709fd-104">DurationUnitChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="709fd-105">Das durationunitchange-Ereignis ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="709fd-105">The DurationUnitChange event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_DurationUnitChange(
  object sender,
  _WMPOCXEvents_DurationUnitChangeEvent e
)

[Visual Basic]
Private Sub player_DurationUnitChange(  
  sender As Object,  
  e As _WMPOCXEvents_DurationUnitChangeEvent
) Handles player.DurationUnitChange
```

## <a name="event-data"></a><span data-ttu-id="709fd-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="709fd-106">Event Data</span></span>

<span data-ttu-id="709fd-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ durationunitchangeeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="709fd-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DurationUnitChangeEventHandler**.</span></span> <span data-ttu-id="709fd-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ durationunitchangeevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="709fd-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DurationUnitChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="709fd-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="709fd-109">Property</span></span>        | <span data-ttu-id="709fd-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="709fd-110">Description</span></span>                               |
|-----------------|-------------------------------------------|
| <span data-ttu-id="709fd-111">newdurationunit</span><span class="sxs-lookup"><span data-stu-id="709fd-111">newDurationUnit</span></span> | <span data-ttu-id="709fd-112">**System. Int32** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="709fd-112">**System.Int32** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="709fd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="709fd-113">Remarks</span></span>

<span data-ttu-id="709fd-114">Dieses Ereignis ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="709fd-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="709fd-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="709fd-115">Requirements</span></span>



| <span data-ttu-id="709fd-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="709fd-116">Requirement</span></span> | <span data-ttu-id="709fd-117">Wert</span><span class="sxs-lookup"><span data-stu-id="709fd-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="709fd-118">Version</span><span class="sxs-lookup"><span data-stu-id="709fd-118">Version</span></span><br/>   | <span data-ttu-id="709fd-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="709fd-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="709fd-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="709fd-120">Namespace</span></span><br/> | <span data-ttu-id="709fd-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="709fd-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="709fd-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="709fd-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="709fd-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="709fd-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="709fd-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="709fd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="709fd-125">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="709fd-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





