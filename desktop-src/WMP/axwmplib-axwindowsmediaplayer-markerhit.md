---
title: Markerhit-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das markerhit-Ereignis tritt auf, wenn ein Marker erreicht wird. | Markerhit-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 247fc22c-18c4-46b6-b42c-4882209a47f4
keywords:
- Markerhit-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MarkerHit Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03bad8d9d64b4711937cd984bbd9d335acebfe67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370772"
---
# <a name="markerhit-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="12e86-105">Markerhit-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="12e86-105">MarkerHit Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="12e86-106">Das markerhit-Ereignis tritt auf, wenn ein Marker erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="12e86-106">The MarkerHit event occurs when a marker is reached.</span></span>

``` syntax
[C#]
private void player_MarkerHit(
  object sender,
  _WMPOCXEvents_MarkerHitEvent e
)

[Visual Basic]
Private Sub player_MarkerHit(  
  sender As Object,  
  e As _WMPOCXEvents_MarkerHitEvent
) Handles player.MarkerHit
```

## <a name="event-data"></a><span data-ttu-id="12e86-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="12e86-107">Event Data</span></span>

<span data-ttu-id="12e86-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ MarkerHitEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="12e86-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MarkerHitEventHandler**.</span></span> <span data-ttu-id="12e86-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ MarkerHitEvent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="12e86-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MarkerHitEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="12e86-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="12e86-110">Property</span></span>      | <span data-ttu-id="12e86-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12e86-111">Description</span></span>                                                             |
|---------------|-------------------------------------------------------------------------|
| <span data-ttu-id="12e86-112">**Markernum**</span><span class="sxs-lookup"><span data-stu-id="12e86-112">**MarkerNum**</span></span> | <span data-ttu-id="12e86-113">System. Int32Indicates die Nummer der Markierung, die getroffen wurde.</span><span class="sxs-lookup"><span data-stu-id="12e86-113">System.Int32Indicates the number of the marker that was hit.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="12e86-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12e86-114">Requirements</span></span>



| <span data-ttu-id="12e86-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12e86-115">Requirement</span></span> | <span data-ttu-id="12e86-116">Wert</span><span class="sxs-lookup"><span data-stu-id="12e86-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12e86-117">Version</span><span class="sxs-lookup"><span data-stu-id="12e86-117">Version</span></span><br/>   | <span data-ttu-id="12e86-118">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="12e86-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="12e86-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="12e86-119">Namespace</span></span><br/> | <span data-ttu-id="12e86-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="12e86-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="12e86-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="12e86-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="12e86-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="12e86-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12e86-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12e86-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e86-124">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="12e86-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





