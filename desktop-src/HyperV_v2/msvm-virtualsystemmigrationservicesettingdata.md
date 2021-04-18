---
description: Stellt die Einstellungen für den Dienst für die virtuelle System Migration auf einem Host dar.
ms.assetid: 56711134-9a4a-49bd-8a0e-ce679b959adf
title: Msvm_VirtualSystemMigrationServiceSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingData
- Msvm_VirtualSystemMigrationServiceSettingData.InstanceID
- Msvm_VirtualSystemMigrationServiceSettingData.Caption
- Msvm_VirtualSystemMigrationServiceSettingData.Description
- Msvm_VirtualSystemMigrationServiceSettingData.ElementName
- Msvm_VirtualSystemMigrationServiceSettingData.EnableVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveStorageMigration
- Msvm_VirtualSystemMigrationServiceSettingData.AuthenticationType
- Msvm_VirtualSystemMigrationServiceSettingData.EnableCompression
- Msvm_VirtualSystemMigrationServiceSettingData.EnableSmbTransport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8c8685e468d60983408c52a985169c61be91f632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339751"
---
# <a name="msvm_virtualsystemmigrationservicesettingdata-class"></a><span data-ttu-id="fd488-103">MSVM \_ virtualsystemmigrationservicesettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="fd488-103">Msvm\_VirtualSystemMigrationServiceSettingData class</span></span>

<span data-ttu-id="fd488-104">Stellt die Einstellungen für den Dienst für die virtuelle System Migration auf einem Host dar.</span><span class="sxs-lookup"><span data-stu-id="fd488-104">Represents the settings for the virtual system migration service on a host.</span></span> <span data-ttu-id="fd488-105">Die Eigenschaften für diese Klasse können nicht direkt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="fd488-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="fd488-106">Der Client muss die **MSVM \_ virtualsystemmigrationservice. modifyservicesettings** -Methode abrufen, um diese Eigenschaften zu ändern.</span><span class="sxs-lookup"><span data-stu-id="fd488-106">The client must call the **Msvm\_VirtualSystemMigrationService.ModifyServiceSettings** method to modify any of these properties.</span></span>

<span data-ttu-id="fd488-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fd488-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd488-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd488-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  boolean EnableVirtualSystemMigration;
  uint32  MaximumActiveVirtualSystemMigration;
  uint32  MaximumActiveStorageMigration;
  uint32  AuthenticationType;
  boolean EnableCompression = True;
  boolean EnableSmbTransport = False;
};
```

## <a name="members"></a><span data-ttu-id="fd488-109">Member</span><span class="sxs-lookup"><span data-stu-id="fd488-109">Members</span></span>

<span data-ttu-id="fd488-110">Die **MSVM \_ virtualsystemmigrationservicesettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fd488-110">The **Msvm\_VirtualSystemMigrationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fd488-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fd488-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd488-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fd488-112">Properties</span></span>

<span data-ttu-id="fd488-113">Die **MSVM \_ virtualsystemmigrationservicesettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fd488-113">The **Msvm\_VirtualSystemMigrationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd488-114">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="fd488-114">**AuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd488-115">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd488-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd488-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd488-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd488-117">Gibt den Authentifizierungsmechanismus an, der für die Netzwerkverbindungen der virtuellen System Migration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd488-117">Specifies the authentication mechanism used for virtual system migration network connections.</span></span> <span data-ttu-id="fd488-118">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) -Methode der [**MSVM \_ virtualsystemmigrationservice**](msvm-virtualsystemmigrationservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fd488-118">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

<dt>

<span id="CredSSP"></span><span id="credssp"></span><span id="CREDSSP"></span>

<span data-ttu-id="fd488-119">" **Kredssp** " (0)</span><span class="sxs-lookup"><span data-stu-id="fd488-119">**CredSSP** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Kerberos"></span><span id="kerberos"></span><span id="KERBEROS"></span>

<span data-ttu-id="fd488-120">**Kerberos** (1)</span><span class="sxs-lookup"><span data-stu-id="fd488-120">**Kerberos** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd488-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fd488-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd488-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd488-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd488-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd488-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd488-124">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="fd488-124">A short description of the object.</span></span> <span data-ttu-id="fd488-125">Diese Eigenschaft wird von der [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="fd488-125">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="fd488-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd488-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd488-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd488-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd488-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd488-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd488-129">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="fd488-129">A description of the object.</span></span> <span data-ttu-id="fd488-130">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fd488-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fd488-131">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fd488-131">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd488-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd488-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd488-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd488-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd488-134">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fd488-134">A display name for the object.</span></span> <span data-ttu-id="fd488-135">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="fd488-135">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fd488-136">**EnableCompression**</span><span class="sxs-lookup"><span data-stu-id="fd488-136">**EnableCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd488-137">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd488-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd488-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fd488-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fd488-139">Gibt an, ob die Komprimierung des Live Migrations Datenverkehrs aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fd488-139">Indicates whether compression of live migration traffic is enabled or disabled.</span></span> <span data-ttu-id="fd488-140">True gibt den Wert aktiviert an.</span><span class="sxs-lookup"><span data-stu-id="fd488-140">True indicates enabled.</span></span>

<span data-ttu-id="fd488-141">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fd488-141">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="fd488-142">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fd488-142">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="fd488-143">**Enablesmbtransport**</span><span class="sxs-lookup"><span data-stu-id="fd488-143">**EnableSmbTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd488-144">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd488-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd488-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fd488-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fd488-146">Gibt an, ob die Verwendung von SMB als Transporttyp für die Übertragung des VM-Zustands zwischen den Hyper-V-Hosts bei der Migration virtueller Systeme aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fd488-146">Indicates whether use of SMB as a transport type for transferring VM state between the Hyper-V hosts during virtual system migration is enabled or disabled.</span></span> <span data-ttu-id="fd488-147">**True** gibt den Wert aktiviert an.</span><span class="sxs-lookup"><span data-stu-id="fd488-147">**True** indicates enabled.</span></span> <span data-ttu-id="fd488-148">Eine höhere Leistung wird erzielt, wenn RDMA-NICs während der VM-Live Migration für den SMB-Transport konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="fd488-148">A higher performance is achieved if RDMA NICs are configured for SMB transport during VM live migration.</span></span> <span data-ttu-id="fd488-149">Wenn der **enablesmbtransport** -Wert true ist, wird der Wert von **EnableCompression** ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fd488-149">If **EnableSmbTransport** value is true, the value of **EnableCompression** is ignored.</span></span>

<span data-ttu-id="fd488-150">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fd488-150">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="fd488-151">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fd488-151">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="fd488-152">**Enablevirtualsystemmigration**</span><span class="sxs-lookup"><span data-stu-id="fd488-152">**EnableVirtualSystemMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd488-153">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd488-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd488-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd488-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd488-155">Gibt an, ob die Migration virtueller Systeme aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fd488-155">Specifies whether virtual system migration is enabled or disabled.</span></span> <span data-ttu-id="fd488-156">Die Speicher Migration ist immer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="fd488-156">Storage migration is always enabled.</span></span> <span data-ttu-id="fd488-157">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) -Methode der [**MSVM \_ virtualsystemmigrationservice**](msvm-virtualsystemmigrationservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fd488-157">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="fd488-158">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fd488-158">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd488-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd488-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd488-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd488-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd488-161">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="fd488-161">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fd488-162">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="fd488-162">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fd488-163">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fd488-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fd488-164">**Maximumactivestoragemigration**</span><span class="sxs-lookup"><span data-stu-id="fd488-164">**MaximumActiveStorageMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd488-165">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd488-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd488-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd488-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd488-167">Gibt die maximal zulässige Anzahl aktiver Speicher Migrationen an.</span><span class="sxs-lookup"><span data-stu-id="fd488-167">Specifies the maximum number of active storage migrations allowed.</span></span> <span data-ttu-id="fd488-168">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) -Methode der [**MSVM \_ virtualsystemmigrationservice**](msvm-virtualsystemmigrationservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fd488-168">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="fd488-169">**Maximumactivevirtualsystemmigration**</span><span class="sxs-lookup"><span data-stu-id="fd488-169">**MaximumActiveVirtualSystemMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd488-170">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd488-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd488-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd488-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd488-172">Gibt die maximal zulässige Anzahl aktiver virtueller System Migrationen an.</span><span class="sxs-lookup"><span data-stu-id="fd488-172">Specifies the maximum number of active virtual system migrations allowed.</span></span> <span data-ttu-id="fd488-173">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) -Methode der [**MSVM \_ virtualsystemmigrationservice**](msvm-virtualsystemmigrationservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fd488-173">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd488-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd488-174">Requirements</span></span>



| <span data-ttu-id="fd488-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd488-175">Requirement</span></span> | <span data-ttu-id="fd488-176">Wert</span><span class="sxs-lookup"><span data-stu-id="fd488-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd488-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd488-177">Minimum supported client</span></span><br/> | <span data-ttu-id="fd488-178">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd488-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fd488-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd488-179">Minimum supported server</span></span><br/> | <span data-ttu-id="fd488-180">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd488-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd488-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="fd488-181">Namespace</span></span><br/>                | <span data-ttu-id="fd488-182">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="fd488-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fd488-183">MOF</span><span class="sxs-lookup"><span data-stu-id="fd488-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd488-184"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fd488-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd488-185">DLL</span><span class="sxs-lookup"><span data-stu-id="fd488-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd488-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fd488-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fd488-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd488-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd488-188">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="fd488-188">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="fd488-189">**Modifyservicesettings**</span><span class="sxs-lookup"><span data-stu-id="fd488-189">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

