---
title: IMsRdpClientAdvancedSettings7 audiocaptureredirectionmode-Eigenschaft
description: Gibt einen booleschen Wert an, der angibt, ob das standardmäßige Audioeingabegerät vom Client an die Remote Sitzung umgeleitet wird, oder ruft diesen ab.
ms.assetid: e75add5e-4652-41a7-b2cb-2c60793cd079
ms.tgt_platform: multiple
keywords:
- Audiocaptureredirectionmode-Eigenschaft Remotedesktopdienste
- Audiocaptureredirectionmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, audiocaptureredirectionmode-Eigenschaft
- Audiocaptureredirectionmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, audiocaptureredirectionmode-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioCaptureRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c752315067ed70103da2e048e9e8f613665ae919
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956674"
---
# <a name="imsrdpclientadvancedsettings7audiocaptureredirectionmode-property"></a><span data-ttu-id="c7714-108">IMsRdpClientAdvancedSettings7:: audiocaptureredirectionmode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c7714-108">IMsRdpClientAdvancedSettings7::AudioCaptureRedirectionMode property</span></span>

<span data-ttu-id="c7714-109">Gibt einen booleschen Wert an, der angibt, ob das standardmäßige Audioeingabegerät vom Client an die Remote Sitzung umgeleitet wird, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="c7714-109">Specifies or retrieves a Boolean value that indicates whether the default audio input device is redirected from the client to the remote session.</span></span>

<span data-ttu-id="c7714-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c7714-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7714-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7714-111">Syntax</span></span>


```C++
HRESULT put_AudioCaptureRedirectionMode(
  [in]          VARIANT_BOOL fRedir
);

HRESULT get_AudioCaptureRedirectionMode(
  [out, retval] VARIANT_BOOL *pfRedir
);
```



## <a name="property-value"></a><span data-ttu-id="c7714-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c7714-112">Property value</span></span>

<span data-ttu-id="c7714-113">Ein **Variant- \_ boolescher** Wert, der angibt, ob die Audioerfassung umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="c7714-113">A **VARIANT\_BOOL** value that specifies whether audio capture is redirected.</span></span> <span data-ttu-id="c7714-114">Geben Sie **Variant \_ true** an, wenn die Audioerfassung umgeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7714-114">Specify **VARIANT\_TRUE** if you want audio capture to be redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7714-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7714-115">Requirements</span></span>



| <span data-ttu-id="c7714-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7714-116">Requirement</span></span> | <span data-ttu-id="c7714-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c7714-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7714-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7714-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c7714-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c7714-119">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="c7714-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7714-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c7714-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c7714-121">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="c7714-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c7714-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="c7714-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7714-123"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c7714-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c7714-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7714-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7714-125"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c7714-126">IID</span><span class="sxs-lookup"><span data-stu-id="c7714-126">IID</span></span><br/>                      | <span data-ttu-id="c7714-127">IID \_ IMsRdpClientAdvancedSettings7 wird als 26036036-4010-4578-8091-0db9a1edf-C3 definiert.</span><span class="sxs-lookup"><span data-stu-id="c7714-127">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7714-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7714-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7714-129">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c7714-129">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c7714-130">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c7714-130">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





