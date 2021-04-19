---
title: Ereignis für die Ereignis Ereignis Änderung des AxWindowsMediaPlayer-Objekts
description: Das Ereignis "Ereignis Ereignisse" tritt auf, wenn sich der Wert von "iwmpcontrols. accesstitem" ändert.
ms.assetid: c5eeafd2-405b-4808-97d1-399a2344ca42
keywords:
- Ereignis für die Ereignis Ereignis Änderung der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- CurrentItemChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c33bb3e9c4c1e512e742c0e679f3c5b53a29735
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366903"
---
# <a name="currentitemchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="63723-104">Ereignis für die Ereignis Ereignis Änderung des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="63723-104">CurrentItemChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="63723-105">Das Ereignis "Ereignis Ereignisse" tritt auf, wenn der Wert von "iwmpcontrols" lautet. das Ereignis **wird geändert.**</span><span class="sxs-lookup"><span data-stu-id="63723-105">The CurrentItemChange event occurs when the value of IWMPControls.**currentItem** changes.</span></span>

``` syntax
[C#]
private void player_CurrentItemChange(
  object sender,
  _WMPOCXEvents_CurrentItemChangeEvent e
)

[Visual Basic]
Private Sub player_CurrentItemChange(  
  sender As Object,
  e As _WMPOCXEvents_CurrentItemChangeEvent
) Handles player.CurrentItemChange
```

## <a name="event-data"></a><span data-ttu-id="63723-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="63723-106">Event Data</span></span>

<span data-ttu-id="63723-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ anwendungtemchangeeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="63723-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentItemChangeEventHandler**.</span></span> <span data-ttu-id="63723-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents- \_ Ereignis Ereignis**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="63723-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentItemChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="63723-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="63723-109">Property</span></span>   | <span data-ttu-id="63723-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63723-110">Description</span></span>                                                                                                   |
|------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63723-111">pdispmedia</span><span class="sxs-lookup"><span data-stu-id="63723-111">pdispMedia</span></span> | <span data-ttu-id="63723-112">System. objectdas neue aktuelle Medien Element.</span><span class="sxs-lookup"><span data-stu-id="63723-112">System.ObjectThe new current media item.</span></span> <span data-ttu-id="63723-113">Sie können dies in eine iwmpmedia-Schnittstelle umwandeln, um darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="63723-113">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="63723-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63723-114">Examples</span></span>

<span data-ttu-id="63723-115">Im folgenden Beispiel wird ein Ereignishandler für das Ereignis "Ereignis Ereignisse" veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="63723-115">The following example demonstrates an event handler for the CurrentItemChange event.</span></span> <span data-ttu-id="63723-116">Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="63723-116">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the CurrentItemChange event
player.CurrentItemChange += new AxWMPLib._WMPOCXEvents_CurrentItemChangeEventHandler(player_CurrentItemChange);

private void player_CurrentItemChange(object sender, AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent e)
{
    // Display the name of the new media item.
    mediaText.Text = player.currentMedia.name;
}
```


```VB

Public Sub player_CurrentItemChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent) Handles player.CurrentItemChange

    &#39; Display the name of the new media item.
    mediaText.Text = player.currentMedia.name

End Sub
```





## <a name="requirements"></a><span data-ttu-id="63723-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63723-117">Requirements</span></span>



| <span data-ttu-id="63723-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63723-118">Requirement</span></span> | <span data-ttu-id="63723-119">Wert</span><span class="sxs-lookup"><span data-stu-id="63723-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63723-120">Version</span><span class="sxs-lookup"><span data-stu-id="63723-120">Version</span></span><br/>   | <span data-ttu-id="63723-121">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="63723-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="63723-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="63723-122">Namespace</span></span><br/> | <span data-ttu-id="63723-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="63723-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="63723-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="63723-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="63723-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="63723-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63723-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63723-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63723-127">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="63723-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="63723-128">**Iwmpcontrols. Currency Item (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="63723-128">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="63723-129">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="63723-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





