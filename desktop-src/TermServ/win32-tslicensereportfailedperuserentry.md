---
title: Win32_TSLicenseReportFailedPerUserEntry-Klasse
description: Enthält Details über die Client Zugriffslizenz für fehlerhafte Remotedesktopdienste pro Benutzer (RDS \ 160; Pro Benutzer-CAL).
ms.assetid: 27d155a4-938e-4bca-8d15-03c44740e506
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportFailedPerUserEntry-Klasse Remotedesktopdienste
- Win32_TSLicenseReportFailedPerUserEntry Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserEntry
- Win32_TSLicenseReportFailedPerUserEntry.User
- Win32_TSLicenseReportFailedPerUserEntry.TriedIssuanceOn
- Win32_TSLicenseReportFailedPerUserEntry.CALType
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersion
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18098ce0510a39f6083edcf688a18c10a3e20278
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391558"
---
# <a name="win32_tslicensereportfailedperuserentry-class"></a><span data-ttu-id="b7436-105">Win32-Klasse "-Klasse (Klasse)" \_</span><span class="sxs-lookup"><span data-stu-id="b7436-105">Win32\_TSLicenseReportFailedPerUserEntry class</span></span>

<span data-ttu-id="b7436-106">Enthält Details zur Client Zugriffslizenz für die fehlerhafte Remotedesktopdienste pro Benutzer (RDS pro Benutzer-CAL).</span><span class="sxs-lookup"><span data-stu-id="b7436-106">Provides details about the failed Remote Desktop Services Per User client access license (RDS Per User CAL).</span></span>

<span data-ttu-id="b7436-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b7436-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7436-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7436-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserEntry
{
  string   User;
  DATETIME TriedIssuanceOn;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="b7436-109">Member</span><span class="sxs-lookup"><span data-stu-id="b7436-109">Members</span></span>

<span data-ttu-id="b7436-110">Die Win32-Klasse " **\_ zlicensereportfailedperuserentry** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b7436-110">The **Win32\_TSLicenseReportFailedPerUserEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="b7436-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b7436-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7436-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b7436-112">Properties</span></span>

<span data-ttu-id="b7436-113">Die Win32-Klasse " **\_ slicensereportfailedperuserentry** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b7436-113">The **Win32\_TSLicenseReportFailedPerUserEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7436-114">**Caltype**</span><span class="sxs-lookup"><span data-stu-id="b7436-114">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7436-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b7436-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7436-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b7436-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7436-117">Gibt den Typ der ausgegebene Cal an.</span><span class="sxs-lookup"><span data-stu-id="b7436-117">Specifies the type of CAL issued.</span></span> <span data-ttu-id="b7436-118">Dabei handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="b7436-118">This will be one of the following values.</span></span>

<span data-ttu-id="b7436-119">"Integrierte TS pro Gerät CAL"</span><span class="sxs-lookup"><span data-stu-id="b7436-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="b7436-120">"TS-CAL pro Gerät"</span><span class="sxs-lookup"><span data-stu-id="b7436-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="b7436-121">"TS Internet Connector CAL"</span><span class="sxs-lookup"><span data-stu-id="b7436-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="b7436-122">"TS pro Benutzer-CAL"</span><span class="sxs-lookup"><span data-stu-id="b7436-122">"TS Per User CAL"</span></span>

<span data-ttu-id="b7436-123">"TS-oder RDS-CAL pro Gerät"</span><span class="sxs-lookup"><span data-stu-id="b7436-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="b7436-124">"TS-oder RDS-pro-Benutzer-CAL"</span><span class="sxs-lookup"><span data-stu-id="b7436-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="b7436-125">"VDI Standard Suite pro Device Abonnement License"</span><span class="sxs-lookup"><span data-stu-id="b7436-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="b7436-126">"VDI Premium Suite pro Device Abonnement License"</span><span class="sxs-lookup"><span data-stu-id="b7436-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="b7436-127">"RDS pro Gerät CAL"</span><span class="sxs-lookup"><span data-stu-id="b7436-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="b7436-128">"RDS pro Benutzer-CAL"</span><span class="sxs-lookup"><span data-stu-id="b7436-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="b7436-129">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="b7436-129">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7436-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b7436-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7436-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b7436-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7436-132">Die Version von Remotedesktopdienste, für die die RDS-Client Zugriffslizenz pro Benutzer ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b7436-132">The version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span> <span data-ttu-id="b7436-133">Dabei handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="b7436-133">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="b7436-134">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="b7436-134">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="b7436-135">Nur Server, auf denen Windows Server 2012, Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7436-135">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="b7436-136">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="b7436-136">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="b7436-137">Nur Server, auf denen Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7436-137">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="b7436-138">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="b7436-138">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="b7436-139">Nur Server, auf denen Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7436-139">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b7436-140">**Productversionid**</span><span class="sxs-lookup"><span data-stu-id="b7436-140">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7436-141">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7436-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7436-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b7436-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7436-143">Die Produkt Versions Kennung für das Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="b7436-143">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="b7436-144">4</span><span class="sxs-lookup"><span data-stu-id="b7436-144">4</span></span>
</dt> <dd>

<span data-ttu-id="b7436-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7436-145">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="b7436-146">3</span><span class="sxs-lookup"><span data-stu-id="b7436-146">3</span></span>
</dt> <dd>

<span data-ttu-id="b7436-147">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7436-147">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="b7436-148">2</span><span class="sxs-lookup"><span data-stu-id="b7436-148">2</span></span>
</dt> <dd>

<span data-ttu-id="b7436-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7436-149">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="b7436-150">1</span><span class="sxs-lookup"><span data-stu-id="b7436-150">1</span></span>
</dt> <dd>

<span data-ttu-id="b7436-151">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7436-151">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b7436-152">0</span><span class="sxs-lookup"><span data-stu-id="b7436-152">0</span></span>
</dt> <dd>

<span data-ttu-id="b7436-153">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7436-153">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b7436-154">**Trieabanceon**</span><span class="sxs-lookup"><span data-stu-id="b7436-154">**TriedIssuanceOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7436-155">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="b7436-155">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="b7436-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b7436-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7436-157">Das Datum, an dem die Lizenz Ausstellung versucht wurde.</span><span class="sxs-lookup"><span data-stu-id="b7436-157">The date on which license issuance was attempted.</span></span>

</dd> <dt>

<span data-ttu-id="b7436-158">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b7436-158">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7436-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b7436-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7436-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b7436-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7436-161">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b7436-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b7436-162">Der Name des Benutzers, für den die Lizenz Ausstellung versucht wurde.</span><span class="sxs-lookup"><span data-stu-id="b7436-162">The name of the user to whom the license issuance was attempted.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7436-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7436-163">Requirements</span></span>



| <span data-ttu-id="b7436-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7436-164">Requirement</span></span> | <span data-ttu-id="b7436-165">Wert</span><span class="sxs-lookup"><span data-stu-id="b7436-165">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7436-166">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7436-166">Minimum supported client</span></span><br/> | <span data-ttu-id="b7436-167">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b7436-167">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="b7436-168">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7436-168">Minimum supported server</span></span><br/> | <span data-ttu-id="b7436-169">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7436-169">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="b7436-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7436-170">Namespace</span></span><br/>                | <span data-ttu-id="b7436-171">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b7436-171">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="b7436-172">MOF</span><span class="sxs-lookup"><span data-stu-id="b7436-172">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7436-173"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b7436-173"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7436-174">DLL</span><span class="sxs-lookup"><span data-stu-id="b7436-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7436-175"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7436-175"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7436-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7436-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7436-177">**Fetchreportfailedperuserentries**</span><span class="sxs-lookup"><span data-stu-id="b7436-177">**FetchReportFailedPerUserEntries**</span></span>](fetchreportfailedperuserentries-win32-tslicensereport.md)
</dt> </dl>

 

