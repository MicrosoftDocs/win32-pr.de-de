---
title: GenerateReport-Methode der Win32_TSLicenseReport-Klasse (GPMgmt. h)
description: GenerateReport ist nicht mehr für die Verwendung ab Windows Server 2012 verfügbar.
ms.assetid: 2d3b16d6-52e8-491f-b6e5-419e9a21013b
ms.tgt_platform: multiple
keywords:
- GenerateReport-Methode Remotedesktopdienste
- GenerateReport-Methode Remotedesktopdienste, Win32_TSLicenseReport-Klasse
- Win32_TSLicenseReport-Klasse Remotedesktopdienste, GenerateReport-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5231c87d379decac8d4f6491042bff735c1ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392079"
---
# <a name="generatereport-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="175dd-106">GenerateReport-Methode der Win32- \_ Klasse "zlicensereport"</span><span class="sxs-lookup"><span data-stu-id="175dd-106">GenerateReport method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="175dd-107">\[**GenerateReport** ist nicht mehr für die Verwendung ab Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="175dd-107">\[**GenerateReport** is no longer available for use as of Windows Server 2012.</span></span> <span data-ttu-id="175dd-108">Verwenden Sie stattdessen [**generatereportex**](generatereportex-win32-tslicensereport.md).\]</span><span class="sxs-lookup"><span data-stu-id="175dd-108">Instead, use [**GenerateReportEx**](generatereportex-win32-tslicensereport.md).\]</span></span>

<span data-ttu-id="175dd-109">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="175dd-109">This method is not supported.</span></span>

<span data-ttu-id="175dd-110">**Windows Server 2008 R2 und Windows Server 2008:** Generiert einen aktuellen Bericht pro Benutzer-Lizenz Verwendung auf dem Remotedesktop-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="175dd-110">**Windows Server 2008 R2 and Windows Server 2008:** Generates a current per user license usage report on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="175dd-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="175dd-111">Syntax</span></span>


```mof
uint32 GenerateReport(
  [in]  uint32 ScopeType,
  [in]  string ScopeValue,
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="175dd-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="175dd-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="175dd-113">*ScopeType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="175dd-113">*ScopeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="175dd-114">Bereich des Lizenz Verwendungs Berichts.</span><span class="sxs-lookup"><span data-stu-id="175dd-114">Scope of the license usage report.</span></span> <span data-ttu-id="175dd-115">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="175dd-115">It can have the following values.</span></span>

<dt>

<span data-ttu-id="175dd-116">1</span><span class="sxs-lookup"><span data-stu-id="175dd-116">1</span></span>
</dt> <dd>

<span data-ttu-id="175dd-117">Der Bericht wird für die gesamte Domäne generiert.</span><span class="sxs-lookup"><span data-stu-id="175dd-117">The report will be generated for the entire domain.</span></span>

</dd> <dt>

<span data-ttu-id="175dd-118">2</span><span class="sxs-lookup"><span data-stu-id="175dd-118">2</span></span>
</dt> <dd>

<span data-ttu-id="175dd-119">Der Bericht wird für die Organisationseinheit (OU) generiert, die im Parameter " *scopevalue* " angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="175dd-119">The report will be generated for the organizational unit (OU) that is specified in the *ScopeValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="175dd-120">3</span><span class="sxs-lookup"><span data-stu-id="175dd-120">3</span></span>
</dt> <dd>

<span data-ttu-id="175dd-121">Der Bericht wird für alle vertrauenswürdigen Domänen generiert.</span><span class="sxs-lookup"><span data-stu-id="175dd-121">The report will be generated for all trusted domains.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="175dd-122"> Bereich \[ in\]</span><span class="sxs-lookup"><span data-stu-id="175dd-122">*ScopeValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="175dd-123">Wenn der *ScopeType* -Parameter 2 ist, gibt *ScopeType* die Organisationseinheit an, für die der Bericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="175dd-123">If the *ScopeType* parameter is 2, *ScopeType* specifies the OU for which the report will be generated.</span></span> <span data-ttu-id="175dd-124">Sie müssen *scopevalue* mit dem Format **OU =**_OUName1_*_, ou =_*_OUName2_*_._*.. angeben.</span><span class="sxs-lookup"><span data-stu-id="175dd-124">You must specify *ScopeValue* by using the format **OU=**_OUName1_*_,OU=_*_OUName2_*_..._*.</span></span>

</dd> <dt>

<span data-ttu-id="175dd-125">*Dateiname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="175dd-125">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="175dd-126">Der Dateiname des generierten Berichts.</span><span class="sxs-lookup"><span data-stu-id="175dd-126">The file name of the generated report.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="175dd-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="175dd-127">Return value</span></span>

<span data-ttu-id="175dd-128">Gibt **WBEM \_ E \_ nicht \_ unterstützt** zurück.</span><span class="sxs-lookup"><span data-stu-id="175dd-128">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="175dd-129">**Windows Server 2008 R2 und Windows Server 2008:** Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="175dd-129">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="175dd-130">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="175dd-130">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="175dd-131">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="175dd-131">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="175dd-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="175dd-132">Remarks</span></span>

<span data-ttu-id="175dd-133">Dies ist eine statische Methode.</span><span class="sxs-lookup"><span data-stu-id="175dd-133">This is a static method.</span></span>

<span data-ttu-id="175dd-134">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="175dd-134">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="175dd-135">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="175dd-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="175dd-136">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="175dd-136">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="175dd-137">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="175dd-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="175dd-138">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="175dd-138">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="175dd-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="175dd-139">Requirements</span></span>



| <span data-ttu-id="175dd-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="175dd-140">Requirement</span></span> | <span data-ttu-id="175dd-141">Wert</span><span class="sxs-lookup"><span data-stu-id="175dd-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="175dd-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="175dd-142">Minimum supported client</span></span><br/> | <span data-ttu-id="175dd-143">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="175dd-143">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="175dd-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="175dd-144">Minimum supported server</span></span><br/> | <span data-ttu-id="175dd-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="175dd-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="175dd-146">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="175dd-146">End of client support</span></span><br/>    | <span data-ttu-id="175dd-147">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="175dd-147">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="175dd-148">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="175dd-148">End of server support</span></span><br/>    | <span data-ttu-id="175dd-149">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="175dd-149">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="175dd-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="175dd-150">Namespace</span></span><br/>                | <span data-ttu-id="175dd-151">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="175dd-151">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="175dd-152">Header</span><span class="sxs-lookup"><span data-stu-id="175dd-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="175dd-153"><dt>GPMgmt. h</dt></span><span class="sxs-lookup"><span data-stu-id="175dd-153"><dt>Gpmgmt.h</dt></span></span> </dl>       |
| <span data-ttu-id="175dd-154">MOF</span><span class="sxs-lookup"><span data-stu-id="175dd-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="175dd-155"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="175dd-155"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="175dd-156">DLL</span><span class="sxs-lookup"><span data-stu-id="175dd-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="175dd-157"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="175dd-157"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="175dd-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="175dd-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="175dd-159">**Win32-Datei- \_ /licensereport**</span><span class="sxs-lookup"><span data-stu-id="175dd-159">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

