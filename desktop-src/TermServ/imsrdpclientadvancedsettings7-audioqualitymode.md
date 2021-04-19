---
title: IMsRdpClientAdvancedSettings7 audioqualitymode (Eigenschaft)
description: Gibt einen Wert an oder ruft ihn ab, der die Einstellung für den audioqualitätsmodus für umgeleitete Audiodaten angibt Standardmäßig ist dieser Wert auf 0 festgelegt.
ms.assetid: 9945c524-ca50-41ae-a7cf-1386cd758c0f
ms.tgt_platform: multiple
keywords:
- Audioqualitymode-Eigenschaft Remotedesktopdienste
- Audioqualitymode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, audioqualitymode-Eigenschaft
- Audioqualitymode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, audioqualitymode-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioQualityMode
- IMsRdpClientAdvancedSettings7.get_AudioQualityMode
- IMsRdpClientAdvancedSettings7.put_AudioQualityMode
- IMsRdpClientAdvancedSettings8.AudioQualityMode
- IMsRdpClientAdvancedSettings8.get_AudioQualityMode
- IMsRdpClientAdvancedSettings8.put_AudioQualityMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fdfc19176e03f8979e5adb25bf0c9eaf4ceed9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345905"
---
# <a name="imsrdpclientadvancedsettings7audioqualitymode-property"></a><span data-ttu-id="95b32-109">IMsRdpClientAdvancedSettings7:: audioqualitymode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="95b32-109">IMsRdpClientAdvancedSettings7::AudioQualityMode property</span></span>

<span data-ttu-id="95b32-110">Gibt einen Wert an oder ruft ihn ab, der die Einstellung für den audioqualitätsmodus für umgeleitete Audiodaten angibt</span><span class="sxs-lookup"><span data-stu-id="95b32-110">Specifies or retrieves a value that indicates the audio quality mode setting for redirected audio.</span></span> <span data-ttu-id="95b32-111">Standardmäßig ist dieser Wert auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="95b32-111">By default this is set to 0.</span></span>

<span data-ttu-id="95b32-112">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="95b32-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="95b32-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="95b32-113">Syntax</span></span>


```C++
HRESULT put_AudioQualityMode(
  [in]          UINT audioQualityMode
);

HRESULT get_AudioQualityMode(
  [out, retval] UINT *pAudioQualityMode
);
```



## <a name="property-value"></a><span data-ttu-id="95b32-114">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="95b32-114">Property value</span></span>

<span data-ttu-id="95b32-115">Ein-Wert, der den audioqualitätsmodus angibt.</span><span class="sxs-lookup"><span data-stu-id="95b32-115">A value that specifies the audio quality mode.</span></span>

<span data-ttu-id="95b32-116">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="95b32-116">The possible values are:</span></span>

<dt>

<span data-ttu-id="95b32-117">0</span><span class="sxs-lookup"><span data-stu-id="95b32-117">0</span></span>
</dt> <dd>

<span data-ttu-id="95b32-118">Dynamische Audioqualität.</span><span class="sxs-lookup"><span data-stu-id="95b32-118">Dynamic audio quality.</span></span> <span data-ttu-id="95b32-119">Dies ist die Standardeinstellung für die Audioqualität.</span><span class="sxs-lookup"><span data-stu-id="95b32-119">This is the default audio quality setting.</span></span> <span data-ttu-id="95b32-120">Der Server passt die Qualität der Audioausgabe in Reaktion auf die Netzwerkbedingungen und die Client-und Serverfunktionen dynamisch an.</span><span class="sxs-lookup"><span data-stu-id="95b32-120">The server dynamically adjusts audio output quality in response to network conditions and the client and server capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="95b32-121">1</span><span class="sxs-lookup"><span data-stu-id="95b32-121">1</span></span>
</dt> <dd>

<span data-ttu-id="95b32-122">Mittlere Audioqualität.</span><span class="sxs-lookup"><span data-stu-id="95b32-122">Medium audio quality.</span></span> <span data-ttu-id="95b32-123">Der Server verwendet ein festes, aber komprimiertes Format für die Audioausgabe.</span><span class="sxs-lookup"><span data-stu-id="95b32-123">The server uses a fixed but compressed format for audio output.</span></span>

</dd> <dt>

<span data-ttu-id="95b32-124">2</span><span class="sxs-lookup"><span data-stu-id="95b32-124">2</span></span>
</dt> <dd>

<span data-ttu-id="95b32-125">Hohe Audioqualität.</span><span class="sxs-lookup"><span data-stu-id="95b32-125">High audio quality.</span></span> <span data-ttu-id="95b32-126">Der Server stellt Audioausgaben im nicht komprimierten PCM-Format bereit, wobei der Verarbeitungsaufwand für die Latenz geringer ist.</span><span class="sxs-lookup"><span data-stu-id="95b32-126">The server provides audio output in uncompressed PCM format with lower processing overhead for latency.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95b32-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95b32-127">Requirements</span></span>



| <span data-ttu-id="95b32-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95b32-128">Requirement</span></span> | <span data-ttu-id="95b32-129">Wert</span><span class="sxs-lookup"><span data-stu-id="95b32-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95b32-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95b32-130">Minimum supported client</span></span><br/> | <span data-ttu-id="95b32-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="95b32-131">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="95b32-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95b32-132">Minimum supported server</span></span><br/> | <span data-ttu-id="95b32-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="95b32-133">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="95b32-134">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="95b32-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="95b32-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95b32-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="95b32-136">DLL</span><span class="sxs-lookup"><span data-stu-id="95b32-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95b32-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95b32-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="95b32-138">IID</span><span class="sxs-lookup"><span data-stu-id="95b32-138">IID</span></span><br/>                      | <span data-ttu-id="95b32-139">IID \_ IMsRdpClientAdvancedSettings7 wird als 26036036-4010-4578-8091-0db9a1edf-C3 definiert.</span><span class="sxs-lookup"><span data-stu-id="95b32-139">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="95b32-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95b32-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95b32-141">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="95b32-141">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="95b32-142">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="95b32-142">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





