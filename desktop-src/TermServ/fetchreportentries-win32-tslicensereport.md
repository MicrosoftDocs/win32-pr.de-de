---
title: Fetchreportentries-Methode der Win32_TSLicenseReport-Klasse
description: Ruft Details zu Remotedesktopdienste Client Zugriffs Lizenzen pro Benutzer (RDS \ 160;) ab. Pro Benutzer-CALs) aus dem Bericht. Jeder Eintrag stellt einen RDS \ 160; dar. Pro Benutzer-CAL, die zurzeit verwendet wird.
ms.assetid: 151ff95c-4ad3-4d19-936d-1cb08b4d5056
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der fetchreportentries-Methode
- Fetchreportentries-Methode Remotedesktopdienste, Win32_TSLicenseReport-Klasse
- Win32_TSLicenseReport-Klasse Remotedesktopdienste, fetchreportentries-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc64c9591444307ba0519da02cf9c6f13d20252e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518848"
---
# <a name="fetchreportentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="81018-107">Fetchreportentries-Methode der Win32- \_ Klasse "zlicensereport"</span><span class="sxs-lookup"><span data-stu-id="81018-107">FetchReportEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="81018-108">Ruft Details zu Remotedesktopdienste Client Zugriffs Lizenzen pro Benutzer (RDS pro Benutzer-CALs) aus dem Bericht ab.</span><span class="sxs-lookup"><span data-stu-id="81018-108">Retrieves details of Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span> <span data-ttu-id="81018-109">Jeder Eintrag stellt eine RDS pro Benutzer-CAL dar, die zurzeit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="81018-109">Each entry represents a RDS Per User CAL that is currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="81018-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="81018-110">Syntax</span></span>


```mof
uint32 FetchReportEntries(
  [in]      uint32                     StartIndex,
  [in, out] uint32                     Count,
  [out]     Win32_TSLicenseReportEntry ReportEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="81018-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="81018-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81018-112">*StartIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81018-112">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81018-113">Der Index des ersten Berichts Eintrags, der empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="81018-113">Index of the first report entry to be received.</span></span> <span data-ttu-id="81018-114">Der erste Berichts Eintrag weist einen Index von 0 (null) auf.</span><span class="sxs-lookup"><span data-stu-id="81018-114">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="81018-115">*Anzahl* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="81018-115">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="81018-116">Anzahl der Berichts Einträge, die aus dem Berichts Objekt abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="81018-116">Number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="81018-117">Der Wert 0 (null) gibt an, dass alle Berichts Einträge, die bei *startIndex* beginnen, abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="81018-117">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="81018-118">Enthält bei der Rückgabe die Anzahl der Einträge im *Report Entries* -Array.</span><span class="sxs-lookup"><span data-stu-id="81018-118">On return, contains the number of entries in the *ReportEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="81018-119">*Report Entries* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="81018-119">*ReportEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81018-120">Gibt ein Array von Win32-Klassen vom Typ " [**\_ tlicensereportentry**](win32-tslicensereportentry.md) " zurück.</span><span class="sxs-lookup"><span data-stu-id="81018-120">Returns an array of [**Win32\_TSLicenseReportEntry**](win32-tslicensereportentry.md) classes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81018-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81018-121">Return value</span></span>

<span data-ttu-id="81018-122">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="81018-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="81018-123">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="81018-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="81018-124">Der Wert **lserver \_ I \_ No \_ \_ Data** (0x4001) gibt an, dass keine weiteren Berichts Einträge vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="81018-124">A value of **LSERVER\_I\_NO\_MORE\_DATA** (0x4001) indicates that there are no more report entries.</span></span>

## <a name="remarks"></a><span data-ttu-id="81018-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81018-125">Remarks</span></span>

<span data-ttu-id="81018-126">Dabei handelt es sich nicht um eine statische Methode.</span><span class="sxs-lookup"><span data-stu-id="81018-126">This is not a static method.</span></span> <span data-ttu-id="81018-127">Diese Methode muss von einem Bericht Objekt pro Benutzer-Lizenz Verwendung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="81018-127">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="81018-128">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="81018-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="81018-129">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="81018-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="81018-130">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="81018-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="81018-131">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="81018-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="81018-132">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="81018-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="81018-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81018-133">Requirements</span></span>



| <span data-ttu-id="81018-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81018-134">Requirement</span></span> | <span data-ttu-id="81018-135">Wert</span><span class="sxs-lookup"><span data-stu-id="81018-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="81018-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81018-136">Minimum supported client</span></span><br/> | <span data-ttu-id="81018-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="81018-137">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="81018-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81018-138">Minimum supported server</span></span><br/> | <span data-ttu-id="81018-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81018-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="81018-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="81018-140">Namespace</span></span><br/>                | <span data-ttu-id="81018-141">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="81018-141">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="81018-142">MOF</span><span class="sxs-lookup"><span data-stu-id="81018-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81018-143"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="81018-143"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="81018-144">DLL</span><span class="sxs-lookup"><span data-stu-id="81018-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81018-145"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81018-145"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81018-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81018-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81018-147">**Win32-Datei- \_ /licensereport**</span><span class="sxs-lookup"><span data-stu-id="81018-147">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="81018-148">**Win32-Wert für "- \_ Lizenzserver"**</span><span class="sxs-lookup"><span data-stu-id="81018-148">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> </dl>

 

