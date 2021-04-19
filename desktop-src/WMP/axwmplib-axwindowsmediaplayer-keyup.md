---
title: KeyUp-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das KeyUp-Ereignis tritt auf, wenn eine Taste losgelassen wird. | KeyUp-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: db814481-6099-4dbd-8ab1-808e1875ae35
keywords:
- Das KeyUp-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- KeyUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 509f520ff7624b0b29302d7bf5cd825cd45b4254
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370207"
---
# <a name="keyup-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="05a68-105">KeyUp-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="05a68-105">KeyUp Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="05a68-106">Das KeyUp-Ereignis tritt auf, wenn eine Taste losgelassen wird.</span><span class="sxs-lookup"><span data-stu-id="05a68-106">The KeyUp event occurs when a key is released.</span></span>

``` syntax
[C#]
private void player_KeyUpEvent(
  object sender,
  _WMPOCXEvents_KeyUpEvent e
)

[Visual Basic]
Private Sub player_KeyUpEvent(
    sender As Object,
    e As _WMPOCXEvents_KeyUpEvent
) Handles player.KeyUpEvent
```

## <a name="event-data"></a><span data-ttu-id="05a68-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="05a68-107">Event Data</span></span>

<span data-ttu-id="05a68-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ keyugventhandler**.</span><span class="sxs-lookup"><span data-stu-id="05a68-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyUpEventHandler**.</span></span> <span data-ttu-id="05a68-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ keyupeer Vent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="05a68-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyUpEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="05a68-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="05a68-110">Property</span></span>    | <span data-ttu-id="05a68-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05a68-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05a68-112">nKeyCode</span><span class="sxs-lookup"><span data-stu-id="05a68-112">nKeyCode</span></span>    | <span data-ttu-id="05a68-113">System. Int16Specifies der physische Schlüssel, auf den geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="05a68-113">System.Int16Specifies which physical key is pressed.</span></span> <span data-ttu-id="05a68-114">Mögliche Werte finden Sie im Abschnitt "Hinweise" des KeyDown-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="05a68-114">For possible values, see the Remarks section of the KeyDown event.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="05a68-115">nshiftstate</span><span class="sxs-lookup"><span data-stu-id="05a68-115">nShiftState</span></span> | <span data-ttu-id="05a68-116">System. Int16A Bitfeld mit den geringsten signifikanten Bits, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="05a68-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="05a68-117">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="05a68-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="05a68-118">Das Shift-Argument gibt den Zustand dieser Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="05a68-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="05a68-119">Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="05a68-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="05a68-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05a68-120">Requirements</span></span>



| <span data-ttu-id="05a68-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05a68-121">Requirement</span></span> | <span data-ttu-id="05a68-122">Wert</span><span class="sxs-lookup"><span data-stu-id="05a68-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05a68-123">Version</span><span class="sxs-lookup"><span data-stu-id="05a68-123">Version</span></span><br/>   | <span data-ttu-id="05a68-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="05a68-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="05a68-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="05a68-125">Namespace</span></span><br/> | <span data-ttu-id="05a68-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="05a68-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="05a68-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="05a68-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="05a68-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="05a68-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05a68-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05a68-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05a68-130">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="05a68-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





