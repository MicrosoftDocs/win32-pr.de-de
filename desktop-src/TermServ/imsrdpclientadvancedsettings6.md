---
title: IMsRdpClientAdvancedSettings6-Schnittstelle
description: Macht Eigenschaften verfügbar, die erweiterte Einstellungen des ActiveX-Steuer Elements verwalten.
ms.assetid: 45b48cdf-3860-4359-99b2-8d2598146d1d
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e61d3358f1af228dcd1b5a7431ee759b486df7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340347"
---
# <a name="imsrdpclientadvancedsettings6-interface"></a><span data-ttu-id="26bef-105">IMsRdpClientAdvancedSettings6-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="26bef-105">IMsRdpClientAdvancedSettings6 interface</span></span>

<span data-ttu-id="26bef-106">Macht Eigenschaften verfügbar, die erweiterte Einstellungen des ActiveX-Steuer Elements verwalten.</span><span class="sxs-lookup"><span data-stu-id="26bef-106">Exposes properties that manage advanced ActiveX control settings.</span></span> <span data-ttu-id="26bef-107">Die **IMsRdpClientAdvancedSettings6** -Schnittstelle wird von der [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) -Schnittstelle abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="26bef-107">The **IMsRdpClientAdvancedSettings6** interface is derived from the [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="26bef-108">Um eine Instanz dieser Schnittstelle abzurufen, verwenden Sie die [**imstscax:: advancedsettings**](imstscax-advancedsettings.md) -Eigenschaft, um einen [**imstscadvancedsettings**](imstscadvancedsettings-interface.md) -Schnittstellen Zeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="26bef-108">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="26bef-109">Nennen Sie dann [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den **imstscadvancedsettings** -Zeiger, und übergeben Sie **IID \_ IMsRdpClientAdvancedSettings6** an **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="26bef-109">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings6** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="26bef-110">Member</span><span class="sxs-lookup"><span data-stu-id="26bef-110">Members</span></span>

<span data-ttu-id="26bef-111">Die **IMsRdpClientAdvancedSettings6** -Schnittstelle erbt von [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md).</span><span class="sxs-lookup"><span data-stu-id="26bef-111">The **IMsRdpClientAdvancedSettings6** interface inherits from [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md).</span></span> <span data-ttu-id="26bef-112">**IMsRdpClientAdvancedSettings6** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="26bef-112">**IMsRdpClientAdvancedSettings6** also has these types of members:</span></span>

-   [<span data-ttu-id="26bef-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="26bef-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26bef-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="26bef-114">Properties</span></span>

<span data-ttu-id="26bef-115">Die **IMsRdpClientAdvancedSettings6** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="26bef-115">The **IMsRdpClientAdvancedSettings6** interface has these properties.</span></span>



| <span data-ttu-id="26bef-116">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="26bef-116">Property</span></span>                                                                                                  | <span data-ttu-id="26bef-117">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="26bef-117">Access type</span></span>           | <span data-ttu-id="26bef-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26bef-118">Description</span></span>                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26bef-119">**Authenticationserviceclass**</span><span class="sxs-lookup"><span data-stu-id="26bef-119">**AuthenticationServiceClass**</span></span>](imsrdpclientadvancedsettings6-authenticationserviceclass.md)<br/> | <span data-ttu-id="26bef-120">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="26bef-120">Read/write</span></span><br/> | <span data-ttu-id="26bef-121">Gibt den Dienst Prinzipal Namen (SPN) an, der für die Authentifizierung beim Server verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="26bef-121">Specifies the service principal name (SPN) to use for authentication to the server.</span></span><br/>                                     |
| [<span data-ttu-id="26bef-122">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="26bef-122">**AuthenticationType**</span></span>](imsrdpclientadvancedsettings6-authenticationtype.md)<br/>                 | <span data-ttu-id="26bef-123">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="26bef-123">Read-only</span></span><br/>  | <span data-ttu-id="26bef-124">Gibt den für diese Verbindung verwendeten Authentifizierungstyp an.</span><span class="sxs-lookup"><span data-stu-id="26bef-124">Specifies the type of authentication used for this connection.</span></span><br/>                                                          |
| [<span data-ttu-id="26bef-125">**Connectum Administration Server**</span><span class="sxs-lookup"><span data-stu-id="26bef-125">**ConnectToAdministerServer**</span></span>](imsrdpclientadvancedsettings6-connecttoadministerserver.md)<br/>   | <span data-ttu-id="26bef-126">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="26bef-126">Read/write</span></span><br/> | <span data-ttu-id="26bef-127">Ruft ab oder legt fest, ob das ActiveX-Steuerelement versuchen soll, eine Verbindung mit dem Server zu Verwaltungszwecken herzustellen.</span><span class="sxs-lookup"><span data-stu-id="26bef-127">Retrieves or specifies whether the ActiveX control should attempt to connect to the server for administrative purposes.</span></span><br/> |
| [<span data-ttu-id="26bef-128">**Enablekredsspsupport**</span><span class="sxs-lookup"><span data-stu-id="26bef-128">**EnableCredSspSupport**</span></span>](imsrdpclientadvancedsettings6-enablecredsspsupport.md)<br/>             | <span data-ttu-id="26bef-129">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="26bef-129">Read/write</span></span><br/> | <span data-ttu-id="26bef-130">Gibt an, ob der Credential Security Service Provider (kredssp) für diese Verbindung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="26bef-130">Specifies whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span><br/>                    |
| [<span data-ttu-id="26bef-131">**Hotkeyfocareleaseleft**</span><span class="sxs-lookup"><span data-stu-id="26bef-131">**HotKeyFocusReleaseLeft**</span></span>](imsrdpclientadvancedsettings6-hotkeyfocusreleaseleft.md)<br/>         | <span data-ttu-id="26bef-132">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="26bef-132">Read/write</span></span><br/> | <span data-ttu-id="26bef-133">Gibt den Code des virtuellen Schlüssels an, der STRG + ALT hinzugefügt werden soll, um die Hotkey-Ersetzung für STRG + ALT + nach-Links zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="26bef-133">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+LEFT ARROW.</span></span><br/>          |
| [<span data-ttu-id="26bef-134">**Hotkeyfocareleaseright**</span><span class="sxs-lookup"><span data-stu-id="26bef-134">**HotKeyFocusReleaseRight**</span></span>](imsrdpclientadvancedsettings6-hotkeyfocusreleaseright.md)<br/>       | <span data-ttu-id="26bef-135">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="26bef-135">Read/write</span></span><br/> | <span data-ttu-id="26bef-136">Gibt den Code des virtuellen Schlüssels an, der STRG + ALT hinzugefügt werden soll, um die Hotkey-Ersetzung für STRG + ALT + nach-rechts zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="26bef-136">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+RIGHT ARROW.</span></span><br/>         |
| [<span data-ttu-id="26bef-137">**PCB**</span><span class="sxs-lookup"><span data-stu-id="26bef-137">**PCB**</span></span>](imsrdpclientadvancedsettings6-pcb.md)<br/>                                               | <span data-ttu-id="26bef-138">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="26bef-138">Read/write</span></span><br/> | <span data-ttu-id="26bef-139">Gibt die Einstellung für die Vorverbindungs-BLOB (Festplatte) an, die vor der Verbindungs Herstellung mit dem Server verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="26bef-139">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span><br/>               |
| [<span data-ttu-id="26bef-140">**Relativemousmode**</span><span class="sxs-lookup"><span data-stu-id="26bef-140">**RelativeMouseMode**</span></span>](imsrdpclientadvancedsettings6-relativemousemode.md)<br/>                   | <span data-ttu-id="26bef-141">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="26bef-141">Read/write</span></span><br/> | <span data-ttu-id="26bef-142">Gibt an, ob die Maus den relativen Modus verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="26bef-142">Specifies whether the mouse should use relative mode.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="26bef-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26bef-143">Remarks</span></span>

<span data-ttu-id="26bef-144">Diese Schnittstelle wurde von der [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) -Schnittstelle erweitert und erbt alle Methoden und Eigenschaften der vorherigen Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="26bef-144">This interface has been extended by the [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface, inheriting all the methods and properties of the previous interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="26bef-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26bef-145">Requirements</span></span>



| <span data-ttu-id="26bef-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26bef-146">Requirement</span></span> | <span data-ttu-id="26bef-147">Wert</span><span class="sxs-lookup"><span data-stu-id="26bef-147">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26bef-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26bef-148">Minimum supported client</span></span><br/> | <span data-ttu-id="26bef-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26bef-149">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="26bef-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26bef-150">Minimum supported server</span></span><br/> | <span data-ttu-id="26bef-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26bef-151">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="26bef-152">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="26bef-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="26bef-153"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26bef-153"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="26bef-154">DLL</span><span class="sxs-lookup"><span data-stu-id="26bef-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26bef-155"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26bef-155"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="26bef-156">IID</span><span class="sxs-lookup"><span data-stu-id="26bef-156">IID</span></span><br/>                      | <span data-ttu-id="26bef-157">IID \_ IMsRdpClientAdvancedSettings6 ist als 222c4b5d-45d9-4df0-a7c6-60cf9089d285 definiert.</span><span class="sxs-lookup"><span data-stu-id="26bef-157">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26bef-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26bef-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26bef-159">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="26bef-159">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="26bef-160">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="26bef-160">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="26bef-161">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="26bef-161">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="26bef-162">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="26bef-162">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="26bef-163">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="26bef-163">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="26bef-164">**Imstscadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="26bef-164">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

