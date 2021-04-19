---
title: MediaError-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das MediaError-Ereignis tritt auf, wenn ein Medienobjekt einen Fehlerzustand aufweist.
ms.assetid: a1fb3422-85c4-4856-951a-332517599984
keywords:
- MediaError-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 874b9297846a8f25f25c68545df234aa1be70594
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361660"
---
# <a name="mediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="e532a-104">MediaError-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="e532a-104">MediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="e532a-105">Das MediaError-Ereignis tritt auf, wenn ein Medienobjekt einen Fehlerzustand aufweist.</span><span class="sxs-lookup"><span data-stu-id="e532a-105">The MediaError event occurs when a media object has an error condition.</span></span>

``` syntax
[C#]
private void player_MediaError(
  object sender,
  _WMPOCXEvents_MediaErrorEvent e
)

[Visual Basic]
Private Sub player_MediaError(
  sender As Object,
  e As _WMPOCXEvents_MediaErrorEvent
) Handles player.MediaError
```

## <a name="event-data"></a><span data-ttu-id="e532a-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="e532a-106">Event Data</span></span>

<span data-ttu-id="e532a-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediaerroreventhandler**.</span><span class="sxs-lookup"><span data-stu-id="e532a-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaErrorEventHandler**.</span></span> <span data-ttu-id="e532a-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediaerrorevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="e532a-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaErrorEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="e532a-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e532a-109">Property</span></span>     | <span data-ttu-id="e532a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e532a-110">Description</span></span>                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e532a-111">pmediaobject</span><span class="sxs-lookup"><span data-stu-id="e532a-111">pMediaObject</span></span> | <span data-ttu-id="e532a-112">System. objectobject mit einem Fehlerzustand.</span><span class="sxs-lookup"><span data-stu-id="e532a-112">System.ObjectObject that has an error condition.</span></span> <span data-ttu-id="e532a-113">Sie können dies in eine iwmpmedia-Schnittstelle umwandeln, um darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e532a-113">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e532a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e532a-114">Requirements</span></span>



| <span data-ttu-id="e532a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e532a-115">Requirement</span></span> | <span data-ttu-id="e532a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e532a-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e532a-117">Version</span><span class="sxs-lookup"><span data-stu-id="e532a-117">Version</span></span><br/>   | <span data-ttu-id="e532a-118">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="e532a-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="e532a-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="e532a-119">Namespace</span></span><br/> | <span data-ttu-id="e532a-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="e532a-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="e532a-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="e532a-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e532a-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e532a-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e532a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e532a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e532a-124">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e532a-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e532a-125">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e532a-125">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





