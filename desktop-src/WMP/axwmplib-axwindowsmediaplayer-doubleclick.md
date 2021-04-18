---
title: DoubleClick-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das Double Click-Ereignis tritt auf, wenn der Benutzer auf eine Maustaste in einem Windows Media Player-Steuerelement doppelklickt.
ms.assetid: 4f116d8a-1ad5-443a-9c91-66214bbdebcf
keywords:
- Das Double Click-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- DoubleClick Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ac809e8ea61b3abbbc964f6dc9ee2976442fc31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358388"
---
# <a name="doubleclick-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="13275-104">DoubleClick-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="13275-104">DoubleClick Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="13275-105">Das Double Click-Ereignis tritt auf, wenn der Benutzer auf eine Maustaste in einem Windows Media Player-Steuerelement doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="13275-105">The DoubleClick event occurs when the user double-clicks a mouse button on a Windows Media Player control.</span></span>

``` syntax
[C#]
private void player_DoubleClickEvent(
  object sender,
  _WMPOCXEvents_DoubleClickEvent e
)

[Visual Basic]
Private Sub player_DoubleClickEvent(  
  sender As Object,  
  e As _WMPOCXEvents_DoubleClickEvent
) Handles player.DoubleClickEvent
```

## <a name="event-data"></a><span data-ttu-id="13275-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="13275-106">Event Data</span></span>

<span data-ttu-id="13275-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ doubleclickeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="13275-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DoubleClickEventHandler**.</span></span> <span data-ttu-id="13275-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ doubleclickevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="13275-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DoubleClickEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="13275-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="13275-109">Property</span></span>    | <span data-ttu-id="13275-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13275-110">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13275-111">nschaltfläche</span><span class="sxs-lookup"><span data-stu-id="13275-111">nButton</span></span>     | <span data-ttu-id="13275-112">System. Int16A Bitfeld mit Bits, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="13275-112">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="13275-113">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="13275-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="13275-114">Es wird nur einer der Bits festgelegt, der die Schaltfläche angibt, die das Ereignis verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="13275-114">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="13275-115">nshiftstate</span><span class="sxs-lookup"><span data-stu-id="13275-115">nShiftState</span></span> | <span data-ttu-id="13275-116">System. Int16A Bitfeld mit den geringsten signifikanten Bits, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="13275-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="13275-117">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="13275-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="13275-118">Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="13275-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="13275-119">Designer</span><span class="sxs-lookup"><span data-stu-id="13275-119">fX</span></span>          | <span data-ttu-id="13275-120">System. Int32The x-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="13275-120">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="13275-121">herrlichen</span><span class="sxs-lookup"><span data-stu-id="13275-121">fY</span></span>          | <span data-ttu-id="13275-122">System. Int32The y-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="13275-122">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="13275-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13275-123">Requirements</span></span>



| <span data-ttu-id="13275-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13275-124">Requirement</span></span> | <span data-ttu-id="13275-125">Wert</span><span class="sxs-lookup"><span data-stu-id="13275-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13275-126">Version</span><span class="sxs-lookup"><span data-stu-id="13275-126">Version</span></span><br/>   | <span data-ttu-id="13275-127">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="13275-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="13275-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="13275-128">Namespace</span></span><br/> | <span data-ttu-id="13275-129">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="13275-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="13275-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="13275-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="13275-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="13275-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13275-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13275-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13275-133">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="13275-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





