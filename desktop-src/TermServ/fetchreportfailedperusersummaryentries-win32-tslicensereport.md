---
title: Fetchreportfailedperusersummaryentries-Methode der Win32_TSLicenseReport-Klasse
description: Hiermit werden zusammenfassende Informationen zu fehlerhaften Remotedesktopdienste pro Benutzer-Client Zugriffs Lizenzen abgerufen (RDS \ 160; Pro Benutzer-CALs) aus dem Bericht.
ms.assetid: dc9c4a36-b2a8-407e-b902-ee9d51227909
ms.tgt_platform: multiple
keywords:
- Die fetchreportfailedperusersummaryentries-Methode Remotedesktopdienste
- Fetchreportfailedperusersummaryentries-Methode Remotedesktopdienste, Win32_TSLicenseReport-Klasse
- Win32_TSLicenseReport-Klasse Remotedesktopdienste, fetchreportfailedperusersummaryentries-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5219c2c854e04dabf8b5bfe0b5b70a07bbc3c57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342475"
---
# <a name="fetchreportfailedperusersummaryentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="7421a-106">Fetchreportfailedperusersummaryentries-Methode der Win32- \_ Klasse "zlicensereport"</span><span class="sxs-lookup"><span data-stu-id="7421a-106">FetchReportFailedPerUserSummaryEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="7421a-107">Hiermit werden zusammenfassende Informationen zu fehlerhaften Remotedesktopdienste pro Benutzer-Client Zugriffs Lizenzen (RDS pro Benutzer-CALs) aus dem Bericht abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7421a-107">Retrieves summary information of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="7421a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7421a-108">Syntax</span></span>


```mof
uint32 FetchReportFailedPerUserSummaryEntries(
  [in]      uint32                                         StartIndex,
  [in, out] uint32                                         Count,
  [out]     Win32_TSLicenseReportFailedPerUserSummaryEntry ReportFailedPerUserSummaryEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="7421a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7421a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7421a-110">*StartIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7421a-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7421a-111">Der Index des ersten Berichts Eintrags, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7421a-111">The index of the first report entry to be retrieved.</span></span> <span data-ttu-id="7421a-112">Der erste Berichts Eintrag weist einen Index von 0 (null) auf.</span><span class="sxs-lookup"><span data-stu-id="7421a-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="7421a-113">*Anzahl* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7421a-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7421a-114">Die Anzahl der Berichts Einträge, die aus dem Berichts Objekt abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7421a-114">The number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="7421a-115">Der Wert 0 (null) gibt an, dass alle Berichts Einträge, die bei *startIndex* beginnen, abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7421a-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="7421a-116">Enthält bei der Rückgabe die Anzahl der Einträge im *reportfailedperusersummaryentries* -Array.</span><span class="sxs-lookup"><span data-stu-id="7421a-116">On return, contains the number of entries in the *ReportFailedPerUserSummaryEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="7421a-117">*Reportfailedperusersummaryentries* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7421a-117">*ReportFailedPerUserSummaryEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7421a-118">Ein Array von Win32-Klassen vom Typ " [**\_ zlicensereportfailedperusersummaryentry**](win32-tslicensereportfailedperusersummaryentry.md) ", die die abgerufenen Lizenzeinträge darstellen.</span><span class="sxs-lookup"><span data-stu-id="7421a-118">An array of [**Win32\_TSLicenseReportFailedPerUserSummaryEntry**](win32-tslicensereportfailedperusersummaryentry.md) classes that represent the license entries retrieved.</span></span> <span data-ttu-id="7421a-119">Der *count* -Parameter enthält die Anzahl der Elemente in diesem Array.</span><span class="sxs-lookup"><span data-stu-id="7421a-119">The *Count* parameter contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7421a-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7421a-120">Return value</span></span>

<span data-ttu-id="7421a-121">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="7421a-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7421a-122">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7421a-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7421a-123">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7421a-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7421a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7421a-124">Requirements</span></span>



| <span data-ttu-id="7421a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7421a-125">Requirement</span></span> | <span data-ttu-id="7421a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="7421a-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7421a-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7421a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7421a-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7421a-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="7421a-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7421a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7421a-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7421a-130">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="7421a-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="7421a-131">Namespace</span></span><br/>                | <span data-ttu-id="7421a-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="7421a-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="7421a-133">MOF</span><span class="sxs-lookup"><span data-stu-id="7421a-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7421a-134"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7421a-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7421a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7421a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7421a-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7421a-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7421a-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7421a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7421a-138">**Win32-Datei- \_ /licensereport**</span><span class="sxs-lookup"><span data-stu-id="7421a-138">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

 





