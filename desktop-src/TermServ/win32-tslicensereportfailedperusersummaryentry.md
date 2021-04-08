---
title: Win32_TSLicenseReportFailedPerUserSummaryEntry-Klasse
description: Gibt Details zu den Domänen an, für die pro Benutzer eine Ausstellung fehlgeschlagen ist.
ms.assetid: f7265734-ac4d-439f-ae8b-3694e6f81f2a
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportFailedPerUserSummaryEntry-Klasse Remotedesktopdienste
- Win32_TSLicenseReportFailedPerUserSummaryEntry Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserSummaryEntry
- Win32_TSLicenseReportFailedPerUserSummaryEntry.DomainName
- Win32_TSLicenseReportFailedPerUserSummaryEntry.FailedIssuanceCount
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f086d275c064f5df18ee01a3a38639a40913f3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949477"
---
# <a name="win32_tslicensereportfailedperusersummaryentry-class"></a><span data-ttu-id="b001b-105">Win32- \_ Klasse "slicensereportfailedperusersummaryentry"</span><span class="sxs-lookup"><span data-stu-id="b001b-105">Win32\_TSLicenseReportFailedPerUserSummaryEntry class</span></span>

<span data-ttu-id="b001b-106">Gibt Details zu den Domänen an, für die pro Benutzer eine Ausstellung fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="b001b-106">Provides details of the domains to which Per User Issuance was failed.</span></span>

<span data-ttu-id="b001b-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b001b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b001b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b001b-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserSummaryEntry
{
  string DomainName;
  uint32 FailedIssuanceCount;
};
```

## <a name="members"></a><span data-ttu-id="b001b-109">Member</span><span class="sxs-lookup"><span data-stu-id="b001b-109">Members</span></span>

<span data-ttu-id="b001b-110">Die Win32-Klasse " **\_ zlicensereportfailedperusersummaryentry** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b001b-110">The **Win32\_TSLicenseReportFailedPerUserSummaryEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="b001b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b001b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b001b-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b001b-112">Properties</span></span>

<span data-ttu-id="b001b-113">Die Win32-Klasse " **\_ slicensereportfailedperusersummaryentry** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b001b-113">The **Win32\_TSLicenseReportFailedPerUserSummaryEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b001b-114">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="b001b-114">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b001b-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b001b-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b001b-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b001b-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b001b-117">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b001b-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b001b-118">Gibt den Domänen Namen an, für den die Lizenz Ausstellung fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="b001b-118">Specifies the domain name to which the license issuance failed.</span></span>

</dd> <dt>

<span data-ttu-id="b001b-119">**Faileabschreck-Anzahl**</span><span class="sxs-lookup"><span data-stu-id="b001b-119">**FailedIssuanceCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b001b-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b001b-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b001b-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b001b-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b001b-122">Die Anzahl der fehlgeschlagenen issuances.</span><span class="sxs-lookup"><span data-stu-id="b001b-122">The number of failed issuances.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b001b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b001b-123">Requirements</span></span>



| <span data-ttu-id="b001b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b001b-124">Requirement</span></span> | <span data-ttu-id="b001b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b001b-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b001b-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b001b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b001b-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b001b-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="b001b-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b001b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b001b-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b001b-129">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="b001b-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="b001b-130">Namespace</span></span><br/>                | <span data-ttu-id="b001b-131">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b001b-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="b001b-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b001b-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b001b-133"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b001b-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b001b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b001b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b001b-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b001b-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b001b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b001b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b001b-137">**Fetchreportfailedperusersummaryentries**</span><span class="sxs-lookup"><span data-stu-id="b001b-137">**FetchReportFailedPerUserSummaryEntries**</span></span>](fetchreportfailedperusersummaryentries-win32-tslicensereport.md)
</dt> </dl>

 

