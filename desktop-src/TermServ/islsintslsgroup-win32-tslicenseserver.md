---
title: Islsinzlsgroup-Methode der Win32_TSLicenseServer-Klasse
description: Ruft ab, ob der Remotedesktop Lizenzserver Mitglied der Remotedesktop-Lizenzserver Gruppe auf einem Domänen Controller in einer bestimmten Domäne ist.
ms.assetid: a6ad7f09-8972-47d4-8b3b-cd129b400ea8
ms.tgt_platform: multiple
keywords:
- Islsinzlsgroup-Methode Remotedesktopdienste
- Islsinzlsgroup-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, islsinzlsgroup-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSinTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de3577e4632167612b4d71841501a2a2845203a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338350"
---
# <a name="islsintslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="2b0bc-106">Islsinzlsgroup-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="2b0bc-106">IsLSinTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="2b0bc-107">Ruft ab, ob der Remotedesktop Lizenzserver Mitglied der Remotedesktop-Lizenzserver Gruppe auf einem Domänen Controller in einer bestimmten Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="2b0bc-107">Retrieves whether the Remote Desktop license server is a member of the Remote Desktop license server group on a domain controller in a given domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b0bc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b0bc-108">Syntax</span></span>


```mof
uint32 IsLSinTSLSGroup(
  [in]  string  Domain,
  [out] boolean IsMember
);
```



## <a name="parameters"></a><span data-ttu-id="2b0bc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b0bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b0bc-110">*Domäne* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b0bc-110">*Domain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b0bc-111">Der Domänenname.</span><span class="sxs-lookup"><span data-stu-id="2b0bc-111">The domain name.</span></span>

</dd> <dt>

<span data-ttu-id="2b0bc-112">*IsMember* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2b0bc-112">*IsMember* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b0bc-113">Boolescher Wert, der angibt, ob der Lizenzserver Mitglied der Remotedesktop-Lizenzserver Gruppe in der Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="2b0bc-113">Boolean value that indicates whether the license server is a member of the Remote Desktop license server group in the domain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b0bc-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b0bc-114">Return value</span></span>

<span data-ttu-id="2b0bc-115">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="2b0bc-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2b0bc-116">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2b0bc-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2b0bc-117">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2b0bc-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2b0bc-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b0bc-118">Remarks</span></span>

<span data-ttu-id="2b0bc-119">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2b0bc-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2b0bc-120">Wenn kein Domänen Name angegeben ist, wird ein Domänen Controller in derselben Domäne wie der Lizenzserver abgefragt.</span><span class="sxs-lookup"><span data-stu-id="2b0bc-120">If no domain name is provided, a domain controller in the same domain as the license server is queried.</span></span>

<span data-ttu-id="2b0bc-121">Der Lizenzserver sollte Mitglied der Gruppe Remotedesktop-Lizenzserver sein, wenn der Server für die Verwendung des Domänen-oder Gesamtstruktur-Ermittlungs Bereichs konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="2b0bc-121">The license server should be a member of the Remote Desktop license server group if the server is configured to use the domain or forest discovery scope.</span></span> <span data-ttu-id="2b0bc-122">Wenn der Lizenzserver nicht Mitglied dieser Gruppe ist, funktionieren die pro-Benutzer-Lizenz Nachverfolgung und-Berichterstellung nicht.</span><span class="sxs-lookup"><span data-stu-id="2b0bc-122">If the license server is not a member of this group, per-user license tracking and reporting will not work.</span></span>

<span data-ttu-id="2b0bc-123">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="2b0bc-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2b0bc-124">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="2b0bc-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2b0bc-125">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2b0bc-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2b0bc-126">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2b0bc-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b0bc-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b0bc-127">Requirements</span></span>



| <span data-ttu-id="2b0bc-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b0bc-128">Requirement</span></span> | <span data-ttu-id="2b0bc-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2b0bc-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b0bc-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b0bc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2b0bc-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2b0bc-131">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="2b0bc-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b0bc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2b0bc-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b0bc-133">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="2b0bc-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b0bc-134">Namespace</span></span><br/>                | <span data-ttu-id="2b0bc-135">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="2b0bc-135">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="2b0bc-136">MOF</span><span class="sxs-lookup"><span data-stu-id="2b0bc-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b0bc-137"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2b0bc-137"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b0bc-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2b0bc-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b0bc-139"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b0bc-139"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b0bc-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b0bc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b0bc-141">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="2b0bc-141">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="2b0bc-142">**Addlstozlsgroup**</span><span class="sxs-lookup"><span data-stu-id="2b0bc-142">**AddLStoTSLSGroup**</span></span>](addlstotslsgroup-win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="2b0bc-143">**Removelsfromzlsgroup**</span><span class="sxs-lookup"><span data-stu-id="2b0bc-143">**RemoveLSfromTSLSGroup**</span></span>](removelsfromtslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

