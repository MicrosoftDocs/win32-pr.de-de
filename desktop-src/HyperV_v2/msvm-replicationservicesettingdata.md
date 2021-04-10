---
description: Stellt die Einstellungen für den Replikations Dienst auf einem Wiederherstellungs Host dar. Die Eigenschaften für diese Klasse können nicht direkt geändert werden. Der Client muss die MSVM \_ replicationservice. modifyservicesettings-Methode aufzurufen, um diese Eigenschaften zu ändern.
ms.assetid: a0c0b45a-3578-412a-910e-cd4b3ff0e262
title: Msvm_ReplicationServiceSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationServiceSettingData
- Msvm_ReplicationServiceSettingData.InstanceID
- Msvm_ReplicationServiceSettingData.Caption
- Msvm_ReplicationServiceSettingData.Description
- Msvm_ReplicationServiceSettingData.ElementName
- Msvm_ReplicationServiceSettingData.RecoveryServerEnabled
- Msvm_ReplicationServiceSettingData.AllowedAuthenticationType
- Msvm_ReplicationServiceSettingData.CertificateThumbPrint
- Msvm_ReplicationServiceSettingData.HttpsPort
- Msvm_ReplicationServiceSettingData.HttpPort
- Msvm_ReplicationServiceSettingData.MonitoringStartTime
- Msvm_ReplicationServiceSettingData.MonitoringInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e2886529ab74fed52ec0c6077bfa3d9222fca55c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866120"
---
# <a name="msvm_replicationservicesettingdata-class"></a><span data-ttu-id="55787-105">MSVM \_ replicationservicesettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="55787-105">Msvm\_ReplicationServiceSettingData class</span></span>

<span data-ttu-id="55787-106">Stellt die Einstellungen für den Replikations Dienst auf einem Wiederherstellungs Host dar.</span><span class="sxs-lookup"><span data-stu-id="55787-106">Represents the settings for the replication service on a recovery host.</span></span> <span data-ttu-id="55787-107">Die Eigenschaften für diese Klasse können nicht direkt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="55787-107">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="55787-108">Der Client muss die [**MSVM \_ replicationservice. modifyservicesettings**](modifyservicesettings-msvm-replicationservice.md) -Methode aufzurufen, um diese Eigenschaften zu ändern.</span><span class="sxs-lookup"><span data-stu-id="55787-108">The client must call the [**Msvm\_ReplicationService.ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="55787-109">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="55787-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="55787-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="55787-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Replication Service Settings";
  string   Description = "Virtual Machine Replication Service Settings Data";
  string   ElementName = "Replication Service Settings";
  boolean  RecoveryServerEnabled = False;
  uint16   AllowedAuthenticationType = 0;
  string   CertificateThumbPrint;
  uint16   HttpsPort = 443;
  uint16   HttpPort = 80;
  datetime MonitoringStartTime;
  uint32   MonitoringInterval = 43200;
};
```

## <a name="members"></a><span data-ttu-id="55787-111">Member</span><span class="sxs-lookup"><span data-stu-id="55787-111">Members</span></span>

<span data-ttu-id="55787-112">Die **MSVM \_ replicationservicesettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="55787-112">The **Msvm\_ReplicationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="55787-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55787-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55787-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55787-114">Properties</span></span>

<span data-ttu-id="55787-115">Die **MSVM \_ replicationservicesettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="55787-115">The **Msvm\_ReplicationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55787-116">**"Zuweisung"**</span><span class="sxs-lookup"><span data-stu-id="55787-116">**AllowedAuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55787-117">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55787-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55787-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55787-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55787-119">Definieren Sie die für die Verbindung mit dem Wiederherstellungs Host Server zulässigen Authentifizierungs Modi.</span><span class="sxs-lookup"><span data-stu-id="55787-119">Define authentication modes allowed for connecting to recovery host server.</span></span>

<dt>

<span data-ttu-id="55787-120">0</span><span class="sxs-lookup"><span data-stu-id="55787-120">0</span></span>
</dt> <dd>

<span data-ttu-id="55787-121">Nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="55787-121">Not defined.</span></span>

</dd> <dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="55787-122"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos-Authentifizierung** (1)</span><span class="sxs-lookup"><span data-stu-id="55787-122"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="55787-123">Kerberos-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="55787-123">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="55787-124"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Zertifikat basierte Authentifizierung** (2)</span><span class="sxs-lookup"><span data-stu-id="55787-124"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="55787-125">Zertifikat basierte Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="55787-125">Certificate based authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="55787-126"><span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>**Zertifikat basierte Authentifizierung und Kerberos-Authentifizierung** (3)</span><span class="sxs-lookup"><span data-stu-id="55787-126"><span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>**Certificate based authentication and kerberos authentication** (3)</span></span>


</dt> <dd>

<span data-ttu-id="55787-127">Die Zertifikat basierte Authentifizierung und die integrierte Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="55787-127">Both certificate based authentication and integrated authentication.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="55787-128">**Caption**</span><span class="sxs-lookup"><span data-stu-id="55787-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55787-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="55787-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55787-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55787-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55787-131">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="55787-131">A short description of the object.</span></span> <span data-ttu-id="55787-132">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Replikations Dienst Einstellungen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="55787-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="55787-133">**CertificateThumbPrint**</span><span class="sxs-lookup"><span data-stu-id="55787-133">**CertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55787-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="55787-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55787-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55787-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55787-136">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="55787-136">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="55787-137">Der Zertifikat Fingerabdruck, der verwendet wird, wenn " **AuthenticationType** " eine Zertifikat basierte Authentifizierung ist.</span><span class="sxs-lookup"><span data-stu-id="55787-137">Certificate thumbprint to use when **AuthenticationType** is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="55787-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55787-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55787-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="55787-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55787-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55787-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55787-141">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="55787-141">A description of the object.</span></span> <span data-ttu-id="55787-142">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Replikations Einstellungsdaten für virtuelle Computer" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="55787-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Machine Replication Settings Data".</span></span>

</dd> <dt>

<span data-ttu-id="55787-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="55787-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55787-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="55787-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55787-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55787-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55787-146">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="55787-146">A display name for the object.</span></span> <span data-ttu-id="55787-147">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Replikations Dienst Einstellungen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="55787-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="55787-148">**HttpPort**</span><span class="sxs-lookup"><span data-stu-id="55787-148">**HttpPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55787-149">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55787-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55787-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55787-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55787-151">Portnummer des Wiederherstellungs Servers, der beim Akzeptieren einer nicht sicheren Verbindung für die Replikation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="55787-151">Recovery server port number to use when accepting a nonsecure connection for replication.</span></span> <span data-ttu-id="55787-152">Der Standardwert ist 80.</span><span class="sxs-lookup"><span data-stu-id="55787-152">The default value is 80.</span></span>

</dd> <dt>

<span data-ttu-id="55787-153">**HttpsPort**</span><span class="sxs-lookup"><span data-stu-id="55787-153">**HttpsPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55787-154">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55787-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55787-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55787-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55787-156">Portnummer des Wiederherstellungs Servers, der beim Akzeptieren einer sicheren Verbindung für die Replikation verwendet wird</span><span class="sxs-lookup"><span data-stu-id="55787-156">Recovery server port number to use when accepting secure connection for replication.</span></span> <span data-ttu-id="55787-157">Der Standardwert ist 443.</span><span class="sxs-lookup"><span data-stu-id="55787-157">The default value is 443.</span></span>

</dd> <dt>

<span data-ttu-id="55787-158">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="55787-158">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55787-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="55787-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55787-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55787-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55787-161">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="55787-161">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="55787-162">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="55787-162">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="55787-163">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="55787-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="55787-164">**Monitoringinterval**</span><span class="sxs-lookup"><span data-stu-id="55787-164">**MonitoringInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55787-165">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55787-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55787-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55787-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55787-167">Das Intervall in Sekunden, in dem die Replikations Statistiken zurückgesetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="55787-167">The interval, in seconds, at which replication statistics should be reset.</span></span> <span data-ttu-id="55787-168">Das Standardintervall beträgt 12 Stunden (43200 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="55787-168">The default interval is 12 hours (43200 seconds).</span></span> <span data-ttu-id="55787-169">Der minimale gültige Wert ist 60 Minuten (3600 Sekunden), und der höchst gültige Wert beträgt 7 Tage (604800 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="55787-169">The minimum valid value is 60 minutes (3600 seconds), and the maximum valid value is 7 days (604800 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="55787-170">**Monitoringstarttime**</span><span class="sxs-lookup"><span data-stu-id="55787-170">**MonitoringStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55787-171">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="55787-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="55787-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55787-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55787-173">Die Startzeit für die Replikations Überwachung in UTC.</span><span class="sxs-lookup"><span data-stu-id="55787-173">The start time for replication monitoring, in UTC.</span></span> <span data-ttu-id="55787-174">Der Standardwert ist 9:00 Uhr, Ortszeit, dargestellt in UTC.</span><span class="sxs-lookup"><span data-stu-id="55787-174">The default value is 9:00 A.M., local time, represented in UTC.</span></span> <span data-ttu-id="55787-175">Die Date-Elemente des **DateTime** -Objekts müssen 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="55787-175">The date elements of the **datetime** object must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="55787-176">**Wiederherstellserveraktivierung**</span><span class="sxs-lookup"><span data-stu-id="55787-176">**RecoveryServerEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55787-177">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="55787-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55787-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="55787-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55787-179">Gibt an, ob der Hyper-V-Host als Wiederherstellungs Server aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="55787-179">Specifies whether the Hyper-V host is enabled as a recovery server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="55787-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55787-180">Requirements</span></span>



| <span data-ttu-id="55787-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55787-181">Requirement</span></span> | <span data-ttu-id="55787-182">Wert</span><span class="sxs-lookup"><span data-stu-id="55787-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55787-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55787-183">Minimum supported client</span></span><br/> | <span data-ttu-id="55787-184">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55787-184">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="55787-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55787-185">Minimum supported server</span></span><br/> | <span data-ttu-id="55787-186">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55787-186">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="55787-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="55787-187">Namespace</span></span><br/>                | <span data-ttu-id="55787-188">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="55787-188">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="55787-189">MOF</span><span class="sxs-lookup"><span data-stu-id="55787-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55787-190"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="55787-190"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="55787-191">DLL</span><span class="sxs-lookup"><span data-stu-id="55787-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55787-192"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="55787-192"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="55787-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55787-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55787-194">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="55787-194">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="55787-195">**Modifyservicesettings**</span><span class="sxs-lookup"><span data-stu-id="55787-195">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-replicationservice.md)
</dt> </dl>

 

