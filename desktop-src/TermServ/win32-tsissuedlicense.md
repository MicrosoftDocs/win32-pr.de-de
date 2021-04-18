---
title: Win32_TSIssuedLicense-Klasse
description: Beschreibt Instanzen von Remotedesktopdienste Client Zugriffs Lizenzen pro Gerät (RDS \ 160; Pro-Gerät-CALs), die von einem Remotedesktop Lizenzserver ausgestellt werden.
ms.assetid: 15825dc5-9ada-4c11-ac77-beb681e9b33c
ms.tgt_platform: multiple
keywords:
- Win32_TSIssuedLicense-Klasse Remotedesktopdienste
- Win32_TSIssuedLicense Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense
- Win32_TSIssuedLicense.LicenseId
- Win32_TSIssuedLicense.KeyPackId
- Win32_TSIssuedLicense.sIssuedToUser
- Win32_TSIssuedLicense.sIssuedToComputer
- Win32_TSIssuedLicense.LicenseStatus
- Win32_TSIssuedLicense.IssueDate
- Win32_TSIssuedLicense.ExpirationDate
- Win32_TSIssuedLicense.sHardwareId
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c3d08a68ddcc15a912de4c674403928211a297e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337934"
---
# <a name="win32_tsissuedlicense-class"></a><span data-ttu-id="10143-105">Win32- \_ Klasse "tsissuedlicense"</span><span class="sxs-lookup"><span data-stu-id="10143-105">Win32\_TSIssuedLicense class</span></span>

<span data-ttu-id="10143-106">Beschreibt Instanzen von Remotedesktopdienste pro Geräte-Client Zugriffs Lizenzen (RDS pro Gerät CALs), die von einem Remotedesktop Lizenzserver ausgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="10143-106">Describes instances of Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) that are issued from a Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="10143-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="10143-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSIssuedLicense
{
  uint32   LicenseId;
  uint32   KeyPackId;
  string   sIssuedToUser;
  string   sIssuedToComputer;
  uint32   LicenseStatus;
  DATETIME IssueDate;
  DATETIME ExpirationDate;
  string   sHardwareId;
};
```

## <a name="members"></a><span data-ttu-id="10143-108">Member</span><span class="sxs-lookup"><span data-stu-id="10143-108">Members</span></span>

<span data-ttu-id="10143-109">Die Win32-Klasse " **\_ tsissuedlicense** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="10143-109">The **Win32\_TSIssuedLicense** class has these types of members:</span></span>

-   [<span data-ttu-id="10143-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="10143-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="10143-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="10143-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="10143-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="10143-112">Methods</span></span>

<span data-ttu-id="10143-113">Die Win32-Klasse " **\_ tsissuedlicense** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="10143-113">The **Win32\_TSIssuedLicense** class has these methods.</span></span>



| <span data-ttu-id="10143-114">Methode</span><span class="sxs-lookup"><span data-stu-id="10143-114">Method</span></span>                                         | <span data-ttu-id="10143-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10143-115">Description</span></span>                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10143-116">**Erteilte**</span><span class="sxs-lookup"><span data-stu-id="10143-116">**Revoke**</span></span>](revoke-win32-tsissuedlicense.md) | <span data-ttu-id="10143-117">Widerruft die RDS-CALs pro Gerät, die durch das Win32-Objekt " **\_ tsissuedlicense** " dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="10143-117">Revokes the RDS Per Device CALs that are represented by the **Win32\_TSIssuedLicense** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="10143-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="10143-118">Properties</span></span>

<span data-ttu-id="10143-119">Die Win32-Klasse " **\_ tsissuedlicense** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="10143-119">The **Win32\_TSIssuedLicense** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10143-120">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="10143-120">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10143-121">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="10143-121">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="10143-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10143-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10143-123">Gibt das Datum an, an dem die Lizenz abläuft.</span><span class="sxs-lookup"><span data-stu-id="10143-123">Identifies the date that the license will expire.</span></span>

</dd> <dt>

<span data-ttu-id="10143-124">**IssueDate**</span><span class="sxs-lookup"><span data-stu-id="10143-124">**IssueDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10143-125">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="10143-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="10143-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10143-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10143-127">Gibt das Datum an, an dem die Lizenz ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="10143-127">Identifies the date that the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="10143-128">**Keypackid**</span><span class="sxs-lookup"><span data-stu-id="10143-128">**KeyPackId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10143-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10143-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10143-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10143-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10143-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="10143-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="10143-132">Identifiziert das Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="10143-132">Identifies the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="10143-133">**Licenseid**</span><span class="sxs-lookup"><span data-stu-id="10143-133">**LicenseId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10143-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10143-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10143-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10143-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10143-136">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="10143-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="10143-137">Eindeutiger Bezeichner für diese Lizenz.</span><span class="sxs-lookup"><span data-stu-id="10143-137">Unique identifier for this license.</span></span>

</dd> <dt>

<span data-ttu-id="10143-138">**LicenseStatus**</span><span class="sxs-lookup"><span data-stu-id="10143-138">**LicenseStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10143-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10143-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10143-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10143-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10143-141">Der Status der Lizenz.</span><span class="sxs-lookup"><span data-stu-id="10143-141">Status of the license.</span></span>

<dt>

<span data-ttu-id="10143-142">0</span><span class="sxs-lookup"><span data-stu-id="10143-142">0</span></span>
</dt> <dd>

<span data-ttu-id="10143-143">Der Lizenzstatus ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="10143-143">The license status is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="10143-144">1</span><span class="sxs-lookup"><span data-stu-id="10143-144">1</span></span>
</dt> <dd>

<span data-ttu-id="10143-145">Die Lizenz ist eine temporäre Lizenz.</span><span class="sxs-lookup"><span data-stu-id="10143-145">The license is a temporary license.</span></span>

</dd> <dt>

<span data-ttu-id="10143-146">2</span><span class="sxs-lookup"><span data-stu-id="10143-146">2</span></span>
</dt> <dd>

<span data-ttu-id="10143-147">Die Lizenz ist aktiv.</span><span class="sxs-lookup"><span data-stu-id="10143-147">The license is active.</span></span>

</dd> <dt>

<span data-ttu-id="10143-148">3</span><span class="sxs-lookup"><span data-stu-id="10143-148">3</span></span>
</dt> <dd>

<span data-ttu-id="10143-149">Die Lizenz ist eine Upgradelizenz.</span><span class="sxs-lookup"><span data-stu-id="10143-149">The license is an upgrade license.</span></span>

</dd> <dt>

<span data-ttu-id="10143-150">4</span><span class="sxs-lookup"><span data-stu-id="10143-150">4</span></span>
</dt> <dd>

<span data-ttu-id="10143-151">Die Lizenz wurde widerrufen.</span><span class="sxs-lookup"><span data-stu-id="10143-151">The license has been revoked.</span></span>

</dd> <dt>

<span data-ttu-id="10143-152">5</span><span class="sxs-lookup"><span data-stu-id="10143-152">5</span></span>
</dt> <dd>

<span data-ttu-id="10143-153">Der Lizenzstatus ist "Ausstehend".</span><span class="sxs-lookup"><span data-stu-id="10143-153">The license status is pending.</span></span>

</dd> <dt>

<span data-ttu-id="10143-154">6</span><span class="sxs-lookup"><span data-stu-id="10143-154">6</span></span>
</dt> <dd>

<span data-ttu-id="10143-155">Die Lizenz ist eine gleichzeitige Lizenz.</span><span class="sxs-lookup"><span data-stu-id="10143-155">The license is a concurrent license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10143-156">**shardwareid**</span><span class="sxs-lookup"><span data-stu-id="10143-156">**sHardwareId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10143-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="10143-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10143-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10143-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10143-159">Der Hardware Bezeichner, für den die Lizenz ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="10143-159">Hardware identifier for which the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="10143-160">**sissuedto Computer**</span><span class="sxs-lookup"><span data-stu-id="10143-160">**sIssuedToComputer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10143-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="10143-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10143-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10143-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10143-163">Der Name des Computers, für den die Lizenz ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="10143-163">Computer name for which the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="10143-164">**sissuedtouser**</span><span class="sxs-lookup"><span data-stu-id="10143-164">**sIssuedToUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10143-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="10143-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10143-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10143-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10143-167">Der Benutzername, für den die Lizenz ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="10143-167">User name for which the license was issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10143-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10143-168">Remarks</span></span>

<span data-ttu-id="10143-169">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="10143-169">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="10143-170">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="10143-170">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="10143-171">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="10143-171">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="10143-172">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="10143-172">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="10143-173">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="10143-173">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="10143-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10143-174">Requirements</span></span>



| <span data-ttu-id="10143-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10143-175">Requirement</span></span> | <span data-ttu-id="10143-176">Wert</span><span class="sxs-lookup"><span data-stu-id="10143-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="10143-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10143-177">Minimum supported client</span></span><br/> | <span data-ttu-id="10143-178">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="10143-178">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="10143-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10143-179">Minimum supported server</span></span><br/> | <span data-ttu-id="10143-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10143-180">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="10143-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="10143-181">Namespace</span></span><br/>                | <span data-ttu-id="10143-182">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="10143-182">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="10143-183">MOF</span><span class="sxs-lookup"><span data-stu-id="10143-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10143-184"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="10143-184"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="10143-185">DLL</span><span class="sxs-lookup"><span data-stu-id="10143-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10143-186"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10143-186"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10143-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10143-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10143-188">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="10143-188">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="10143-189">**Win32-Datei- \_ /licensereport**</span><span class="sxs-lookup"><span data-stu-id="10143-189">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="10143-190">**Win32-Wert für "- \_ Lizenzserver"**</span><span class="sxs-lookup"><span data-stu-id="10143-190">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="10143-191">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="10143-191">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

