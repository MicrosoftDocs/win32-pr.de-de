---
description: Stellt die Bandbreiteneinstellungen für einen virtuellen Switch dar.
ms.assetid: bc6f8cd3-f74a-4f4a-9ffe-a88def3966d9
title: Msvm_VirtualEthernetSwitchBandwidthSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchBandwidthSettingData
- Msvm_VirtualEthernetSwitchBandwidthSettingData.InstanceID
- Msvm_VirtualEthernetSwitchBandwidthSettingData.Caption
- Msvm_VirtualEthernetSwitchBandwidthSettingData.Description
- Msvm_VirtualEthernetSwitchBandwidthSettingData.ElementName
- Msvm_VirtualEthernetSwitchBandwidthSettingData.DefaultFlowReservation
- Msvm_VirtualEthernetSwitchBandwidthSettingData.DefaultFlowWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ec94409366761ee208d3e8a6af59a4d07527d82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348110"
---
# <a name="msvm_virtualethernetswitchbandwidthsettingdata-class"></a><span data-ttu-id="b0f60-103">MSVM \_ virtualethernetzwitchbandwidthsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="b0f60-103">Msvm\_VirtualEthernetSwitchBandwidthSettingData class</span></span>

<span data-ttu-id="b0f60-104">Stellt die Bandbreiteneinstellungen für einen virtuellen Switch dar.</span><span class="sxs-lookup"><span data-stu-id="b0f60-104">Represents the bandwidth settings for a virtual switch.</span></span>

<span data-ttu-id="b0f60-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b0f60-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0f60-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0f60-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("3EB2B8E8-4ABF-4DBF-9071-16DD47481FBE"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Bandwidth Settings"), AMENDMENT]
class Msvm_VirtualEthernetSwitchBandwidthSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  string InstanceID = "Microsoft:Definition\GUID\Default";
  string Caption = "Ethernet Switch Bandwidth Settings";
  string Description = "Represents the switch bandwidth settings.";
  string ElementName = "Ethernet Switch Bandwidth Settings";
  UINT64 DefaultFlowReservation = 0;
  UINT64 DefaultFlowWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="b0f60-107">Member</span><span class="sxs-lookup"><span data-stu-id="b0f60-107">Members</span></span>

<span data-ttu-id="b0f60-108">Die **MSVM \_ virtualethernetzwitchbandwidthsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b0f60-108">The **Msvm\_VirtualEthernetSwitchBandwidthSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b0f60-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b0f60-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b0f60-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b0f60-110">Properties</span></span>

<span data-ttu-id="b0f60-111">Die **MSVM \_ virtualethernetzwitchbandwidthsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b0f60-111">The **Msvm\_VirtualEthernetSwitchBandwidthSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0f60-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b0f60-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0f60-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b0f60-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0f60-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b0f60-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0f60-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b0f60-115">A short description of the object.</span></span> <span data-ttu-id="b0f60-116">Diese Eigenschaft wird von der [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Klasse geerbt und ist immer auf "Ethernet Switch Bandwidth Settings" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b0f60-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Ethernet Switch Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="b0f60-117">**Defaultflowreservierung**</span><span class="sxs-lookup"><span data-stu-id="b0f60-117">**DefaultFlowReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0f60-118">Datentyp: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="b0f60-118">Data type: **UINT64**</span></span>
</dt> <dt>

<span data-ttu-id="b0f60-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b0f60-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b0f60-120">Qualifizierer: **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b0f60-120">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b0f60-121">Gibt die absolute Bandbreiten Reservierung für nicht klassifizierte Flows auf dem zugrunde liegenden Adapter an.</span><span class="sxs-lookup"><span data-stu-id="b0f60-121">Specifies the absolute bandwidth reservation for unclassified flows on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b0f60-122">**Defaultflowweight**</span><span class="sxs-lookup"><span data-stu-id="b0f60-122">**DefaultFlowWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0f60-123">Datentyp: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="b0f60-123">Data type: **UINT64**</span></span>
</dt> <dt>

<span data-ttu-id="b0f60-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b0f60-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b0f60-125">Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b0f60-125">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b0f60-126">Gibt die Bandbreiten Reservierung für nicht klassifizierte Flows auf dem zugrunde liegenden Adapter an.</span><span class="sxs-lookup"><span data-stu-id="b0f60-126">Specifies the bandwidth reservation in weight for unclassified flows on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b0f60-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b0f60-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0f60-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b0f60-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0f60-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b0f60-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0f60-130">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="b0f60-130">A description of the object.</span></span> <span data-ttu-id="b0f60-131">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "stellt die Einstellungen für die switchbandbreite" fest.</span><span class="sxs-lookup"><span data-stu-id="b0f60-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the switch bandwidth settings.".</span></span>

</dd> <dt>

<span data-ttu-id="b0f60-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b0f60-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0f60-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b0f60-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0f60-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b0f60-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0f60-135">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b0f60-135">A display name for the object.</span></span> <span data-ttu-id="b0f60-136">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt und ist immer auf "Ethernet Switch Bandwidth Settings" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b0f60-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Ethernet Switch Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="b0f60-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b0f60-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0f60-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b0f60-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0f60-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b0f60-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0f60-140">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="b0f60-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b0f60-141">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="b0f60-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b0f60-142">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) geerbt und ist immer auf "Microsoft: Definition \\ *GUID* \\ default" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b0f60-142">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:Definition\\*GUID*\\Default".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0f60-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0f60-143">Requirements</span></span>



| <span data-ttu-id="b0f60-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0f60-144">Requirement</span></span> | <span data-ttu-id="b0f60-145">Wert</span><span class="sxs-lookup"><span data-stu-id="b0f60-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f60-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0f60-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b0f60-147">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0f60-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b0f60-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0f60-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b0f60-149">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0f60-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b0f60-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0f60-150">Namespace</span></span><br/>                | <span data-ttu-id="b0f60-151">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b0f60-151">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b0f60-152">MOF</span><span class="sxs-lookup"><span data-stu-id="b0f60-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0f60-153"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b0f60-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0f60-154">DLL</span><span class="sxs-lookup"><span data-stu-id="b0f60-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0f60-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b0f60-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

