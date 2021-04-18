---
title: Removetscgroup-Methode der Win32_TSLicenseServer-Klasse
description: Removetscgroup ist nicht mehr für die Verwendung ab Windows Server 2012 verfügbar.
ms.assetid: e5e3eca9-4990-4322-b41d-c6b6b3356272
ms.tgt_platform: multiple
keywords:
- Removetscgroup-Methode Remotedesktopdienste
- Removetscgroup-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, removetscgroup-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RemoveTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26ca693e7e98ca811ce52292fb26622b7f2174cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518995"
---
# <a name="removetscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="17741-106">Removetscgroup-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="17741-106">RemoveTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="17741-107">\[**Removetscgroup** ist nicht mehr für die Verwendung ab Windows Server 2012 verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="17741-107">\[**RemoveTSCGroup** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="17741-108">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="17741-108">This method is not supported.</span></span>

<span data-ttu-id="17741-109">**Windows Server 2008 R2 und Windows Server 2008:** Entfernt die lokale Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenz Server.</span><span class="sxs-lookup"><span data-stu-id="17741-109">**Windows Server 2008 R2 and Windows Server 2008:** Removes the Terminal Server Computers local group from the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="17741-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="17741-110">Syntax</span></span>


```mof
uint32 RemoveTSCGroup();
```



## <a name="parameters"></a><span data-ttu-id="17741-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="17741-111">Parameters</span></span>

<span data-ttu-id="17741-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="17741-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17741-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17741-113">Return value</span></span>

<span data-ttu-id="17741-114">Gibt **WBEM \_ E \_ nicht \_ unterstützt** zurück.</span><span class="sxs-lookup"><span data-stu-id="17741-114">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="17741-115">**Windows Server 2008 R2 und Windows Server 2008:** Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="17741-115">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="17741-116">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="17741-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="17741-117">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="17741-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="17741-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17741-118">Remarks</span></span>

<span data-ttu-id="17741-119">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="17741-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="17741-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="17741-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="17741-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="17741-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="17741-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="17741-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="17741-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="17741-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="17741-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17741-124">Requirements</span></span>



| <span data-ttu-id="17741-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17741-125">Requirement</span></span> | <span data-ttu-id="17741-126">Wert</span><span class="sxs-lookup"><span data-stu-id="17741-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="17741-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17741-127">Minimum supported client</span></span><br/> | <span data-ttu-id="17741-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="17741-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="17741-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17741-129">Minimum supported server</span></span><br/> | <span data-ttu-id="17741-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17741-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="17741-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="17741-131">End of client support</span></span><br/>    | <span data-ttu-id="17741-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="17741-132">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="17741-133">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="17741-133">End of server support</span></span><br/>    | <span data-ttu-id="17741-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="17741-134">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="17741-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="17741-135">Namespace</span></span><br/>                | <span data-ttu-id="17741-136">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="17741-136">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="17741-137">MOF</span><span class="sxs-lookup"><span data-stu-id="17741-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17741-138"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="17741-138"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="17741-139">DLL</span><span class="sxs-lookup"><span data-stu-id="17741-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17741-140"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17741-140"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17741-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17741-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17741-142">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="17741-142">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="17741-143">**Istscgrouppresent**</span><span class="sxs-lookup"><span data-stu-id="17741-143">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

