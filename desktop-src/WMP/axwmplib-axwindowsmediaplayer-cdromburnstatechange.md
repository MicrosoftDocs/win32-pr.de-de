---
title: Cdromburnstatechange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das cdromburnstatechange-Ereignis tritt auf, wenn sich der Zustand eines CD-Brennvorgangs ändert.
ms.assetid: fec8a8e5-e282-454e-9713-fd9bb131df6a
keywords:
- Cdromburnstatechange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- CdromBurnStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc679a96600bff5aa4ca805018d364a6aeea8174
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355855"
---
# <a name="cdromburnstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="6d702-104">Cdromburnstatechange-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="6d702-104">CdromBurnStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="6d702-105">Das cdromburnstatechange-Ereignis tritt auf, wenn sich der Zustand eines CD-Brennvorgangs ändert.</span><span class="sxs-lookup"><span data-stu-id="6d702-105">The CdromBurnStateChange event occurs when a CD burning operation changes state.</span></span>

``` syntax
[C#]
private void player_CdromBurnStateChange(
  object sender,
  _WMPOCXEvents_CdromBurnStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromBurnStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnStateChangeEvent
) Handles player.CdromBurnStateChange
```

## <a name="event-data"></a><span data-ttu-id="6d702-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="6d702-106">Event Data</span></span>

<span data-ttu-id="6d702-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromburnstatechangeeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="6d702-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnStateChangeEventHandler**.</span></span> <span data-ttu-id="6d702-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromburnstatechangeevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="6d702-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnStateChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="6d702-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6d702-109">Property</span></span>   | <span data-ttu-id="6d702-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d702-110">Description</span></span>                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d702-111">pcdromburn</span><span class="sxs-lookup"><span data-stu-id="6d702-111">pCdromBurn</span></span> | <span data-ttu-id="6d702-112">WMPLib. iwmpcdromburndie-Schnittstelle, die den Brennvorgang darstellt, der den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="6d702-112">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/> |
| <span data-ttu-id="6d702-113">wmpsb</span><span class="sxs-lookup"><span data-stu-id="6d702-113">wmpbs</span></span>      | <span data-ttu-id="6d702-114">WMPLib. wmpburnstateder Enumerationswert, der den neuen Zustand angibt.</span><span class="sxs-lookup"><span data-stu-id="6d702-114">WMPLib.WMPBurnStateThe enumeration value that indicates the new state.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="6d702-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d702-115">Requirements</span></span>



| <span data-ttu-id="6d702-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d702-116">Requirement</span></span> | <span data-ttu-id="6d702-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6d702-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d702-118">Version</span><span class="sxs-lookup"><span data-stu-id="6d702-118">Version</span></span><br/>   | <span data-ttu-id="6d702-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="6d702-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="6d702-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d702-120">Namespace</span></span><br/> | <span data-ttu-id="6d702-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="6d702-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="6d702-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="6d702-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6d702-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6d702-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d702-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d702-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d702-125">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6d702-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6d702-126">**Iwmpcdromburn-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6d702-126">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6d702-127">**Wmpburnstate**</span><span class="sxs-lookup"><span data-stu-id="6d702-127">**WMPBurnState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





