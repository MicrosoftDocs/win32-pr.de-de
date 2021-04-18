---
title: IMsRdpClientAdvancedSettings7 videoplaybackmode (Eigenschaft)
description: Gibt einen Wert an, der den Videowiedergabe Modus angibt, oder ruft ihn ab.
ms.assetid: 83f0baa3-3ac2-47ee-b106-5beaf60d73d2
ms.tgt_platform: multiple
keywords:
- Videoplaybackmode-Eigenschaft Remotedesktopdienste
- Videoplaybackmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, videoplaybackmode (Eigenschaft)
- Videoplaybackmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, videoplaybackmode (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.put_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.put_VideoPlaybackMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f864224f402814ada268b9b7cbc85ec115a1fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392226"
---
# <a name="imsrdpclientadvancedsettings7videoplaybackmode-property"></a><span data-ttu-id="9bf0c-108">IMsRdpClientAdvancedSettings7:: videoplaybackmode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9bf0c-108">IMsRdpClientAdvancedSettings7::VideoPlaybackMode property</span></span>

<span data-ttu-id="9bf0c-109">Gibt einen Wert an, der den Videowiedergabe Modus angibt, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="9bf0c-109">Specifies or retrieves a value that indicates the video playback mode.</span></span>

<span data-ttu-id="9bf0c-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="9bf0c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bf0c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bf0c-111">Syntax</span></span>


```C++
HRESULT put_VideoPlaybackMode(
  [in]          UINT videoPlaybackMode
);

HRESULT get_VideoPlaybackMode(
  [out, retval] UINT *pVideoPlaybackMode
);
```



## <a name="property-value"></a><span data-ttu-id="9bf0c-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9bf0c-112">Property value</span></span>

<span data-ttu-id="9bf0c-113">Ein-Wert, der den Videowiedergabe Modus angibt.</span><span class="sxs-lookup"><span data-stu-id="9bf0c-113">A value that specifies the video playback mode.</span></span>

<span data-ttu-id="9bf0c-114">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="9bf0c-114">The possible values are:</span></span>

<dt>

<span data-ttu-id="9bf0c-115">1</span><span class="sxs-lookup"><span data-stu-id="9bf0c-115">1</span></span>
</dt> <dd>

<span data-ttu-id="9bf0c-116">Der Standardmodus für die Videowiedergabe.</span><span class="sxs-lookup"><span data-stu-id="9bf0c-116">The default video playback mode.</span></span> <span data-ttu-id="9bf0c-117">Wenn der Videowiedergabe Modus auf diesen Wert festgelegt ist, wird die Video Umleitung von der [**audioredirectionmode**](imsrdpclientsecuredsettings-autoredirectionmode.md) -Eigenschaft gesteuert.</span><span class="sxs-lookup"><span data-stu-id="9bf0c-117">When the video playback mode is set to this value, video redirection is controlled by the [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) property.</span></span> <span data-ttu-id="9bf0c-118">Wenn die **audioredirectionmode** -Eigenschaft auf **audiomodusumleitung \_ \_** festgelegt ist, wird das Video decodiert und auf dem Client gerendert.</span><span class="sxs-lookup"><span data-stu-id="9bf0c-118">When the **AudioRedirectionMode** property is set to **AUDIO\_MODE\_REDIRECT**, video is decoded and rendered on the client.</span></span>

</dd> <dt>

<span data-ttu-id="9bf0c-119">0</span><span class="sxs-lookup"><span data-stu-id="9bf0c-119">0</span></span>
</dt> <dd>

<span data-ttu-id="9bf0c-120">Die Umleitung der Video Wiedergabe ist deaktiviert, auch wenn [**audioredirectionmode**](imsrdpclientsecuredsettings-autoredirectionmode.md) auf **audiomodusumleitung \_ \_** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9bf0c-120">Video playback redirection is disabled, even when [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) is set to **AUDIO\_MODE\_REDIRECT**.</span></span> <span data-ttu-id="9bf0c-121">In diesem Modus wird das Video auf dem RD-Sitzungshost Server decodiert und gerendert.</span><span class="sxs-lookup"><span data-stu-id="9bf0c-121">In this mode, video is decoded and rendered on the RD Session Host server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9bf0c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9bf0c-122">Requirements</span></span>



| <span data-ttu-id="9bf0c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9bf0c-123">Requirement</span></span> | <span data-ttu-id="9bf0c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9bf0c-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf0c-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9bf0c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9bf0c-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9bf0c-126">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="9bf0c-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9bf0c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9bf0c-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9bf0c-128">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="9bf0c-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9bf0c-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="9bf0c-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bf0c-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="9bf0c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9bf0c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bf0c-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bf0c-132"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="9bf0c-133">IID</span><span class="sxs-lookup"><span data-stu-id="9bf0c-133">IID</span></span><br/>                      | <span data-ttu-id="9bf0c-134">IID \_ IMsRdpClientAdvancedSettings7 wird als 26036036-4010-4578-8091-0db9a1edf-C3 definiert.</span><span class="sxs-lookup"><span data-stu-id="9bf0c-134">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9bf0c-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bf0c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bf0c-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="9bf0c-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="9bf0c-137">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9bf0c-137">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





