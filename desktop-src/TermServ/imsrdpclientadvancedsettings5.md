---
title: IMsRdpClientAdvancedSettings5-Schnittstelle
description: Verwaltet erweiterte Client Einstellungen. Wird von der IMsRdpClientAdvancedSettings4-Schnittstelle abgeleitet.
ms.assetid: a927cd4c-7f70-493e-a4f6-056d0352d56e
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14e37eb28c1fb7a272291c44661c52ec3548708b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340332"
---
# <a name="imsrdpclientadvancedsettings5-interface"></a><span data-ttu-id="2a93a-106">IMsRdpClientAdvancedSettings5-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2a93a-106">IMsRdpClientAdvancedSettings5 interface</span></span>

<span data-ttu-id="2a93a-107">Verwaltet erweiterte Client Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="2a93a-107">Manages advanced client settings.</span></span> <span data-ttu-id="2a93a-108">Wird von der [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) -Schnittstelle abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2a93a-108">Derives from the [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span>

<span data-ttu-id="2a93a-109">Um eine Instanz dieser Schnittstelle abzurufen, verwenden Sie die [**imstscax:: advancedsettings**](imstscax-advancedsettings.md) -Eigenschaft, um einen [**imstscadvancedsettings**](imstscadvancedsettings-interface.md) -Schnittstellen Zeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2a93a-109">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="2a93a-110">Nennen Sie dann [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den **imstscadvancedsettings** -Zeiger, und übergeben Sie **IID \_ IMsRdpClientAdvancedSettings5** an **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="2a93a-110">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings5** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="2a93a-111">Member</span><span class="sxs-lookup"><span data-stu-id="2a93a-111">Members</span></span>

<span data-ttu-id="2a93a-112">Die **IMsRdpClientAdvancedSettings5** -Schnittstelle erbt von [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md).</span><span class="sxs-lookup"><span data-stu-id="2a93a-112">The **IMsRdpClientAdvancedSettings5** interface inherits from [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md).</span></span> <span data-ttu-id="2a93a-113">**IMsRdpClientAdvancedSettings5** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2a93a-113">**IMsRdpClientAdvancedSettings5** also has these types of members:</span></span>

-   [<span data-ttu-id="2a93a-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a93a-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a93a-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a93a-115">Properties</span></span>

<span data-ttu-id="2a93a-116">Die **IMsRdpClientAdvancedSettings5** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2a93a-116">The **IMsRdpClientAdvancedSettings5** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="2a93a-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2a93a-117">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="2a93a-118">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="2a93a-118">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="2a93a-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a93a-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="2a93a-120"><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>Audioredirectionmode</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a93a-120"><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="2a93a-121">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2a93a-121">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="2a93a-122">Der audioumleitungs Modus.</span><span class="sxs-lookup"><span data-stu-id="2a93a-122">The audio redirection mode.</span></span> <span data-ttu-id="2a93a-123">Die <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>audioredirectionmode</strong></a> -Eigenschaft verfügt über die folgenden möglichen Werte.</span><span class="sxs-lookup"><span data-stu-id="2a93a-123">The <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a> property has the following possible values.</span></span><br/><span data-ttu-id="2a93a-124">
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (die Audioumleitung ist aktiviert, und die Option für die Umleitung wird &quot; auf diesen Computer übertragen &quot; .</span><span class="sxs-lookup"><span data-stu-id="2a93a-124">
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (Audio redirection is enabled and the option for redirection is &quot;Bring to this computer&quot;.</span></span> <span data-ttu-id="2a93a-125">Dies ist der Standardmodus.)</span><span class="sxs-lookup"><span data-stu-id="2a93a-125">This is the default mode.)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2a93a-126"><dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (die Audioumleitung ist aktiviert, und die Option ist &quot; auf dem Remote Computer belassen &quot; .</span><span class="sxs-lookup"><span data-stu-id="2a93a-126"><dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (Audio redirection is enabled and the option is &quot;Leave at remote computer&quot;.</span></span> <span data-ttu-id="2a93a-127">Die &quot; Option auf Remote Computer belassen &quot; wird nur unterstützt, wenn eine Remote Verbindung mit einem Host Computer hergestellt wird, auf dem Windows Vista ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a93a-127">The &quot;Leave at remote computer&quot; option is supported only when connecting remotely to a host computer that is running Windows Vista.</span></span> <span data-ttu-id="2a93a-128">Wenn die Verbindung mit einem Host Computer hergestellt wird, auf dem Windows Server 2008 ausgeführt wird, wird die Option &quot; auf dem Remote Computer belassen &quot; nicht wieder &quot; geben geändert &quot; .)</span><span class="sxs-lookup"><span data-stu-id="2a93a-128">If the connection is to a host computer that is running Windows Server 2008, the option &quot;Leave at remote computer&quot; is changed to &quot;Do not play&quot;.)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2a93a-129"><dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (die Audioumleitung ist aktiviert, und der Modus ist &quot; nicht wiedergeben &quot; .)</span><span class="sxs-lookup"><span data-stu-id="2a93a-129"><dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (Audio redirection is enabled and the mode is &quot;Do not play&quot;.)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="2a93a-130"><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a93a-130"><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="2a93a-131">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2a93a-131">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="2a93a-132">Gibt die Größe der virtuellen Cachedatei für bpp-Bitmaps (32 Bits pro Pixel) an.</span><span class="sxs-lookup"><span data-stu-id="2a93a-132">Specifies the virtual cache file size for 32 bits per pixel (bpp) bitmaps.</span></span> <span data-ttu-id="2a93a-133">Der Höchstwert beträgt 48 Megabyte (MB).</span><span class="sxs-lookup"><span data-stu-id="2a93a-133">The maximum value is 48 megabytes (MB).</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="2a93a-134"><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>Connectionbarshowpinbutton</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a93a-134"><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="2a93a-135">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2a93a-135">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="2a93a-136">Gibt an, ob die PIN-Schaltfläche auf der Verbindungs Leiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a93a-136">Specifies whether the pin button should be shown on the connection bar.</span></span> <span data-ttu-id="2a93a-137">Standardmäßig ist der Wert <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a93a-137">By default, the value is <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="2a93a-138"><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>Publicmode</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a93a-138"><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>PublicMode</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="2a93a-139">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2a93a-139">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="2a93a-140">Gibt an, ob der öffentliche Modus aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a93a-140">Specifies whether public mode should be enabled or disabled.</span></span> <span data-ttu-id="2a93a-141">Der öffentliche Modus ist standardmäßig auf <strong>false</strong>festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2a93a-141">By default, public mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="2a93a-142"><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>Redirectclipboard</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a93a-142"><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="2a93a-143">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2a93a-143">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="2a93a-144">Gibt an, ob die Umleitung der Zwischenablage aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a93a-144">Specifies whether clipboard redirection should be enabled or disabled.</span></span> <span data-ttu-id="2a93a-145">Standardmäßig ist der Umleitungs Modus für die Zwischenablage auf <strong>true</strong> (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2a93a-145">By default, clipboard redirection mode is set to <strong>TRUE</strong> (enabled).</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="2a93a-146"><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>Redirectdevices</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a93a-146"><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="2a93a-147">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2a93a-147">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="2a93a-148">Gibt an, ob umgeleitete Geräte aktiviert oder deaktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2a93a-148">Specifies whether redirected devices should be enabled or disabled.</span></span> <span data-ttu-id="2a93a-149">Standardmäßig ist der Modus für umgeleitete Geräte auf <strong>false</strong>festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2a93a-149">By default, redirected devices mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="2a93a-150"><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>Redirectposdevices</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a93a-150"><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="2a93a-151">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2a93a-151">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="2a93a-152">Gibt an, ob die Dienst Punkte, die umgeleitet werden sollen, aktiviert oder deaktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2a93a-152">Specifies whether Point of Service redirected devices should be enabled or disabled.</span></span> <span data-ttu-id="2a93a-153">Standardmäßig ist der Modus für umgeleitete Geräte des Dienstanbieter auf <strong>false</strong>festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2a93a-153">By default, Point of Service redirected devices mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="2a93a-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a93a-154">Remarks</span></span>

<span data-ttu-id="2a93a-155">Diese Schnittstelle wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:</span><span class="sxs-lookup"><span data-stu-id="2a93a-155">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="2a93a-156">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="2a93a-156">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="2a93a-157">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="2a93a-157">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
-   [<span data-ttu-id="2a93a-158">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="2a93a-158">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)

## <a name="requirements"></a><span data-ttu-id="2a93a-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a93a-159">Requirements</span></span>



| <span data-ttu-id="2a93a-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a93a-160">Requirement</span></span> | <span data-ttu-id="2a93a-161">Wert</span><span class="sxs-lookup"><span data-stu-id="2a93a-161">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a93a-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a93a-162">Minimum supported client</span></span><br/> | <span data-ttu-id="2a93a-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a93a-163">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="2a93a-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a93a-164">Minimum supported server</span></span><br/> | <span data-ttu-id="2a93a-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a93a-165">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="2a93a-166">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2a93a-166">Type library</span></span><br/>             | <dl> <span data-ttu-id="2a93a-167"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a93a-167"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="2a93a-168">DLL</span><span class="sxs-lookup"><span data-stu-id="2a93a-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a93a-169"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a93a-169"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="2a93a-170">IID</span><span class="sxs-lookup"><span data-stu-id="2a93a-170">IID</span></span><br/>                      | <span data-ttu-id="2a93a-171">IID \_ IMsRdpClientAdvancedSettings5 ist als FBA7F64E-6783-4405-DA45-FA4A763DABD0 definiert.</span><span class="sxs-lookup"><span data-stu-id="2a93a-171">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a93a-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a93a-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a93a-173">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="2a93a-173">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="2a93a-174">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="2a93a-174">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="2a93a-175">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="2a93a-175">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="2a93a-176">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="2a93a-176">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="2a93a-177">**Imstscadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="2a93a-177">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="2a93a-178">Remotedesktop-Webverbindung Referenz</span><span class="sxs-lookup"><span data-stu-id="2a93a-178">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

