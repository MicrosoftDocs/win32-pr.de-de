---
title: IMsRdpClientAdvancedSettings4-Schnittstelle
description: Verwaltet erweiterte Client Einstellungen. Wird von der IMsRdpClientAdvancedSettings3-Schnittstelle abgeleitet.
ms.assetid: cb1785d6-1f94-4423-bdda-0e3e4e9b8641
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d840206a139e3c3272551eab6a187a7b18416e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391877"
---
# <a name="imsrdpclientadvancedsettings4-interface"></a><span data-ttu-id="43805-106">IMsRdpClientAdvancedSettings4-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="43805-106">IMsRdpClientAdvancedSettings4 interface</span></span>

<span data-ttu-id="43805-107">Verwaltet erweiterte Client Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="43805-107">Manages advanced client settings.</span></span> <span data-ttu-id="43805-108">Wird von der [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) -Schnittstelle abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="43805-108">Derives from the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span> <span data-ttu-id="43805-109">Diese Schnittstelle enthält Methoden zum Abrufen und Festlegen erweiterter (optionaler) Eigenschaften für das Remotedesktop ActiveX-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="43805-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="43805-110">Um eine Instanz dieser Schnittstelle abzurufen, verwenden Sie die [**imstscax:: advancedsettings**](imstscax-advancedsettings.md) -Eigenschaft, um einen [**imstscadvancedsettings**](imstscadvancedsettings-interface.md) -Schnittstellen Zeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="43805-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="43805-111">Nennen Sie dann [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den **imstscadvancedsettings** -Zeiger, und übergeben Sie **IID \_ IMsRdpClientAdvancedSettings4** an **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="43805-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings4** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="43805-112">Member</span><span class="sxs-lookup"><span data-stu-id="43805-112">Members</span></span>

<span data-ttu-id="43805-113">Die **IMsRdpClientAdvancedSettings4** -Schnittstelle erbt von [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md).</span><span class="sxs-lookup"><span data-stu-id="43805-113">The **IMsRdpClientAdvancedSettings4** interface inherits from [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md).</span></span> <span data-ttu-id="43805-114">**IMsRdpClientAdvancedSettings4** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="43805-114">**IMsRdpClientAdvancedSettings4** also has these types of members:</span></span>

-   [<span data-ttu-id="43805-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43805-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43805-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43805-116">Properties</span></span>

<span data-ttu-id="43805-117">Die **IMsRdpClientAdvancedSettings4** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="43805-117">The **IMsRdpClientAdvancedSettings4** interface has these properties.</span></span>



| <span data-ttu-id="43805-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="43805-118">Property</span></span>                                                                                    | <span data-ttu-id="43805-119">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="43805-119">Access type</span></span>           | <span data-ttu-id="43805-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43805-120">Description</span></span>                                                              |
|:--------------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="43805-121">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="43805-121">**AuthenticationLevel**</span></span>](imsrdpclientadvancedsettings4-authenticationlevel.md)<br/> | <span data-ttu-id="43805-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="43805-122">Read/write</span></span><br/> | <span data-ttu-id="43805-123">Gibt die Authentifizierungs Ebene an, die für die Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43805-123">Specifies the authentication level to use for the connection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43805-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43805-124">Remarks</span></span>

<span data-ttu-id="43805-125">Diese Schnittstelle wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:</span><span class="sxs-lookup"><span data-stu-id="43805-125">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="43805-126">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="43805-126">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="43805-127">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="43805-127">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="43805-128">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="43805-128">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="43805-129">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="43805-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43805-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43805-130">Requirements</span></span>



| <span data-ttu-id="43805-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43805-131">Requirement</span></span> | <span data-ttu-id="43805-132">Wert</span><span class="sxs-lookup"><span data-stu-id="43805-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43805-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43805-133">Minimum supported client</span></span><br/> | <span data-ttu-id="43805-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43805-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="43805-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43805-135">Minimum supported server</span></span><br/> | <span data-ttu-id="43805-136">Windows Server 2008, Windows Server 2008 mit SP1</span><span class="sxs-lookup"><span data-stu-id="43805-136">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                     |
| <span data-ttu-id="43805-137">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="43805-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="43805-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43805-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="43805-139">DLL</span><span class="sxs-lookup"><span data-stu-id="43805-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43805-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43805-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="43805-141">IID</span><span class="sxs-lookup"><span data-stu-id="43805-141">IID</span></span><br/>                      | <span data-ttu-id="43805-142">IID \_ IMsRdpClientAdvancedSettings4 ist als FBA7F64E-7345-4405-AE50-FA4A763DC0DE definiert.</span><span class="sxs-lookup"><span data-stu-id="43805-142">IID\_IMsRdpClientAdvancedSettings4 is defined as FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43805-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43805-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43805-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="43805-144">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="43805-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="43805-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="43805-146">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="43805-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="43805-147">**Imstscadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="43805-147">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="43805-148">Remotedesktop-Webverbindung Referenz</span><span class="sxs-lookup"><span data-stu-id="43805-148">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

