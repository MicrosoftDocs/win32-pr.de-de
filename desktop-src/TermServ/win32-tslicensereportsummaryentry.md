---
title: Win32_TSLicenseReportSummaryEntry-Klasse
description: Bietet eine Zusammenfassung der installierten und ausgestellten Remotedesktopdienste pro-Benutzer-Client Zugriffs Lizenzen (RDS \ 160; Pro Benutzer-CALs).
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportSummaryEntry-Klasse Remotedesktopdienste
- Win32_TSLicenseReportSummaryEntry Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportSummaryEntry
- Win32_TSLicenseReportSummaryEntry.ProductVersion
- Win32_TSLicenseReportSummaryEntry.ProductVersionID
- Win32_TSLicenseReportSummaryEntry.TSCALType
- Win32_TSLicenseReportSummaryEntry.InstalledLicenses
- Win32_TSLicenseReportSummaryEntry.IssuedLicenses
- Win32_TSLicenseReportSummaryEntry.TSCALAvailability
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34482e9c6199ef6586024d43d586421a54071ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339122"
---
# <a name="win32_tslicensereportsummaryentry-class"></a><span data-ttu-id="1bec2-105">Win32-Klasse "-Klasse (Klasse)" \_</span><span class="sxs-lookup"><span data-stu-id="1bec2-105">Win32\_TSLicenseReportSummaryEntry class</span></span>

<span data-ttu-id="1bec2-106">Bietet eine Zusammenfassung der installierten und ausgestellten Remotedesktopdienste pro Benutzer-Client Zugriffs Lizenzen (RDS pro Benutzer-CALs).</span><span class="sxs-lookup"><span data-stu-id="1bec2-106">Provides a summary of the installed and issued Remote Desktop Services Per User client access licenses (RDS Per User CALs).</span></span>

## <a name="syntax"></a><span data-ttu-id="1bec2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bec2-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportSummaryEntry
{
  string ProductVersion;
  uint32 ProductVersionID;
  string TSCALType;
  uint32 InstalledLicenses;
  uint32 IssuedLicenses;
  string TSCALAvailability;
};
```

## <a name="members"></a><span data-ttu-id="1bec2-108">Member</span><span class="sxs-lookup"><span data-stu-id="1bec2-108">Members</span></span>

<span data-ttu-id="1bec2-109">Die Win32-Klasse " **\_ tylicensereportsummaryentry** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1bec2-109">The **Win32\_TSLicenseReportSummaryEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="1bec2-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1bec2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1bec2-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1bec2-111">Properties</span></span>

<span data-ttu-id="1bec2-112">Die Win32-Klasse " **\_ stilicensereportsummaryentry** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1bec2-112">The **Win32\_TSLicenseReportSummaryEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1bec2-113">**Installedlicenses**</span><span class="sxs-lookup"><span data-stu-id="1bec2-113">**InstalledLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bec2-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1bec2-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1bec2-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1bec2-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bec2-116">Anzahl der installierten RDS-pro-Benutzer-CALs.</span><span class="sxs-lookup"><span data-stu-id="1bec2-116">Number of RDS Per User CALs that are installed.</span></span>

</dd> <dt>

<span data-ttu-id="1bec2-117">**Issuedlicenses**</span><span class="sxs-lookup"><span data-stu-id="1bec2-117">**IssuedLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bec2-118">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1bec2-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1bec2-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1bec2-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bec2-120">Anzahl der ausgegebenen RDS-Client Zugriffs Lizenzen pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="1bec2-120">Number of RDS Per User CALs that are issued.</span></span>

</dd> <dt>

<span data-ttu-id="1bec2-121">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="1bec2-121">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bec2-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1bec2-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bec2-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1bec2-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bec2-124">Die Version von Remotedesktopdienste, für die die RDS-Client Zugriffslizenz pro Benutzer ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1bec2-124">Version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span>

<dt>

<span data-ttu-id="1bec2-125">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="1bec2-125">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="1bec2-126">Nur Server, auf denen Windows Server 2012, Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1bec2-126">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="1bec2-127">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="1bec2-127">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="1bec2-128">Nur Server, auf denen Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1bec2-128">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="1bec2-129">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="1bec2-129">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="1bec2-130">Nur Server, auf denen Windows Server 2008 ausgeführt wird, werden mit dieser Lizenz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1bec2-130">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1bec2-131">**Productversionid**</span><span class="sxs-lookup"><span data-stu-id="1bec2-131">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bec2-132">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1bec2-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1bec2-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1bec2-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bec2-134">Die Produkt Versions Kennung für das Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="1bec2-134">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="1bec2-135">4</span><span class="sxs-lookup"><span data-stu-id="1bec2-135">4</span></span>
</dt> <dd>

<span data-ttu-id="1bec2-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1bec2-136">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="1bec2-137">3</span><span class="sxs-lookup"><span data-stu-id="1bec2-137">3</span></span>
</dt> <dd>

<span data-ttu-id="1bec2-138">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1bec2-138">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="1bec2-139">2</span><span class="sxs-lookup"><span data-stu-id="1bec2-139">2</span></span>
</dt> <dd>

<span data-ttu-id="1bec2-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1bec2-140">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="1bec2-141">1</span><span class="sxs-lookup"><span data-stu-id="1bec2-141">1</span></span>
</dt> <dd>

<span data-ttu-id="1bec2-142">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1bec2-142">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="1bec2-143">0</span><span class="sxs-lookup"><span data-stu-id="1bec2-143">0</span></span>
</dt> <dd>

<span data-ttu-id="1bec2-144">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1bec2-144">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1bec2-145">**Tscalavailability**</span><span class="sxs-lookup"><span data-stu-id="1bec2-145">**TSCALAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bec2-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1bec2-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bec2-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1bec2-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bec2-148">Die Verfügbarkeit der RDS pro Benutzer-CALs.</span><span class="sxs-lookup"><span data-stu-id="1bec2-148">The availability of the RDS Per User CALs.</span></span> <span data-ttu-id="1bec2-149">Dabei handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="1bec2-149">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="1bec2-150">Frei</span><span class="sxs-lookup"><span data-stu-id="1bec2-150">"Available"</span></span>
</dt> <dd>

<span data-ttu-id="1bec2-151">Die RDS-Client Zugriffs Lizenzen pro Benutzer sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1bec2-151">The RDS Per User CALs are available.</span></span>

</dd> <dt>

<span data-ttu-id="1bec2-152">GmbH</span><span class="sxs-lookup"><span data-stu-id="1bec2-152">"Limited"</span></span>
</dt> <dd>

<span data-ttu-id="1bec2-153">Die Verfügbarkeit der RDS pro Benutzer-CALs ist beschränkt.</span><span class="sxs-lookup"><span data-stu-id="1bec2-153">The availability of the RDS Per User CALs is limited.</span></span>

</dd> <dt>

<span data-ttu-id="1bec2-154">"None"</span><span class="sxs-lookup"><span data-stu-id="1bec2-154">"None"</span></span>
</dt> <dd>

<span data-ttu-id="1bec2-155">Die RDS pro Benutzer-CALs sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1bec2-155">The RDS Per User CALs are not available.</span></span>

</dd> <dt>

<span data-ttu-id="1bec2-156">"Nicht nachverfolgt"</span><span class="sxs-lookup"><span data-stu-id="1bec2-156">"Not Tracking"</span></span>
</dt> <dd>

<span data-ttu-id="1bec2-157">Die Verfügbarkeit der RDS-Client Zugriffs Lizenzen pro Benutzer wird nicht nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="1bec2-157">The availability of the RDS Per User CALs is not being tracked.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1bec2-158">**Tscaltype**</span><span class="sxs-lookup"><span data-stu-id="1bec2-158">**TSCALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bec2-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1bec2-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bec2-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1bec2-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bec2-161">Der Typ der RDS pro Benutzer-CALs.</span><span class="sxs-lookup"><span data-stu-id="1bec2-161">The type of RDS Per User CALs.</span></span> <span data-ttu-id="1bec2-162">Dabei handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="1bec2-162">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="1bec2-163">"Pro Gerät"</span><span class="sxs-lookup"><span data-stu-id="1bec2-163">"Per Device"</span></span>
</dt> <dd>

<span data-ttu-id="1bec2-164">Die RDS-Client Zugriffs Lizenzen pro Benutzer werden pro Gerät ausgestellt.</span><span class="sxs-lookup"><span data-stu-id="1bec2-164">The RDS Per User CALs are issued per device.</span></span>

</dd> <dt>

<span data-ttu-id="1bec2-165">"Pro Benutzer"</span><span class="sxs-lookup"><span data-stu-id="1bec2-165">"Per User"</span></span>
</dt> <dd>

<span data-ttu-id="1bec2-166">Die RDS-Client Zugriffs Lizenzen pro Benutzer werden pro Benutzer ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="1bec2-166">The RDS Per User CALs are issued per user.</span></span>

</dd> <dt>

<span data-ttu-id="1bec2-167">Unbekannter</span><span class="sxs-lookup"><span data-stu-id="1bec2-167">"Unknown"</span></span>
</dt> <dd>

<span data-ttu-id="1bec2-168">Der Typ der RDS pro Benutzer-CALs ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="1bec2-168">The type of RDS Per User CALs is unknown.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1bec2-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1bec2-169">Requirements</span></span>



| <span data-ttu-id="1bec2-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1bec2-170">Requirement</span></span> | <span data-ttu-id="1bec2-171">Wert</span><span class="sxs-lookup"><span data-stu-id="1bec2-171">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bec2-172">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1bec2-172">Minimum supported client</span></span><br/> | <span data-ttu-id="1bec2-173">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1bec2-173">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="1bec2-174">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1bec2-174">Minimum supported server</span></span><br/> | <span data-ttu-id="1bec2-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1bec2-175">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="1bec2-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="1bec2-176">Namespace</span></span><br/>                | <span data-ttu-id="1bec2-177">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="1bec2-177">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="1bec2-178">MOF</span><span class="sxs-lookup"><span data-stu-id="1bec2-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1bec2-179"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1bec2-179"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1bec2-180">DLL</span><span class="sxs-lookup"><span data-stu-id="1bec2-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bec2-181"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bec2-181"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



 

 





