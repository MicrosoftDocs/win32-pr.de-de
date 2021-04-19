---
description: Stellt die Einstellungsdaten für das virtuelle LAN (VLAN) dar.
ms.assetid: c3a49021-5256-4751-a5a5-81bf1c6d6e6d
title: Msvm_EthernetSwitchPortVlanSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortVlanSettingData
- Msvm_EthernetSwitchPortVlanSettingData.InstanceID
- Msvm_EthernetSwitchPortVlanSettingData.Caption
- Msvm_EthernetSwitchPortVlanSettingData.Description
- Msvm_EthernetSwitchPortVlanSettingData.ElementName
- Msvm_EthernetSwitchPortVlanSettingData.OperationMode
- Msvm_EthernetSwitchPortVlanSettingData.AccessVlanId
- Msvm_EthernetSwitchPortVlanSettingData.NativeVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PvlanMode
- Msvm_EthernetSwitchPortVlanSettingData.PrimaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PruneVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.TrunkVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanIdArray
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6fce6416696a99e5d928b774e2ba2a05b1dc21d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364266"
---
# <a name="msvm_ethernetswitchportvlansettingdata-class"></a><span data-ttu-id="052b1-103">MSVM \_ ethernetzwitchportvlansettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="052b1-103">Msvm\_EthernetSwitchPortVlanSettingData class</span></span>

<span data-ttu-id="052b1-104">Stellt die Einstellungsdaten für das virtuelle LAN (VLAN) dar.</span><span class="sxs-lookup"><span data-stu-id="052b1-104">Represents the virtual LAN (VLAN) setting data.</span></span>

<span data-ttu-id="052b1-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="052b1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="052b1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="052b1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("952C5004-4465-451C-8CB8-FA9AB382B773"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VLAN Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortVlanSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port VLAN Settings";
  string Description = "Represents the vlan setting data.";
  string ElementName = "Ethernet Switch Port VLAN Settings";
  uint32 OperationMode = 0;
  uint16 AccessVlanId = 0;
  uint16 NativeVlanId = 0;
  uint32 PvlanMode = 0;
  uint16 PrimaryVlanId = 0;
  uint16 SecondaryVlanId = 0;
  uint16 PruneVlanIdArray[] = {};
  uint16 TrunkVlanIdArray[] = {};
  uint16 SecondaryVlanIdArray[] = {};
};
```

## <a name="members"></a><span data-ttu-id="052b1-107">Member</span><span class="sxs-lookup"><span data-stu-id="052b1-107">Members</span></span>

<span data-ttu-id="052b1-108">Die **MSVM \_ ethernetzwitchportvlansettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="052b1-108">The **Msvm\_EthernetSwitchPortVlanSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="052b1-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="052b1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="052b1-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="052b1-110">Properties</span></span>

<span data-ttu-id="052b1-111">Die **MSVM \_ ethernetzwitchportvlansettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="052b1-111">The **Msvm\_EthernetSwitchPortVlanSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="052b1-112">**Accessvlanid**</span><span class="sxs-lookup"><span data-stu-id="052b1-112">**AccessVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="052b1-113">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="052b1-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="052b1-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="052b1-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="052b1-115">Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="052b1-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="052b1-116">Gibt die VLAN-Kennung im Zugriffsmodus an.</span><span class="sxs-lookup"><span data-stu-id="052b1-116">Specifies the VLAN identifier in access mode.</span></span>

</dd> <dt>

<span data-ttu-id="052b1-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="052b1-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="052b1-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="052b1-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="052b1-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="052b1-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="052b1-120">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="052b1-120">A short description of the object.</span></span> <span data-ttu-id="052b1-121">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port VLAN Settings" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="052b1-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port VLAN Settings".</span></span>

</dd> <dt>

<span data-ttu-id="052b1-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="052b1-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="052b1-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="052b1-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="052b1-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="052b1-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="052b1-125">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="052b1-125">A description of the object.</span></span> <span data-ttu-id="052b1-126">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "stellt die VLAN-Einstellungsdaten" fest.</span><span class="sxs-lookup"><span data-stu-id="052b1-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the vlan setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="052b1-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="052b1-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="052b1-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="052b1-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="052b1-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="052b1-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="052b1-130">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="052b1-130">A display name for the object.</span></span> <span data-ttu-id="052b1-131">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port VLAN Settings" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="052b1-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port VLAN Settings".</span></span>

</dd> <dt>

<span data-ttu-id="052b1-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="052b1-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="052b1-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="052b1-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="052b1-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="052b1-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="052b1-135">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="052b1-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="052b1-136">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="052b1-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="052b1-137">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="052b1-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="052b1-138">**Nativevlanid**</span><span class="sxs-lookup"><span data-stu-id="052b1-138">**NativeVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="052b1-139">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="052b1-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="052b1-140">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="052b1-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="052b1-141">Qualifizierer: **wmidataid** (3), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="052b1-141">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="052b1-142">Gibt die VLAN-Kennung im trunk Modus an.</span><span class="sxs-lookup"><span data-stu-id="052b1-142">Specifies the VLAN identifier in trunk mode.</span></span>

</dd> <dt>

<span data-ttu-id="052b1-143">**OperationMode**</span><span class="sxs-lookup"><span data-stu-id="052b1-143">**OperationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="052b1-144">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="052b1-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="052b1-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="052b1-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="052b1-146">Qualifizierer: **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="052b1-146">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="052b1-147">Gibt den VLAN-Betriebsmodus an.</span><span class="sxs-lookup"><span data-stu-id="052b1-147">Specifies the VLAN operation mode.</span></span>

<dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="052b1-148">**Zugriff** (1)</span><span class="sxs-lookup"><span data-stu-id="052b1-148">**Access** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="052b1-149">**Trunk** (2)</span><span class="sxs-lookup"><span data-stu-id="052b1-149">**Trunk** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Private"></span><span id="private"></span><span id="PRIVATE"></span>

<span data-ttu-id="052b1-150">**Privat** (3)</span><span class="sxs-lookup"><span data-stu-id="052b1-150">**Private** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="052b1-151">**PrimaryVlanId**</span><span class="sxs-lookup"><span data-stu-id="052b1-151">**PrimaryVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="052b1-152">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="052b1-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="052b1-153">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="052b1-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="052b1-154">Qualifizierer: **wmidataid** (5), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="052b1-154">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="052b1-155">Gibt den primären VLAN-Bezeichner im privaten Modus an.</span><span class="sxs-lookup"><span data-stu-id="052b1-155">Specifies the primary VLAN identifier in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="052b1-156">**Prunevlanidarray**</span><span class="sxs-lookup"><span data-stu-id="052b1-156">**PruneVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="052b1-157">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="052b1-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="052b1-158">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="052b1-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="052b1-159">Qualifizierer: **wmidataid** (7), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="052b1-159">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="052b1-160">Gibt die Bitmap des VLAN-Bezeichners im trunk Modus an.</span><span class="sxs-lookup"><span data-stu-id="052b1-160">Specifies the prune VLAN identifier bitmap in trunk mode.</span></span>

</dd> <dt>

<span data-ttu-id="052b1-161">**Pvlanmode**</span><span class="sxs-lookup"><span data-stu-id="052b1-161">**PvlanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="052b1-162">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="052b1-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="052b1-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="052b1-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="052b1-164">Qualifizierer: **wmidataid** (4), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="052b1-164">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="052b1-165">Gibt den privaten VLAN-Modus an.</span><span class="sxs-lookup"><span data-stu-id="052b1-165">Specifies the private VLAN mode.</span></span>

<dt>

<span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>

<span data-ttu-id="052b1-166">**Isoliert** (1)</span><span class="sxs-lookup"><span data-stu-id="052b1-166">**Isolated** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Community"></span><span id="community"></span><span id="COMMUNITY"></span>

<span data-ttu-id="052b1-167">**Community** (2)</span><span class="sxs-lookup"><span data-stu-id="052b1-167">**Community** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Promiscuous"></span><span id="promiscuous"></span><span id="PROMISCUOUS"></span>

<span data-ttu-id="052b1-168">**Promiscuous** (3)</span><span class="sxs-lookup"><span data-stu-id="052b1-168">**Promiscuous** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="052b1-169">**SecondaryVlanId**</span><span class="sxs-lookup"><span data-stu-id="052b1-169">**SecondaryVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="052b1-170">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="052b1-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="052b1-171">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="052b1-171">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="052b1-172">Qualifizierer: **wmidataid** (6), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="052b1-172">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="052b1-173">Gibt den sekundären VLAN-Bezeichner im privaten Modus an.</span><span class="sxs-lookup"><span data-stu-id="052b1-173">Specifies the secondary VLAN identifier in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="052b1-174">**Secondaryvlanidarray**</span><span class="sxs-lookup"><span data-stu-id="052b1-174">**SecondaryVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="052b1-175">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="052b1-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="052b1-176">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="052b1-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="052b1-177">Qualifizierer: **wmidataid** (9), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="052b1-177">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="052b1-178">Gibt die sekundäre VLAN-bezeichnerbitmap im privaten Modus an.</span><span class="sxs-lookup"><span data-stu-id="052b1-178">Specifies the secondary VLAN identifier bitmap in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="052b1-179">**Trunkvlanidarray**</span><span class="sxs-lookup"><span data-stu-id="052b1-179">**TrunkVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="052b1-180">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="052b1-180">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="052b1-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="052b1-181">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="052b1-182">Qualifizierer: **wmidataid** (8), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="052b1-182">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="052b1-183">Gibt die Bitmap des trunk-VLAN-Bezeichners im trunk Modus an.</span><span class="sxs-lookup"><span data-stu-id="052b1-183">Specifies the trunk VLAN identifier bitmap in trunk mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="052b1-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="052b1-184">Requirements</span></span>



| <span data-ttu-id="052b1-185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="052b1-185">Requirement</span></span> | <span data-ttu-id="052b1-186">Wert</span><span class="sxs-lookup"><span data-stu-id="052b1-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="052b1-187">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="052b1-187">Minimum supported client</span></span><br/> | <span data-ttu-id="052b1-188">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="052b1-188">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="052b1-189">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="052b1-189">Minimum supported server</span></span><br/> | <span data-ttu-id="052b1-190">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="052b1-190">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="052b1-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="052b1-191">Namespace</span></span><br/>                | <span data-ttu-id="052b1-192">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="052b1-192">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="052b1-193">MOF</span><span class="sxs-lookup"><span data-stu-id="052b1-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="052b1-194"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="052b1-194"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="052b1-195">DLL</span><span class="sxs-lookup"><span data-stu-id="052b1-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="052b1-196"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="052b1-196"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

