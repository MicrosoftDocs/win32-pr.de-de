---
title: Win32_TSGatewayResourceGroup-Klasse
description: Beschreibt eine Ressourcengruppe, die eine Gruppe von Ressourcen (Computernamen) einer einzelnen Entität zuordnet.
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceGroup-Klasse Remotedesktopdienste
- Win32_TSGatewayResourceGroup Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup.Name
- Win32_TSGatewayResourceGroup.Description
- Win32_TSGatewayResourceGroup.AssociatedRAPs
- Win32_TSGatewayResourceGroup.Resources
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffeda42abafd24526360f5e549f004cae0c3140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339964"
---
# <a name="win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="6e5c9-105">Win32- \_ Klasse "zgatewayresourcegroup"</span><span class="sxs-lookup"><span data-stu-id="6e5c9-105">Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="6e5c9-106">Beschreibt eine Ressourcengruppe, die eine Gruppe von Ressourcen (Computernamen) einer einzelnen Entität zuordnet.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-106">Describes a resource group, which maps a set of resources (computer names) to a single entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e5c9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e5c9-107">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceGroup
{
  string Name;
  string Description;
  string AssociatedRAPs;
  string Resources;
};
```

## <a name="members"></a><span data-ttu-id="6e5c9-108">Member</span><span class="sxs-lookup"><span data-stu-id="6e5c9-108">Members</span></span>

<span data-ttu-id="6e5c9-109">Die Win32-Klasse "t- **\_ gatewayresourcegroup** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6e5c9-109">The **Win32\_TSGatewayResourceGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="6e5c9-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="6e5c9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6e5c9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e5c9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6e5c9-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="6e5c9-112">Methods</span></span>

<span data-ttu-id="6e5c9-113">Die Win32-Klasse "t- **\_ gatewayresourcegroup** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-113">The **Win32\_TSGatewayResourceGroup** class has these methods.</span></span>



| <span data-ttu-id="6e5c9-114">Methode</span><span class="sxs-lookup"><span data-stu-id="6e5c9-114">Method</span></span>                                                                  | <span data-ttu-id="6e5c9-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e5c9-115">Description</span></span>                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e5c9-116">**AddResource**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-116">**AddResources**</span></span>](addresources-win32-tsgatewayresourcegroup.md)       | <span data-ttu-id="6e5c9-117">Fügt der **Ressourcen** Eigenschaft für diese Ressourcengruppe Ressourcen hinzu.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-117">Adds resources to the **Resources** property for this resource group.</span></span><br/>      |
| [<span data-ttu-id="6e5c9-118">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-118">**Create**</span></span>](create-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="6e5c9-119">Erstellt eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-119">Creates a resource group.</span></span><br/>                                                  |
| [<span data-ttu-id="6e5c9-120">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-120">**Delete**</span></span>](delete-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="6e5c9-121">Löscht diese Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-121">Deletes this resource group.</span></span><br/>                                               |
| [<span data-ttu-id="6e5c9-122">**Removeresources**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-122">**RemoveResources**</span></span>](removeresources-win32-tsgatewayresourcegroup.md) | <span data-ttu-id="6e5c9-123">Löscht Ressourcen aus der **Ressourcen** Eigenschaft für diese Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-123">Deletes resources from the **Resources** property for this resource group.</span></span><br/> |
| [<span data-ttu-id="6e5c9-124">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-124">**SetDescription**</span></span>](setdescription-win32-tsgatewayresourcegroup.md)   | <span data-ttu-id="6e5c9-125">Legt die **Beschreibungs** Eigenschaft für diese Ressourcengruppe fest.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-125">Sets the **Description** property for this resource group.</span></span><br/>                 |
| [<span data-ttu-id="6e5c9-126">**SetName**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-126">**SetName**</span></span>](setname-win32-tsgatewayresourcegroup.md)                 | <span data-ttu-id="6e5c9-127">Legt die **Name** -Eigenschaft für diese Ressourcengruppe fest.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-127">Sets the **Name** property for this resource group.</span></span><br/>                        |
| [<span data-ttu-id="6e5c9-128">**Abtresources**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-128">**SetResources**</span></span>](setresources-win32-tsgatewayresourcegroup.md)       | <span data-ttu-id="6e5c9-129">Legt die **Ressourcen** Eigenschaft für diese Ressourcengruppe fest.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-129">Sets the **Resources** property for this resource group.</span></span><br/>                   |
| [<span data-ttu-id="6e5c9-130">**Aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-130">**Update**</span></span>](update-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="6e5c9-131">Aktualisiert diese Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-131">Updates this resource group.</span></span><br/>                                               |



 

### <a name="properties"></a><span data-ttu-id="6e5c9-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e5c9-132">Properties</span></span>

<span data-ttu-id="6e5c9-133">Die Win32-Klasse " **\_ zgatewayresourcegroup** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-133">The **Win32\_TSGatewayResourceGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e5c9-134">**Associatedraps**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-134">**AssociatedRAPs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e5c9-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e5c9-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e5c9-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e5c9-137">Durch Semikolons getrennte Liste von Remotedesktopdienste-Ressourcen Autorisierungs Richtlinien (RD-RAPs), die dieser Ressourcengruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-137">Semicolon-separated list of Remote Desktop Services resource authorization policies (RD RAPs) that are associated with this resource group.</span></span>

</dd> <dt>

<span data-ttu-id="6e5c9-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e5c9-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e5c9-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e5c9-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e5c9-141">Beschreibung der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-141">Description of the resource group.</span></span> <span data-ttu-id="6e5c9-142">Diese Eigenschaft kann mit der [**setDescription**](setdescription-win32-tsgatewayresourcegroup.md) -Methode geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-142">This property can be changed with the [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="6e5c9-143">**Name**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e5c9-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e5c9-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e5c9-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e5c9-146">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6e5c9-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6e5c9-147">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6e5c9-147">Name of the resource group.</span></span> <span data-ttu-id="6e5c9-148">Diese Eigenschaft kann mit der [**SetName**](setname-win32-tsgatewayresourcegroup.md) -Methode geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-148">This property can be changed with the [**SetName**](setname-win32-tsgatewayresourcegroup.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="6e5c9-149">**Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-149">**Resources**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e5c9-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e5c9-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e5c9-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e5c9-152">Durch Semikolons getrennte Liste von Ressourcen in dieser Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-152">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="6e5c9-153">Ein " \* " bedeutet alle Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-153">An "\*" means all resources.</span></span> <span data-ttu-id="6e5c9-154">Diese Eigenschaft kann mit den Methoden "Settings", " [**adresssources**](addresources-win32-tsgatewayresourcegroup.md) [**", "**](setresources-win32-tsgatewayresourcegroup.md) [**removeresources**](removeresources-win32-tsgatewayresourcegroup.md)" und " [**Update**](update-win32-tsgatewayresourcegroup.md) " geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-154">This property can be changed with the [**SetResources**](setresources-win32-tsgatewayresourcegroup.md), [**AddResources**](addresources-win32-tsgatewayresourcegroup.md), [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md), and [**Update**](update-win32-tsgatewayresourcegroup.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e5c9-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e5c9-155">Remarks</span></span>

<span data-ttu-id="6e5c9-156">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-156">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="6e5c9-157">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-157">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6e5c9-158">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-158">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6e5c9-159">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6e5c9-159">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6e5c9-160">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6e5c9-160">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e5c9-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e5c9-161">Requirements</span></span>



| <span data-ttu-id="6e5c9-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e5c9-162">Requirement</span></span> | <span data-ttu-id="6e5c9-163">Wert</span><span class="sxs-lookup"><span data-stu-id="6e5c9-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e5c9-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6e5c9-164">Minimum supported client</span></span><br/> | <span data-ttu-id="6e5c9-165">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6e5c9-165">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6e5c9-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6e5c9-166">Minimum supported server</span></span><br/> | <span data-ttu-id="6e5c9-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e5c9-167">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6e5c9-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e5c9-168">Namespace</span></span><br/>                | <span data-ttu-id="6e5c9-169">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6e5c9-169">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6e5c9-170">MOF</span><span class="sxs-lookup"><span data-stu-id="6e5c9-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e5c9-171"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="6e5c9-171"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e5c9-172">DLL</span><span class="sxs-lookup"><span data-stu-id="6e5c9-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e5c9-173"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e5c9-173"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6e5c9-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e5c9-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e5c9-175">**Win32-"- \_ gatewayconnection"**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-175">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="6e5c9-176">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-176">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="6e5c9-177">**Win32-"t- \_ gatewayloadbalancer"**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-177">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="6e5c9-178">**Win32-"t- \_ gatewayradiusserver"**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-178">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="6e5c9-179">**Win32- \_ faigatewayresourceauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-179">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="6e5c9-180">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="6e5c9-180">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

