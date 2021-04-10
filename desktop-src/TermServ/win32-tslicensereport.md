---
title: Win32_TSLicenseReport-Klasse
description: Stellt Instanzen von Remotedesktopdienste pro Benutzer-Client Zugriffslizenz bereit (RDS \ 160; Pro Benutzer-CAL) Verwendungs Berichte, die auf dem Remotedesktop-Lizenzserver generiert werden, sowie Methoden zum generieren, abrufen und Löschen von Lizenz Berichten.
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReport-Klasse Remotedesktopdienste
- Win32_TSLicenseReport Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport
- Win32_TSLicenseReport.FileName
- Win32_TSLicenseReport.LicenseUsageCount
- Win32_TSLicenseReport.InstalledLicenses
- Win32_TSLicenseReport.GenerationDateTime
- Win32_TSLicenseReport.ScopeType
- Win32_TSLicenseReport.ScopeValue
- Win32_TSLicenseReport.Version
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de997056222c1b525253f320f6fe191f017614f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858696"
---
# <a name="win32_tslicensereport-class"></a><span data-ttu-id="24919-105">Win32-Klasse "" \_</span><span class="sxs-lookup"><span data-stu-id="24919-105">Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="24919-106">Stellt Instanzen von Remotedesktopdienste Client Zugriffslizenz-Verwendungs Berichte pro Benutzer (RDS pro Benutzer) bereit, die auf dem Remotedesktop-Lizenzserver generiert werden, sowie Methoden zum generieren, abrufen und Löschen von Lizenz Berichten.</span><span class="sxs-lookup"><span data-stu-id="24919-106">Provides instances of Remote Desktop Services Per User client access license (RDS Per User CAL) usage reports that are generated on the Remote Desktop license server, and methods for license report generation, fetch, and delete operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="24919-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="24919-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseReport
{
  string   FileName;
  uint32   LicenseUsageCount;
  uint32   InstalledLicenses;
  DATETIME GenerationDateTime;
  uint32   ScopeType;
  string   ScopeValue;
  uint32   Version;
};
```

## <a name="members"></a><span data-ttu-id="24919-108">Member</span><span class="sxs-lookup"><span data-stu-id="24919-108">Members</span></span>

<span data-ttu-id="24919-109">Die Win32-Klasse " **\_ zlicensereport** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="24919-109">The **Win32\_TSLicenseReport** class has these types of members:</span></span>

-   [<span data-ttu-id="24919-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="24919-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="24919-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24919-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="24919-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="24919-112">Methods</span></span>

<span data-ttu-id="24919-113">Die Win32-Klasse " **\_ zlicensereport** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="24919-113">The **Win32\_TSLicenseReport** class has these methods.</span></span>



| <span data-ttu-id="24919-114">Methode</span><span class="sxs-lookup"><span data-stu-id="24919-114">Method</span></span>                                                                                                         | <span data-ttu-id="24919-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24919-115">Description</span></span>                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24919-116">**DeleteReport**</span><span class="sxs-lookup"><span data-stu-id="24919-116">**DeleteReport**</span></span>](deletereport-win32-tslicensereport.md)                                                     | <span data-ttu-id="24919-117">Löscht ein Berichts Objekt auf dem Remotedesktop-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="24919-117">Deletes a report object on the Remote Desktop license server.</span></span> <span data-ttu-id="24919-118">Dabei handelt es sich nicht um eine statische Methode.</span><span class="sxs-lookup"><span data-stu-id="24919-118">This is not a static method.</span></span><br/>                                                                                           |
| [<span data-ttu-id="24919-119">**Fetchreportentries**</span><span class="sxs-lookup"><span data-stu-id="24919-119">**FetchReportEntries**</span></span>](fetchreportentries-win32-tslicensereport.md)                                         | <span data-ttu-id="24919-120">Ruft Einträge im Berichts Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="24919-120">Retrieves entries in the report object.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="24919-121">**Fetchreportfailedperuserentries**</span><span class="sxs-lookup"><span data-stu-id="24919-121">**FetchReportFailedPerUserEntries**</span></span>](fetchreportfailedperuserentries-win32-tslicensereport.md)               | <span data-ttu-id="24919-122">Ruft Details der fehlerhaften Remotedesktopdienste pro Benutzer-Client Zugriffs Lizenzen (RDS pro Benutzer-CALs) aus dem Bericht ab.</span><span class="sxs-lookup"><span data-stu-id="24919-122">Retrieves details of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span><br/>                                                             |
| [<span data-ttu-id="24919-123">**Fetchreportfailedperusersummaryentries**</span><span class="sxs-lookup"><span data-stu-id="24919-123">**FetchReportFailedPerUserSummaryEntries**</span></span>](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | <span data-ttu-id="24919-124">Hiermit werden zusammenfassende Informationen zu fehlerhaften Remotedesktopdienste pro Benutzer-Client Zugriffs Lizenzen (RDS pro Benutzer-CALs) aus dem Bericht abgerufen.</span><span class="sxs-lookup"><span data-stu-id="24919-124">Retrieves summary information of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span><br/>                                                 |
| [<span data-ttu-id="24919-125">**Fetchreportperdeviceentries**</span><span class="sxs-lookup"><span data-stu-id="24919-125">**FetchReportPerDeviceEntries**</span></span>](fetchreportperdeviceentries-win32-tslicensereport.md)                       | <span data-ttu-id="24919-126">Ruft Informationen zu ausgestellten Remotedesktopdienste pro Geräte-Client Zugriffs Lizenzen (RDS pro Gerät CALs) aus dem Bericht ab.</span><span class="sxs-lookup"><span data-stu-id="24919-126">Retrieves information of issued Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) from the report.</span></span><br/>                                                     |
| [<span data-ttu-id="24919-127">**Fetchreportsummaryentries**</span><span class="sxs-lookup"><span data-stu-id="24919-127">**FetchReportSummaryEntries**</span></span>](win32-tslicensereport-fetchreportsummaryentries.md)                           | <span data-ttu-id="24919-128">Ruft Lizenz Zusammenfassungen aus dem Berichts Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="24919-128">Retrieves license summaries from the report object.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="24919-129">**GenerateReport**</span><span class="sxs-lookup"><span data-stu-id="24919-129">**GenerateReport**</span></span>](generatereport-win32-tslicensereport.md)                                                 | <span data-ttu-id="24919-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="24919-130">This method is not supported.</span></span><br/> <span data-ttu-id="24919-131">**Windows Server 2008 R2 und Windows Server 2008:** Generiert einen aktuellen Bericht pro Benutzer-Lizenz Verwendung auf dem Remotedesktop-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="24919-131">**Windows Server 2008 R2 and Windows Server 2008:** Generates a current per user license usage report on the Remote Desktop license server.</span></span><br/> |
| [<span data-ttu-id="24919-132">**Generatereportex**</span><span class="sxs-lookup"><span data-stu-id="24919-132">**GenerateReportEx**</span></span>](generatereportex-win32-tslicensereport.md)                                             | <span data-ttu-id="24919-133">Generiert einen aktuellen Bericht pro Benutzer-Lizenz Verwendung auf dem Remotedesktop-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="24919-133">Generates a current per user license usage report on the Remote Desktop license server.</span></span><br/>                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="24919-134">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24919-134">Properties</span></span>

<span data-ttu-id="24919-135">Die Win32-Klasse " **\_ slicensereport** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="24919-135">The **Win32\_TSLicenseReport** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="24919-136">**FileName**</span><span class="sxs-lookup"><span data-stu-id="24919-136">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24919-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="24919-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24919-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="24919-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24919-139">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="24919-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="24919-140">Der Name des Berichts.</span><span class="sxs-lookup"><span data-stu-id="24919-140">The report name.</span></span>

</dd> <dt>

<span data-ttu-id="24919-141">**Generationdatetime**</span><span class="sxs-lookup"><span data-stu-id="24919-141">**GenerationDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24919-142">**[Datentyp: DateTime](/windows/desktop/WmiSdk/datetime)**</span><span class="sxs-lookup"><span data-stu-id="24919-142">Data type: **[DATETIME](/windows/desktop/WmiSdk/datetime)**</span></span>
</dt> <dt>

<span data-ttu-id="24919-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="24919-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24919-144">RD-Lizenzierung Datum und Uhrzeit der Berichtsgenerierung.</span><span class="sxs-lookup"><span data-stu-id="24919-144">RD Licensing report generation date and time.</span></span>

</dd> <dt>

<span data-ttu-id="24919-145">**Installedlicenses**</span><span class="sxs-lookup"><span data-stu-id="24919-145">**InstalledLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24919-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24919-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24919-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="24919-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24919-148">Qualifizierer: [ **veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="24919-148">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="24919-149">Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="24919-149">This property is not supported.</span></span>

<span data-ttu-id="24919-150">**Windows Server 2008 R2 und Windows Server 2008:** Anzahl der installierten RDS-pro-Benutzer-CALs.</span><span class="sxs-lookup"><span data-stu-id="24919-150">**Windows Server 2008 R2 and Windows Server 2008:** Number of RDS Per User CALs that are installed.</span></span>

</dd> <dt>

<span data-ttu-id="24919-151">**Licenseusagecount**</span><span class="sxs-lookup"><span data-stu-id="24919-151">**LicenseUsageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24919-152">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24919-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24919-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="24919-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24919-154">Qualifizierer: [ **veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="24919-154">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="24919-155">Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="24919-155">This property is not supported.</span></span>

<span data-ttu-id="24919-156">**Windows Server 2008 R2 und Windows Server 2008:** Anzahl der RDS-Client Zugriffs Lizenzen pro Benutzer, die zurzeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24919-156">**Windows Server 2008 R2 and Windows Server 2008:** Number of RDS Per User CALs that are currently in use.</span></span>

</dd> <dt>

<span data-ttu-id="24919-157">**ScopeType**</span><span class="sxs-lookup"><span data-stu-id="24919-157">**ScopeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24919-158">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24919-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24919-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="24919-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24919-160">Qualifizierer: [ **veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="24919-160">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="24919-161">Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="24919-161">This property is not supported.</span></span>

<span data-ttu-id="24919-162">**Windows Server 2008 R2 und Windows Server 2008:** RD-Lizenzierung Berichts Bereichstyp.</span><span class="sxs-lookup"><span data-stu-id="24919-162">**Windows Server 2008 R2 and Windows Server 2008:** RD Licensing report scope type.</span></span>

</dd> <dt>

<span data-ttu-id="24919-163">**Bereich**</span><span class="sxs-lookup"><span data-stu-id="24919-163">**ScopeValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24919-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="24919-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24919-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="24919-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24919-166">Qualifizierer: [ **veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="24919-166">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="24919-167">Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="24919-167">This property is not supported.</span></span>

<span data-ttu-id="24919-168">**Windows Server 2008 R2 und Windows Server 2008:** RD-Lizenzierung Berichts Bereichs Wert.</span><span class="sxs-lookup"><span data-stu-id="24919-168">**Windows Server 2008 R2 and Windows Server 2008:** RD Licensing report scope value.</span></span>

</dd> <dt>

<span data-ttu-id="24919-169">**Version**</span><span class="sxs-lookup"><span data-stu-id="24919-169">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24919-170">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24919-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24919-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="24919-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24919-172">RD-Lizenzierung Berichts Version.</span><span class="sxs-lookup"><span data-stu-id="24919-172">RD Licensing report version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24919-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24919-173">Remarks</span></span>

<span data-ttu-id="24919-174">Berichte, die mithilfe von WMI generiert werden, werden in RD-Lizenzierungs-Manager angezeigt.</span><span class="sxs-lookup"><span data-stu-id="24919-174">Reports that are generated by using WMI are displayed in RD Licensing Manager.</span></span> <span data-ttu-id="24919-175">Berichte, die mithilfe von WMI gelöscht werden, werden auch aus RD-Lizenzierungs-Manager gelöscht.</span><span class="sxs-lookup"><span data-stu-id="24919-175">Reports that are deleted by using WMI are also deleted from RD Licensing Manager.</span></span>

<span data-ttu-id="24919-176">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="24919-176">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="24919-177">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="24919-177">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="24919-178">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="24919-178">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="24919-179">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="24919-179">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="24919-180">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="24919-180">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="24919-181">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24919-181">Requirements</span></span>



| <span data-ttu-id="24919-182">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24919-182">Requirement</span></span> | <span data-ttu-id="24919-183">Wert</span><span class="sxs-lookup"><span data-stu-id="24919-183">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="24919-184">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24919-184">Minimum supported client</span></span><br/> | <span data-ttu-id="24919-185">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="24919-185">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="24919-186">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24919-186">Minimum supported server</span></span><br/> | <span data-ttu-id="24919-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24919-187">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="24919-188">Namespace</span><span class="sxs-lookup"><span data-stu-id="24919-188">Namespace</span></span><br/>                | <span data-ttu-id="24919-189">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="24919-189">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="24919-190">MOF</span><span class="sxs-lookup"><span data-stu-id="24919-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24919-191"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="24919-191"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="24919-192">DLL</span><span class="sxs-lookup"><span data-stu-id="24919-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24919-193"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24919-193"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24919-194">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24919-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24919-195">**Win32-" \_ tsissuedlicense"**</span><span class="sxs-lookup"><span data-stu-id="24919-195">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="24919-196">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="24919-196">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="24919-197">**Win32-Wert für "- \_ Lizenzserver"**</span><span class="sxs-lookup"><span data-stu-id="24919-197">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="24919-198">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="24919-198">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

