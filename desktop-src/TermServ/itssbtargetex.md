---
title: Itssbtargetex-Schnittstelle
description: Macht Eigenschaften verfügbar, die Konfigurations-und Zustandsinformationen zu einem Ziel speichern.
ms.assetid: 3f0f26fb-e8bc-47eb-8038-e51792ad4376
ms.tgt_platform: multiple
keywords:
- Itssbtargetex-Schnittstelle Remotedesktopdienste
- Itssbtargetex-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- ITsSbTargetEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d53d126d9419f87d91b027b0d69847f67de84be6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957129"
---
# <a name="itssbtargetex-interface"></a><span data-ttu-id="dc5c9-105">Itssbtargetex-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="dc5c9-105">ITsSbTargetEx interface</span></span>

<span data-ttu-id="dc5c9-106">Macht Eigenschaften verfügbar, die Konfigurations-und Zustandsinformationen zu einem Ziel speichern.</span><span class="sxs-lookup"><span data-stu-id="dc5c9-106">Exposes properties that store configuration and state information about a target.</span></span>

<span data-ttu-id="dc5c9-107">Diese Schnittstelle ist nur unter Windows Server 2012 R2 mit installiertem [KB3091411](https://support.microsoft.com/kb/3091411) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dc5c9-107">This interface is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed.</span></span> <span data-ttu-id="dc5c9-108">Die [**targetload**](itssbtarget-targetload.md) -Eigenschaft der [**itssbtarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) -Schnittstelle ist ab Windows Server 2016 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dc5c9-108">The [**TargetLoad**](itssbtarget-targetload.md) property of the [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) interface is available starting with Windows Server 2016.</span></span>

## <a name="members"></a><span data-ttu-id="dc5c9-109">Member</span><span class="sxs-lookup"><span data-stu-id="dc5c9-109">Members</span></span>

<span data-ttu-id="dc5c9-110">Die **itssbtargetex** -Schnittstelle erbt von [**itssbtarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget).</span><span class="sxs-lookup"><span data-stu-id="dc5c9-110">The **ITsSbTargetEx** interface inherits from [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget).</span></span> <span data-ttu-id="dc5c9-111">**Itssbtargetex** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dc5c9-111">**ITsSbTargetEx** also has these types of members:</span></span>

-   [<span data-ttu-id="dc5c9-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc5c9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc5c9-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc5c9-113">Properties</span></span>

<span data-ttu-id="dc5c9-114">Die **itssbtargetex** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc5c9-114">The **ITsSbTargetEx** interface has these properties.</span></span>



| <span data-ttu-id="dc5c9-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dc5c9-115">Property</span></span>                                                                      | <span data-ttu-id="dc5c9-116">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="dc5c9-116">Access type</span></span>           | <span data-ttu-id="dc5c9-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc5c9-117">Description</span></span>                                                                               |
|:------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc5c9-118">**EnvironmentName**</span><span class="sxs-lookup"><span data-stu-id="dc5c9-118">**EnvironmentName**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_environmentname)<br/>             | <span data-ttu-id="dc5c9-119">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc5c9-119">Read/write</span></span><br/> | <span data-ttu-id="dc5c9-120">Ruft den Namen der Umgebung ab, die dem Ziel zugeordnet ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="dc5c9-120">Retrieves or specifies the name of the environment associated with the target.</span></span><br/> |
| [<span data-ttu-id="dc5c9-121">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="dc5c9-121">**FarmName**</span></span>](itssbtarget-farmname.md)<br/>                           | <span data-ttu-id="dc5c9-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc5c9-122">Read/write</span></span><br/> | <span data-ttu-id="dc5c9-123">Gibt den Namen der Farm an, mit der dieses Ziel verknüpft ist, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="dc5c9-123">Specifies or retrieves the name of the farm to which this target is joined.</span></span><br/>    |
| [<span data-ttu-id="dc5c9-124">**IpAddresses**</span><span class="sxs-lookup"><span data-stu-id="dc5c9-124">**IpAddresses**</span></span>](itssbtarget-ipaddresses.md)<br/>                     | <span data-ttu-id="dc5c9-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc5c9-125">Read/write</span></span><br/> | <span data-ttu-id="dc5c9-126">Ruft die externen IP-Adressen des Ziels ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="dc5c9-126">Retrieves or specifies the external IP addresses of the target.</span></span><br/>                |
| [<span data-ttu-id="dc5c9-127">**Numpenidingconnections**</span><span class="sxs-lookup"><span data-stu-id="dc5c9-127">**NumPendingConnections**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numpendingconnections)<br/> | <span data-ttu-id="dc5c9-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc5c9-128">Read-only</span></span><br/>  | <span data-ttu-id="dc5c9-129">Ruft die Anzahl der ausstehenden Benutzer Verbindungen für das Ziel ab.</span><span class="sxs-lookup"><span data-stu-id="dc5c9-129">Retrieves the number of pending user connections for the target.</span></span><br/>               |
| [<span data-ttu-id="dc5c9-130">**Numsessions**</span><span class="sxs-lookup"><span data-stu-id="dc5c9-130">**NumSessions**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numsessions)<br/>                     | <span data-ttu-id="dc5c9-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc5c9-131">Read-only</span></span><br/>  | <span data-ttu-id="dc5c9-132">Ruft die Anzahl der Sitzungen ab, die vom Broker für das Ziel verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="dc5c9-132">Retrieves the number of sessions maintained by broker for the target.</span></span><br/>          |
| [<span data-ttu-id="dc5c9-133">**Target-qdn**</span><span class="sxs-lookup"><span data-stu-id="dc5c9-133">**TargetFQDN**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetfqdn)<br/>                       | <span data-ttu-id="dc5c9-134">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc5c9-134">Read/write</span></span><br/> | <span data-ttu-id="dc5c9-135">Gibt den voll qualifizierten Domänen Namen des Ziels an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="dc5c9-135">Specifies or retrieves the fully qualified domain name of the target.</span></span><br/>          |
| <span data-ttu-id="dc5c9-136">[**Targetload**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dc5c9-136">[**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))</span></span><br/>                     | <span data-ttu-id="dc5c9-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc5c9-137">Read-only</span></span><br/>  | <span data-ttu-id="dc5c9-138">Ruft die relative Auslastung eines Ziels ab.</span><span class="sxs-lookup"><span data-stu-id="dc5c9-138">Retrieves the relative load on a target.</span></span><br/>                                       |
| [<span data-ttu-id="dc5c9-139">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="dc5c9-139">**TargetName**</span></span>](itssbtarget-targetname.md)<br/>                       | <span data-ttu-id="dc5c9-140">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc5c9-140">Read/write</span></span><br/> | <span data-ttu-id="dc5c9-141">Gibt den Namen des Ziels an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="dc5c9-141">Specifies or retrieves the name of the target.</span></span><br/>                                 |
| [<span data-ttu-id="dc5c9-142">**Targetnetbios**</span><span class="sxs-lookup"><span data-stu-id="dc5c9-142">**TargetNetbios**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetnetbios)<br/>                 | <span data-ttu-id="dc5c9-143">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc5c9-143">Read/write</span></span><br/> | <span data-ttu-id="dc5c9-144">Gibt den NetBIOS-Namen des Ziels an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="dc5c9-144">Specifies or retrieves the NetBIOS name of the target.</span></span><br/>                         |
| [<span data-ttu-id="dc5c9-145">**Targetpropertyset**</span><span class="sxs-lookup"><span data-stu-id="dc5c9-145">**TargetPropertySet**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetpropertyset)<br/>         | <span data-ttu-id="dc5c9-146">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc5c9-146">Read/write</span></span><br/> | <span data-ttu-id="dc5c9-147">Gibt die für das Ziel festgelegte Eigenschaft an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="dc5c9-147">Specifies or retrieves the property set for the target.</span></span><br/>                        |
| [<span data-ttu-id="dc5c9-148">**TargetState**</span><span class="sxs-lookup"><span data-stu-id="dc5c9-148">**TargetState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate)<br/>                     | <span data-ttu-id="dc5c9-149">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc5c9-149">Read/write</span></span><br/> | <span data-ttu-id="dc5c9-150">Gibt den Ziel Status an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="dc5c9-150">Specifies or retrieves the target state.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="dc5c9-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc5c9-151">Requirements</span></span>



| <span data-ttu-id="dc5c9-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc5c9-152">Requirement</span></span> | <span data-ttu-id="dc5c9-153">Wert</span><span class="sxs-lookup"><span data-stu-id="dc5c9-153">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dc5c9-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc5c9-154">Minimum supported client</span></span><br/> | <span data-ttu-id="dc5c9-155">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dc5c9-155">None supported</span></span><br/>                                                        |
| <span data-ttu-id="dc5c9-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc5c9-156">Minimum supported server</span></span><br/> | <span data-ttu-id="dc5c9-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dc5c9-157">Windows Server 2012 R2</span></span><br/>                                                |
| <span data-ttu-id="dc5c9-158">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="dc5c9-158">End of server support</span></span><br/>    | <span data-ttu-id="dc5c9-159">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dc5c9-159">Windows Server 2012 R2</span></span><br/>                                                |
| <span data-ttu-id="dc5c9-160">IID</span><span class="sxs-lookup"><span data-stu-id="dc5c9-160">IID</span></span><br/>                      | <span data-ttu-id="dc5c9-161">IID \_ itssbtargetex ist als 74f 99987-625d-11e5-bea1-a0481c7e9064 definiert</span><span class="sxs-lookup"><span data-stu-id="dc5c9-161">IID\_ITsSbTargetEx is defined as 74f99987-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dc5c9-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc5c9-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc5c9-163">**Itssbtarget**</span><span class="sxs-lookup"><span data-stu-id="dc5c9-163">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[<span data-ttu-id="dc5c9-164">Remotedesktop Virtualisierungsschnittstellen</span><span class="sxs-lookup"><span data-stu-id="dc5c9-164">Remote Desktop Virtualization Interfaces</span></span>](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

