---
title: Win32_TSLicenseReportPerDeviceEntry-Klasse
description: Enthält Details zur Client Zugriffslizenz für das fehlgeschlagene Remotedesktopdienste pro Gerät (RDS \ 160; Pro-Gerät-CAL).
ms.assetid: b26f2518-439c-4562-9492-a0cfa60c457a
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportPerDeviceEntry-Klasse Remotedesktopdienste
- Win32_TSLicenseReportPerDeviceEntry Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportPerDeviceEntry
- Win32_TSLicenseReportPerDeviceEntry.sIssuedToComputer
- Win32_TSLicenseReportPerDeviceEntry.sHardwareId
- Win32_TSLicenseReportPerDeviceEntry.ExpirationDate
- Win32_TSLicenseReportPerDeviceEntry.CALType
- Win32_TSLicenseReportPerDeviceEntry.ProductVersion
- Win32_TSLicenseReportPerDeviceEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a120d477ff03675f160d94f1506f59cdf1462fa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475462"
---
# <a name="win32_tslicensereportperdeviceentry-class"></a><span data-ttu-id="4d69a-105">Win32- \_ Klasse "zlicensereportperdeviceentry"</span><span class="sxs-lookup"><span data-stu-id="4d69a-105">Win32\_TSLicenseReportPerDeviceEntry class</span></span>

<span data-ttu-id="4d69a-106">Enthält Details zu den fehlerhaften Remotedesktopdienste pro Geräte-Client Zugriffslizenz (RDS pro Gerät CAL).</span><span class="sxs-lookup"><span data-stu-id="4d69a-106">Provides details about the failed Remote Desktop Services Per Device client access license (RDS Per Device CAL).</span></span>

<span data-ttu-id="4d69a-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4d69a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d69a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d69a-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportPerDeviceEntry
{
  string   sIssuedToComputer;
  string   sHardwareId;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="4d69a-109">Member</span><span class="sxs-lookup"><span data-stu-id="4d69a-109">Members</span></span>

<span data-ttu-id="4d69a-110">Die Win32-Klasse " **\_ zlicensereportperdeviceentry** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4d69a-110">The **Win32\_TSLicenseReportPerDeviceEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="4d69a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d69a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d69a-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d69a-112">Properties</span></span>

<span data-ttu-id="4d69a-113">Die Win32-Klasse " **\_ zlicensereportperdeviceentry** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4d69a-113">The **Win32\_TSLicenseReportPerDeviceEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d69a-114">**Caltype**</span><span class="sxs-lookup"><span data-stu-id="4d69a-114">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d69a-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4d69a-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d69a-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d69a-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d69a-117">Gibt den Typ der ausgegebene Cal an.</span><span class="sxs-lookup"><span data-stu-id="4d69a-117">Specifies the type of CAL issued.</span></span> <span data-ttu-id="4d69a-118">Dabei handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="4d69a-118">This will be one of the following values.</span></span>

<span data-ttu-id="4d69a-119">"Integrierte TS pro Gerät CAL"</span><span class="sxs-lookup"><span data-stu-id="4d69a-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="4d69a-120">"TS-CAL pro Gerät"</span><span class="sxs-lookup"><span data-stu-id="4d69a-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="4d69a-121">"TS Internet Connector CAL"</span><span class="sxs-lookup"><span data-stu-id="4d69a-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="4d69a-122">"TS pro Benutzer-CAL"</span><span class="sxs-lookup"><span data-stu-id="4d69a-122">"TS Per User CAL"</span></span>

<span data-ttu-id="4d69a-123">"TS-oder RDS-CAL pro Gerät"</span><span class="sxs-lookup"><span data-stu-id="4d69a-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="4d69a-124">"TS-oder RDS-pro-Benutzer-CAL"</span><span class="sxs-lookup"><span data-stu-id="4d69a-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="4d69a-125">"VDI Standard Suite pro Device Abonnement License"</span><span class="sxs-lookup"><span data-stu-id="4d69a-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="4d69a-126">"VDI Premium Suite pro Device Abonnement License"</span><span class="sxs-lookup"><span data-stu-id="4d69a-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="4d69a-127">"RDS pro Gerät CAL"</span><span class="sxs-lookup"><span data-stu-id="4d69a-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="4d69a-128">"RDS pro Benutzer-CAL"</span><span class="sxs-lookup"><span data-stu-id="4d69a-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="4d69a-129">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="4d69a-129">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d69a-130">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="4d69a-130">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="4d69a-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d69a-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d69a-132">Das Ablaufdatum der Lizenz.</span><span class="sxs-lookup"><span data-stu-id="4d69a-132">The expiration date of the license.</span></span>

</dd> <dt>

<span data-ttu-id="4d69a-133">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="4d69a-133">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d69a-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4d69a-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d69a-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d69a-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d69a-136">Die Version von Remotedesktopdienste, für die die RDS-Client Zugriffslizenz pro Benutzer ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4d69a-136">The version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span> <span data-ttu-id="4d69a-137">Dabei handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="4d69a-137">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="4d69a-138">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="4d69a-138">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="4d69a-139">Nur Server, auf denen Windows Server 2012, Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4d69a-139">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="4d69a-140">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="4d69a-140">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="4d69a-141">Nur Server, auf denen Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4d69a-141">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="4d69a-142">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="4d69a-142">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="4d69a-143">Nur Server, auf denen Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4d69a-143">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d69a-144">**Productversionid**</span><span class="sxs-lookup"><span data-stu-id="4d69a-144">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d69a-145">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d69a-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d69a-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d69a-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d69a-147">Die Produkt Versions Kennung für das Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="4d69a-147">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="4d69a-148">4</span><span class="sxs-lookup"><span data-stu-id="4d69a-148">4</span></span>
</dt> <dd>

<span data-ttu-id="4d69a-149">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4d69a-149">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="4d69a-150">3</span><span class="sxs-lookup"><span data-stu-id="4d69a-150">3</span></span>
</dt> <dd>

<span data-ttu-id="4d69a-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4d69a-151">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="4d69a-152">2</span><span class="sxs-lookup"><span data-stu-id="4d69a-152">2</span></span>
</dt> <dd>

<span data-ttu-id="4d69a-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d69a-153">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="4d69a-154">1</span><span class="sxs-lookup"><span data-stu-id="4d69a-154">1</span></span>
</dt> <dd>

<span data-ttu-id="4d69a-155">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4d69a-155">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4d69a-156">0</span><span class="sxs-lookup"><span data-stu-id="4d69a-156">0</span></span>
</dt> <dd>

<span data-ttu-id="4d69a-157">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4d69a-157">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d69a-158">**shardwareid**</span><span class="sxs-lookup"><span data-stu-id="4d69a-158">**sHardwareId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d69a-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4d69a-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d69a-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d69a-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d69a-161">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4d69a-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4d69a-162">Die Hardware-ID des Computers.</span><span class="sxs-lookup"><span data-stu-id="4d69a-162">The hardware identifier of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="4d69a-163">**sissuedto Computer**</span><span class="sxs-lookup"><span data-stu-id="4d69a-163">**sIssuedToComputer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d69a-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4d69a-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d69a-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d69a-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d69a-166">Der Name des Computers, für den die Lizenz Ausstellung versucht wurde.</span><span class="sxs-lookup"><span data-stu-id="4d69a-166">The name of the computer that the license issuance was attempted for.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d69a-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d69a-167">Requirements</span></span>



| <span data-ttu-id="4d69a-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d69a-168">Requirement</span></span> | <span data-ttu-id="4d69a-169">Wert</span><span class="sxs-lookup"><span data-stu-id="4d69a-169">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d69a-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d69a-170">Minimum supported client</span></span><br/> | <span data-ttu-id="4d69a-171">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4d69a-171">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="4d69a-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4d69a-172">Minimum supported server</span></span><br/> | <span data-ttu-id="4d69a-173">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4d69a-173">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="4d69a-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="4d69a-174">Namespace</span></span><br/>                | <span data-ttu-id="4d69a-175">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="4d69a-175">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="4d69a-176">MOF</span><span class="sxs-lookup"><span data-stu-id="4d69a-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d69a-177"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4d69a-177"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d69a-178">DLL</span><span class="sxs-lookup"><span data-stu-id="4d69a-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d69a-179"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d69a-179"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d69a-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d69a-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d69a-181">**Fetchreportperdeviceentries**</span><span class="sxs-lookup"><span data-stu-id="4d69a-181">**FetchReportPerDeviceEntries**</span></span>](fetchreportperdeviceentries-win32-tslicensereport.md)
</dt> </dl>

 

