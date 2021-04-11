---
title: Canaccesslicenseserver-Methode der Win32_TerminalServiceSetting-Klasse
description: Canaccesslicenseserver ist nicht mehr verfügbar.
ms.assetid: b09fa901-8ae1-431e-8d97-27ee84a84779
ms.tgt_platform: multiple
keywords:
- Canaccesslicenseserver-Methode Remotedesktopdienste
- Canaccesslicenseserver-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, canaccesslicenseserver-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CanAccessLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa5bd0e108c0ccceed6890adedea7901834804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103174"
---
# <a name="canaccesslicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="0ca20-106">Canaccesslicenseserver-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="0ca20-106">CanAccessLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="0ca20-107">\[**Canaccesslicenseserver** ist nicht mehr für die Verwendung ab Windows Server 2008 R2 verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0ca20-107">\[**CanAccessLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="0ca20-108">\* \* Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="0ca20-108">\*\*Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="0ca20-109">Bestimmt, ob der Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server Remotedesktopdienste Client Zugriffs Lizenzen (RDS-CALs) von einem Remotedesktop Lizenzserver basierend auf folgenden Anforderungen anfordern kann:</span><span class="sxs-lookup"><span data-stu-id="0ca20-109">Determines whether the Remote Desktop Session Host (RD Session Host) server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from a Remote Desktop license server based on the following:</span></span>

-   <span data-ttu-id="0ca20-110">Die Gruppenrichtlinien Einstellung "Lizenzserver-Sicherheitsgruppe" auf dem Remotedesktop-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="0ca20-110">The "license server security group" group policy setting on the Remote Desktop license server.</span></span>
-   <span data-ttu-id="0ca20-111">Mitgliedschaft in der lokalen Gruppe "Terminal Server Computer" auf dem Lizenz Server.</span><span class="sxs-lookup"><span data-stu-id="0ca20-111">Membership in the Terminal Server Computers local group on the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ca20-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ca20-112">Syntax</span></span>


```mof
uint32 CanAccessLicenseServer(
  [in]  string ServerName,
  [out] uint32 AccessAllowed
);
```



## <a name="parameters"></a><span data-ttu-id="0ca20-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ca20-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ca20-114">*Servername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ca20-114">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ca20-115">Der Name des Remotedesktop Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="0ca20-115">The name of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="0ca20-116">*AccessAllowed* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0ca20-116">*AccessAllowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ca20-117">Gibt an, ob der RD-Sitzungshost Server RDS-CALs vom Lizenzserver anfordern darf.</span><span class="sxs-lookup"><span data-stu-id="0ca20-117">Whether the RD Session Host server is allowed to request RDS CALs from the license server.</span></span>

<dt>

<span data-ttu-id="0ca20-118">0</span><span class="sxs-lookup"><span data-stu-id="0ca20-118">0</span></span>
</dt> <dd>

<span data-ttu-id="0ca20-119">Die Anforderung ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="0ca20-119">The request is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="0ca20-120">1</span><span class="sxs-lookup"><span data-stu-id="0ca20-120">1</span></span>
</dt> <dd>

<span data-ttu-id="0ca20-121">Die Anforderung ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="0ca20-121">The request is not allowed.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ca20-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ca20-122">Return value</span></span>

<span data-ttu-id="0ca20-123">Gibt **S \_ OK** zurück, wenn der RD-Sitzungshost Server Zugriff auf den Lizenzserver hat.</span><span class="sxs-lookup"><span data-stu-id="0ca20-123">Returns **S\_OK** if the RD Session Host server has access to the license server.</span></span> <span data-ttu-id="0ca20-124">Gibt **" \_ false** " zurück, wenn der RD-Sitzungshost Server keinen Zugriff auf den Lizenzserver hat.</span><span class="sxs-lookup"><span data-stu-id="0ca20-124">Returns **S\_FALSE** if the RD Session Host server does not have access to the license server.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ca20-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ca20-125">Remarks</span></span>

<span data-ttu-id="0ca20-126">Mit der Richtlinien Einstellung "Lizenzserver-Sicherheitsgruppe" können Sie die RD-Sitzungshost Server angeben, die den Lizenzserver zum Abrufen von RDS-CALs kontaktieren dürfen.</span><span class="sxs-lookup"><span data-stu-id="0ca20-126">The "license server security group" policy setting allows you to specify the RD Session Host servers that are permitted to contact the license server to obtain RDS CALs.</span></span> <span data-ttu-id="0ca20-127">Wenn die Richtlinien Einstellung auf dem Lizenzserver aktiviert ist, antwortet der Lizenzserver nur auf RDS-Client Zugriffs Anforderungen von RD-Sitzungshost Servern, deren Computer Konten Mitglied der lokalen Gruppe "Terminal Server Computer" auf dem Lizenzserver sind.</span><span class="sxs-lookup"><span data-stu-id="0ca20-127">If the policy setting is enabled on the license server, the license server will only respond to RDS CAL requests from RD Session Host servers whose computer accounts are members of the Terminal Server Computers local group on the license server.</span></span>

<span data-ttu-id="0ca20-128">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="0ca20-128">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="0ca20-129">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**.</span><span class="sxs-lookup"><span data-stu-id="0ca20-129">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="0ca20-130">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="0ca20-130">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="0ca20-131">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0ca20-131">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="0ca20-132">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="0ca20-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0ca20-133">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="0ca20-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0ca20-134">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0ca20-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0ca20-135">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0ca20-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ca20-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ca20-136">Requirements</span></span>



| <span data-ttu-id="0ca20-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ca20-137">Requirement</span></span> | <span data-ttu-id="0ca20-138">Wert</span><span class="sxs-lookup"><span data-stu-id="0ca20-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ca20-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ca20-139">Minimum supported client</span></span><br/> | <span data-ttu-id="0ca20-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0ca20-140">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0ca20-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ca20-141">Minimum supported server</span></span><br/> | <span data-ttu-id="0ca20-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ca20-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0ca20-143">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0ca20-143">End of client support</span></span><br/>    | <span data-ttu-id="0ca20-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0ca20-144">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0ca20-145">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="0ca20-145">End of server support</span></span><br/>    | <span data-ttu-id="0ca20-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ca20-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0ca20-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ca20-147">Namespace</span></span><br/>                | <span data-ttu-id="0ca20-148">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0ca20-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0ca20-149">MOF</span><span class="sxs-lookup"><span data-stu-id="0ca20-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ca20-150"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0ca20-150"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ca20-151">DLL</span><span class="sxs-lookup"><span data-stu-id="0ca20-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ca20-152"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ca20-152"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ca20-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ca20-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ca20-154">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="0ca20-154">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

