---
title: Deletereport-Methode der Win32_TSLicenseReport-Klasse
description: Löscht ein Berichts Objekt auf dem Remotedesktop-Lizenzserver. Dabei handelt es sich nicht um eine statische Methode.
ms.assetid: cc70526c-7ce5-4d55-b72e-8a5e8799b1d8
ms.tgt_platform: multiple
keywords:
- Deletereport-Methode Remotedesktopdienste
- Deletereport-Methode Remotedesktopdienste, Win32_TSLicenseReport-Klasse
- Win32_TSLicenseReport-Klasse Remotedesktopdienste, deletereport-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.DeleteReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a96c8626e4ecc1f89d0f2fcefa69845fec4df8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517450"
---
# <a name="deletereport-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="661d5-107">Deletereport-Methode der Win32- \_ Klasse "zlicensereport"</span><span class="sxs-lookup"><span data-stu-id="661d5-107">DeleteReport method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="661d5-108">Löscht ein Berichts Objekt auf dem Remotedesktop-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="661d5-108">Deletes a report object on the Remote Desktop license server.</span></span> <span data-ttu-id="661d5-109">Dabei handelt es sich nicht um eine statische Methode.</span><span class="sxs-lookup"><span data-stu-id="661d5-109">This is not a static method.</span></span>

## <a name="syntax"></a><span data-ttu-id="661d5-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="661d5-110">Syntax</span></span>


```mof
uint32 DeleteReport();
```



## <a name="parameters"></a><span data-ttu-id="661d5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="661d5-111">Parameters</span></span>

<span data-ttu-id="661d5-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="661d5-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="661d5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="661d5-113">Return value</span></span>

<span data-ttu-id="661d5-114">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="661d5-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="661d5-115">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="661d5-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="661d5-116">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="661d5-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="661d5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="661d5-117">Remarks</span></span>

<span data-ttu-id="661d5-118">Dabei handelt es sich nicht um eine statische Methode.</span><span class="sxs-lookup"><span data-stu-id="661d5-118">This is not a static method.</span></span> <span data-ttu-id="661d5-119">Diese Methode muss von einem Bericht Objekt pro Benutzer-Lizenz Verwendung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="661d5-119">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="661d5-120">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="661d5-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="661d5-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="661d5-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="661d5-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="661d5-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="661d5-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="661d5-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="661d5-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="661d5-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="661d5-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="661d5-125">Requirements</span></span>



| <span data-ttu-id="661d5-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="661d5-126">Requirement</span></span> | <span data-ttu-id="661d5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="661d5-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="661d5-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="661d5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="661d5-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="661d5-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="661d5-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="661d5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="661d5-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="661d5-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="661d5-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="661d5-132">Namespace</span></span><br/>                | <span data-ttu-id="661d5-133">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="661d5-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="661d5-134">MOF</span><span class="sxs-lookup"><span data-stu-id="661d5-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="661d5-135"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="661d5-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="661d5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="661d5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="661d5-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="661d5-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="661d5-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="661d5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="661d5-139">**Win32-Datei- \_ /licensereport**</span><span class="sxs-lookup"><span data-stu-id="661d5-139">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

