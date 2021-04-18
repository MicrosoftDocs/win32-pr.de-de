---
title: Win32_TSLicenseReportEntry-Klasse
description: Enthält Details zur Client Zugriffslizenz für die ausgestellten Remotedesktopdienste pro Benutzer (RDS \ 160; Pro Benutzer-CAL).
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportEntry-Klasse Remotedesktopdienste
- Win32_TSLicenseReportEntry Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportEntry
- Win32_TSLicenseReportEntry.User
- Win32_TSLicenseReportEntry.ExpirationDate
- Win32_TSLicenseReportEntry.CALType
- Win32_TSLicenseReportEntry.ProductVersion
- Win32_TSLicenseReportEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44fa97a91561a9d4cf3fd571c773288796754858
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391559"
---
# <a name="win32_tslicensereportentry-class"></a><span data-ttu-id="7c010-105">Win32-Klasse "-Klasse (Klasse)" \_</span><span class="sxs-lookup"><span data-stu-id="7c010-105">Win32\_TSLicenseReportEntry class</span></span>

<span data-ttu-id="7c010-106">Stellt Details der pro Benutzer-Client Zugriffslizenz ausgestellten Remotedesktopdienste (RDS pro Benutzer-CAL) bereit.</span><span class="sxs-lookup"><span data-stu-id="7c010-106">Provides details of the issued Remote Desktop Services Per User client access license (RDS Per User CAL).</span></span>

## <a name="syntax"></a><span data-ttu-id="7c010-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c010-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportEntry
{
  string   User;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="7c010-108">Member</span><span class="sxs-lookup"><span data-stu-id="7c010-108">Members</span></span>

<span data-ttu-id="7c010-109">Die Win32-Klasse " **\_ zlicensereportentry** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7c010-109">The **Win32\_TSLicenseReportEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="7c010-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c010-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7c010-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c010-111">Properties</span></span>

<span data-ttu-id="7c010-112">Die Win32-Klasse " **\_ stilicensereportentry** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7c010-112">The **Win32\_TSLicenseReportEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c010-113">**Caltype**</span><span class="sxs-lookup"><span data-stu-id="7c010-113">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c010-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c010-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c010-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c010-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c010-116">Gibt den Typ der ausgegebene Cal an.</span><span class="sxs-lookup"><span data-stu-id="7c010-116">Specifies the type of CAL issued.</span></span> <span data-ttu-id="7c010-117">Dabei handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="7c010-117">This will be one of the following values.</span></span>

<span data-ttu-id="7c010-118">**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7c010-118">**Windows Server 2008 R2 and Windows Server 2008:** This property is not supported.</span></span>

<span data-ttu-id="7c010-119">"Integrierte TS pro Gerät CAL"</span><span class="sxs-lookup"><span data-stu-id="7c010-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="7c010-120">"TS-CAL pro Gerät"</span><span class="sxs-lookup"><span data-stu-id="7c010-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="7c010-121">"TS Internet Connector CAL"</span><span class="sxs-lookup"><span data-stu-id="7c010-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="7c010-122">"TS pro Benutzer-CAL"</span><span class="sxs-lookup"><span data-stu-id="7c010-122">"TS Per User CAL"</span></span>

<span data-ttu-id="7c010-123">"TS-oder RDS-CAL pro Gerät"</span><span class="sxs-lookup"><span data-stu-id="7c010-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="7c010-124">"TS-oder RDS-pro-Benutzer-CAL"</span><span class="sxs-lookup"><span data-stu-id="7c010-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="7c010-125">"VDI Standard Suite pro Device Abonnement License"</span><span class="sxs-lookup"><span data-stu-id="7c010-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="7c010-126">"VDI Premium Suite pro Device Abonnement License"</span><span class="sxs-lookup"><span data-stu-id="7c010-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="7c010-127">"RDS pro Gerät CAL"</span><span class="sxs-lookup"><span data-stu-id="7c010-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="7c010-128">"RDS pro Benutzer-CAL"</span><span class="sxs-lookup"><span data-stu-id="7c010-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="7c010-129">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="7c010-129">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c010-130">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="7c010-130">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="7c010-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c010-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c010-132">Ablaufdatum der Lizenz, die für den Benutzer ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7c010-132">Expiration date of the license that was issued to the user.</span></span>

</dd> <dt>

<span data-ttu-id="7c010-133">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="7c010-133">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c010-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c010-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c010-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c010-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c010-136">Die Version von Remotedesktopdienste, für die die RDS-Client Zugriffslizenz pro Benutzer ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7c010-136">Version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span>

<dt>

<span data-ttu-id="7c010-137">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="7c010-137">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="7c010-138">Nur Server, auf denen Windows Server 2012, Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7c010-138">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="7c010-139">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="7c010-139">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="7c010-140">Nur Server, auf denen Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7c010-140">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="7c010-141">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="7c010-141">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="7c010-142">Nur Server, auf denen Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7c010-142">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7c010-143">**Productversionid**</span><span class="sxs-lookup"><span data-stu-id="7c010-143">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c010-144">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7c010-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7c010-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c010-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c010-146">Die Produkt Versions Kennung für das Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="7c010-146">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="7c010-147">4</span><span class="sxs-lookup"><span data-stu-id="7c010-147">4</span></span>
</dt> <dd>

<span data-ttu-id="7c010-148">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7c010-148">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="7c010-149">3</span><span class="sxs-lookup"><span data-stu-id="7c010-149">3</span></span>
</dt> <dd>

<span data-ttu-id="7c010-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7c010-150">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="7c010-151">2</span><span class="sxs-lookup"><span data-stu-id="7c010-151">2</span></span>
</dt> <dd>

<span data-ttu-id="7c010-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c010-152">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="7c010-153">1</span><span class="sxs-lookup"><span data-stu-id="7c010-153">1</span></span>
</dt> <dd>

<span data-ttu-id="7c010-154">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7c010-154">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7c010-155">0</span><span class="sxs-lookup"><span data-stu-id="7c010-155">0</span></span>
</dt> <dd>

<span data-ttu-id="7c010-156">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7c010-156">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7c010-157">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="7c010-157">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c010-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7c010-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c010-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7c010-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c010-160">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7c010-160">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7c010-161">Der Name des Benutzers, für den die Lizenz ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7c010-161">Name of the user to whom the license was issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c010-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c010-162">Remarks</span></span>

<span data-ttu-id="7c010-163">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="7c010-163">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="7c010-164">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="7c010-164">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7c010-165">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="7c010-165">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7c010-166">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7c010-166">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7c010-167">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7c010-167">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c010-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c010-168">Requirements</span></span>



| <span data-ttu-id="7c010-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c010-169">Requirement</span></span> | <span data-ttu-id="7c010-170">Wert</span><span class="sxs-lookup"><span data-stu-id="7c010-170">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c010-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c010-171">Minimum supported client</span></span><br/> | <span data-ttu-id="7c010-172">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7c010-172">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="7c010-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c010-173">Minimum supported server</span></span><br/> | <span data-ttu-id="7c010-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c010-174">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="7c010-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="7c010-175">Namespace</span></span><br/>                | <span data-ttu-id="7c010-176">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="7c010-176">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="7c010-177">MOF</span><span class="sxs-lookup"><span data-stu-id="7c010-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c010-178"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7c010-178"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c010-179">DLL</span><span class="sxs-lookup"><span data-stu-id="7c010-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c010-180"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c010-180"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c010-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c010-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c010-182">**Fetchreportentries**</span><span class="sxs-lookup"><span data-stu-id="7c010-182">**FetchReportEntries**</span></span>](fetchreportentries-win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="7c010-183">**Win32-" \_ tsissuedlicense"**</span><span class="sxs-lookup"><span data-stu-id="7c010-183">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="7c010-184">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="7c010-184">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="7c010-185">**Win32-Datei- \_ /licensereport**</span><span class="sxs-lookup"><span data-stu-id="7c010-185">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="7c010-186">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="7c010-186">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

