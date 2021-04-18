---
title: Iwmpsettings Autostart (Eigenschaft)
description: Mit der Autostart-Eigenschaft wird ein Wert abgerufen oder festgelegt, der angibt, ob das aktuelle Medien Element automatisch wiedergegeben wird.
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- Autostart-Eigenschaften Fenster Media Player
- AutoStart-Eigenschaft, Windows Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows Media Player, AutoStart-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPSettings.autoStart
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf6c1fb43107df11462737286e26fa7801360d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360930"
---
# <a name="iwmpsettingsautostart-property"></a><span data-ttu-id="70c0a-106">Iwmpsettings:: AutoStart-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="70c0a-106">IWMPSettings::autoStart property</span></span>

<span data-ttu-id="70c0a-107">Mit der **Autostart** -Eigenschaft wird ein Wert abgerufen oder festgelegt, der angibt, ob das aktuelle Medien Element automatisch wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="70c0a-107">The **autoStart** property gets or sets a value indicating whether the current media item begins playing automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="70c0a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="70c0a-108">Syntax</span></span>


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="70c0a-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="70c0a-109">Property value</span></span>

<span data-ttu-id="70c0a-110">Ein **System. Boolean** -Wert, der angibt, ob das aktuelle Medien Element automatisch wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="70c0a-110">A **System.Boolean** value that indicates whether the current media item begins playing automatically.</span></span> <span data-ttu-id="70c0a-111">Der Standardwert ist **true**.</span><span class="sxs-lookup"><span data-stu-id="70c0a-111">The default is **true**.</span></span>

## <a name="remarks"></a><span data-ttu-id="70c0a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70c0a-112">Remarks</span></span>

<span data-ttu-id="70c0a-113">Wenn **Autostart** auf **true** festgelegt ist, wird das Medien Element abgespielt, wenn **AxWindowsMediaPlayer. URL**, **AxWindowsMediaPlayer. currentwiedergabe** oder **AxWindowsMediaPlayer. currentMedia** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="70c0a-113">If **autoStart** is set to **true**, the media item will begin playing when **AxWindowsMediaPlayer.URL**, **AxWindowsMediaPlayer.currentPlaylist**, or **AxWindowsMediaPlayer.currentMedia** is set.</span></span> <span data-ttu-id="70c0a-114">Andernfalls wird das Medien Element erst wieder abgespielt, wenn die **iwmpcontrols. Play** -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="70c0a-114">Otherwise, the media item will not start playing until the **IWMPControls.play** method is called.</span></span>

<span data-ttu-id="70c0a-115">Wenn Sie " **Autostart** " nicht unmittelbar vor der Angabe eines Medien Elements auf " **true** " festlegen, sollten Sie diese Einstellung nicht als Ersatz für die Verwendung der **iwmpcontrols. Play** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="70c0a-115">Unless you set **autoStart** to **true** immediately before specifying a media item, you should not rely on this setting as a substitute for using the **IWMPControls.play** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="70c0a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70c0a-116">Requirements</span></span>



| <span data-ttu-id="70c0a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70c0a-117">Requirement</span></span> | <span data-ttu-id="70c0a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="70c0a-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70c0a-119">Version</span><span class="sxs-lookup"><span data-stu-id="70c0a-119">Version</span></span><br/>   | <span data-ttu-id="70c0a-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="70c0a-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="70c0a-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="70c0a-121">Namespace</span></span><br/> | <span data-ttu-id="70c0a-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="70c0a-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="70c0a-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="70c0a-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="70c0a-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="70c0a-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70c0a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70c0a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70c0a-126">**AxWindowsMediaPlayer. currentMedia (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="70c0a-126">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="70c0a-127">**AxWindowsMediaPlayer. currentwiedergabe (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="70c0a-127">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="70c0a-128">**AxWindowsMediaPlayer. URL (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="70c0a-128">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="70c0a-129">**Iwmpcontrols. Play (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="70c0a-129">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="70c0a-130">**Iwmpsettings-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="70c0a-130">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





