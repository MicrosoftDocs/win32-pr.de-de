---
description: Stellt einen Autorisierungs Eintrag für einen Wiederherstellungs Server dar.
ms.assetid: 8c057b39-7102-4fbf-b4be-f18627a88834
title: Msvm_ReplicationAuthorizationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationAuthorizationSettingData
- Msvm_ReplicationAuthorizationSettingData.InstanceID
- Msvm_ReplicationAuthorizationSettingData.Caption
- Msvm_ReplicationAuthorizationSettingData.Description
- Msvm_ReplicationAuthorizationSettingData.ElementName
- Msvm_ReplicationAuthorizationSettingData.AllowedPrimaryHostSystem
- Msvm_ReplicationAuthorizationSettingData.TrustGroup
- Msvm_ReplicationAuthorizationSettingData.ReplicaStorageLocation
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ba069de1bbe005e8a2a06891db8218ab313baa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216241"
---
# <a name="msvm_replicationauthorizationsettingdata-class"></a><span data-ttu-id="e2e56-103">MSVM \_ replicationauthorizationsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="e2e56-103">Msvm\_ReplicationAuthorizationSettingData class</span></span>

<span data-ttu-id="e2e56-104">Stellt einen Autorisierungs Eintrag für einen Wiederherstellungs Server dar.</span><span class="sxs-lookup"><span data-stu-id="e2e56-104">Represents an authorization entry for a recovery server.</span></span>

<span data-ttu-id="e2e56-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e2e56-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e56-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2e56-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationAuthorizationSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string AllowedPrimaryHostSystem;
  string TrustGroup;
  string ReplicaStorageLocation;
};
```

## <a name="members"></a><span data-ttu-id="e2e56-107">Member</span><span class="sxs-lookup"><span data-stu-id="e2e56-107">Members</span></span>

<span data-ttu-id="e2e56-108">Die **MSVM \_ replicationauthorizationsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e2e56-108">The **Msvm\_ReplicationAuthorizationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e2e56-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2e56-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2e56-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2e56-110">Properties</span></span>

<span data-ttu-id="e2e56-111">Die **MSVM \_ replicationauthorizationsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e2e56-111">The **Msvm\_ReplicationAuthorizationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2e56-112">**"Bereitstellungs-Hostsystem"**</span><span class="sxs-lookup"><span data-stu-id="e2e56-112">**AllowedPrimaryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2e56-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2e56-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2e56-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e2e56-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e2e56-115">Der voll qualifizierte Domänen Name oder Gruppenname der primären Server, die auf diesem Wiederherstellungs Server repliziert werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="e2e56-115">The fully qualified domain name or group name of the primary servers that are allowed to replicate to this recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="e2e56-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e2e56-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2e56-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2e56-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2e56-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2e56-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2e56-119">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e2e56-119">A short description of the object.</span></span> <span data-ttu-id="e2e56-120">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2e56-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2e56-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2e56-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2e56-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2e56-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2e56-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2e56-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2e56-124">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="e2e56-124">A description of the object.</span></span> <span data-ttu-id="e2e56-125">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2e56-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2e56-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e2e56-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2e56-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2e56-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2e56-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2e56-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2e56-129">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e2e56-129">A display name for the object.</span></span> <span data-ttu-id="e2e56-130">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2e56-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2e56-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e2e56-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2e56-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2e56-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2e56-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2e56-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2e56-134">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="e2e56-134">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e2e56-135">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="e2e56-135">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e2e56-136">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e2e56-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e2e56-137">**Replicastorageloation**</span><span class="sxs-lookup"><span data-stu-id="e2e56-137">**ReplicaStorageLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2e56-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2e56-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2e56-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e2e56-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e2e56-140">Der Speicherort, an dem die Replikations Dateien aus dem " **Zustellungs System" zugeordnet** werden.</span><span class="sxs-lookup"><span data-stu-id="e2e56-140">The location where replication files from the **AllowedPrimaryHostSystem** will be stored.</span></span>

</dd> <dt>

<span data-ttu-id="e2e56-141">**Trust Group**</span><span class="sxs-lookup"><span data-stu-id="e2e56-141">**TrustGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2e56-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2e56-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2e56-143">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e2e56-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e2e56-144">Der Name der Vertrauens Gruppe für den Autorisierungs Eintrag.</span><span class="sxs-lookup"><span data-stu-id="e2e56-144">The name of the trust group for the authorization entry.</span></span> <span data-ttu-id="e2e56-145">Dadurch werden die mehrfach gruppierten Autorisierungs Einträge identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e2e56-145">This identifies the multiple authorization entries that are grouped together.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2e56-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2e56-146">Requirements</span></span>



| <span data-ttu-id="e2e56-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2e56-147">Requirement</span></span> | <span data-ttu-id="e2e56-148">Wert</span><span class="sxs-lookup"><span data-stu-id="e2e56-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e56-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2e56-149">Minimum supported client</span></span><br/> | <span data-ttu-id="e2e56-150">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2e56-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e2e56-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2e56-151">Minimum supported server</span></span><br/> | <span data-ttu-id="e2e56-152">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2e56-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e2e56-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2e56-153">Namespace</span></span><br/>                | <span data-ttu-id="e2e56-154">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e2e56-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e2e56-155">MOF</span><span class="sxs-lookup"><span data-stu-id="e2e56-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2e56-156"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e2e56-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2e56-157">DLL</span><span class="sxs-lookup"><span data-stu-id="e2e56-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2e56-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e2e56-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e2e56-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2e56-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e56-160">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="e2e56-160">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="e2e56-161">**Addauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="e2e56-161">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="e2e56-162">**Modifyauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="e2e56-162">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="e2e56-163">**Removeauthorizationentry**</span><span class="sxs-lookup"><span data-stu-id="e2e56-163">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> </dl>

 

