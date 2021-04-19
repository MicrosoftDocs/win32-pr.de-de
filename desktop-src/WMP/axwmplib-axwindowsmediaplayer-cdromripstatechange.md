---
title: Cdromripstatechange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das cdromripstatechange-Ereignis tritt auf, wenn sich der Zustand eines CD-einreißen-Vorgangs ändert.
ms.assetid: 0a0bd11f-a685-4c4e-8704-8eabe80d6f86
keywords:
- Cdromripstatechange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- CdromRipStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20fae9eb1fa6d5f65876e3f6758a7594f0bdbb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373558"
---
# <a name="cdromripstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="71096-104">Cdromripstatechange-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="71096-104">CdromRipStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="71096-105">Das cdromripstatechange-Ereignis tritt auf, wenn sich der Zustand eines CD-einreißen-Vorgangs ändert.</span><span class="sxs-lookup"><span data-stu-id="71096-105">The CdromRipStateChange event occurs when a CD ripping operation changes state.</span></span>

``` syntax
[C#]
private void player_CdromRipStateChange(
  object sender,
  _WMPOCXEvents_CdromRipStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromRipStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromRipStateChangeEvent
) Handles player.CdromRipStateChange
```

## <a name="event-data"></a><span data-ttu-id="71096-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="71096-106">Event Data</span></span>

<span data-ttu-id="71096-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromripstatechangeeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="71096-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromRipStateChangeEventHandler**.</span></span> <span data-ttu-id="71096-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromripstatechangeevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="71096-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromRipStateChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="71096-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="71096-109">Property</span></span>  | <span data-ttu-id="71096-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71096-110">Description</span></span>                                                                                              |
|-----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71096-111">pcdromrip</span><span class="sxs-lookup"><span data-stu-id="71096-111">pCdromRip</span></span> | <span data-ttu-id="71096-112">WMPLib. iwmpcdromripdie Schnittstelle, die den einreißen-Vorgang darstellt, der den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="71096-112">WMPLib.IWMPCdromRipThe interface that represents the ripping operation that raised the error.</span></span><br/> |
| <span data-ttu-id="71096-113">wmprs</span><span class="sxs-lookup"><span data-stu-id="71096-113">wmprs</span></span>     | <span data-ttu-id="71096-114">WMPLib. wmpripstateder Enumerationswert, der den neuen Zustand angibt.</span><span class="sxs-lookup"><span data-stu-id="71096-114">WMPLib.WMPRipStateThe enumeration value that indicates the new state.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="71096-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71096-115">Requirements</span></span>



| <span data-ttu-id="71096-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71096-116">Requirement</span></span> | <span data-ttu-id="71096-117">Wert</span><span class="sxs-lookup"><span data-stu-id="71096-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71096-118">Version</span><span class="sxs-lookup"><span data-stu-id="71096-118">Version</span></span><br/>   | <span data-ttu-id="71096-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="71096-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="71096-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="71096-120">Namespace</span></span><br/> | <span data-ttu-id="71096-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="71096-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="71096-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="71096-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="71096-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="71096-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71096-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71096-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71096-125">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="71096-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="71096-126">**Iwmpcdromrip-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="71096-126">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="71096-127">**Wmpripstate**</span><span class="sxs-lookup"><span data-stu-id="71096-127">**WMPRipState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)
</dt> </dl>

 

 





