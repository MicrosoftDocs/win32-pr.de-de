---
title: Cdromburnerror-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das cdromburnerror-Ereignis tritt auf, wenn während eines CD-Brennvorgangs ein generischer Fehler auftritt.
ms.assetid: 512a3417-c8f3-42c7-ab2e-bea35cadbd4e
keywords:
- Cdromburnerror-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- CdromBurnError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c27969ea83089b225ba92eb93854fc1dcde9bde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364024"
---
# <a name="cdromburnerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="28fe4-104">Cdromburnerror-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="28fe4-104">CdromBurnError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="28fe4-105">Das cdromburnerror-Ereignis tritt auf, wenn während eines CD-Brennvorgangs ein generischer Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="28fe4-105">The CdromBurnError event occurs when a generic error happens during a CD burning operation.</span></span>

``` syntax
[C#]
private void player_CdromBurnError(
  object sender,
  _WMPOCXEvents_CdromBurnErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnError(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnErrorEvent
) Handles player.CdromBurnError
```

## <a name="event-data"></a><span data-ttu-id="28fe4-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="28fe4-106">Event Data</span></span>

<span data-ttu-id="28fe4-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromburnerroreventhandler**.</span><span class="sxs-lookup"><span data-stu-id="28fe4-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnErrorEventHandler**.</span></span> <span data-ttu-id="28fe4-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromburnerrorevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="28fe4-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="28fe4-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="28fe4-109">Property</span></span>   | <span data-ttu-id="28fe4-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28fe4-110">Description</span></span>                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28fe4-111">hrError</span><span class="sxs-lookup"><span data-stu-id="28fe4-111">hrError</span></span>    | <span data-ttu-id="28fe4-112">**System. Int32** Der Fehler, der das Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="28fe4-112">**System.Int32** The error that raised the event.</span></span><br/>                                               |
| <span data-ttu-id="28fe4-113">pcdromburn</span><span class="sxs-lookup"><span data-stu-id="28fe4-113">pCdromBurn</span></span> | <span data-ttu-id="28fe4-114">WMPLib. iwmpcdromburndie-Schnittstelle, die den Brennvorgang darstellt, der den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="28fe4-114">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="28fe4-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28fe4-115">Remarks</span></span>

<span data-ttu-id="28fe4-116">Um medienspezifische Fehler zu erfassen, behandeln Sie AxWMPLib. \_ Wmpocxevents \_ cdromburnmediaerror-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="28fe4-116">To capture media specific errors, handle the AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaError event.</span></span>

## <a name="requirements"></a><span data-ttu-id="28fe4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28fe4-117">Requirements</span></span>



| <span data-ttu-id="28fe4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28fe4-118">Requirement</span></span> | <span data-ttu-id="28fe4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="28fe4-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28fe4-120">Version</span><span class="sxs-lookup"><span data-stu-id="28fe4-120">Version</span></span><br/>   | <span data-ttu-id="28fe4-121">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="28fe4-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="28fe4-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="28fe4-122">Namespace</span></span><br/> | <span data-ttu-id="28fe4-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="28fe4-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="28fe4-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="28fe4-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="28fe4-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="28fe4-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28fe4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28fe4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28fe4-127">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="28fe4-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="28fe4-128">**AxWindowsMediaPlayer. cdromburnmediaerror-Ereignis (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="28fe4-128">**AxWindowsMediaPlayer.CdromBurnMediaError Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)
</dt> <dt>

[<span data-ttu-id="28fe4-129">**Iwmpcdromburn-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="28fe4-129">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





