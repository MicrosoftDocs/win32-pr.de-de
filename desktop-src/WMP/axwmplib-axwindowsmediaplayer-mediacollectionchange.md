---
title: Mediacollectionchange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das mediacollectionchange-Ereignis tritt auf, wenn die Mediensammlung geändert wird. | Mediacollectionchange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 99a6d512-ed8e-4f1b-856a-22ca8092741d
keywords:
- Mediacollectionchange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MediaCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 720207de3475544074b87c56686d0a47da97785c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369222"
---
# <a name="mediacollectionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="8e571-105">Mediacollectionchange-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="8e571-105">MediaCollectionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="8e571-106">Das mediacollectionchange-Ereignis tritt auf, wenn die Mediensammlung geändert wird.</span><span class="sxs-lookup"><span data-stu-id="8e571-106">The MediaCollectionChange event occurs when the media collection changes.</span></span>

``` syntax
[C#]
private void player_MediaCollectionChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_MediaCollectionChange(
  sender As Object,
  e As System.EventArgs
) Handles player.MediaCollectionChange
```

## <a name="event-data"></a><span data-ttu-id="8e571-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="8e571-107">Event Data</span></span>

<span data-ttu-id="8e571-108">Dieses Ereignis enthält keine Daten.</span><span class="sxs-lookup"><span data-stu-id="8e571-108">This event does not contain data.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e571-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e571-109">Requirements</span></span>



| <span data-ttu-id="8e571-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e571-110">Requirement</span></span> | <span data-ttu-id="8e571-111">Wert</span><span class="sxs-lookup"><span data-stu-id="8e571-111">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e571-112">Version</span><span class="sxs-lookup"><span data-stu-id="8e571-112">Version</span></span><br/>   | <span data-ttu-id="8e571-113">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="8e571-113">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="8e571-114">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e571-114">Namespace</span></span><br/> | <span data-ttu-id="8e571-115">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="8e571-115">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="8e571-116">Assembly</span><span class="sxs-lookup"><span data-stu-id="8e571-116">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8e571-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8e571-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e571-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e571-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e571-119">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="8e571-119">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8e571-120">**AxWindowsMediaPlayer. mediacollection (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="8e571-120">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8e571-121">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="8e571-121">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





