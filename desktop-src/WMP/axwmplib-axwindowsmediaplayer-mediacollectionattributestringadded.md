---
title: Mediacollectionattributestringadded-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das mediacollectionattributestringadded-Ereignis tritt auf, wenn der Bibliothek ein Attribut Wert hinzugefügt wird. | Mediacollectionattributestringadded-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: b14db0ce-bd78-4e28-a42c-1a231c29da2b
keywords:
- Mediacollectionattributestringadded-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6712b6caa8f014ec75bf2b031e2d3f6db429dbd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371996"
---
# <a name="mediacollectionattributestringadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="ee32f-105">Mediacollectionattributestringadded-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="ee32f-105">MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="ee32f-106">Das mediacollectionattributestringadded-Ereignis tritt auf, wenn der Bibliothek ein Attribut Wert hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ee32f-106">The MediaCollectionAttributeStringAdded event occurs when an attribute value is added to the library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent
) Handles player.MediaCollectionAttributeStringAdded
```

## <a name="event-data"></a><span data-ttu-id="ee32f-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="ee32f-107">Event Data</span></span>

<span data-ttu-id="ee32f-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionattributestringaddedeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="ee32f-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringAddedEventHandler**.</span></span> <span data-ttu-id="ee32f-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionattributestringaddedevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="ee32f-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringAddedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="ee32f-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ee32f-110">Property</span></span>           | <span data-ttu-id="ee32f-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee32f-111">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee32f-112">**bstrattribname**</span><span class="sxs-lookup"><span data-stu-id="ee32f-112">**bstrAttribName**</span></span> | <span data-ttu-id="ee32f-113">System. StringGibt den Namen des Attributs an.</span><span class="sxs-lookup"><span data-stu-id="ee32f-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="ee32f-114">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attribut Referenz](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ee32f-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="ee32f-115">bstrattribval</span><span class="sxs-lookup"><span data-stu-id="ee32f-115">bstrAttribVal</span></span>      | <span data-ttu-id="ee32f-116">System. StringGibt den Wert des Attributs an.</span><span class="sxs-lookup"><span data-stu-id="ee32f-116">System.StringSpecifies the value of the attribute.</span></span><br/>                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="ee32f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee32f-117">Remarks</span></span>

<span data-ttu-id="ee32f-118">Wenn der Bibliothek ein Medien Element hinzugefügt wird, werden die zugehörigen Metadaten der Medien Auflistung hinzugefügt, und dieses Ereignis wird für jedes hinzugefügte Attribut ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ee32f-118">When a media item is added to the library, its metadata is added to the media collection and this event is fired for each attribute added.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee32f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee32f-119">Requirements</span></span>



| <span data-ttu-id="ee32f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee32f-120">Requirement</span></span> | <span data-ttu-id="ee32f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ee32f-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee32f-122">Version</span><span class="sxs-lookup"><span data-stu-id="ee32f-122">Version</span></span><br/>   | <span data-ttu-id="ee32f-123">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="ee32f-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="ee32f-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee32f-124">Namespace</span></span><br/> | <span data-ttu-id="ee32f-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ee32f-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ee32f-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="ee32f-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ee32f-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ee32f-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee32f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee32f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee32f-129">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ee32f-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ee32f-130">**AxWindowsMediaPlayer. mediacollection (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ee32f-130">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ee32f-131">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ee32f-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





