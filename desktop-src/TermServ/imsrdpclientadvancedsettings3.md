---
title: IMsRdpClientAdvancedSettings3-Schnittstelle
description: Verwaltet erweiterte Client Einstellungen. Wird von der IMsRdpClientAdvancedSettings2-Schnittstelle abgeleitet.
ms.assetid: bfa9cf74-5943-45ca-9259-3ef0cc9ab2ab
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 760ae7d40742a800556b3d62bc5a1609b89c986b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741345"
---
# <a name="imsrdpclientadvancedsettings3-interface"></a><span data-ttu-id="92b78-106">IMsRdpClientAdvancedSettings3-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="92b78-106">IMsRdpClientAdvancedSettings3 interface</span></span>

<span data-ttu-id="92b78-107">Verwaltet erweiterte Client Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="92b78-107">Manages advanced client settings.</span></span> <span data-ttu-id="92b78-108">Wird von der [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) -Schnittstelle abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="92b78-108">Derives from the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span> <span data-ttu-id="92b78-109">Diese Schnittstelle enthält Methoden zum Abrufen und Festlegen erweiterter (optionaler) Eigenschaften für das Remotedesktop ActiveX-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="92b78-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="92b78-110">Um eine Instanz dieser Schnittstelle abzurufen, verwenden Sie die [**imstscax:: advancedsettings**](imstscax-advancedsettings.md) -Eigenschaft, um einen [**imstscadvancedsettings**](imstscadvancedsettings-interface.md) -Schnittstellen Zeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="92b78-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="92b78-111">Nennen Sie dann [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den **imstscadvancedsettings** -Zeiger, und übergeben Sie **IID \_ IMsRdpClientAdvancedSettings3** an **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="92b78-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings3** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="92b78-112">Member</span><span class="sxs-lookup"><span data-stu-id="92b78-112">Members</span></span>

<span data-ttu-id="92b78-113">Die **IMsRdpClientAdvancedSettings3** -Schnittstelle erbt von [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md).</span><span class="sxs-lookup"><span data-stu-id="92b78-113">The **IMsRdpClientAdvancedSettings3** interface inherits from [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md).</span></span> <span data-ttu-id="92b78-114">**IMsRdpClientAdvancedSettings3** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="92b78-114">**IMsRdpClientAdvancedSettings3** also has these types of members:</span></span>

-   [<span data-ttu-id="92b78-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92b78-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92b78-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92b78-116">Properties</span></span>

<span data-ttu-id="92b78-117">Die **IMsRdpClientAdvancedSettings3** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="92b78-117">The **IMsRdpClientAdvancedSettings3** interface has these properties.</span></span>



| <span data-ttu-id="92b78-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="92b78-118">Property</span></span>                                                                                                            | <span data-ttu-id="92b78-119">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="92b78-119">Access type</span></span>           | <span data-ttu-id="92b78-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92b78-120">Description</span></span>                                                                            |
|:--------------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="92b78-121">**Connectionbarshowminimizebutton**</span><span class="sxs-lookup"><span data-stu-id="92b78-121">**ConnectionBarShowMinimizeButton**</span></span>](imsrdpclientadvancedsettings3-connectionbarshowminimizebutton.md)<br/> | <span data-ttu-id="92b78-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="92b78-122">Read/write</span></span><br/> | <span data-ttu-id="92b78-123">Gibt an, ob die Schaltfläche **minimieren** auf der Verbindungs Leiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="92b78-123">Specifies whether to display the **Minimize** button on the connection bar.</span></span><br/> |
| [<span data-ttu-id="92b78-124">**Connectionbarshowrestorebutton**</span><span class="sxs-lookup"><span data-stu-id="92b78-124">**ConnectionBarShowRestoreButton**</span></span>](imsrdpclientadvancedsettings3-connectionbarshowrestorebutton.md)<br/>   | <span data-ttu-id="92b78-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="92b78-125">Read/write</span></span><br/> | <span data-ttu-id="92b78-126">Gibt an, ob die Schaltfläche **Wiederherstellen** auf der Verbindungs Leiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="92b78-126">Specifies whether to display the **Restore** button on the connection bar.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="92b78-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92b78-127">Remarks</span></span>

<span data-ttu-id="92b78-128">Diese Schnittstelle wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:</span><span class="sxs-lookup"><span data-stu-id="92b78-128">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="92b78-129">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="92b78-129">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="92b78-130">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="92b78-130">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="92b78-131">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="92b78-131">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="92b78-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="92b78-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
-   [<span data-ttu-id="92b78-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="92b78-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)

<span data-ttu-id="92b78-134">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="92b78-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="92b78-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92b78-135">Requirements</span></span>



| <span data-ttu-id="92b78-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92b78-136">Requirement</span></span> | <span data-ttu-id="92b78-137">Wert</span><span class="sxs-lookup"><span data-stu-id="92b78-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92b78-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92b78-138">Minimum supported client</span></span><br/> | <span data-ttu-id="92b78-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92b78-139">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="92b78-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92b78-140">Minimum supported server</span></span><br/> | <span data-ttu-id="92b78-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92b78-141">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="92b78-142">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="92b78-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="92b78-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92b78-143"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="92b78-144">DLL</span><span class="sxs-lookup"><span data-stu-id="92b78-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92b78-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92b78-145"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="92b78-146">IID</span><span class="sxs-lookup"><span data-stu-id="92b78-146">IID</span></span><br/>                      | <span data-ttu-id="92b78-147">IID \_ IMsRdpClientAdvancedSettings3 ist als 19cd856b-c542-4c53-ACee-B127 e3be1a59 definiert.</span><span class="sxs-lookup"><span data-stu-id="92b78-147">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92b78-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92b78-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b78-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="92b78-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="92b78-150">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="92b78-150">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="92b78-151">**Imstscadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="92b78-151">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="92b78-152">Remotedesktop-Webverbindung Referenz</span><span class="sxs-lookup"><span data-stu-id="92b78-152">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

