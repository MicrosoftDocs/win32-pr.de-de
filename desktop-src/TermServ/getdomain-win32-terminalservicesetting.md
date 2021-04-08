---
title: GetDomain-Methode der Win32_TerminalServiceSetting-Klasse
description: Ruft den Namen der Domäne ab, der der Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server angehört.
ms.assetid: 11d58068-56df-4040-b7ba-afdd55bd417a
ms.tgt_platform: multiple
keywords:
- GetDomain-Methode Remotedesktopdienste
- GetDomain-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, GetDomain-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetDomain
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e9b2e5ba62f12c67a753cf8e5c41e8296b31e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949506"
---
# <a name="getdomain-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="cd204-106">GetDomain-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="cd204-106">GetDomain method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="cd204-107">Ruft den Namen der Domäne ab, der der Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server angehört.</span><span class="sxs-lookup"><span data-stu-id="cd204-107">Retrieves the name of the domain that the Remote Desktop Session Host (RD Session Host) server is a member of.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd204-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd204-108">Syntax</span></span>


```mof
uint32 GetDomain(
  [out] string Domain
);
```



## <a name="parameters"></a><span data-ttu-id="cd204-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd204-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd204-110">*Domäne* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cd204-110">*Domain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd204-111">Der Domänen Name des RD-Sitzungshost Servers.</span><span class="sxs-lookup"><span data-stu-id="cd204-111">The domain name of the RD Session Host server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd204-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd204-112">Remarks</span></span>

<span data-ttu-id="cd204-113">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="cd204-113">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="cd204-114">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**.</span><span class="sxs-lookup"><span data-stu-id="cd204-114">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="cd204-115">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="cd204-115">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="cd204-116">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cd204-116">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="cd204-117">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="cd204-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cd204-118">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="cd204-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="cd204-119">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cd204-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cd204-120">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="cd204-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd204-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd204-121">Requirements</span></span>



| <span data-ttu-id="cd204-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd204-122">Requirement</span></span> | <span data-ttu-id="cd204-123">Wert</span><span class="sxs-lookup"><span data-stu-id="cd204-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd204-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd204-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cd204-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd204-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cd204-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd204-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cd204-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd204-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cd204-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd204-128">Namespace</span></span><br/>                | <span data-ttu-id="cd204-129">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cd204-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="cd204-130">MOF</span><span class="sxs-lookup"><span data-stu-id="cd204-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd204-131"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cd204-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd204-132">DLL</span><span class="sxs-lookup"><span data-stu-id="cd204-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd204-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd204-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd204-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd204-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd204-135">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="cd204-135">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

