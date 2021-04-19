---
title: Mediacollectionattributestringchanged-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das mediacollectionattributestringchanged-Ereignis tritt auf, wenn ein Attribut Wert in der Bibliothek geändert wird. | Mediacollectionattributestringchanged-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: f5b91399-42b7-4202-9b65-caa9b15847b9
keywords:
- Mediacollectionattributestringchanged-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b83d8036ca0dca7f79e2a9ba721830447f9c5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365613"
---
# <a name="mediacollectionattributestringchanged-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="cf8fb-105">Mediacollectionattributestringchanged-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="cf8fb-105">MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="cf8fb-106">Das mediacollectionattributestringchanged-Ereignis tritt auf, wenn ein Attribut Wert in der Bibliothek geändert wird.</span><span class="sxs-lookup"><span data-stu-id="cf8fb-106">The MediaCollectionAttributeStringChanged event occurs when an attribute value in the library is changed.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringChanged(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringChanged(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent
) Handles player.MediaCollectionAttributeStringChanged
```

## <a name="event-data"></a><span data-ttu-id="cf8fb-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="cf8fb-107">Event Data</span></span>

<span data-ttu-id="cf8fb-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionattributestringchangedeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="cf8fb-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringChangedEventHandler**.</span></span> <span data-ttu-id="cf8fb-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionattributestringchangedevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="cf8fb-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringChangedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="cf8fb-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cf8fb-110">Property</span></span>         | <span data-ttu-id="cf8fb-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf8fb-111">Description</span></span>                                                                                                                                                                                  |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf8fb-112">bstrattribname</span><span class="sxs-lookup"><span data-stu-id="cf8fb-112">bstrAttribName</span></span>   | <span data-ttu-id="cf8fb-113">System. StringGibt den Namen des Attributs an.</span><span class="sxs-lookup"><span data-stu-id="cf8fb-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="cf8fb-114">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attribut Referenz](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="cf8fb-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="cf8fb-115">bstroldattribval</span><span class="sxs-lookup"><span data-stu-id="cf8fb-115">bstrOldAttribVal</span></span> | <span data-ttu-id="cf8fb-116">System. StringGibt den alten Wert des Attributs an.</span><span class="sxs-lookup"><span data-stu-id="cf8fb-116">System.StringSpecifies the old value of the attribute.</span></span><br/>                                                                                                                            |
| <span data-ttu-id="cf8fb-117">bstraunetwattribval</span><span class="sxs-lookup"><span data-stu-id="cf8fb-117">bstrNewAttribVal</span></span> | <span data-ttu-id="cf8fb-118">System. StringGibt den neuen Wert des Attributs an.</span><span class="sxs-lookup"><span data-stu-id="cf8fb-118">System.StringSpecifies the new value of the attribute.</span></span><br/>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="cf8fb-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf8fb-119">Remarks</span></span>

<span data-ttu-id="cf8fb-120">Wenn ein Benutzer Bibliotheks Metadaten ändert, wird die Mediensammlung aktualisiert, und dieses Ereignis wird für jedes geänderte Attribut ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="cf8fb-120">When a user modifies library metadata, the media collection is updated and this event fires for each attribute changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf8fb-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf8fb-121">Requirements</span></span>



| <span data-ttu-id="cf8fb-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf8fb-122">Requirement</span></span> | <span data-ttu-id="cf8fb-123">Wert</span><span class="sxs-lookup"><span data-stu-id="cf8fb-123">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf8fb-124">Version</span><span class="sxs-lookup"><span data-stu-id="cf8fb-124">Version</span></span><br/>   | <span data-ttu-id="cf8fb-125">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="cf8fb-125">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="cf8fb-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="cf8fb-126">Namespace</span></span><br/> | <span data-ttu-id="cf8fb-127">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="cf8fb-127">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="cf8fb-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="cf8fb-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cf8fb-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cf8fb-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf8fb-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf8fb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf8fb-131">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="cf8fb-131">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf8fb-132">**AxWindowsMediaPlayer. mediacollection (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="cf8fb-132">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf8fb-133">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="cf8fb-133">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





