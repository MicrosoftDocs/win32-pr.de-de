---
title: PositionChange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das Positions Change-Ereignis tritt auf, wenn die aktuelle Wiedergabe Position innerhalb des Medien Elements geändert wurde.
ms.assetid: 92d469b9-813a-4148-be68-0fcef2e41491
keywords:
- Positions Change-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- PositionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 552b748121668e71ee4d2ffb54feed441620a1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354086"
---
# <a name="positionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="c82f0-104">PositionChange-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="c82f0-104">PositionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="c82f0-105">Das Positions Change-Ereignis tritt auf, wenn die aktuelle Wiedergabe Position innerhalb des Medien Elements geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c82f0-105">The PositionChange event occurs when the current playback position within the media item has been changed.</span></span>

``` syntax
[C#]
private void player_PositionChange(
  object sender,
  _WMPOCXEvents_PositionChangeEvent e
)

[Visual Basic]
Private Sub player_PositionChange(  
  sender As Object,
  e As _WMPOCXEvents_PositionChangeEvent
) Handles player.PositionChange
```

## <a name="event-data"></a><span data-ttu-id="c82f0-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="c82f0-106">Event Data</span></span>

<span data-ttu-id="c82f0-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ positionchangeeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="c82f0-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PositionChangeEventHandler**.</span></span> <span data-ttu-id="c82f0-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ PositionChangeEvent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="c82f0-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PositionChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="c82f0-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c82f0-109">Property</span></span>    | <span data-ttu-id="c82f0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c82f0-110">Description</span></span>                                         |
|-------------|-----------------------------------------------------|
| <span data-ttu-id="c82f0-111">oldposition</span><span class="sxs-lookup"><span data-stu-id="c82f0-111">oldPosition</span></span> | <span data-ttu-id="c82f0-112">System. doublegibt die alte Position an.</span><span class="sxs-lookup"><span data-stu-id="c82f0-112">System.DoubleSpecifies the old position.</span></span><br/> |
| <span data-ttu-id="c82f0-113">neuposition</span><span class="sxs-lookup"><span data-stu-id="c82f0-113">newPosition</span></span> | <span data-ttu-id="c82f0-114">System. doublegibt die neue Position an.</span><span class="sxs-lookup"><span data-stu-id="c82f0-114">System.DoubleSpecifies the new position.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c82f0-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c82f0-115">Remarks</span></span>

<span data-ttu-id="c82f0-116">Dieses Ereignis wird während der Wiedergabe nicht routinemäßig ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="c82f0-116">This event is not raised routinely during playback.</span></span> <span data-ttu-id="c82f0-117">Sie tritt nur dann auf, wenn die aktuelle Position des Wiedergabe-Medien Elements aktiv geändert wird, z. b. wenn der Benutzer das Seek-handle verschiebt oder wenn Code ausgeführt wird, der einen Wert für iwmpcontrols angibt. **CurrentPosition**.</span><span class="sxs-lookup"><span data-stu-id="c82f0-117">It only occurs when something actively changes the current position of the playing media item, such as when the user moves the seek handle or when code is executed that specifies a value for IWMPControls.**currentPosition**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c82f0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c82f0-118">Requirements</span></span>



| <span data-ttu-id="c82f0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c82f0-119">Requirement</span></span> | <span data-ttu-id="c82f0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c82f0-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c82f0-121">Version</span><span class="sxs-lookup"><span data-stu-id="c82f0-121">Version</span></span><br/>   | <span data-ttu-id="c82f0-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="c82f0-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c82f0-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="c82f0-123">Namespace</span></span><br/> | <span data-ttu-id="c82f0-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c82f0-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c82f0-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="c82f0-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c82f0-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c82f0-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c82f0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c82f0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c82f0-128">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c82f0-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c82f0-129">**Iwmpcontrols. CurrentPosition (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c82f0-129">**IWMPControls.currentPosition (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





