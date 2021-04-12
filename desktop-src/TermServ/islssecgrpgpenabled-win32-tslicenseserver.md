---
title: Islssecgrpgpabled-Methode der Win32_TSLicenseServer-Klasse
description: Ruft ab, ob die Sicherheitsgruppe \ 0034; Lizenzserver \ 0034; die Gruppenrichtlinien Einstellung ist auf dem Remotedesktop-Lizenzserver aktiviert.
ms.assetid: 715b619b-f082-4fed-ac4c-70d5e286e37c
ms.tgt_platform: multiple
keywords:
- Islssecgrpgpabled-Methode Remotedesktopdienste
- Islssecgrpgpabled-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, islssecgrpgpabled-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSSecGrpGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f3d7ec9de3d98849f9680f1b2a87bf5b22922a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104301"
---
# <a name="islssecgrpgpenabled-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="fd3de-106">Islssecgrpgpabled-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="fd3de-106">IsLSSecGrpGPEnabled method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="fd3de-107">Ruft ab, ob die Gruppenrichtlinien Einstellung "Lizenzserver-Sicherheitsgruppe" auf dem Remotedesktop-Lizenzserver aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fd3de-107">Retrieves whether the "license server security group" group policy setting is enabled on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd3de-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd3de-108">Syntax</span></span>


```mof
uint32 IsLSSecGrpGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="fd3de-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd3de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd3de-110">*Aktiviert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fd3de-110">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd3de-111">Boolescher Wert, der angibt, ob die Richtlinien Einstellung für die Sicherheitsgruppe "Lizenzserver" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fd3de-111">Boolean value that indicates whether the "license server security group" policy setting is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd3de-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd3de-112">Return value</span></span>

<span data-ttu-id="fd3de-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="fd3de-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fd3de-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fd3de-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fd3de-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fd3de-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fd3de-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd3de-116">Remarks</span></span>

<span data-ttu-id="fd3de-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="fd3de-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fd3de-118">Mit der Richtlinien Einstellung "Lizenzserver-Sicherheitsgruppe" können Sie die Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server angeben, die zum Abrufen von Remotedesktopdienste Client Zugriffs Lizenzen (RDS-CALs) mit dem Lizenzserver berechtigt sind.</span><span class="sxs-lookup"><span data-stu-id="fd3de-118">The "license server security group" policy setting allows you to specify the Remote Desktop Session Host (RD Session Host) servers that are permitted to contact the license server to obtain Remote Desktop Services client access licenses (RDS CALs).</span></span> <span data-ttu-id="fd3de-119">Wenn die Richtlinien Einstellung auf dem Lizenzserver aktiviert ist, antwortet der Server nur auf RDS-Anforderungen von RD-Sitzungshost Servern, deren Computer Konten Mitglied der lokalen Gruppe "Terminal Server Computer" auf dem Lizenzserver sind.</span><span class="sxs-lookup"><span data-stu-id="fd3de-119">If the policy setting is enabled on the license server, the server will only respond to RDS CAL requests from RD Session Host servers whose computer accounts are members of the Terminal Server Computers local group on the license server.</span></span>

<span data-ttu-id="fd3de-120">Die Richtlinien Einstellung befindet sich im folgenden Knoten des Editors für lokale Gruppenrichtlinien:</span><span class="sxs-lookup"><span data-stu-id="fd3de-120">The policy setting is located in the following node of the local group policy editor:</span></span>

<span data-ttu-id="fd3de-121">Computer Konfiguration \\ Administrative Vorlagen \\ \\ terminaldiensteterminaldienstelizenzierung von Windows-Komponenten \\</span><span class="sxs-lookup"><span data-stu-id="fd3de-121">Computer Configuration\\Administrative Templates\\Windows Components\\Terminal Services\\TS Licensing</span></span>

<span data-ttu-id="fd3de-122">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="fd3de-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fd3de-123">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="fd3de-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fd3de-124">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fd3de-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fd3de-125">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fd3de-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd3de-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd3de-126">Requirements</span></span>



| <span data-ttu-id="fd3de-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd3de-127">Requirement</span></span> | <span data-ttu-id="fd3de-128">Wert</span><span class="sxs-lookup"><span data-stu-id="fd3de-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd3de-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd3de-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fd3de-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fd3de-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="fd3de-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd3de-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fd3de-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd3de-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="fd3de-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="fd3de-133">Namespace</span></span><br/>                | <span data-ttu-id="fd3de-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="fd3de-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="fd3de-135">MOF</span><span class="sxs-lookup"><span data-stu-id="fd3de-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd3de-136"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fd3de-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd3de-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fd3de-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd3de-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd3de-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd3de-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd3de-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd3de-140">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="fd3de-140">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

