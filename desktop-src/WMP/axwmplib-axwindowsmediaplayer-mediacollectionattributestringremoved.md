---
title: Mediacollectionattributestraningrebewegereignis des AxWindowsMediaPlayer-Objekts
description: Das Ereignis mediacollectionattributestraningrebewegt tritt auf, wenn ein Attribut Wert aus der Bibliothek entfernt wird. | Mediacollectionattributestraningrebewegereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 2f264416-0bc5-41d0-8863-32c284393082
keywords:
- Mediacollectionattributestraningreverschogereignis der "AxWindowsMediaPlayer"-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b6b028a2a47585b06159ed46b986124583950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370549"
---
# <a name="mediacollectionattributestringremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="b4651-105">Mediacollectionattributestraningrebewegereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="b4651-105">MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="b4651-106">Das Ereignis mediacollectionattributestraningrebewegt tritt auf, wenn ein Attribut Wert aus der Bibliothek entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b4651-106">The MediaCollectionAttributeStringRemoved event occurs when an attribute value is removed from the library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent
) Handles player.MediaCollectionAttributeStringRemoved
```

## <a name="event-data"></a><span data-ttu-id="b4651-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="b4651-107">Event Data</span></span>

<span data-ttu-id="b4651-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionattributestrauingrefivedeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="b4651-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringRemovedEventHandler**.</span></span> <span data-ttu-id="b4651-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionattributestrauingremuvedevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="b4651-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringRemovedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="b4651-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b4651-110">Property</span></span>           | <span data-ttu-id="b4651-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4651-111">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4651-112">**bstrattribname**</span><span class="sxs-lookup"><span data-stu-id="b4651-112">**bstrAttribName**</span></span> | <span data-ttu-id="b4651-113">System. StringGibt den Namen des Attributs an.</span><span class="sxs-lookup"><span data-stu-id="b4651-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="b4651-114">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attribut Referenz](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="b4651-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="b4651-115">bstrattribval</span><span class="sxs-lookup"><span data-stu-id="b4651-115">bstrAttribVal</span></span>      | <span data-ttu-id="b4651-116">System. StringGibt den Wert des Attributs an.</span><span class="sxs-lookup"><span data-stu-id="b4651-116">System.StringSpecifies the value of the attribute.</span></span><br/>                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="b4651-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4651-117">Remarks</span></span>

<span data-ttu-id="b4651-118">Wenn ein Medien Element aus der Bibliothek entfernt wird, werden die zugehörigen Metadaten aus der **mediacollection** entfernt, und dieses Ereignis wird für jedes entfernte Attribut ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b4651-118">When a media item is removed from the library, its metadata is removed from the **MediaCollection** and this event is fired for each attribute removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4651-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4651-119">Requirements</span></span>



| <span data-ttu-id="b4651-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4651-120">Requirement</span></span> | <span data-ttu-id="b4651-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b4651-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4651-122">Version</span><span class="sxs-lookup"><span data-stu-id="b4651-122">Version</span></span><br/>   | <span data-ttu-id="b4651-123">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="b4651-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="b4651-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="b4651-124">Namespace</span></span><br/> | <span data-ttu-id="b4651-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="b4651-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b4651-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="b4651-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b4651-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b4651-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4651-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4651-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4651-129">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b4651-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b4651-130">**AxWindowsMediaPlayer. mediacollection (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b4651-130">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b4651-131">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b4651-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





