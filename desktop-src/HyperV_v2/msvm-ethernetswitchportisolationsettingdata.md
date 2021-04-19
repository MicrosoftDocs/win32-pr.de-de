---
description: Stellt die Isolations Einstellungsdaten dar.
ms.assetid: f6bf5fcf-61c4-4e69-8ba0-fff4c4873368
title: Msvm_EthernetSwitchPortIsolationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortIsolationSettingData
- Msvm_EthernetSwitchPortIsolationSettingData.IsolationMode
- Msvm_EthernetSwitchPortIsolationSettingData.AllowUntaggedTraffic
- Msvm_EthernetSwitchPortIsolationSettingData.DefaultIsolationId
- Msvm_EthernetSwitchPortIsolationSettingData.EnableMultiTenantStack
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d7761b090cfd3bf2ae6aaaa92e9c5d09d55eae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368834"
---
# <a name="msvm_ethernetswitchportisolationsettingdata-class"></a><span data-ttu-id="79b46-103">MSVM \_ ethernetzwitchportisolationsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="79b46-103">Msvm\_EthernetSwitchPortIsolationSettingData class</span></span>

<span data-ttu-id="79b46-104">Stellt die Isolations Einstellungsdaten dar.</span><span class="sxs-lookup"><span data-stu-id="79b46-104">Represents the Isolation setting data.</span></span>

<span data-ttu-id="79b46-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="79b46-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="79b46-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="79b46-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("83AF2CCB-72C9-4479-A285-94E58A98CAA6"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Isolation Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortIsolationSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32  IsolationMode = 0;
  boolean AllowUntaggedTraffic = FALSE;
  uint32  DefaultIsolationId = 0;
  Boolean EnableMultiTenantStack = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="79b46-107">Member</span><span class="sxs-lookup"><span data-stu-id="79b46-107">Members</span></span>

<span data-ttu-id="79b46-108">Die **MSVM \_ ethernetzwitchportisolationsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="79b46-108">The **Msvm\_EthernetSwitchPortIsolationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="79b46-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="79b46-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79b46-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="79b46-110">Properties</span></span>

<span data-ttu-id="79b46-111">Die **MSVM \_ ethernetzwitchportisolationsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="79b46-111">The **Msvm\_EthernetSwitchPortIsolationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79b46-112">**"Zugewuntaggedtraffic"**</span><span class="sxs-lookup"><span data-stu-id="79b46-112">**AllowUntaggedTraffic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79b46-113">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="79b46-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79b46-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="79b46-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="79b46-115">Qualifizierer: **wmidataid** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="79b46-115">Qualifiers: **WmiDataId** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="79b46-116">Gibt an, ob der Port nicht markierten Datenverkehr senden/empfangen darf.</span><span class="sxs-lookup"><span data-stu-id="79b46-116">Whether the port is allowed to send/receive untagged traffic.</span></span>

</dd> <dt>

<span data-ttu-id="79b46-117">**Defaultisolationid**</span><span class="sxs-lookup"><span data-stu-id="79b46-117">**DefaultIsolationId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79b46-118">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79b46-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79b46-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="79b46-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="79b46-120">Qualifizierer: **wmidataid** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="79b46-120">Qualifiers: **WmiDataId** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="79b46-121">Die standardvirtualsubnetz-ID oder VLAN, die für den gesamten Sende-/empfangsdatenverkehr festgelegt wird, wenn " **zuordnduntaggedtraffic** " **true**</span><span class="sxs-lookup"><span data-stu-id="79b46-121">The default VirtualSubnetId or VLAN that will be set on all send/receive traffic if **AllowedUntaggedTraffic** is **true**.</span></span>

</dd> <dt>

<span data-ttu-id="79b46-122">**Enablemultitenantstack**</span><span class="sxs-lookup"><span data-stu-id="79b46-122">**EnableMultiTenantStack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79b46-123">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="79b46-123">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79b46-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="79b46-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="79b46-125">Qualifizierer: **wmidataid** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="79b46-125">Qualifiers: **WmiDataId** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="79b46-126">**True** gibt an, dass der Netzwerk Stapel auf der VM auf die Isolations Konfiguration zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="79b46-126">If **true**, the network stack in the VM will be able to access the isolation configuration.</span></span> <span data-ttu-id="79b46-127">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="79b46-127">The default value is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="79b46-128">**IsolationMode**</span><span class="sxs-lookup"><span data-stu-id="79b46-128">**IsolationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79b46-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79b46-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79b46-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="79b46-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="79b46-131">Qualifizierer: **wmidataid** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="79b46-131">Qualifiers: **WmiDataId** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="79b46-132">Gibt an, ob der Port **VLAN** oder **virtualsubnetztid** für die Isolation verwendet.</span><span class="sxs-lookup"><span data-stu-id="79b46-132">Whether the port is using **VLAN** or **VirtualSubnetId** for isolation.</span></span> <span data-ttu-id="79b46-133">**Nativevirtualsubnettid** wird für wNv-virtualsubnetztid-basierte Netzwerke verwendet.</span><span class="sxs-lookup"><span data-stu-id="79b46-133">**NativeVirtualSubnetId** is used for WNV VirtualSubnetId-based networks.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="79b46-134">**Keine** (0)</span><span class="sxs-lookup"><span data-stu-id="79b46-134">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="NativeVirtualSubnetId"></span><span id="nativevirtualsubnetid"></span><span id="NATIVEVIRTUALSUBNETID"></span>

<span data-ttu-id="79b46-135">**Nativevirtualsubnetztid** (1)</span><span class="sxs-lookup"><span data-stu-id="79b46-135">**NativeVirtualSubnetId** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ExternalVirtualSubnetId"></span><span id="externalvirtualsubnetid"></span><span id="EXTERNALVIRTUALSUBNETID"></span>

<span data-ttu-id="79b46-136">**Externalvirtualsubnetztid** (2)</span><span class="sxs-lookup"><span data-stu-id="79b46-136">**ExternalVirtualSubnetId** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VLAN"></span><span id="vlan"></span>

<span data-ttu-id="79b46-137">**VLAN** (3)</span><span class="sxs-lookup"><span data-stu-id="79b46-137">**VLAN** (3)</span></span>


<span data-ttu-id="79b46-138"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="79b46-138"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="79b46-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79b46-139">Requirements</span></span>



| <span data-ttu-id="79b46-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79b46-140">Requirement</span></span> | <span data-ttu-id="79b46-141">Wert</span><span class="sxs-lookup"><span data-stu-id="79b46-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79b46-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79b46-142">Minimum supported client</span></span><br/> | <span data-ttu-id="79b46-143">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="79b46-143">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="79b46-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79b46-144">Minimum supported server</span></span><br/> | <span data-ttu-id="79b46-145">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="79b46-145">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="79b46-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="79b46-146">Namespace</span></span><br/>                | <span data-ttu-id="79b46-147">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="79b46-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="79b46-148">MOF</span><span class="sxs-lookup"><span data-stu-id="79b46-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79b46-149"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="79b46-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="79b46-150">DLL</span><span class="sxs-lookup"><span data-stu-id="79b46-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79b46-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79b46-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="79b46-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79b46-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79b46-153">**MSVM \_ ethernetzwitchportfeaturesettingdata**</span><span class="sxs-lookup"><span data-stu-id="79b46-153">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

