---
title: Die Methode "kreatetscgroup" der Win32_TSLicenseServer-Klasse
description: "\"\" Ist für Windows Server 2012 nicht mehr verfügbar."
ms.assetid: 31751da7-263b-4911-a328-246457a606f0
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "kreatetscgroup"
- Methode Remotedesktopdienste der Methode "kreatetscgroup", Win32_TSLicenseServer
- Win32_TSLicenseServer Klasse Remotedesktopdienste, Methode "kreatetscgroup"
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.CreateTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63f10db61cb02ece09d168cb462e31246e498494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858720"
---
# <a name="createtscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="03f86-106">Methode "foratetscgroup" der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="03f86-106">CreateTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="03f86-107">\[" **" Ist für** Windows Server 2012 nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="03f86-107">\[**CreateTSCGroup** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="03f86-108">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03f86-108">This method is not supported.</span></span>

<span data-ttu-id="03f86-109">**Windows Server 2008 R2 und Windows Server 2008:** Erstellt die lokale Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenz Server.</span><span class="sxs-lookup"><span data-stu-id="03f86-109">**Windows Server 2008 R2 and Windows Server 2008:** Creates the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="03f86-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="03f86-110">Syntax</span></span>


```mof
uint32 CreateTSCGroup();
```



## <a name="parameters"></a><span data-ttu-id="03f86-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="03f86-111">Parameters</span></span>

<span data-ttu-id="03f86-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="03f86-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03f86-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03f86-113">Return value</span></span>

<span data-ttu-id="03f86-114">Gibt **WBEM \_ E \_ nicht \_ unterstützt** zurück.</span><span class="sxs-lookup"><span data-stu-id="03f86-114">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="03f86-115">**Windows Server 2008 R2 und Windows Server 2008:** Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="03f86-115">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="03f86-116">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="03f86-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="03f86-117">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="03f86-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="03f86-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03f86-118">Remarks</span></span>

<span data-ttu-id="03f86-119">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="03f86-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="03f86-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="03f86-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="03f86-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="03f86-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="03f86-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="03f86-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="03f86-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="03f86-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="03f86-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03f86-124">Requirements</span></span>



| <span data-ttu-id="03f86-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03f86-125">Requirement</span></span> | <span data-ttu-id="03f86-126">Wert</span><span class="sxs-lookup"><span data-stu-id="03f86-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="03f86-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03f86-127">Minimum supported client</span></span><br/> | <span data-ttu-id="03f86-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="03f86-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="03f86-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03f86-129">Minimum supported server</span></span><br/> | <span data-ttu-id="03f86-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03f86-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="03f86-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="03f86-131">End of client support</span></span><br/>    | <span data-ttu-id="03f86-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="03f86-132">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="03f86-133">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="03f86-133">End of server support</span></span><br/>    | <span data-ttu-id="03f86-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="03f86-134">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="03f86-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="03f86-135">Namespace</span></span><br/>                | <span data-ttu-id="03f86-136">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="03f86-136">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="03f86-137">MOF</span><span class="sxs-lookup"><span data-stu-id="03f86-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03f86-138"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="03f86-138"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="03f86-139">DLL</span><span class="sxs-lookup"><span data-stu-id="03f86-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03f86-140"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03f86-140"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03f86-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03f86-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f86-142">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="03f86-142">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="03f86-143">**Istscgrouppresent**</span><span class="sxs-lookup"><span data-stu-id="03f86-143">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

