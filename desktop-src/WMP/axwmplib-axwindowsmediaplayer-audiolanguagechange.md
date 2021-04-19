---
title: Audiolanguagechange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das audiolanguagechange-Ereignis tritt auf, wenn sich die aktuelle Audiosprache ändert. | Audiolanguagechange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 35e4ff82-fc59-4d28-b7fc-1527fb46b960
keywords:
- Audiolanguagechange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- AudioLanguageChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354a34f30df237827e3d369721963ec2c1797e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355252"
---
# <a name="audiolanguagechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="69c7a-105">Audiolanguagechange-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="69c7a-105">AudioLanguageChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="69c7a-106">Das audiolanguagechange-Ereignis tritt auf, wenn sich die aktuelle Audiosprache ändert.</span><span class="sxs-lookup"><span data-stu-id="69c7a-106">The AudioLanguageChange event occurs when the current audio language changes.</span></span>

``` syntax
[C#]
private void player_AudioLanguageChange(
  object sender,
  _WMPOCXEvents_AudioLanguageChangeEvent e
)

[Visual Basic]
Private Sub player_AudioLanguageChange(
  sender As Object,
  e As _WMPOCXEvents_AudioLanguageChangeEvent
) Handles player.AudioLanguageChange
```

## <a name="event-data"></a><span data-ttu-id="69c7a-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="69c7a-107">Event Data</span></span>

<span data-ttu-id="69c7a-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ audiolanguagechangeeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="69c7a-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_AudioLanguageChangeEventHandler**.</span></span> <span data-ttu-id="69c7a-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ audiolanguagechangeevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="69c7a-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_AudioLanguageChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="69c7a-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="69c7a-110">Property</span></span>   | <span data-ttu-id="69c7a-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69c7a-111">Description</span></span>                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69c7a-112">**langID**</span><span class="sxs-lookup"><span data-stu-id="69c7a-112">**langID**</span></span> | <span data-ttu-id="69c7a-113">**System. Int32** Identifiziert eindeutig einen bestimmten Sprach Dialekt, der als Gebiets Schema bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="69c7a-113">**System.Int32** Uniquely identifies a particular language dialect, called a locale.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="69c7a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69c7a-114">Remarks</span></span>

<span data-ttu-id="69c7a-115">Ein Gebiets Schema Bezeichner (Locale Identifier, LCID) identifiziert eindeutig einen bestimmten Sprach Dialekt, der als locale bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="69c7a-115">A locale identifier (LCID) uniquely identifies a particular language dialect, called a locale.</span></span>

## <a name="requirements"></a><span data-ttu-id="69c7a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69c7a-116">Requirements</span></span>



| <span data-ttu-id="69c7a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69c7a-117">Requirement</span></span> | <span data-ttu-id="69c7a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="69c7a-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69c7a-119">Version</span><span class="sxs-lookup"><span data-stu-id="69c7a-119">Version</span></span><br/>   | <span data-ttu-id="69c7a-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="69c7a-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="69c7a-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="69c7a-121">Namespace</span></span><br/> | <span data-ttu-id="69c7a-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="69c7a-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="69c7a-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="69c7a-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="69c7a-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="69c7a-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69c7a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69c7a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69c7a-126">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="69c7a-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="69c7a-127">**IWMPControls3. currentaudiolanguage (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="69c7a-127">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> </dl>

 

 





