---
title: Issecureaccessallowed-Methode der Win32_TSLicenseServer-Klasse
description: Ruft ab, ob ein Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server Remotedesktopdienste Client Zugriffs Lizenzen anfordern darf (RDS \ 160; CALs) auf dem Remotedesktop-Lizenzserver.
ms.assetid: b9124808-79be-4b94-b12b-f093d5e8195a
ms.tgt_platform: multiple
keywords:
- Issecureaccessallowed-Methode Remotedesktopdienste
- Issecureaccessallowed-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, issecureaccessallowed-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsSecureAccessAllowed
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf35fd8b38139027955fde51a209000435744f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517741"
---
# <a name="issecureaccessallowed-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="c2111-106">Issecureaccessallowed-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="c2111-106">IsSecureAccessAllowed method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="c2111-107">Ruft ab, ob ein Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server Remotedesktopdienste Client Zugriffs Lizenzen (RDS-CALs) vom Remotedesktop Lizenzserver anfordern darf.</span><span class="sxs-lookup"><span data-stu-id="c2111-107">Retrieves whether a Remote Desktop Session Host (RD Session Host) server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2111-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2111-108">Syntax</span></span>


```mof
uint32 IsSecureAccessAllowed(
  [in]  string  tsname,
  [out] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="c2111-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2111-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2111-110">*zname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2111-110">*tsname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2111-111">Der Name des RD-Sitzungshost Servers.</span><span class="sxs-lookup"><span data-stu-id="c2111-111">Name of the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="c2111-112">*Zulässig* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c2111-112">*Allowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2111-113">Boolescher Wert, der angibt, ob der RD-Sitzungshost Server RDS-CALs vom Lizenzserver anfordern darf.</span><span class="sxs-lookup"><span data-stu-id="c2111-113">Boolean value that indicates whether the RD Session Host server is allowed to request RDS CALs from the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2111-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2111-114">Return value</span></span>

<span data-ttu-id="c2111-115">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c2111-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c2111-116">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c2111-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c2111-117">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c2111-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c2111-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2111-118">Remarks</span></span>

<span data-ttu-id="c2111-119">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c2111-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c2111-120">Der zurückgegebene Wert basiert auf der Gruppenrichtlinien Einstellung "Lizenzserver-Sicherheitsgruppe" und der lokalen Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="c2111-120">The returned value is based on the "license server security group" group policy setting, and membership in the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

<span data-ttu-id="c2111-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="c2111-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c2111-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="c2111-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c2111-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c2111-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c2111-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c2111-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2111-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2111-125">Requirements</span></span>



| <span data-ttu-id="c2111-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2111-126">Requirement</span></span> | <span data-ttu-id="c2111-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c2111-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2111-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2111-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c2111-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c2111-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c2111-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2111-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c2111-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2111-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c2111-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2111-132">Namespace</span></span><br/>                | <span data-ttu-id="c2111-133">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c2111-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="c2111-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c2111-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2111-135"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c2111-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2111-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c2111-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2111-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2111-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2111-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2111-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2111-139">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="c2111-139">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="c2111-140">**Islssecgrpgpabled**</span><span class="sxs-lookup"><span data-stu-id="c2111-140">**IsLSSecGrpGPEnabled**</span></span>](islssecgrpgpenabled-win32-tslicenseserver.md)
</dt> </dl>

 

