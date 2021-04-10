---
title: Fetchreportsummaryentries-Methode der Win32_TSLicenseReport-Klasse
description: Hiermit werden Zusammenfassungen von Remotedesktopdienste Client Zugriffs Lizenzen pro Benutzer abgerufen (RDS \ 160; Pro Benutzer-CALs) aus dem Bericht.
ms.assetid: 0312B787-83E9-42FC-B21B-904B804C5C94
ms.tgt_platform: multiple
keywords:
- Die fetchreportsummaryentries-Methode Remotedesktopdienste
- Fetchreportsummaryentries-Methode Remotedesktopdienste, Win32_TSLicenseReport-Klasse
- Win32_TSLicenseReport-Klasse Remotedesktopdienste, fetchreportsummaryentries-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e47100c71e195cacb6a1004975955eae778765a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103010"
---
# <a name="fetchreportsummaryentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="1fd79-106">Fetchreportsummaryentries-Methode der Win32- \_ Klasse "zlicensereport"</span><span class="sxs-lookup"><span data-stu-id="1fd79-106">FetchReportSummaryEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="1fd79-107">Ruft Zusammenfassungen von Remotedesktopdienste Client Zugriffs Lizenzen pro Benutzer (RDS pro Benutzer-CALs) aus dem Bericht ab.</span><span class="sxs-lookup"><span data-stu-id="1fd79-107">Retrieves summaries of Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fd79-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fd79-108">Syntax</span></span>


```mof
uint32 FetchReportSummaryEntries(
  [in]      uint32                            StartIndex,
  [in, out] uint32                            Count,
  [out]     Win32_TSLicenseReportSummaryEntry ReportSummaryEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="1fd79-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fd79-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fd79-110">*StartIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1fd79-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fd79-111">Der Index des ersten Berichts Eintrags, der empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1fd79-111">Index of the first report entry to be received.</span></span> <span data-ttu-id="1fd79-112">Der erste Berichts Eintrag weist einen Index von 0 (null) auf.</span><span class="sxs-lookup"><span data-stu-id="1fd79-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="1fd79-113">*Anzahl* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1fd79-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fd79-114">Anzahl der Berichts Einträge, die aus dem Berichts Objekt abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1fd79-114">Number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="1fd79-115">Der Wert 0 (null) gibt an, dass alle Berichts Einträge, die bei *startIndex* beginnen, abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1fd79-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="1fd79-116">Enthält bei der Rückgabe die Anzahl der Einträge im *reportsummaryentries* -Array.</span><span class="sxs-lookup"><span data-stu-id="1fd79-116">On return, contains the number of entries in the *ReportSummaryEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="1fd79-117">*Reportsummaryentries* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1fd79-117">*ReportSummaryEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fd79-118">Gibt ein Array von Win32-Klassen vom Typ " [**\_ tlicensereportsummaryentry**](win32-tslicensereportsummaryentry.md) " zurück.</span><span class="sxs-lookup"><span data-stu-id="1fd79-118">Returns an array of [**Win32\_TSLicenseReportSummaryEntry**](win32-tslicensereportsummaryentry.md) classes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fd79-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1fd79-119">Return value</span></span>

<span data-ttu-id="1fd79-120">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="1fd79-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1fd79-121">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1fd79-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1fd79-122">Der Wert **lserver \_ I \_ No \_ \_ Data** (0x4001) gibt an, dass keine weiteren Berichts Einträge vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="1fd79-122">A value of **LSERVER\_I\_NO\_MORE\_DATA** (0x4001) indicates that there are no more report entries.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fd79-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1fd79-123">Remarks</span></span>

<span data-ttu-id="1fd79-124">Dabei handelt es sich nicht um eine statische Methode.</span><span class="sxs-lookup"><span data-stu-id="1fd79-124">This is not a static method.</span></span> <span data-ttu-id="1fd79-125">Diese Methode muss von einem Bericht Objekt pro Benutzer-Lizenz Verwendung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1fd79-125">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="1fd79-126">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1fd79-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1fd79-127">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="1fd79-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1fd79-128">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="1fd79-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1fd79-129">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1fd79-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1fd79-130">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1fd79-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fd79-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1fd79-131">Requirements</span></span>



| <span data-ttu-id="1fd79-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1fd79-132">Requirement</span></span> | <span data-ttu-id="1fd79-133">Wert</span><span class="sxs-lookup"><span data-stu-id="1fd79-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fd79-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1fd79-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1fd79-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1fd79-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="1fd79-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1fd79-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1fd79-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fd79-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="1fd79-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="1fd79-138">Namespace</span></span><br/>                | <span data-ttu-id="1fd79-139">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="1fd79-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="1fd79-140">MOF</span><span class="sxs-lookup"><span data-stu-id="1fd79-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fd79-141"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1fd79-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fd79-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1fd79-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fd79-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fd79-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fd79-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fd79-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fd79-145">**Win32-Datei- \_ /licensereport**</span><span class="sxs-lookup"><span data-stu-id="1fd79-145">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="1fd79-146">**Win32-Datei Eintrag ("-Name)" \_**</span><span class="sxs-lookup"><span data-stu-id="1fd79-146">**Win32\_TSLicenseReportSummaryEntry**</span></span>](win32-tslicensereportsummaryentry.md)
</dt> </dl>

 

