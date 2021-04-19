---
title: Click-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das Click-Ereignis tritt auf, wenn der Benutzer auf eine Maustaste in einem Windows Media Player-Steuerelement klickt.
ms.assetid: 41a719a2-103a-46b5-806d-5c21c4a09e00
keywords:
- Das Click-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- Click Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d316e5dc4c12e75d75dd0b292c1df6db974bc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371961"
---
# <a name="click-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="374fd-104">Click-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="374fd-104">Click Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="374fd-105">Das Click-Ereignis tritt auf, wenn der Benutzer auf eine Maustaste in einem Windows Media Player-Steuerelement klickt.</span><span class="sxs-lookup"><span data-stu-id="374fd-105">The Click event occurs when the user clicks a mouse button on a Windows Media Player control.</span></span>

``` syntax
[C#]
private void player_OnClick(
  object  sender,
  _WMPOCXEvents_ClickEvent e
);

[Visual Basic]
Private Sub player_OnClick(  
  sender As Object,
  e As WMPOCXEvents_ClickEvent
) Handles player.ClickEvent
```

## <a name="event-data"></a><span data-ttu-id="374fd-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="374fd-106">Event Data</span></span>

<span data-ttu-id="374fd-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ ClickEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="374fd-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ClickEventHandler**.</span></span> <span data-ttu-id="374fd-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ ClickEvent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="374fd-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ClickEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="374fd-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="374fd-109">Property</span></span>    | <span data-ttu-id="374fd-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="374fd-110">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="374fd-111">nschaltfläche</span><span class="sxs-lookup"><span data-stu-id="374fd-111">nButton</span></span>     | <span data-ttu-id="374fd-112">System. Int16A Bitfeld mit Bits, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="374fd-112">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="374fd-113">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="374fd-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="374fd-114">Es wird nur einer der Bits festgelegt, der die Schaltfläche angibt, die das Ereignis verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="374fd-114">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="374fd-115">nshiftstate</span><span class="sxs-lookup"><span data-stu-id="374fd-115">nShiftState</span></span> | <span data-ttu-id="374fd-116">System. Int16A Bitfeld mit den geringsten signifikanten Bits, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="374fd-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="374fd-117">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="374fd-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="374fd-118">Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="374fd-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="374fd-119">Designer</span><span class="sxs-lookup"><span data-stu-id="374fd-119">fX</span></span>          | <span data-ttu-id="374fd-120">System. Int32The x-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="374fd-120">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="374fd-121">herrlichen</span><span class="sxs-lookup"><span data-stu-id="374fd-121">fY</span></span>          | <span data-ttu-id="374fd-122">System. Int32The y-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="374fd-122">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="374fd-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="374fd-123">Requirements</span></span>



| <span data-ttu-id="374fd-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="374fd-124">Requirement</span></span> | <span data-ttu-id="374fd-125">Wert</span><span class="sxs-lookup"><span data-stu-id="374fd-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="374fd-126">Version</span><span class="sxs-lookup"><span data-stu-id="374fd-126">Version</span></span><br/>   | <span data-ttu-id="374fd-127">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="374fd-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="374fd-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="374fd-128">Namespace</span></span><br/> | <span data-ttu-id="374fd-129">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="374fd-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="374fd-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="374fd-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="374fd-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="374fd-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="374fd-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="374fd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="374fd-133">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="374fd-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





