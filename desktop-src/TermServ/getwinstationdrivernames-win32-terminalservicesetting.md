---
title: Getwinstationdrivernames-Methode der Win32_TerminalServiceSetting-Klasse
description: Ruft eine Liste der Namen von WinStation-Treibern ab.
ms.assetid: 578c2a07-17e7-4bd6-b520-942cd48ee40f
ms.tgt_platform: multiple
keywords:
- Getwinstationdrivernames-Methode Remotedesktopdienste
- Getwinstationdrivernames-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, getwinstationdrivernames-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetWinstationDriverNames
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41bc0157f368edf129f578765c1b8d73f6f48a33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338132"
---
# <a name="getwinstationdrivernames-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="aa003-106">Getwinstationdrivernames-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="aa003-106">GetWinstationDriverNames method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="aa003-107">Ruft eine Liste der Namen von WinStation-Treibern ab.</span><span class="sxs-lookup"><span data-stu-id="aa003-107">Retrieves a list of Winstation driver names.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa003-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa003-108">Syntax</span></span>


```mof
uint32 GetWinstationDriverNames(
  [out] string WinstaDriverNames[]
);
```



## <a name="parameters"></a><span data-ttu-id="aa003-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa003-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa003-110">*Winstadrivernames* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="aa003-110">*WinstaDriverNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa003-111">Die Liste der Namen der Winstation-Treiber.</span><span class="sxs-lookup"><span data-stu-id="aa003-111">The list of Winstation driver names.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa003-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa003-112">Remarks</span></span>

<span data-ttu-id="aa003-113">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="aa003-113">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="aa003-114">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**.</span><span class="sxs-lookup"><span data-stu-id="aa003-114">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="aa003-115">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="aa003-115">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="aa003-116">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="aa003-116">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="aa003-117">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="aa003-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="aa003-118">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="aa003-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="aa003-119">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="aa003-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="aa003-120">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="aa003-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa003-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa003-121">Requirements</span></span>



| <span data-ttu-id="aa003-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa003-122">Requirement</span></span> | <span data-ttu-id="aa003-123">Wert</span><span class="sxs-lookup"><span data-stu-id="aa003-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa003-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa003-124">Minimum supported client</span></span><br/> | <span data-ttu-id="aa003-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa003-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aa003-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa003-126">Minimum supported server</span></span><br/> | <span data-ttu-id="aa003-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa003-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aa003-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa003-128">Namespace</span></span><br/>                | <span data-ttu-id="aa003-129">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="aa003-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="aa003-130">MOF</span><span class="sxs-lookup"><span data-stu-id="aa003-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa003-131"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="aa003-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa003-132">DLL</span><span class="sxs-lookup"><span data-stu-id="aa003-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa003-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa003-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa003-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa003-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa003-135">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="aa003-135">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

