---
title: IMsRdpClientAdvancedSettings2-Schnittstelle
description: Verwaltet erweiterte Client Einstellungen. Wird von der imsrdpclientadvancedsettings-Schnittstelle abgeleitet.
ms.assetid: 78cffdf5-bd99-4140-80b6-aa8632894487
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d7f9ad9b93c0f3cd1d62fdbbaddf4faa55ad9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340877"
---
# <a name="imsrdpclientadvancedsettings2-interface"></a><span data-ttu-id="6e9e2-106">IMsRdpClientAdvancedSettings2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6e9e2-106">IMsRdpClientAdvancedSettings2 interface</span></span>

<span data-ttu-id="6e9e2-107">Verwaltet erweiterte Client Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-107">Manages advanced client settings.</span></span> <span data-ttu-id="6e9e2-108">Wird von der [**imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md) -Schnittstelle abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-108">Derives from the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="6e9e2-109">Diese Schnittstelle enthält Methoden zum Abrufen und Festlegen erweiterter (optionaler) Eigenschaften für das Remotedesktop ActiveX-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="6e9e2-110">Um eine Instanz dieser Schnittstelle abzurufen, verwenden Sie die [**imstscax:: advancedsettings**](imstscax-advancedsettings.md) -Eigenschaft, um einen [**imstscadvancedsettings**](imstscadvancedsettings-interface.md) -Schnittstellen Zeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="6e9e2-111">Nennen Sie dann [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den **imstscadvancedsettings** -Zeiger, und übergeben Sie **IID \_ IMsRdpClientAdvancedSettings2** an **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings2** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="6e9e2-112">Member</span><span class="sxs-lookup"><span data-stu-id="6e9e2-112">Members</span></span>

<span data-ttu-id="6e9e2-113">Die **IMsRdpClientAdvancedSettings2** -Schnittstelle erbt von [**imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="6e9e2-113">The **IMsRdpClientAdvancedSettings2** interface inherits from [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md).</span></span> <span data-ttu-id="6e9e2-114">**IMsRdpClientAdvancedSettings2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6e9e2-114">**IMsRdpClientAdvancedSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="6e9e2-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e9e2-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6e9e2-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e9e2-116">Properties</span></span>

<span data-ttu-id="6e9e2-117">Die **IMsRdpClientAdvancedSettings2** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-117">The **IMsRdpClientAdvancedSettings2** interface has these properties.</span></span>



| <span data-ttu-id="6e9e2-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6e9e2-118">Property</span></span>                                                                                      | <span data-ttu-id="6e9e2-119">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="6e9e2-119">Access type</span></span>           | <span data-ttu-id="6e9e2-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e9e2-120">Description</span></span>                                                                                                                                           |
|:----------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e9e2-121">**Canautoreconnetct**</span><span class="sxs-lookup"><span data-stu-id="6e9e2-121">**CanAutoReconnect**</span></span>](imsrdpclientadvancedsettings2-canautoreconnect.md)<br/>         | <span data-ttu-id="6e9e2-122">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e9e2-122">Read-only</span></span><br/>  | <span data-ttu-id="6e9e2-123">Gibt an, ob das Client Steuerelement automatisch eine Verbindung mit der aktuellen Sitzung herstellen kann, wenn eine Netzwerkverbindung getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-123">Specifies whether the client control is able to reconnect automatically to the current session in the event of a network disconnection.</span></span><br/>    |
| [<span data-ttu-id="6e9e2-124">**Enableautoreconnetct**</span><span class="sxs-lookup"><span data-stu-id="6e9e2-124">**EnableAutoReconnect**</span></span>](imsrdpclientadvancedsettings2-enableautoreconnect.md)<br/>   | <span data-ttu-id="6e9e2-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6e9e2-125">Read/write</span></span><br/> | <span data-ttu-id="6e9e2-126">Gibt an, ob das Client Steuerelement das automatische erneute Herstellen einer Verbindung mit einer Sitzung im Falle einer Netzwerk Trennung aktivieren soll.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-126">Specifies whether to enable the client control to reconnect automatically to a session in the event of a network disconnection.</span></span><br/>            |
| [<span data-ttu-id="6e9e2-127">**Maxreconnectattempts**</span><span class="sxs-lookup"><span data-stu-id="6e9e2-127">**MaxReconnectAttempts**</span></span>](imsrdpclientadvancedsettings2-maxreconnectattempts.md)<br/> | <span data-ttu-id="6e9e2-128">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6e9e2-128">Read/write</span></span><br/> | <span data-ttu-id="6e9e2-129">Gibt an, wie oft versucht werden soll, während der automatischen erneuten Verbindung erneut eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-129">Specifies the number of times to try to reconnect during automatic reconnection.</span></span> <span data-ttu-id="6e9e2-130">Gültige Werte für diese Eigenschaft sind 0 bis einschließlich 200.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-130">The valid values of this property are 0 to 200 inclusive.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6e9e2-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e9e2-131">Remarks</span></span>

<span data-ttu-id="6e9e2-132">Diese Schnittstelle wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:</span><span class="sxs-lookup"><span data-stu-id="6e9e2-132">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="6e9e2-133">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="6e9e2-133">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
-   [<span data-ttu-id="6e9e2-134">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="6e9e2-134">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="6e9e2-135">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="6e9e2-135">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="6e9e2-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="6e9e2-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="6e9e2-137">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="6e9e2-137">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="6e9e2-138">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6e9e2-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e9e2-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e9e2-139">Requirements</span></span>



| <span data-ttu-id="6e9e2-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e9e2-140">Requirement</span></span> | <span data-ttu-id="6e9e2-141">Wert</span><span class="sxs-lookup"><span data-stu-id="6e9e2-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e9e2-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6e9e2-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6e9e2-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e9e2-143">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="6e9e2-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6e9e2-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6e9e2-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e9e2-145">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="6e9e2-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6e9e2-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="6e9e2-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e9e2-147"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="6e9e2-148">DLL</span><span class="sxs-lookup"><span data-stu-id="6e9e2-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e9e2-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e9e2-149"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="6e9e2-150">IID</span><span class="sxs-lookup"><span data-stu-id="6e9e2-150">IID</span></span><br/>                      | <span data-ttu-id="6e9e2-151">IID \_ IMsRdpClientAdvancedSettings2 ist als 9ac42117-2b76-4320-aa44-0e616ab8437b definiert.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-151">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e9e2-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e9e2-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e9e2-153">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="6e9e2-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="6e9e2-154">**Imstscadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="6e9e2-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="6e9e2-155">Remotedesktop-Webverbindung Referenz</span><span class="sxs-lookup"><span data-stu-id="6e9e2-155">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

