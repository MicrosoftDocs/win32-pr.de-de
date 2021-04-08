---
title: Win32_TSGatewayLoadBalancer-Klasse
description: Beschreibt eine Gruppe von Remotedesktop Gateway-Lasten Ausgleichs Servern (RD-Gateway). Diese werden verwendet, um einen Lastenausgleich RD-Gateway Verbindungen über mehrere Server hinweg durchzusetzen.
ms.assetid: aa7e7b77-7233-4c6a-8f41-cc332fa509d5
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayLoadBalancer-Klasse Remotedesktopdienste
- Win32_TSGatewayLoadBalancer Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer.Servers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4956ed4dc9536ff6f7e3263071a2a477cb0f515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741249"
---
# <a name="win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="114f9-106">Win32-Klasse "t- \_ gatewayloadbalancer"</span><span class="sxs-lookup"><span data-stu-id="114f9-106">Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="114f9-107">Beschreibt eine Gruppe von Remotedesktop Gateway-Lasten Ausgleichs Servern (RD-Gateway).</span><span class="sxs-lookup"><span data-stu-id="114f9-107">Describes a set of Remote Desktop Gateway (RD Gateway) load-balancing servers.</span></span> <span data-ttu-id="114f9-108">Diese werden verwendet, um einen Lastenausgleich RD-Gateway Verbindungen über mehrere Server hinweg durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="114f9-108">These are used to load balance RD Gateway connections across multiple servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="114f9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="114f9-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayLoadBalancer
{
  string Servers;
};
```

## <a name="members"></a><span data-ttu-id="114f9-110">Member</span><span class="sxs-lookup"><span data-stu-id="114f9-110">Members</span></span>

<span data-ttu-id="114f9-111">Die Win32-Klasse " **\_ zgatewayloadbalancer** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="114f9-111">The **Win32\_TSGatewayLoadBalancer** class has these types of members:</span></span>

-   [<span data-ttu-id="114f9-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="114f9-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="114f9-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="114f9-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="114f9-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="114f9-114">Methods</span></span>

<span data-ttu-id="114f9-115">Die Win32-Klasse " **\_ zgatewayloadbalancer** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="114f9-115">The **Win32\_TSGatewayLoadBalancer** class has these methods.</span></span>



| <span data-ttu-id="114f9-116">Methode</span><span class="sxs-lookup"><span data-stu-id="114f9-116">Method</span></span>                                                                             | <span data-ttu-id="114f9-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="114f9-117">Description</span></span>                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="114f9-118">**Addservers**</span><span class="sxs-lookup"><span data-stu-id="114f9-118">**AddServers**</span></span>](addservers-win32-tsgatewayloadbalancer.md)                       | <span data-ttu-id="114f9-119">Fügt der **Server** Eigenschaft Server hinzu.</span><span class="sxs-lookup"><span data-stu-id="114f9-119">Adds servers to the **Servers** property.</span></span><br/>                                                             |
| [<span data-ttu-id="114f9-120">**Deleteallservers**</span><span class="sxs-lookup"><span data-stu-id="114f9-120">**DeleteAllServers**</span></span>](deleteallservers-win32-tsgatewayloadbalancer.md)           | <span data-ttu-id="114f9-121">Löscht alle RD-Gateway Lasten Ausgleichs Server, die Teil der Lasten Ausgleichs Farm sind.</span><span class="sxs-lookup"><span data-stu-id="114f9-121">Deletes all RD Gateway load-balancing servers participating in the load-balancing farm.</span></span><br/>               |
| [<span data-ttu-id="114f9-122">**Delta Server**</span><span class="sxs-lookup"><span data-stu-id="114f9-122">**DeleteServers**</span></span>](deleteservers-win32-tsgatewayloadbalancer.md)                 | <span data-ttu-id="114f9-123">Löscht Server aus der **Server** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="114f9-123">Deletes servers from the **Servers** property.</span></span><br/>                                                        |
| [<span data-ttu-id="114f9-124">**Isloadbalancingserver**</span><span class="sxs-lookup"><span data-stu-id="114f9-124">**IsLoadBalancingServer**</span></span>](win32-tsgatewayloadbalancer-isloadbalancingserver.md) | <span data-ttu-id="114f9-125">Bestimmt, ob der Server einen Lastenausgleich durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="114f9-125">Determines whether the server can perform load balancing.</span></span><br/>                                             |
| [<span data-ttu-id="114f9-126">**Setservers**</span><span class="sxs-lookup"><span data-stu-id="114f9-126">**SetServers**</span></span>](setservers-win32-tsgatewayloadbalancer.md)                       | <span data-ttu-id="114f9-127">Legt die **Server** -Eigenschaft mit der durch Semikolons getrennten Liste von RD-Gateway Lasten Ausgleichs Servern fest.</span><span class="sxs-lookup"><span data-stu-id="114f9-127">Sets the **Servers** property with the semicolon-separated list of RD Gateway load-balancing servers.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="114f9-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="114f9-128">Properties</span></span>

<span data-ttu-id="114f9-129">Die Win32-Klasse "t- **\_ gatewayloadbalancer** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="114f9-129">The **Win32\_TSGatewayLoadBalancer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="114f9-130">**Server**</span><span class="sxs-lookup"><span data-stu-id="114f9-130">**Servers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="114f9-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="114f9-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="114f9-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="114f9-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="114f9-133">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="114f9-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="114f9-134">Durch Semikolons getrennte Liste der RD-Gateway Lasten Ausgleichs Server.</span><span class="sxs-lookup"><span data-stu-id="114f9-134">Semicolon-separated list of RD Gateway load-balancing servers.</span></span> <span data-ttu-id="114f9-135">Diese Eigenschaft kann mit den Methoden [**setservers**](setservers-win32-tsgatewayloadbalancer.md), [**addservers**](addservers-win32-tsgatewayloadbalancer.md), [**deleteservers**](deleteservers-win32-tsgatewayloadbalancer.md)und [**deleteallservers**](deleteallservers-win32-tsgatewayloadbalancer.md) geändert werden.</span><span class="sxs-lookup"><span data-stu-id="114f9-135">This property can be changed with the [**SetServers**](setservers-win32-tsgatewayloadbalancer.md), [**AddServers**](addservers-win32-tsgatewayloadbalancer.md), [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md), and [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="114f9-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="114f9-136">Remarks</span></span>

<span data-ttu-id="114f9-137">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="114f9-137">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="114f9-138">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="114f9-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="114f9-139">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="114f9-139">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="114f9-140">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="114f9-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="114f9-141">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="114f9-141">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="114f9-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="114f9-142">Requirements</span></span>



| <span data-ttu-id="114f9-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="114f9-143">Requirement</span></span> | <span data-ttu-id="114f9-144">Wert</span><span class="sxs-lookup"><span data-stu-id="114f9-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="114f9-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="114f9-145">Minimum supported client</span></span><br/> | <span data-ttu-id="114f9-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="114f9-146">None supported</span></span><br/>                                                                |
| <span data-ttu-id="114f9-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="114f9-147">Minimum supported server</span></span><br/> | <span data-ttu-id="114f9-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="114f9-148">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="114f9-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="114f9-149">Namespace</span></span><br/>                | <span data-ttu-id="114f9-150">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="114f9-150">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="114f9-151">MOF</span><span class="sxs-lookup"><span data-stu-id="114f9-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="114f9-152"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="114f9-152"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="114f9-153">DLL</span><span class="sxs-lookup"><span data-stu-id="114f9-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="114f9-154"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="114f9-154"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="114f9-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="114f9-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="114f9-156">**Win32-"- \_ gatewayconnection"**</span><span class="sxs-lookup"><span data-stu-id="114f9-156">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="114f9-157">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="114f9-157">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="114f9-158">**Win32-"t- \_ gatewayradiusserver"**</span><span class="sxs-lookup"><span data-stu-id="114f9-158">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="114f9-159">**Win32- \_ faigatewayresourceauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="114f9-159">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="114f9-160">**Win32-Datei " \_ zgatewayresourcegroup"**</span><span class="sxs-lookup"><span data-stu-id="114f9-160">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="114f9-161">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="114f9-161">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

