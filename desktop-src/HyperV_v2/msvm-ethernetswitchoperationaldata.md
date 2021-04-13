---
description: Stellt Switch-Betriebsparameter dar.
ms.assetid: f225d321-8f40-4e6c-b30d-8fab3f84761d
title: Msvm_EthernetSwitchOperationalData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchOperationalData
- Msvm_EthernetSwitchOperationalData.InstanceID
- Msvm_EthernetSwitchOperationalData.Caption
- Msvm_EthernetSwitchOperationalData.Description
- Msvm_EthernetSwitchOperationalData.ElementName
- Msvm_EthernetSwitchOperationalData.SystemCreationClassName
- Msvm_EthernetSwitchOperationalData.SystemName
- Msvm_EthernetSwitchOperationalData.CreationClassName
- Msvm_EthernetSwitchOperationalData.Name
- Msvm_EthernetSwitchOperationalData.CurrentSwitchingMode
- Msvm_EthernetSwitchOperationalData.SupportedSwitchingModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d9aacd8380650ddaf2790aeacf4a2327b54f973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350659"
---
# <a name="msvm_ethernetswitchoperationaldata-class"></a><span data-ttu-id="d4de3-103">MSVM \_ ethernetzwitchoperationaldata-Klasse</span><span class="sxs-lookup"><span data-stu-id="d4de3-103">Msvm\_EthernetSwitchOperationalData class</span></span>

<span data-ttu-id="d4de3-104">Stellt Switch-Betriebsparameter dar.</span><span class="sxs-lookup"><span data-stu-id="d4de3-104">Represents switch operational parameters.</span></span>

<span data-ttu-id="d4de3-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d4de3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4de3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4de3-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1D18CDCF-209E-4172-875D-6D208A0A8375"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Modes Supported "), AMENDMENT]
class Msvm_EthernetSwitchOperationalData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Modes Supported";
  string Description = "Represents switch operational parameters.";
  string ElementName = "Ethernet Switch Modes Supported";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = " Msvm_EthernetSwitchOperationalData";
  string Name;
  uint32 CurrentSwitchingMode = 1;
  uint32 SupportedSwitchingModes[] = {1};
};
```

## <a name="members"></a><span data-ttu-id="d4de3-107">Member</span><span class="sxs-lookup"><span data-stu-id="d4de3-107">Members</span></span>

<span data-ttu-id="d4de3-108">Die **MSVM \_ ethernetzwitchoperationaldata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d4de3-108">The **Msvm\_EthernetSwitchOperationalData** class has these types of members:</span></span>

-   [<span data-ttu-id="d4de3-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4de3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d4de3-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4de3-110">Properties</span></span>

<span data-ttu-id="d4de3-111">Die **MSVM \_ ethernetzwitchoperationaldata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d4de3-111">The **Msvm\_EthernetSwitchOperationalData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d4de3-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d4de3-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4de3-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d4de3-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4de3-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4de3-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4de3-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d4de3-115">A short description of the object.</span></span> <span data-ttu-id="d4de3-116">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d4de3-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d4de3-117">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="d4de3-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4de3-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d4de3-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4de3-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4de3-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4de3-120">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d4de3-120">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="d4de3-121">Der Name der Klasse oder Unterklasse, die bei der Erstellung dieser Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4de3-121">The name of the class or subclass used in the creation of this instance.</span></span> <span data-ttu-id="d4de3-122">Diese Eigenschaft wird von [**MSVM \_ ethernetzwitchdata**](msvm-ethernetswitchdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d4de3-122">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4de3-123">**Currentswitchingmode**</span><span class="sxs-lookup"><span data-stu-id="d4de3-123">**CurrentSwitchingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4de3-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4de3-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4de3-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4de3-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4de3-126">Qualifizierer: **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="d4de3-126">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="d4de3-127">Der aktuelle Wechsel Modus auf dem Switch.</span><span class="sxs-lookup"><span data-stu-id="d4de3-127">The current switching mode on the switch.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d4de3-128">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="d4de3-128">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Q"></span><span id="802.1q"></span>

<span data-ttu-id="d4de3-129">**802.1 q** (1)</span><span class="sxs-lookup"><span data-stu-id="d4de3-129">**802.1Q** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Qbg"></span><span id="802.1qbg"></span><span id="802.1QBG"></span>

<span data-ttu-id="d4de3-130">**802.1 qbg** (2)</span><span class="sxs-lookup"><span data-stu-id="d4de3-130">**802.1Qbg** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Qbh"></span><span id="802.1qbh"></span><span id="802.1QBH"></span>

<span data-ttu-id="d4de3-131">**802.1 QBH** (3)</span><span class="sxs-lookup"><span data-stu-id="d4de3-131">**802.1Qbh** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d4de3-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d4de3-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4de3-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d4de3-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4de3-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4de3-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4de3-135">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="d4de3-135">A description of the object.</span></span> <span data-ttu-id="d4de3-136">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d4de3-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d4de3-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d4de3-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4de3-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d4de3-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4de3-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4de3-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4de3-140">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d4de3-140">A display name for the object.</span></span> <span data-ttu-id="d4de3-141">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d4de3-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d4de3-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d4de3-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4de3-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d4de3-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4de3-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4de3-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4de3-145">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="d4de3-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d4de3-146">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="d4de3-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d4de3-147">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d4de3-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d4de3-148">**Name**</span><span class="sxs-lookup"><span data-stu-id="d4de3-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4de3-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d4de3-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4de3-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4de3-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4de3-151">Qualifizierer: **Key**, **override**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d4de3-151">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="d4de3-152">Der eindeutige Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="d4de3-152">The unique name of the resource.</span></span> <span data-ttu-id="d4de3-153">Diese Eigenschaft wird von [**MSVM \_ ethernetzwitchdata**](msvm-ethernetswitchdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d4de3-153">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4de3-154">**Supportedswitchingmodes**</span><span class="sxs-lookup"><span data-stu-id="d4de3-154">**SupportedSwitchingModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4de3-155">Datentyp: **UInt32** Array</span><span class="sxs-lookup"><span data-stu-id="d4de3-155">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="d4de3-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4de3-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4de3-157">Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="d4de3-157">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="d4de3-158">Die vom Switch unterstützten Wechsel Modi.</span><span class="sxs-lookup"><span data-stu-id="d4de3-158">The switching modes supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="d4de3-159">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="d4de3-159">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4de3-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d4de3-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4de3-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4de3-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4de3-162">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d4de3-162">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="d4de3-163">Der Name der Erstellungs Klasse des hostingsystems.</span><span class="sxs-lookup"><span data-stu-id="d4de3-163">The hosting system's creation class name.</span></span> <span data-ttu-id="d4de3-164">Diese Eigenschaft wird von [**MSVM \_ ethernetzwitchdata**](msvm-ethernetswitchdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d4de3-164">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4de3-165">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="d4de3-165">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4de3-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d4de3-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4de3-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4de3-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4de3-168">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d4de3-168">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="d4de3-169">Der Name des virtuellen Switchs, an den die zugeordnete Ressourcen Instanz gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="d4de3-169">The name of the virtual switch to which the associated resource instance is bound.</span></span> <span data-ttu-id="d4de3-170">Diese Eigenschaft wird von [**MSVM \_ ethernetzwitchdata**](msvm-ethernetswitchdata.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d4de3-170">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4de3-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4de3-171">Requirements</span></span>



| <span data-ttu-id="d4de3-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4de3-172">Requirement</span></span> | <span data-ttu-id="d4de3-173">Wert</span><span class="sxs-lookup"><span data-stu-id="d4de3-173">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4de3-174">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4de3-174">Minimum supported client</span></span><br/> | <span data-ttu-id="d4de3-175">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4de3-175">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d4de3-176">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4de3-176">Minimum supported server</span></span><br/> | <span data-ttu-id="d4de3-177">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4de3-177">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d4de3-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="d4de3-178">Namespace</span></span><br/>                | <span data-ttu-id="d4de3-179">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d4de3-179">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d4de3-180">MOF</span><span class="sxs-lookup"><span data-stu-id="d4de3-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4de3-181"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d4de3-181"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4de3-182">DLL</span><span class="sxs-lookup"><span data-stu-id="d4de3-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4de3-183"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d4de3-183"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

