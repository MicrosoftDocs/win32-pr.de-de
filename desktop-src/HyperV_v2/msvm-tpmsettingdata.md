---
description: Stellt den konfigurierten Status des TPM-Geräts dar.
ms.assetid: 948ccb47-3626-48f1-b18f-ef1d05978b21
title: Msvm_TPMSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TPMSettingData
- Msvm_TPMSettingData.Shielded
- Msvm_TPMSettingData.DataProtected
- Msvm_TPMSettingData.EnabledState
- Msvm_TPMSettingData.KeyProtector
- Msvm_TPMSettingData.LastKnownGoodKeyProtector
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8a14f50f01212129ed34cc7e45ee28facbdb991f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527668"
---
# <a name="msvm_tpmsettingdata-class"></a><span data-ttu-id="823e2-103">MSVM \_ tpmsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="823e2-103">Msvm\_TPMSettingData class</span></span>

<span data-ttu-id="823e2-104">Stellt den konfigurierten Status des TPM-Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="823e2-104">Represents the configured state of the TPM device.</span></span>

<span data-ttu-id="823e2-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="823e2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="823e2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="823e2-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TPMSettingData : CIM_ResourceAllocationSettingData
{
  boolean Shielded = FALSE;
  boolean DataProtected = FALSE;
  uint16  EnabledState = 3;
  uint8   KeyProtector[];
  uint8   LastKnownGoodKeyProtector[];
};
```

## <a name="members"></a><span data-ttu-id="823e2-107">Member</span><span class="sxs-lookup"><span data-stu-id="823e2-107">Members</span></span>

<span data-ttu-id="823e2-108">Die **MSVM \_ tpmsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="823e2-108">The **Msvm\_TPMSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="823e2-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="823e2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="823e2-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="823e2-110">Properties</span></span>

<span data-ttu-id="823e2-111">Die **MSVM \_ tpmsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="823e2-111">The **Msvm\_TPMSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="823e2-112">**Dataprotected**</span><span class="sxs-lookup"><span data-stu-id="823e2-112">**DataProtected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823e2-113">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="823e2-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="823e2-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="823e2-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="823e2-115">Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="823e2-115">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="823e2-116">" **true** ", um eine Richtlinie zum Schutz der Daten eines virtuellen Computers festzulegen. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="823e2-116">**true** to set a policy to protect a VM's data; otherwise, **false**.</span></span> <span data-ttu-id="823e2-117">Ein neu erstelltes TPM ist deaktiviert, sodass der anfängliche Datenschutz Status " **false**" lautet.</span><span class="sxs-lookup"><span data-stu-id="823e2-117">A newly created TPM is disabled, so the initial data protection state is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="823e2-118">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="823e2-118">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823e2-119">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="823e2-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="823e2-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="823e2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="823e2-121">Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="823e2-121">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="823e2-122">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="823e2-122">The enabled and disabled states of an element.</span></span> <span data-ttu-id="823e2-123">Der Standardwert ist **deaktiviert**.</span><span class="sxs-lookup"><span data-stu-id="823e2-123">The default value is **Disabled**.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="823e2-124">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="823e2-124">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="823e2-125">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="823e2-125">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="823e2-126">**Keyprotector**</span><span class="sxs-lookup"><span data-stu-id="823e2-126">**KeyProtector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823e2-127">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="823e2-127">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="823e2-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="823e2-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="823e2-129">Qualifizierer: [**erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers), **octetstring**</span><span class="sxs-lookup"><span data-stu-id="823e2-129">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span></span>
</dt> </dl>

<span data-ttu-id="823e2-130">Die Schlüssel Schutzvorrichtung von Host-Überwachungsdienst Client.</span><span class="sxs-lookup"><span data-stu-id="823e2-130">The key protector from Host Guardian Service client.</span></span>

</dd> <dt>

<span data-ttu-id="823e2-131">**Lastknowngoodkeyprotector**</span><span class="sxs-lookup"><span data-stu-id="823e2-131">**LastKnownGoodKeyProtector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823e2-132">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="823e2-132">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="823e2-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="823e2-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="823e2-134">Qualifizierer: [**erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers), **octetstring**</span><span class="sxs-lookup"><span data-stu-id="823e2-134">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span></span>
</dt> </dl>

<span data-ttu-id="823e2-135">Die letzte bekannte gute Schlüssel Schutzvorrichtung hat beim letzten VM-Start erfolgreich den TPM-Gerätestatus verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="823e2-135">The last known good key protector successfully encrypted TPM device state in the last VM boot.</span></span>

<span data-ttu-id="823e2-136">Diese Eigenschaft ist für den WMI-Client schreibgeschützt und kann nur vom TPM-Gerät der VM geändert werden.</span><span class="sxs-lookup"><span data-stu-id="823e2-136">This property is read-only for the WMI client, and can only be modified by the VM TPM device.</span></span>

</dd> <dt>

<span data-ttu-id="823e2-137">**Geschützt**</span><span class="sxs-lookup"><span data-stu-id="823e2-137">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823e2-138">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="823e2-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="823e2-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="823e2-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="823e2-140">Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="823e2-140">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="823e2-141">**true** , um eine Richtlinie zu definieren, die eine virtuelle Maschine schützt. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="823e2-141">**true** to define a policy that shields a virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="823e2-142">Ein neu erstelltes TPM ist deaktiviert, sodass der anfängliche Schutzstatus " **false**" lautet.</span><span class="sxs-lookup"><span data-stu-id="823e2-142">A newly created TPM is disabled, so the initial shielding state is **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="823e2-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="823e2-143">Requirements</span></span>



| <span data-ttu-id="823e2-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="823e2-144">Requirement</span></span> | <span data-ttu-id="823e2-145">Wert</span><span class="sxs-lookup"><span data-stu-id="823e2-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="823e2-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="823e2-146">Minimum supported client</span></span><br/> | <span data-ttu-id="823e2-147">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="823e2-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="823e2-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="823e2-148">Minimum supported server</span></span><br/> | <span data-ttu-id="823e2-149">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="823e2-149">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="823e2-150">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="823e2-150">End of client support</span></span><br/>    | <span data-ttu-id="823e2-151">Windows 10</span><span class="sxs-lookup"><span data-stu-id="823e2-151">Windows 10</span></span><br/>                                                                                   |
| <span data-ttu-id="823e2-152">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="823e2-152">End of server support</span></span><br/>    | <span data-ttu-id="823e2-153">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="823e2-153">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="823e2-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="823e2-154">Namespace</span></span><br/>                | <span data-ttu-id="823e2-155">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="823e2-155">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="823e2-156">MOF</span><span class="sxs-lookup"><span data-stu-id="823e2-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="823e2-157"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="823e2-157"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="823e2-158">DLL</span><span class="sxs-lookup"><span data-stu-id="823e2-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="823e2-159"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="823e2-159"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="823e2-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="823e2-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="823e2-161">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="823e2-161">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

