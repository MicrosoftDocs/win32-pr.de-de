---
description: Stellt die verfügbaren Anbieter für die Replikation dar.
ms.assetid: CAAD1CFC-6473-4642-8366-0A5625AE1F70
title: Msvm_ReplicationProvider-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationProvider
- Msvm_ReplicationProvider.InstanceID
- Msvm_ReplicationProvider.Caption
- Msvm_ReplicationProvider.Description
- Msvm_ReplicationProvider.ElementName
- Msvm_ReplicationProvider.Name
- Msvm_ReplicationProvider.OperationalStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8cc821b6bdd5d6f5d1c1085a804799c662f9d62e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865520"
---
# <a name="msvm_replicationprovider-class"></a><span data-ttu-id="9da1d-103">MSVM \_ replicationprovider-Klasse</span><span class="sxs-lookup"><span data-stu-id="9da1d-103">Msvm\_ReplicationProvider class</span></span>

<span data-ttu-id="9da1d-104">Stellt die verfügbaren Anbieter für die Replikation dar.</span><span class="sxs-lookup"><span data-stu-id="9da1d-104">Represents the available providers for replication.</span></span>

<span data-ttu-id="9da1d-105">Die folgende Syntax wird aus dem MOF-Code vereinfacht und enthält diese geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9da1d-105">The following syntax is simplified from MOF code and includes these inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9da1d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9da1d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationProvider : CIM_ManagedSystemElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  uint16 OperationalStatus[];
};
```

## <a name="members"></a><span data-ttu-id="9da1d-107">Member</span><span class="sxs-lookup"><span data-stu-id="9da1d-107">Members</span></span>

<span data-ttu-id="9da1d-108">Die **MSVM- \_ replicationprovider** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9da1d-108">The **Msvm\_ReplicationProvider** class has these types of members:</span></span>

-   [<span data-ttu-id="9da1d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9da1d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9da1d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9da1d-110">Properties</span></span>

<span data-ttu-id="9da1d-111">Die **MSVM- \_ replicationprovider** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9da1d-111">The **Msvm\_ReplicationProvider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9da1d-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9da1d-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9da1d-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9da1d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9da1d-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9da1d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9da1d-115">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="9da1d-115">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="9da1d-116">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9da1d-116">A short description of the object.</span></span> <span data-ttu-id="9da1d-117">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9da1d-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="9da1d-118">Für dieses Objekt lautet der Wert:</span><span class="sxs-lookup"><span data-stu-id="9da1d-118">For this object, the value is:</span></span>

<span data-ttu-id="9da1d-119">"Replikations Anbieter"</span><span class="sxs-lookup"><span data-stu-id="9da1d-119">"Replication Provider"</span></span>

</dd> <dt>

<span data-ttu-id="9da1d-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9da1d-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9da1d-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9da1d-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9da1d-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9da1d-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9da1d-123">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="9da1d-123">A description of the object.</span></span> <span data-ttu-id="9da1d-124">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9da1d-124">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="9da1d-125">Für externe Anbieter wird der Wert von Ihnen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="9da1d-125">For external providers, the value is provided by them.</span></span> <span data-ttu-id="9da1d-126">Für Host zum Hosten des integrierten Anbieters lautet der Wert:</span><span class="sxs-lookup"><span data-stu-id="9da1d-126">For host to host inbuilt provider, the value is:</span></span>

<span data-ttu-id="9da1d-127">"Replikations Anbieter für virtuelle Computer auf Hyper-V-Host"</span><span class="sxs-lookup"><span data-stu-id="9da1d-127">"Virtual machine replication provider to Hyper-V host"</span></span>

</dd> <dt>

<span data-ttu-id="9da1d-128">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9da1d-128">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9da1d-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9da1d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9da1d-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9da1d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9da1d-131">Ein Anzeige Name für den Endpunkt Anbieter.</span><span class="sxs-lookup"><span data-stu-id="9da1d-131">A display name for the endpoint provider.</span></span> <span data-ttu-id="9da1d-132">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9da1d-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="9da1d-133">Damit Host den integrierten Anbieter hostet, wird diese Eigenschaft immer auf festgelegt:</span><span class="sxs-lookup"><span data-stu-id="9da1d-133">For host to host inbuilt provider, this property is always set to:</span></span>

<span data-ttu-id="9da1d-134">"Replikations Anbieter für virtuelle Computer auf Hyper-V-Host"</span><span class="sxs-lookup"><span data-stu-id="9da1d-134">"Virtual machine replication provider to Hyper-V host"</span></span>

</dd> <dt>

<span data-ttu-id="9da1d-135">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9da1d-135">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9da1d-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9da1d-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9da1d-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9da1d-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9da1d-138">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="9da1d-138">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="9da1d-139">Die WMI-Instanz-ID, die den Anbieter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9da1d-139">The WMI instance ID, which identifies the provider.</span></span> <span data-ttu-id="9da1d-140">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9da1d-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="9da1d-141">Das Format dieser Eigenschaft ist "Microsoft: <Host-Computername>\\ replicationprovider \\<Provider-Name>".</span><span class="sxs-lookup"><span data-stu-id="9da1d-141">The format of this property is "Microsoft:<host-machine-name>\\ReplicationProvider\\<provider-Name>."</span></span>

</dd> <dt>

<span data-ttu-id="9da1d-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="9da1d-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9da1d-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9da1d-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9da1d-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9da1d-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9da1d-145">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9da1d-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9da1d-146">Der Globally Unique Identifier (GUID) des Anbieters, der den Endpunkt Anbieter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9da1d-146">The globally unique identifier (GUID) of the provider that identifies the endpoint provider.</span></span> <span data-ttu-id="9da1d-147">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9da1d-147">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="9da1d-148">Bei einem externen Anbieter ist diese Eigenschaft die CLSID des COM-Klassen Objekts des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="9da1d-148">In the case of an external provider, this property is the CLSID of the provider COM class object.</span></span> <span data-ttu-id="9da1d-149">Damit Host den integrierten Anbieter hostet, wird diese Eigenschaft wie folgt korrigiert:</span><span class="sxs-lookup"><span data-stu-id="9da1d-149">For host to host inbuilt provider, this property is fixed as:</span></span>

<span data-ttu-id="9da1d-150">"22391cdc-272c-4ddf-ba88-9bebb1a0975c"</span><span class="sxs-lookup"><span data-stu-id="9da1d-150">"22391CDC-272C-4DDF-BA88-9BEFB1A0975C"</span></span>

</dd> <dt>

<span data-ttu-id="9da1d-151">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9da1d-151">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9da1d-152">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="9da1d-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9da1d-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9da1d-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9da1d-154">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9da1d-154">The current statuses of the object.</span></span> <span data-ttu-id="9da1d-155">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf festgelegt:</span><span class="sxs-lookup"><span data-stu-id="9da1d-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to:</span></span>

<dl> <dt>

<span data-ttu-id="9da1d-156"><span id="S_OK"></span><span id="s_ok"></span>**S \_ OK** (2)</span><span class="sxs-lookup"><span data-stu-id="9da1d-156"><span id="S_OK"></span><span id="s_ok"></span>**S\_OK** (2)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9da1d-157">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9da1d-157">Remarks</span></span>

<span data-ttu-id="9da1d-158">Zum Aktivieren einer Replikations Beziehung können Sie einen beliebigen verfügbaren Anbieter und die [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="9da1d-158">You can use any of available providers and the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to enable a replication relationship.</span></span> <span data-ttu-id="9da1d-159">Standardmäßig wählt Hyper-V den integrierten Host zum Hosten des Anbieters aus, der beim Erstellen der Replikation geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9da1d-159">Hyper-V by default chooses the inbuilt host to host provider, which can be changed while creating the replication.</span></span> <span data-ttu-id="9da1d-160">Der Hyper-V-Verwaltungsdienst kommuniziert mit einem externen Anbieter mithilfe von com.</span><span class="sxs-lookup"><span data-stu-id="9da1d-160">Hyper-V management service communicates with an external provider by using COM.</span></span>

## <a name="requirements"></a><span data-ttu-id="9da1d-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9da1d-161">Requirements</span></span>



| <span data-ttu-id="9da1d-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9da1d-162">Requirement</span></span> | <span data-ttu-id="9da1d-163">Wert</span><span class="sxs-lookup"><span data-stu-id="9da1d-163">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9da1d-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9da1d-164">Minimum supported client</span></span><br/> | <span data-ttu-id="9da1d-165">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="9da1d-165">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9da1d-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9da1d-166">Minimum supported server</span></span><br/> | <span data-ttu-id="9da1d-167">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9da1d-167">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9da1d-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="9da1d-168">Namespace</span></span><br/>                | <span data-ttu-id="9da1d-169">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9da1d-169">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9da1d-170">MOF</span><span class="sxs-lookup"><span data-stu-id="9da1d-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9da1d-171"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9da1d-171"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9da1d-172">DLL</span><span class="sxs-lookup"><span data-stu-id="9da1d-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9da1d-173"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9da1d-173"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9da1d-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9da1d-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9da1d-175">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="9da1d-175">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="9da1d-176">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="9da1d-176">**CIM\_ManagedSystemElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

