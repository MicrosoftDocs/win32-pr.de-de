---
title: IMsRdpClientAdvancedSettings5 audioredirectionmode-Eigenschaft
description: Legt den audioumleitungs Modus und andere audioumleitungs Optionen fest und ruft ihn ab.
ms.assetid: c0f5762b-00fd-40bb-ac97-3351b999f38d
ms.tgt_platform: multiple
keywords:
- Audioredirectionmode-Eigenschaft Remotedesktopdienste
- Audioredirectionmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, audioredirectionmode-Eigenschaft
- Audioredirectionmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, audioredirectionmode-Eigenschaft
- Audioredirectionmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, audioredirectionmode-Eigenschaft
- Audioredirectionmode-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, audioredirectionmode-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40be8b8e63f210d060c0f585c9fe31328ac6ed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340527"
---
# <a name="imsrdpclientadvancedsettings5audioredirectionmode-property"></a><span data-ttu-id="e25fa-112">IMsRdpClientAdvancedSettings5:: audioredirectionmode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e25fa-112">IMsRdpClientAdvancedSettings5::AudioRedirectionMode property</span></span>

<span data-ttu-id="e25fa-113">Legt den audioumleitungs Modus und andere audioumleitungs Optionen fest und ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="e25fa-113">Sets and retrieves the audio redirection mode and different audio redirection options.</span></span>

<span data-ttu-id="e25fa-114">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e25fa-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e25fa-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="e25fa-115">Syntax</span></span>


```C++
HRESULT put_AudioRedirectionMode(
  [in]  UINT uiAudioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] UINT *puiAudioRedirectionMode
);
```



## <a name="property-value"></a><span data-ttu-id="e25fa-116">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e25fa-116">Property value</span></span>

<span data-ttu-id="e25fa-117">Legt verschiedene Werte für den audioumleitungs Modus fest.</span><span class="sxs-lookup"><span data-stu-id="e25fa-117">Sets different values for the audio redirection mode.</span></span> <span data-ttu-id="e25fa-118">Dieser Parameter verfügt über die folgenden möglichen Werte.</span><span class="sxs-lookup"><span data-stu-id="e25fa-118">This parameter has the following possible values.</span></span>

<dt>

<span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span>

<span data-ttu-id="e25fa-119">**Audiodatei \_ \_Modusumleitung 0** (die Audioumleitung ist aktiviert, und die Option für die Umleitung lautet "an diesen Computer übertragen".</span><span class="sxs-lookup"><span data-stu-id="e25fa-119">**AUDIO\_MODE\_REDIRECT 0** (Audio redirection is enabled and the option for redirection is "Bring to this computer".</span></span> <span data-ttu-id="e25fa-120">Dies ist der Standardmodus.)</span><span class="sxs-lookup"><span data-stu-id="e25fa-120">This is the default mode.)</span></span>


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span>

<span data-ttu-id="e25fa-121">**Audiodatei \_ Der Modus wird \_ \_ auf \_ Server 1 abgespielt** (die Audioumleitung ist aktiviert, und die Option ist "auf Remote Computer verlassen".</span><span class="sxs-lookup"><span data-stu-id="e25fa-121">**AUDIO\_MODE\_PLAY\_ON\_SERVER 1** (Audio redirection is enabled and the option is "Leave at remote computer".</span></span> <span data-ttu-id="e25fa-122">Die Option "Remote Computer verlassen" wird nur unterstützt, wenn eine Remote Verbindung mit einem Host Computer hergestellt wird, auf dem Windows Vista ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e25fa-122">The "Leave at remote computer" option is supported only when connecting remotely to a host computer that is running Windows Vista.</span></span> <span data-ttu-id="e25fa-123">Wenn die Verbindung mit einem Host Computer hergestellt wird, auf dem Windows Server 2008 ausgeführt wird, wird die Option "auf Remote Computer verlassen" in "nicht wiedergeben" geändert.)</span><span class="sxs-lookup"><span data-stu-id="e25fa-123">If the connection is to a host computer that is running Windows Server 2008, the option "Leave at remote computer" is changed to "Do not play".)</span></span>


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span>

<span data-ttu-id="e25fa-124">**Audiodatei \_ Modus \_ None 2** (Audioumleitung ist aktiviert, und der Modus ist nicht wiedergeben).</span><span class="sxs-lookup"><span data-stu-id="e25fa-124">**AUDIO\_MODE\_NONE 2** (Audio redirection is enabled and the mode is "Do not play".)</span></span>


<span data-ttu-id="e25fa-125"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e25fa-125"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e25fa-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e25fa-126">Requirements</span></span>



| <span data-ttu-id="e25fa-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e25fa-127">Requirement</span></span> | <span data-ttu-id="e25fa-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e25fa-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e25fa-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e25fa-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e25fa-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e25fa-130">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="e25fa-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e25fa-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e25fa-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e25fa-132">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="e25fa-133">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e25fa-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="e25fa-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e25fa-134"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e25fa-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e25fa-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e25fa-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e25fa-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e25fa-137">IID</span><span class="sxs-lookup"><span data-stu-id="e25fa-137">IID</span></span><br/>                      | <span data-ttu-id="e25fa-138">IID \_ IMsRdpClientAdvancedSettings5 ist als FBA7F64E-6783-4405-DA45-FA4A763DABD0 definiert.</span><span class="sxs-lookup"><span data-stu-id="e25fa-138">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e25fa-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e25fa-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e25fa-140">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e25fa-140">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="e25fa-141">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e25fa-141">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e25fa-142">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e25fa-142">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e25fa-143">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e25fa-143">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





