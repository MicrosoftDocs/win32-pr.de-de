---
title: Win32_TSDiscoveredLicenseServer-Klasse
description: Enthält Details zum ermittelten Remotedesktop-Lizenzserver.
ms.assetid: 88523f30-26ad-4f78-a214-f54b7bc1c676
ms.tgt_platform: multiple
keywords:
- Win32_TSDiscoveredLicenseServer-Klasse Remotedesktopdienste
- Win32_TSDiscoveredLicenseServer Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSDiscoveredLicenseServer
- Win32_TSDiscoveredLicenseServer.LicenseServer
- Win32_TSDiscoveredLicenseServer.HowDiscovered
- Win32_TSDiscoveredLicenseServer.IsLSAvailable
- Win32_TSDiscoveredLicenseServer.IsAdminOnLS
- Win32_TSDiscoveredLicenseServer.IssuingCALs
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d633031df533068f2cf5da65f2f6820a93c78513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478825"
---
# <a name="win32_tsdiscoveredlicenseserver-class"></a><span data-ttu-id="47f41-105">Win32-Klasse "-Klasse (Klasse)" \_</span><span class="sxs-lookup"><span data-stu-id="47f41-105">Win32\_TSDiscoveredLicenseServer class</span></span>

<span data-ttu-id="47f41-106">Enthält Details zum ermittelten Remotedesktop-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="47f41-106">Provides details about the discovered Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f41-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="47f41-107">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_TSDiscoveredLicenseServer
{
  string LicenseServer;
  uint32 HowDiscovered;
  uint32 IsLSAvailable;
  uint32 IsAdminOnLS;
  uint32 IssuingCALs;
};
```

## <a name="members"></a><span data-ttu-id="47f41-108">Member</span><span class="sxs-lookup"><span data-stu-id="47f41-108">Members</span></span>

<span data-ttu-id="47f41-109">Die Win32-Klasse " **\_ zdiscoveredlicenseserver** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="47f41-109">The **Win32\_TSDiscoveredLicenseServer** class has these types of members:</span></span>

-   [<span data-ttu-id="47f41-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47f41-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47f41-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47f41-111">Properties</span></span>

<span data-ttu-id="47f41-112">Die **Win32 \_** -Klasse "TS-Klasse" hat diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="47f41-112">The **Win32\_TSDiscoveredLicenseServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47f41-113">**Howentdeckt**</span><span class="sxs-lookup"><span data-stu-id="47f41-113">**HowDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47f41-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="47f41-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47f41-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47f41-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47f41-116">Qualifizierer: [ **veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="47f41-116">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="47f41-117">Diese Eigenschaft wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="47f41-117">This property is no longer supported.</span></span>

<span data-ttu-id="47f41-118">**Windows Server 2008:** Die Remotedesktop-Lizenzserver-Ermittlungsmethode.</span><span class="sxs-lookup"><span data-stu-id="47f41-118">**Windows Server 2008:** The Remote Desktop license server discovery method.</span></span>

<dt>

<span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>

<span data-ttu-id="47f41-119"><span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**Grouppolicykonfigurierte** (0)</span><span class="sxs-lookup"><span data-stu-id="47f41-119"><span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**GroupPolicyConfigured** (0)</span></span>


</dt> <dd>

<span data-ttu-id="47f41-120">Der Lizenzserver wurde mithilfe der Gruppenrichtlinie ermittelt.</span><span class="sxs-lookup"><span data-stu-id="47f41-120">The license server was discovered by using group policy.</span></span>

</dd> <dt>

<span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>

<span data-ttu-id="47f41-121"><span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**Registrykonfigurierte** (1)</span><span class="sxs-lookup"><span data-stu-id="47f41-121"><span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**RegistryConfigured** (1)</span></span>


</dt> <dd>

<span data-ttu-id="47f41-122">Der Lizenzserver wurde mithilfe einer Registrierungs Einstellung ermittelt.</span><span class="sxs-lookup"><span data-stu-id="47f41-122">The license server was discovered by using a registry setting.</span></span>

</dd> <dt>

<span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>

<span data-ttu-id="47f41-123"><span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**Workgroupdiscovery** (2)</span><span class="sxs-lookup"><span data-stu-id="47f41-123"><span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**WorkgroupDiscovery** (2)</span></span>


</dt> <dd>

<span data-ttu-id="47f41-124">Der Lizenzserver wurde mithilfe des Arbeitsgruppen-Ermittlungs Bereichs erkannt.</span><span class="sxs-lookup"><span data-stu-id="47f41-124">The license server was discovered by using the workgroup discovery scope.</span></span>

</dd> <dt>

<span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>

<span data-ttu-id="47f41-125"><span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**Domaindiscovery** (3)</span><span class="sxs-lookup"><span data-stu-id="47f41-125"><span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**DomainDiscovery** (3)</span></span>


</dt> <dd>

<span data-ttu-id="47f41-126">Der Lizenzserver wurde mit dem Domänen Ermittlungs Bereich ermittelt.</span><span class="sxs-lookup"><span data-stu-id="47f41-126">The license server was discovered by using the domain discovery scope.</span></span>

</dd> <dt>

<span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>

<span data-ttu-id="47f41-127"><span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**Enterpriseediscovery** (4)</span><span class="sxs-lookup"><span data-stu-id="47f41-127"><span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**EnterpriseDiscovery** (4)</span></span>


</dt> <dd>

<span data-ttu-id="47f41-128">Der Lizenzserver wurde mithilfe des Bereichs der Gesamtstruktur Ermittlung ermittelt.</span><span class="sxs-lookup"><span data-stu-id="47f41-128">The license server was discovered by using the forest discovery scope.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="47f41-129">**Isadminonls**</span><span class="sxs-lookup"><span data-stu-id="47f41-129">**IsAdminOnLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47f41-130">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="47f41-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47f41-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47f41-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47f41-132">Gibt an, ob das Konto, das zum Ausführen des Skripts oder der exe-Datei verwendet wird, das die **Win32 \_ tsdiscoveredlicenseserver** -Klasse verwendet, über Administrator Zugriff auf den Lizenzserver verfügt.</span><span class="sxs-lookup"><span data-stu-id="47f41-132">Indicates whether the account that is being used to run the script or .exe file that is using the **Win32\_TSDiscoveredLicenseServer** class has administrator access to the license server.</span></span>

<dt>

<span id="No"></span><span id="no"></span><span id="NO"></span>

<span data-ttu-id="47f41-133"><span id="No"></span><span id="no"></span><span id="NO"></span>**Nein** (0)</span><span class="sxs-lookup"><span data-stu-id="47f41-133"><span id="No"></span><span id="no"></span><span id="NO"></span>**No** (0)</span></span>


</dt> <dd>

<span data-ttu-id="47f41-134">Das verwendete Konto hat keinen Administrator Zugriff auf den Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="47f41-134">The account that is being used does not have administrator access to the license server.</span></span>

</dd> <dt>

<span id="Yes"></span><span id="yes"></span><span id="YES"></span>

<span data-ttu-id="47f41-135"><span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Ja** (1)</span><span class="sxs-lookup"><span data-stu-id="47f41-135"><span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Yes** (1)</span></span>


</dt> <dd>

<span data-ttu-id="47f41-136">Das verwendete Konto hat Administrator Zugriff auf den Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="47f41-136">The account that is being used has administrator access to the license server.</span></span>

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span data-ttu-id="47f41-137"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>Nicht **bekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="47f41-137"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Dont know** (2)</span></span>


</dt> <dd>

<span data-ttu-id="47f41-138">Es kann nicht bestimmt werden, ob das verwendete Konto über Administrator Zugriff auf den Lizenzserver verfügt.</span><span class="sxs-lookup"><span data-stu-id="47f41-138">It cannot be determined whether the account that is being used has administrator access to the license server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="47f41-139">**Islsavailable**</span><span class="sxs-lookup"><span data-stu-id="47f41-139">**IsLSAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47f41-140">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="47f41-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47f41-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47f41-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47f41-142">Gibt an, ob der Lizenzserver verfügbar ist (ob eine RPC-Verbindung des Remote Prozedur Aufrufs \[ \] zum Server hergestellt werden kann).</span><span class="sxs-lookup"><span data-stu-id="47f41-142">Indicates whether the license server is available (whether a remote procedure call \[RPC\] connection can be made to the server).</span></span>

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="47f41-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="47f41-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>


</dt> <dd>

<span data-ttu-id="47f41-144">Der Lizenzserver ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="47f41-144">The license server is not available.</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="47f41-145"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="47f41-145"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (1)</span></span>


</dt> <dd>

<span data-ttu-id="47f41-146">Der Lizenzserver ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="47f41-146">The license server is available.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="47f41-147">**Issuingcals**</span><span class="sxs-lookup"><span data-stu-id="47f41-147">**IssuingCALs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47f41-148">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="47f41-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47f41-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47f41-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47f41-150">Gibt an, ob der Lizenzserver Remotedesktopdienste Client Zugriffs Lizenzen (RDS-CALs) für den RD-Sitzungshost Server ausgeben darf.</span><span class="sxs-lookup"><span data-stu-id="47f41-150">Indicates whether the license server is allowed to issue Remote Desktop Services client access licenses (RDS CALs) to the RD Session Host server.</span></span>

<dt>

<span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="47f41-151"><span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Nicht zulässig** (0)</span><span class="sxs-lookup"><span data-stu-id="47f41-151"><span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Not Allowed** (0)</span></span>


</dt> <dd>

<span data-ttu-id="47f41-152">Der Lizenzserver darf keine RDS-CALs für den RD-Sitzungshost Server ausgeben.</span><span class="sxs-lookup"><span data-stu-id="47f41-152">The license server is not allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> <dt>

<span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>

<span data-ttu-id="47f41-153"><span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Zulässig** (1)</span><span class="sxs-lookup"><span data-stu-id="47f41-153"><span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Allowed** (1)</span></span>


</dt> <dd>

<span data-ttu-id="47f41-154">Der Lizenzserver kann RDS-CALs für den RD-Sitzungshost Server ausgeben.</span><span class="sxs-lookup"><span data-stu-id="47f41-154">The license server is allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span data-ttu-id="47f41-155"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>Nicht **bekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="47f41-155"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Dont know** (2)</span></span>


</dt> <dd>

<span data-ttu-id="47f41-156">Es kann nicht bestimmt werden, ob der Lizenzserver RDS-CALs für den RD-Sitzungshost Server ausgeben darf.</span><span class="sxs-lookup"><span data-stu-id="47f41-156">It cannot be determined whether the license server is allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="47f41-157">**Licenseserver**</span><span class="sxs-lookup"><span data-stu-id="47f41-157">**LicenseServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47f41-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="47f41-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47f41-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47f41-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47f41-160">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="47f41-160">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="47f41-161">Der Name des ermittelten Remotedesktop Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="47f41-161">Name of the discovered Remote Desktop license server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47f41-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47f41-162">Remarks</span></span>

<span data-ttu-id="47f41-163">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="47f41-163">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="47f41-164">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**.</span><span class="sxs-lookup"><span data-stu-id="47f41-164">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="47f41-165">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="47f41-165">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="47f41-166">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="47f41-166">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="47f41-167">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="47f41-167">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="47f41-168">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="47f41-168">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="47f41-169">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="47f41-169">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="47f41-170">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="47f41-170">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="47f41-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47f41-171">Requirements</span></span>



| <span data-ttu-id="47f41-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47f41-172">Requirement</span></span> | <span data-ttu-id="47f41-173">Wert</span><span class="sxs-lookup"><span data-stu-id="47f41-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47f41-174">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47f41-174">Minimum supported client</span></span><br/> | <span data-ttu-id="47f41-175">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="47f41-175">None supported</span></span><br/>                                                               |
| <span data-ttu-id="47f41-176">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47f41-176">Minimum supported server</span></span><br/> | <span data-ttu-id="47f41-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47f41-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="47f41-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="47f41-178">Namespace</span></span><br/>                | <span data-ttu-id="47f41-179">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="47f41-179">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="47f41-180">MOF</span><span class="sxs-lookup"><span data-stu-id="47f41-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47f41-181"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="47f41-181"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="47f41-182">DLL</span><span class="sxs-lookup"><span data-stu-id="47f41-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47f41-183"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47f41-183"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

