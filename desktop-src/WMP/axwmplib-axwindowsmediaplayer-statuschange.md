---
title: StatusChange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das statusChange-Ereignis tritt auf, wenn sich der Wert der Status-Eigenschaft ändert. | StatusChange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 5295fccb-7be0-46d3-85ba-b481e575d393
keywords:
- StatusChange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- StatusChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3ef3224afadb1f98a3067913a8beb095d4e46e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364978"
---
# <a name="statuschange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="c4e3a-105">StatusChange-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="c4e3a-105">StatusChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="c4e3a-106">Das **statusChange** -Ereignis tritt auf, wenn sich der Wert der **Status** -Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="c4e3a-106">The **StatusChange** event occurs when the **status** property changes value.</span></span>

``` syntax
[C#]
private void player_StatusChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_StatusChange(
  sender As Object,
  e As System.EventArgs
) Handles player.StatusChange
```

## <a name="event-data"></a><span data-ttu-id="c4e3a-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="c4e3a-107">Event Data</span></span>

<span data-ttu-id="c4e3a-108">Dieses Ereignis enthält keine Daten.</span><span class="sxs-lookup"><span data-stu-id="c4e3a-108">This event does not contain data.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4e3a-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4e3a-109">Requirements</span></span>



| <span data-ttu-id="c4e3a-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4e3a-110">Requirement</span></span> | <span data-ttu-id="c4e3a-111">Wert</span><span class="sxs-lookup"><span data-stu-id="c4e3a-111">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4e3a-112">Version</span><span class="sxs-lookup"><span data-stu-id="c4e3a-112">Version</span></span><br/>   | <span data-ttu-id="c4e3a-113">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="c4e3a-113">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c4e3a-114">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4e3a-114">Namespace</span></span><br/> | <span data-ttu-id="c4e3a-115">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c4e3a-115">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c4e3a-116">Assembly</span><span class="sxs-lookup"><span data-stu-id="c4e3a-116">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c4e3a-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c4e3a-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4e3a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4e3a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4e3a-119">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c4e3a-119">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c4e3a-120">**AxWindowsMediaPlayer. Status (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c4e3a-120">**AxWindowsMediaPlayer.status (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)
</dt> </dl>

 

 





