---
description: Stellt die Einstellungen für die Port Bandbreite dar.
ms.assetid: 62a42c4c-8ea1-47c6-8ae6-e9252f2ed0e4
title: Msvm_EthernetSwitchPortBandwidthSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthSettingData
- Msvm_EthernetSwitchPortBandwidthSettingData.InstanceID
- Msvm_EthernetSwitchPortBandwidthSettingData.Caption
- Msvm_EthernetSwitchPortBandwidthSettingData.Description
- Msvm_EthernetSwitchPortBandwidthSettingData.ElementName
- Msvm_EthernetSwitchPortBandwidthSettingData.Reservation
- Msvm_EthernetSwitchPortBandwidthSettingData.Weight
- Msvm_EthernetSwitchPortBandwidthSettingData.Limit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstLimit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 932207a8157e34c5f42894c31efa78090a6a80f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362896"
---
# <a name="msvm_ethernetswitchportbandwidthsettingdata-class"></a><span data-ttu-id="5ade8-103">MSVM \_ ethernetzwitchportbandwidthsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="5ade8-103">Msvm\_EthernetSwitchPortBandwidthSettingData class</span></span>

<span data-ttu-id="5ade8-104">Stellt die Einstellungen für die Port Bandbreite dar.</span><span class="sxs-lookup"><span data-stu-id="5ade8-104">Represents the port bandwidth settings.</span></span>

<span data-ttu-id="5ade8-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5ade8-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ade8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ade8-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Settings";
  string Description = "Represents the port bandwidth settings.";
  string ElementName = "Ethernet Switch Port Bandwidth Settings";
  uint64 Reservation = 0;
  uint64 Weight = 0;
  uint64 Limit = 0;
  uint64 BurstLimit = 0;
  uint64 BurstSize = 0;
};
```

## <a name="members"></a><span data-ttu-id="5ade8-107">Member</span><span class="sxs-lookup"><span data-stu-id="5ade8-107">Members</span></span>

<span data-ttu-id="5ade8-108">Die **MSVM \_ ethernetzwitchportbandwidthsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5ade8-108">The **Msvm\_EthernetSwitchPortBandwidthSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5ade8-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5ade8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ade8-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5ade8-110">Properties</span></span>

<span data-ttu-id="5ade8-111">Die **MSVM \_ ethernetzwitchportbandwidthsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5ade8-111">The **Msvm\_EthernetSwitchPortBandwidthSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ade8-112">**Burstlimit**</span><span class="sxs-lookup"><span data-stu-id="5ade8-112">**BurstLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ade8-113">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5ade8-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5ade8-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5ade8-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ade8-115">Qualifizierer: **wmidataid** (4), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5ade8-115">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ade8-116">Die vom Port zulässige Spitzen Bandbreite während des auftretende.</span><span class="sxs-lookup"><span data-stu-id="5ade8-116">The peak bandwidth allowed from the port during bursts.</span></span>

</dd> <dt>

<span data-ttu-id="5ade8-117">**Burstsize**</span><span class="sxs-lookup"><span data-stu-id="5ade8-117">**BurstSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ade8-118">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5ade8-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5ade8-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5ade8-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ade8-120">Qualifizierer: **wmidataid** (5), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5ade8-120">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ade8-121">Die maximal zulässige Burst Größe.</span><span class="sxs-lookup"><span data-stu-id="5ade8-121">The maximum burst size allowed.</span></span>

</dd> <dt>

<span data-ttu-id="5ade8-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5ade8-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ade8-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5ade8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ade8-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5ade8-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ade8-125">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5ade8-125">A short description of the object.</span></span> <span data-ttu-id="5ade8-126">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port Bandwidth Settings" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5ade8-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="5ade8-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5ade8-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ade8-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5ade8-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ade8-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5ade8-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ade8-130">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="5ade8-130">A description of the object.</span></span> <span data-ttu-id="5ade8-131">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "stellt die Einstellungen für die Port Bandbreite" fest.</span><span class="sxs-lookup"><span data-stu-id="5ade8-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port bandwidth settings.".</span></span>

</dd> <dt>

<span data-ttu-id="5ade8-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5ade8-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ade8-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5ade8-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ade8-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5ade8-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ade8-135">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5ade8-135">A display name for the object.</span></span> <span data-ttu-id="5ade8-136">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port Bandwidth Settings" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5ade8-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="5ade8-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5ade8-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ade8-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5ade8-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ade8-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5ade8-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ade8-140">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="5ade8-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5ade8-141">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="5ade8-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5ade8-142">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5ade8-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5ade8-143">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="5ade8-143">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ade8-144">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5ade8-144">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5ade8-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5ade8-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ade8-146">Qualifizierer: **wmidataid** (3), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5ade8-146">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ade8-147">Die für den Port zulässige Bandbreitenbegrenzung.</span><span class="sxs-lookup"><span data-stu-id="5ade8-147">The bandwidth limit allowed for the port.</span></span>

</dd> <dt>

<span data-ttu-id="5ade8-148">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="5ade8-148">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ade8-149">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5ade8-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5ade8-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5ade8-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ade8-151">Qualifizierer: **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5ade8-151">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ade8-152">Die minimale absolute Bandbreite, die für den Port garantiert wird.</span><span class="sxs-lookup"><span data-stu-id="5ade8-152">The minimum absolute bandwidth guaranteed for the port.</span></span>

</dd> <dt>

<span data-ttu-id="5ade8-153">**Weight**</span><span class="sxs-lookup"><span data-stu-id="5ade8-153">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ade8-154">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5ade8-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5ade8-155">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5ade8-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ade8-156">Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5ade8-156">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ade8-157">Die minimale Bandbreite, die für den Port garantiert ist.</span><span class="sxs-lookup"><span data-stu-id="5ade8-157">The minimum bandwidth in weight guaranteed for the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ade8-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ade8-158">Requirements</span></span>



| <span data-ttu-id="5ade8-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ade8-159">Requirement</span></span> | <span data-ttu-id="5ade8-160">Wert</span><span class="sxs-lookup"><span data-stu-id="5ade8-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ade8-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ade8-161">Minimum supported client</span></span><br/> | <span data-ttu-id="5ade8-162">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ade8-162">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5ade8-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ade8-163">Minimum supported server</span></span><br/> | <span data-ttu-id="5ade8-164">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ade8-164">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5ade8-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ade8-165">Namespace</span></span><br/>                | <span data-ttu-id="5ade8-166">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="5ade8-166">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5ade8-167">MOF</span><span class="sxs-lookup"><span data-stu-id="5ade8-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ade8-168"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5ade8-168"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ade8-169">DLL</span><span class="sxs-lookup"><span data-stu-id="5ade8-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ade8-170"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5ade8-170"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

