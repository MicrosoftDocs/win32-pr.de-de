---
title: Warning-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das Warning-Ereignis ist für die zukünftige Verwendung reserviert.
ms.assetid: 3de63756-2726-4864-8988-fd614f23bcad
keywords:
- Warn Ereignis des AxWindowsMediaPlayer-Objekt Windows-Media Player
topic_type:
- apiref
api_name:
- Warning Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a868ba7f619287cd96929c62d89dee3555d908b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352051"
---
# <a name="warning-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="17f87-104">Warning-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="17f87-104">Warning Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="17f87-105">Das Warning-Ereignis ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="17f87-105">The Warning event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_Warning(
  object sender,
  _WMPOCXEvents_WarningEvent e
)

[Visual Basic]
Private Sub player_Warning(
  sender As Object,
  e As _WMPOCXEvents_WarningEvent
) Handles player.Warning
```

## <a name="event-data"></a><span data-ttu-id="17f87-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="17f87-106">Event Data</span></span>

<span data-ttu-id="17f87-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ warningeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="17f87-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_WarningEventHandler**.</span></span> <span data-ttu-id="17f87-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ warningevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="17f87-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_WarningEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="17f87-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="17f87-109">Property</span></span>    | <span data-ttu-id="17f87-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17f87-110">Description</span></span>                                |
|-------------|--------------------------------------------|
| <span data-ttu-id="17f87-111">warningtype</span><span class="sxs-lookup"><span data-stu-id="17f87-111">warningType</span></span> | <span data-ttu-id="17f87-112">**System. Int32** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="17f87-112">**System.Int32** Not supported.</span></span><br/>  |
| <span data-ttu-id="17f87-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="17f87-113">param</span></span>       | <span data-ttu-id="17f87-114">**System. Int32** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="17f87-114">**System.Int32** Not supported.</span></span><br/>  |
| <span data-ttu-id="17f87-115">description</span><span class="sxs-lookup"><span data-stu-id="17f87-115">description</span></span> | <span data-ttu-id="17f87-116">**System. String** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="17f87-116">**System.String** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="17f87-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17f87-117">Remarks</span></span>

<span data-ttu-id="17f87-118">Dieses Ereignis ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="17f87-118">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="17f87-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17f87-119">Requirements</span></span>



| <span data-ttu-id="17f87-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17f87-120">Requirement</span></span> | <span data-ttu-id="17f87-121">Wert</span><span class="sxs-lookup"><span data-stu-id="17f87-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17f87-122">Version</span><span class="sxs-lookup"><span data-stu-id="17f87-122">Version</span></span><br/>   | <span data-ttu-id="17f87-123">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="17f87-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="17f87-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="17f87-124">Namespace</span></span><br/> | <span data-ttu-id="17f87-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="17f87-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="17f87-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="17f87-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="17f87-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="17f87-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17f87-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17f87-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17f87-129">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="17f87-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





