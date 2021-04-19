---
title: IMsRdpClientAdvancedSettings7-Schnittstelle
description: Macht Methoden und Eigenschaften verfügbar, die erweiterte Einstellungen des ActiveX-Steuer Elements verwalten.
ms.assetid: 2d6848b4-2ce6-4624-b46e-65e7daf2d0f1
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed28c5d26ecf280507ce3cce835a6d0a71fc3bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342189"
---
# <a name="imsrdpclientadvancedsettings7-interface"></a><span data-ttu-id="c2984-105">IMsRdpClientAdvancedSettings7-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c2984-105">IMsRdpClientAdvancedSettings7 interface</span></span>

<span data-ttu-id="c2984-106">Macht Methoden und Eigenschaften verfügbar, die erweiterte Einstellungen des ActiveX-Steuer Elements verwalten.</span><span class="sxs-lookup"><span data-stu-id="c2984-106">Exposes methods and properties that manage advanced settings of the ActiveX control.</span></span>

<span data-ttu-id="c2984-107">Um eine Instanz dieser Schnittstelle abzurufen, verwenden Sie die [**imstscax:: advancedsettings**](imstscax-advancedsettings.md) -Eigenschaft, um einen [**imstscadvancedsettings**](imstscadvancedsettings-interface.md) -Schnittstellen Zeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c2984-107">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="c2984-108">Nennen Sie dann [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den **imstscadvancedsettings** -Zeiger, und übergeben Sie **IID \_ IMsRdpClientAdvancedSettings7** an **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="c2984-108">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings7** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="c2984-109">Member</span><span class="sxs-lookup"><span data-stu-id="c2984-109">Members</span></span>

<span data-ttu-id="c2984-110">Die **IMsRdpClientAdvancedSettings7** -Schnittstelle erbt von **IMsRdpClientAdvancedSettings6**.</span><span class="sxs-lookup"><span data-stu-id="c2984-110">The **IMsRdpClientAdvancedSettings7** interface inherits from **IMsRdpClientAdvancedSettings6**.</span></span> <span data-ttu-id="c2984-111">**IMsRdpClientAdvancedSettings7** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c2984-111">**IMsRdpClientAdvancedSettings7** also has these types of members:</span></span>

-   [<span data-ttu-id="c2984-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2984-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2984-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2984-113">Properties</span></span>

<span data-ttu-id="c2984-114">Die **IMsRdpClientAdvancedSettings7** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c2984-114">The **IMsRdpClientAdvancedSettings7** interface has these properties.</span></span>



| <span data-ttu-id="c2984-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c2984-115">Property</span></span>                                                                                                    | <span data-ttu-id="c2984-116">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="c2984-116">Access type</span></span>           | <span data-ttu-id="c2984-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2984-117">Description</span></span>                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2984-118">**Audiocaptureredirectionmode**</span><span class="sxs-lookup"><span data-stu-id="c2984-118">**AudioCaptureRedirectionMode**</span></span>](imsrdpclientadvancedsettings7-audiocaptureredirectionmode.md)<br/> | <span data-ttu-id="c2984-119">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c2984-119">Read/write</span></span><br/> | <span data-ttu-id="c2984-120">Gibt einen Wert an, der angibt, ob das standardmäßige Audioeingabegerät vom Client an die Remote Sitzung umgeleitet wird, oder ruft diesen Wert ab.</span><span class="sxs-lookup"><span data-stu-id="c2984-120">Specifies or retrieves a value that indicates whether the default audio input device is redirected from the client to the remote session.</span></span><br/> |
| [<span data-ttu-id="c2984-121">**Audioqualitymode**</span><span class="sxs-lookup"><span data-stu-id="c2984-121">**AudioQualityMode**</span></span>](imsrdpclientadvancedsettings7-audioqualitymode.md)<br/>                       | <span data-ttu-id="c2984-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c2984-122">Read/write</span></span><br/> | <span data-ttu-id="c2984-123">Gibt einen Wert an oder ruft ihn ab, der die Einstellung für den audioqualitätsmodus für umgeleitete Audiodaten angibt</span><span class="sxs-lookup"><span data-stu-id="c2984-123">Specifies or retrieves a value that indicates the audio quality mode setting for redirected audio.</span></span><br/>                                        |
| [<span data-ttu-id="c2984-124">**Enablesuperpan**</span><span class="sxs-lookup"><span data-stu-id="c2984-124">**EnableSuperPan**</span></span>](imsrdpclientadvancedsettings7-enablesuperpan.md)<br/>                           | <span data-ttu-id="c2984-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c2984-125">Read/write</span></span><br/> | <span data-ttu-id="c2984-126">Gibt einen Wert an, der angibt, ob superpan aktiviert oder deaktiviert ist, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="c2984-126">Specifies or retrieves a value that indicates whether SuperPan is enabled or disabled.</span></span><br/>                                                    |
| [<span data-ttu-id="c2984-127">**Networkconnectiontype**</span><span class="sxs-lookup"><span data-stu-id="c2984-127">**NetworkConnectionType**</span></span>](imsrdpclientadvancedsettings7-networkconnectiontype.md)<br/>             | <span data-ttu-id="c2984-128">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c2984-128">Read/write</span></span><br/> | <span data-ttu-id="c2984-129">Gibt einen Wert an, der den Netzwerk Verbindungstyp angibt, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="c2984-129">Specifies or retrieves a value that indicates the network connection type.</span></span><br/>                                                                |
| [<span data-ttu-id="c2984-130">**Redirectdirectx**</span><span class="sxs-lookup"><span data-stu-id="c2984-130">**RedirectDirectX**</span></span>](imsrdpclientadvancedsettings7-redirectdirectx.md)<br/>                         | <span data-ttu-id="c2984-131">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c2984-131">Read/write</span></span><br/> | <span data-ttu-id="c2984-132">Diese Eigenschaft wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2984-132">This property is not used.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="c2984-133">**Superpanaccelerationfactor**</span><span class="sxs-lookup"><span data-stu-id="c2984-133">**SuperPanAccelerationFactor**</span></span>](imsrdpclientadvancedsettings7-superpanaccelerationfactor.md)<br/>   | <span data-ttu-id="c2984-134">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c2984-134">Read/write</span></span><br/> | <span data-ttu-id="c2984-135">Gibt einen Wert an, der den superpan-Beschleunigungs Faktor angibt, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="c2984-135">Specifies or retrieves a value that indicates the SuperPan acceleration factor.</span></span><br/>                                                           |
| [<span data-ttu-id="c2984-136">**Videoplaybackmode**</span><span class="sxs-lookup"><span data-stu-id="c2984-136">**VideoPlaybackMode**</span></span>](imsrdpclientadvancedsettings7-videoplaybackmode.md)<br/>                     | <span data-ttu-id="c2984-137">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c2984-137">Read/write</span></span><br/> | <span data-ttu-id="c2984-138">Gibt einen Wert an, der den Videowiedergabe Modus angibt, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="c2984-138">Specifies or retrieves a value that indicates the video playback mode.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="c2984-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2984-139">Requirements</span></span>



| <span data-ttu-id="c2984-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2984-140">Requirement</span></span> | <span data-ttu-id="c2984-141">Wert</span><span class="sxs-lookup"><span data-stu-id="c2984-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2984-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2984-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c2984-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c2984-143">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="c2984-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2984-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c2984-145">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2984-145">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="c2984-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c2984-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="c2984-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2984-147"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c2984-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c2984-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2984-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2984-149"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c2984-150">IID</span><span class="sxs-lookup"><span data-stu-id="c2984-150">IID</span></span><br/>                      | <span data-ttu-id="c2984-151">IID \_ IMsRdpClientAdvancedSettings7 wird als 26036036-4010-4578-8091-0db9a1edf-C3 definiert.</span><span class="sxs-lookup"><span data-stu-id="c2984-151">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c2984-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2984-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2984-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c2984-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c2984-154">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c2984-154">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="c2984-155">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c2984-155">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="c2984-156">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="c2984-156">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="c2984-157">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="c2984-157">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="c2984-158">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="c2984-158">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c2984-159">**Imstscadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="c2984-159">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

