---
title: Fetchreportfailedperuserentries-Methode der Win32_TSLicenseReport-Klasse
description: Hiermit werden Details zu fehlerhaften Remotedesktopdienste pro Benutzer-Client Zugriffs Lizenzen abgerufen (RDS \ 160; Pro Benutzer-CALs) aus dem Bericht.
ms.assetid: 2c16723c-1755-4ec1-a6db-55d769f8b6fd
ms.tgt_platform: multiple
keywords:
- Die fetchreportfailedperuserentries-Methode Remotedesktopdienste
- Fetchreportfailedperuserentries-Methode Remotedesktopdienste, Win32_TSLicenseReport-Klasse
- Win32_TSLicenseReport-Klasse Remotedesktopdienste, fetchreportfailedperuserentries-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 159f980944c70dbad4c6948a614d0c9964a5f0cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518845"
---
# <a name="fetchreportfailedperuserentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="13e3b-106">Fetchreportfailedperuserentries-Methode der Win32- \_ Klasse "zlicensereport"</span><span class="sxs-lookup"><span data-stu-id="13e3b-106">FetchReportFailedPerUserEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="13e3b-107">Ruft Details der fehlerhaften Remotedesktopdienste pro Benutzer-Client Zugriffs Lizenzen (RDS pro Benutzer-CALs) aus dem Bericht ab.</span><span class="sxs-lookup"><span data-stu-id="13e3b-107">Retrieves details of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="13e3b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="13e3b-108">Syntax</span></span>


```mof
uint32 FetchReportFailedPerUserEntries(
  [in]      uint32                                  StartIndex,
  [in, out] uint32                                  Count,
  [out]     Win32_TSLicenseReportFailedPerUserEntry ReportFailedPerUserEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="13e3b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="13e3b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13e3b-110">*StartIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13e3b-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13e3b-111">Der Index des ersten Berichts Eintrags, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="13e3b-111">The index of the first report entry to be retrieved.</span></span> <span data-ttu-id="13e3b-112">Der erste Berichts Eintrag weist einen Index von 0 (null) auf.</span><span class="sxs-lookup"><span data-stu-id="13e3b-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="13e3b-113">*Anzahl* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="13e3b-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="13e3b-114">Die Anzahl der Berichts Einträge, die aus dem Berichts Objekt abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="13e3b-114">The number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="13e3b-115">Der Wert 0 (null) gibt an, dass alle Berichts Einträge, die bei *startIndex* beginnen, abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="13e3b-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="13e3b-116">Enthält bei der Rückgabe die Anzahl der Einträge im *reportfailedperuserentries* -Array.</span><span class="sxs-lookup"><span data-stu-id="13e3b-116">On return, contains the number of entries in the *ReportFailedPerUserEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="13e3b-117">*Reportfailedperuserentries* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13e3b-117">*ReportFailedPerUserEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13e3b-118">Ein Array von Win32-Klassen vom Typ " [**\_ zlicensereportfailedperuserentry**](win32-tslicensereportfailedperuserentry.md) ", die die abgerufenen Lizenzeinträge darstellen.</span><span class="sxs-lookup"><span data-stu-id="13e3b-118">An array of [**Win32\_TSLicenseReportFailedPerUserEntry**](win32-tslicensereportfailedperuserentry.md) classes that represent the license entries retrieved.</span></span> <span data-ttu-id="13e3b-119">Der *count* -Parameter enthält die Anzahl der Elemente in diesem Array.</span><span class="sxs-lookup"><span data-stu-id="13e3b-119">The *Count* parameter contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13e3b-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13e3b-120">Return value</span></span>

<span data-ttu-id="13e3b-121">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="13e3b-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="13e3b-122">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13e3b-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="13e3b-123">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="13e3b-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13e3b-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13e3b-124">Requirements</span></span>



| <span data-ttu-id="13e3b-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13e3b-125">Requirement</span></span> | <span data-ttu-id="13e3b-126">Wert</span><span class="sxs-lookup"><span data-stu-id="13e3b-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="13e3b-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13e3b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="13e3b-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="13e3b-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="13e3b-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13e3b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="13e3b-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13e3b-130">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="13e3b-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="13e3b-131">Namespace</span></span><br/>                | <span data-ttu-id="13e3b-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="13e3b-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="13e3b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="13e3b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13e3b-134"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="13e3b-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="13e3b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="13e3b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13e3b-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13e3b-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13e3b-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13e3b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13e3b-138">**Win32-Datei- \_ /licensereport**</span><span class="sxs-lookup"><span data-stu-id="13e3b-138">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

 





