---
title: Cdromburnmediaerror-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das cdromburnmediaerror-Ereignis tritt auf, wenn beim Brennen eines einzelnen Medien Elements auf einer CD ein Fehler auftritt.
ms.assetid: 0847a8a2-1fef-41a0-affb-9fa6bd10b925
keywords:
- Cdromburnmediaerror-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- CdromBurnMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d9fac8902fe8700171d2c909e8140c74c8cc3c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365148"
---
# <a name="cdromburnmediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="ca7a8-104">Cdromburnmediaerror-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="ca7a8-104">CdromBurnMediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="ca7a8-105">Das cdromburnmediaerror-Ereignis tritt auf, wenn beim Brennen eines einzelnen Medien Elements auf einer CD ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="ca7a8-105">The CdromBurnMediaError event occurs when an error happens while burning an individual media item to a CD.</span></span>

``` syntax
[C#]
private void player_CdromBurnMediaError(
  object sender,
  _WMPOCXEvents_CdromBurnMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnMediaError(
  sender As Object,
  e As _WMPOCXEvents_CdromBurnMediaErrorEvent
) Handles player.CdromBurnMediaError
```

## <a name="event-data"></a><span data-ttu-id="ca7a8-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="ca7a8-106">Event Data</span></span>

<span data-ttu-id="ca7a8-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromburnmediaerroreventhandler**.</span><span class="sxs-lookup"><span data-stu-id="ca7a8-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaErrorEventHandler**.</span></span> <span data-ttu-id="ca7a8-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromburnmediaerrorevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="ca7a8-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="ca7a8-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ca7a8-109">Property</span></span>   | <span data-ttu-id="ca7a8-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca7a8-110">Description</span></span>                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca7a8-111">pcdromburn</span><span class="sxs-lookup"><span data-stu-id="ca7a8-111">pCdromBurn</span></span> | <span data-ttu-id="ca7a8-112">WMPLib. iwmpcdromburndie-Schnittstelle, die den Brennvorgang darstellt, der den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="ca7a8-112">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/>               |
| <span data-ttu-id="ca7a8-113">pmedia</span><span class="sxs-lookup"><span data-stu-id="ca7a8-113">pMedia</span></span>     | <span data-ttu-id="ca7a8-114">System. objectdas Medien Element, das den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="ca7a8-114">System.ObjectThe media item that raised the error.</span></span> <span data-ttu-id="ca7a8-115">Sie können dies in eine iwmpmedia-Schnittstelle umwandeln, um darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ca7a8-115">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ca7a8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca7a8-116">Remarks</span></span>

<span data-ttu-id="ca7a8-117">Um generische Fehler zu erfassen, behandeln Sie AxWMPLib. \_ Wmpocxevents \_ cdromburnerror-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ca7a8-117">To capture generic errors, handle the AxWMPLib.\_WMPOCXEvents\_CdromBurnError event.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca7a8-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca7a8-118">Requirements</span></span>



| <span data-ttu-id="ca7a8-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca7a8-119">Requirement</span></span> | <span data-ttu-id="ca7a8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ca7a8-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca7a8-121">Version</span><span class="sxs-lookup"><span data-stu-id="ca7a8-121">Version</span></span><br/>   | <span data-ttu-id="ca7a8-122">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="ca7a8-122">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="ca7a8-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca7a8-123">Namespace</span></span><br/> | <span data-ttu-id="ca7a8-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ca7a8-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ca7a8-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="ca7a8-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ca7a8-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ca7a8-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca7a8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca7a8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca7a8-128">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ca7a8-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ca7a8-129">**AxWindowsMediaPlayer. cdromburnerror-Ereignis (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ca7a8-129">**AxWindowsMediaPlayer.CdromBurnError Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-cdromburnerror.md)
</dt> <dt>

[<span data-ttu-id="ca7a8-130">**Iwmpcdromburn-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ca7a8-130">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ca7a8-131">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ca7a8-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





