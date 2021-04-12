---
title: Removelsfromzlsgroup-Methode der Win32_TSLicenseServer-Klasse
description: Hierdurch wird der Remotedesktop Lizenzserver aus der Gruppe Remotedesktopdienste Lizenzserver auf einem Domänen Controller in derselben Domäne wie der Lizenzserver entfernt.
ms.assetid: 5ed4595b-0668-4dd8-953e-b6fc61088cfd
ms.tgt_platform: multiple
keywords:
- Removelsfromzlsgroup-Methode Remotedesktopdienste
- Removelsfromzlsgroup-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, removelsfromzlsgroup-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RemoveLSfromTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60c7a0e6b836b8fcf268942ba5d8eae1304b818
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518029"
---
# <a name="removelsfromtslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="31c95-106">Removelsfromzlsgroup-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="31c95-106">RemoveLSfromTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="31c95-107">Hierdurch wird der Remotedesktop Lizenzserver aus der Gruppe Remotedesktopdienste Lizenzserver auf einem Domänen Controller in derselben Domäne wie der Lizenzserver entfernt.</span><span class="sxs-lookup"><span data-stu-id="31c95-107">Removes the Remote Desktop license server from the Remote Desktop Services License Servers group on a domain controller in the same domain as the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="31c95-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="31c95-108">Syntax</span></span>


```mof
uint32 RemoveLSfromTSLSGroup();
```



## <a name="parameters"></a><span data-ttu-id="31c95-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="31c95-109">Parameters</span></span>

<span data-ttu-id="31c95-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="31c95-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="31c95-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31c95-111">Return value</span></span>

<span data-ttu-id="31c95-112">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="31c95-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="31c95-113">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="31c95-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="31c95-114">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="31c95-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="31c95-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31c95-115">Remarks</span></span>

<span data-ttu-id="31c95-116">Sie müssen Mitglied der Gruppe "Domänen-Admins" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="31c95-116">You must be a member of the Domain Admins group to call this method.</span></span>

<span data-ttu-id="31c95-117">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="31c95-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="31c95-118">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="31c95-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="31c95-119">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="31c95-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="31c95-120">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="31c95-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="31c95-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31c95-121">Requirements</span></span>



| <span data-ttu-id="31c95-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31c95-122">Requirement</span></span> | <span data-ttu-id="31c95-123">Wert</span><span class="sxs-lookup"><span data-stu-id="31c95-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="31c95-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31c95-124">Minimum supported client</span></span><br/> | <span data-ttu-id="31c95-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="31c95-125">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="31c95-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31c95-126">Minimum supported server</span></span><br/> | <span data-ttu-id="31c95-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31c95-127">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="31c95-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="31c95-128">Namespace</span></span><br/>                | <span data-ttu-id="31c95-129">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="31c95-129">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="31c95-130">MOF</span><span class="sxs-lookup"><span data-stu-id="31c95-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31c95-131"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="31c95-131"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="31c95-132">DLL</span><span class="sxs-lookup"><span data-stu-id="31c95-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31c95-133"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31c95-133"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31c95-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31c95-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31c95-135">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="31c95-135">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

