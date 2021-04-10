---
title: Istscgrouppresent-Methode der Win32_TSLicenseServer-Klasse
description: Istscgrouppresent ist nicht mehr für die Verwendung ab Windows Server 2012 verfügbar.
ms.assetid: 2bbb00ff-4fb3-4a7a-a0e7-3daabf97d70a
ms.tgt_platform: multiple
keywords:
- Istscgrouppresent-Methode Remotedesktopdienste
- Istscgrouppresent-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, istscgrouppresent-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSCGroupPresent
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a16683b10bbfdd08812454d67ebc8ffc169b0ca0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040385"
---
# <a name="istscgrouppresent-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="6a270-106">Istscgrouppresent-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="6a270-106">IsTSCGroupPresent method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="6a270-107">\[**Istscgrouppresent** ist nicht mehr für die Verwendung ab Windows Server 2012 verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="6a270-107">\[**IsTSCGroupPresent** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="6a270-108">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6a270-108">This method is not supported.</span></span>

<span data-ttu-id="6a270-109">**Windows Server 2008 R2 und Windows Server 2008:** Ruft ab, ob die lokale Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenz Server vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6a270-109">**Windows Server 2008 R2 and Windows Server 2008:** Retrieves whether the Terminal Server Computers local group exists on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a270-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a270-110">Syntax</span></span>


```mof
uint32 IsTSCGroupPresent(
  [out] boolean Present
);
```



## <a name="parameters"></a><span data-ttu-id="6a270-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a270-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a270-112">*Vorhanden* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6a270-112">*Present* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a270-113">Boolescher Wert, der angibt, ob die lokale Gruppe "Terminal Server Computer" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6a270-113">Boolean value that indicates whether the Terminal Server Computers local group exists.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a270-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a270-114">Return value</span></span>

<span data-ttu-id="6a270-115">Gibt **WBEM \_ E \_ nicht \_ unterstützt** zurück.</span><span class="sxs-lookup"><span data-stu-id="6a270-115">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="6a270-116">**Windows Server 2008 R2 und Windows Server 2008:** Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="6a270-116">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6a270-117">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6a270-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6a270-118">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6a270-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6a270-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a270-119">Remarks</span></span>

<span data-ttu-id="6a270-120">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="6a270-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6a270-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="6a270-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6a270-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="6a270-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6a270-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6a270-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6a270-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6a270-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a270-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a270-125">Requirements</span></span>



| <span data-ttu-id="6a270-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a270-126">Requirement</span></span> | <span data-ttu-id="6a270-127">Wert</span><span class="sxs-lookup"><span data-stu-id="6a270-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a270-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a270-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6a270-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6a270-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="6a270-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a270-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6a270-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a270-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="6a270-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6a270-132">End of client support</span></span><br/>    | <span data-ttu-id="6a270-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6a270-133">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="6a270-134">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6a270-134">End of server support</span></span><br/>    | <span data-ttu-id="6a270-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6a270-135">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="6a270-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a270-136">Namespace</span></span><br/>                | <span data-ttu-id="6a270-137">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="6a270-137">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="6a270-138">MOF</span><span class="sxs-lookup"><span data-stu-id="6a270-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a270-139"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6a270-139"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a270-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6a270-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a270-141"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a270-141"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a270-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a270-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a270-143">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="6a270-143">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

