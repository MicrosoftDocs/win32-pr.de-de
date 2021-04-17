---
title: Generatereportex-Methode der Win32_TSLicenseReport-Klasse
description: Generiert einen aktuellen Lizenz Verwendungs Bericht für die Lizenzen pro Benutzer und pro Gerät.
ms.assetid: c454e0c5-ca1c-41c7-86b2-1e52c414aeb5
ms.tgt_platform: multiple
keywords:
- Generatereportex-Methode Remotedesktopdienste
- Generatereportex-Methode Remotedesktopdienste, Win32_TSLicenseReport-Klasse
- Win32_TSLicenseReport-Klasse Remotedesktopdienste, generatereportex-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReportEx
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893e6e29d1e4716560b0f0f6b41e6109c89e2f5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391611"
---
# <a name="generatereportex-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="677a1-106">Generatereportex-Methode der Win32- \_ Klasse "zlicensereport"</span><span class="sxs-lookup"><span data-stu-id="677a1-106">GenerateReportEx method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="677a1-107">Generiert einen aktuellen Lizenz Verwendungs Bericht für die Lizenzen pro Benutzer und pro Gerät.</span><span class="sxs-lookup"><span data-stu-id="677a1-107">Generates a current license usage report for both Per User and Per Device licenses.</span></span>

## <a name="syntax"></a><span data-ttu-id="677a1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="677a1-108">Syntax</span></span>


```mof
uint32 GenerateReportEx(
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="677a1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="677a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="677a1-110">*Dateiname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="677a1-110">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="677a1-111">Der Dateiname des generierten Berichts.</span><span class="sxs-lookup"><span data-stu-id="677a1-111">The file name of the generated report.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="677a1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="677a1-112">Return value</span></span>

<span data-ttu-id="677a1-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="677a1-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="677a1-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="677a1-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="677a1-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="677a1-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="677a1-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="677a1-116">Remarks</span></span>

<span data-ttu-id="677a1-117">Dies ist eine statische Methode.</span><span class="sxs-lookup"><span data-stu-id="677a1-117">This is a static method.</span></span>

<span data-ttu-id="677a1-118">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="677a1-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="677a1-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="677a1-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="677a1-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="677a1-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="677a1-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="677a1-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="677a1-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="677a1-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="677a1-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="677a1-123">Requirements</span></span>



| <span data-ttu-id="677a1-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="677a1-124">Requirement</span></span> | <span data-ttu-id="677a1-125">Wert</span><span class="sxs-lookup"><span data-stu-id="677a1-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="677a1-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="677a1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="677a1-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="677a1-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="677a1-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="677a1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="677a1-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="677a1-129">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="677a1-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="677a1-130">Namespace</span></span><br/>                | <span data-ttu-id="677a1-131">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="677a1-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="677a1-132">MOF</span><span class="sxs-lookup"><span data-stu-id="677a1-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="677a1-133"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="677a1-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="677a1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="677a1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="677a1-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="677a1-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="677a1-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="677a1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="677a1-137">**Win32-Datei- \_ /licensereport**</span><span class="sxs-lookup"><span data-stu-id="677a1-137">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

