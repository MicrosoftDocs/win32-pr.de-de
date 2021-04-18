---
description: Stellt den konfigurierten Zustand der Sicherheitseinstellungen für dar.
ms.assetid: c57ab966-591e-4dd9-87be-0d2b81611d5d
title: Msvm_SecuritySettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecuritySettingData
- Msvm_SecuritySettingData.TpmEnabled
- Msvm_SecuritySettingData.KsdEnabled
- Msvm_SecuritySettingData.ShieldingRequested
- Msvm_SecuritySettingData.DataProtectionRequested
- Msvm_SecuritySettingData.EncryptStateAndVmMigrationTraffic
- Msvm_SecuritySettingData.VirtualizationBasedSecurityOptOut
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7125e06ad4ce33e70a8cf84b24933e7390e7a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347396"
---
# <a name="msvm_securitysettingdata-class"></a><span data-ttu-id="b2b29-103">MSVM \_ securitysettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="b2b29-103">Msvm\_SecuritySettingData class</span></span>

<span data-ttu-id="b2b29-104">Stellt den konfigurierten Zustand der Sicherheitseinstellungen für einen virtuellen Computer dar.</span><span class="sxs-lookup"><span data-stu-id="b2b29-104">Represents the configured state of the security settings for a virtual machine.</span></span>

<span data-ttu-id="b2b29-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b2b29-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b29-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2b29-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecuritySettingData : CIM_SettingData
{
  boolean TpmEnabled;
  boolean KsdEnabled;
  boolean ShieldingRequested;
  boolean DataProtectionRequested;
  boolean EncryptStateAndVmMigrationTraffic;
  boolean VirtualizationBasedSecurityOptOut;
};
```

## <a name="members"></a><span data-ttu-id="b2b29-107">Member</span><span class="sxs-lookup"><span data-stu-id="b2b29-107">Members</span></span>

<span data-ttu-id="b2b29-108">Die **MSVM \_ securitysettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b2b29-108">The **Msvm\_SecuritySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b2b29-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2b29-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2b29-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2b29-110">Properties</span></span>

<span data-ttu-id="b2b29-111">Die **MSVM \_ securitysettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b2b29-111">The **Msvm\_SecuritySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2b29-112">**Dataschutzanforderung**</span><span class="sxs-lookup"><span data-stu-id="b2b29-112">**DataProtectionRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b29-113">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b2b29-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2b29-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b2b29-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b29-115">Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b2b29-115">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b2b29-116">" **true** ", um den Schutz von Daten für eine VM anzufordern. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="b2b29-116">**true** to request data protection for a VM; otherwise, **false**.</span></span> <span data-ttu-id="b2b29-117">Der Standardwert ist **false.**</span><span class="sxs-lookup"><span data-stu-id="b2b29-117">The default value is **false.**</span></span>

</dd> <dt>

<span data-ttu-id="b2b29-118">**Verschlüsselungsstateandvmmigrationtraffic**</span><span class="sxs-lookup"><span data-stu-id="b2b29-118">**EncryptStateAndVmMigrationTraffic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b29-119">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b2b29-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2b29-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b2b29-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b29-121">Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b2b29-121">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b2b29-122">**true** , wenn der Zustands-und Migrations Datenverkehr einer verschlüsselten VM verschlüsselt werden soll. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="b2b29-122">**true** to have the state and migration traffic of a VM encrypted; otherwise, **false**.</span></span> <span data-ttu-id="b2b29-123">Der Standardwert für eine neu erstellte VM ist **false**.</span><span class="sxs-lookup"><span data-stu-id="b2b29-123">The default value for a newly-created VM is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="b2b29-124">**Ksdenabled**</span><span class="sxs-lookup"><span data-stu-id="b2b29-124">**KsdEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b29-125">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b2b29-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2b29-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b2b29-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b29-127">Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b2b29-127">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b2b29-128">" **true** ", um ein Schlüsselspeicher Gerät (KSD) für diesen virtuellen Computer zu aktivieren. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="b2b29-128">**true** to enable a key storage device (KSD) for this virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="b2b29-129">Eine neu erstellte VM verfügt über eine deaktivierte KSD.</span><span class="sxs-lookup"><span data-stu-id="b2b29-129">A newly-created VM has a disable KSD.</span></span>

</dd> <dt>

<span data-ttu-id="b2b29-130">**Shieldingrequessiert**</span><span class="sxs-lookup"><span data-stu-id="b2b29-130">**ShieldingRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b29-131">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b2b29-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2b29-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b2b29-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b29-133">Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b2b29-133">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b2b29-134">" **true** ", um den Schutz für eine VM anzufordern. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="b2b29-134">**true** to request shielding for a VM; otherwise, **false**.</span></span> <span data-ttu-id="b2b29-135">Ein neu erstellter virtueller Computer verfügt über einen anfänglichen Schutz angeforderten Status **false**.</span><span class="sxs-lookup"><span data-stu-id="b2b29-135">A newly-created VM has an initial shielding requested state of **false**.</span></span>

</dd> <dt>

<span data-ttu-id="b2b29-136">**Tpmenabled**</span><span class="sxs-lookup"><span data-stu-id="b2b29-136">**TpmEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b29-137">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b2b29-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2b29-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b2b29-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b29-139">Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b2b29-139">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b2b29-140">" **true** ", um ein vertrauenswürdiges Plattform-nodule (TPM) für diesen virtuellen Computer zu aktivieren. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="b2b29-140">**true** to enable a trusted platform nodule (TPM) for this virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="b2b29-141">Ein neu erstellter virtueller Computer verfügt über ein TPM deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b2b29-141">A newly-created VM has a disable TPM.</span></span>

</dd> <dt>

<span data-ttu-id="b2b29-142">**Virtualizationbasedsecurityoptout**</span><span class="sxs-lookup"><span data-stu-id="b2b29-142">**VirtualizationBasedSecurityOptOut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b29-143">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b2b29-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2b29-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b2b29-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b29-145">Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b2b29-145">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b2b29-146">" **true** ", wenn keine VM-virtualisierungsbasierte Sicherheit angeboten werden soll. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="b2b29-146">**true** to not offer a VM virtualization-based security; otherwise, **false**.</span></span> <span data-ttu-id="b2b29-147">Die Standardeinstellung für einen neu erstellten VM-Abmelde Status ist **false**.</span><span class="sxs-lookup"><span data-stu-id="b2b29-147">The default setting for a newly-crated VM's opt-out state is **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2b29-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2b29-148">Requirements</span></span>



| <span data-ttu-id="b2b29-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2b29-149">Requirement</span></span> | <span data-ttu-id="b2b29-150">Wert</span><span class="sxs-lookup"><span data-stu-id="b2b29-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b29-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2b29-151">Minimum supported client</span></span><br/> | <span data-ttu-id="b2b29-152">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2b29-152">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b2b29-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2b29-153">Minimum supported server</span></span><br/> | <span data-ttu-id="b2b29-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b2b29-154">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b2b29-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="b2b29-155">Namespace</span></span><br/>                | <span data-ttu-id="b2b29-156">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b2b29-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b2b29-157">MOF</span><span class="sxs-lookup"><span data-stu-id="b2b29-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2b29-158"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b2b29-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2b29-159">DLL</span><span class="sxs-lookup"><span data-stu-id="b2b29-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2b29-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2b29-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b2b29-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2b29-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2b29-162">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="b2b29-162">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

