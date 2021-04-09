---
title: Findlicenseservers-Methode der Win32_TerminalServiceSetting-Klasse
description: Listet alle Remotedesktop-Lizenzserver und die Ermittlungsmethode auf.
ms.assetid: 0de2ee6f-6c56-4293-84da-131b433c6a9d
ms.tgt_platform: multiple
keywords:
- Findlicenseservers-Methode Remotedesktopdienste
- Findlicenseservers-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, findlicenseservers-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.FindLicenseServers
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83376876009a691fed233cf723f04dcc3bc3c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957065"
---
# <a name="findlicenseservers-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="f4b4c-106">Findlicenseservers-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="f4b4c-106">FindLicenseServers method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="f4b4c-107">Listet alle Remotedesktop-Lizenzserver und die Ermittlungsmethode auf.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-107">Enumerates all of the Remote Desktop license servers, and the method of discovery.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4b4c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4b4c-108">Syntax</span></span>


```mof
uint32 FindLicenseServers(
  [out] Win32_TSDiscoveredLicenseServer LicenseServersList[],
  [out] uint32                          Count
);
```



## <a name="parameters"></a><span data-ttu-id="f4b4c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4b4c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4b4c-110">*Licenseserverslist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f4b4c-110">*LicenseServersList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4b4c-111">Die Liste der Win32-Objekte von " [**\_ zdiscoveredlicenseserver**](win32-tsdiscoveredlicenseserver.md) ".</span><span class="sxs-lookup"><span data-stu-id="f4b4c-111">The list of [**Win32\_TSDiscoveredLicenseServer**](win32-tsdiscoveredlicenseserver.md) objects.</span></span> <span data-ttu-id="f4b4c-112">Jedes Objekt in der Ausgabeliste enthält den Namen des Remotedesktop Lizenzservers und die Ermittlungsmethode.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-112">Each object in the output list has the name of the Remote Desktop license server, and the method of discovery.</span></span>

</dd> <dt>

<span data-ttu-id="f4b4c-113">*Anzahl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f4b4c-113">*Count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4b4c-114">Die Gesamtanzahl der ermittelten Remotedesktop Lizenzserver in der Ausgabeliste.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-114">The total number of discovered Remote Desktop license servers in the output list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4b4c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4b4c-115">Remarks</span></span>

<span data-ttu-id="f4b4c-116">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-116">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="f4b4c-117">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-117">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="f4b4c-118">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-118">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="f4b4c-119">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-119">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="f4b4c-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f4b4c-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f4b4c-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f4b4c-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f4b4c-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f4b4c-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4b4c-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4b4c-124">Requirements</span></span>



| <span data-ttu-id="f4b4c-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4b4c-125">Requirement</span></span> | <span data-ttu-id="f4b4c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="f4b4c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4b4c-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4b4c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f4b4c-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4b4c-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f4b4c-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4b4c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f4b4c-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4b4c-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f4b4c-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="f4b4c-131">Namespace</span></span><br/>                | <span data-ttu-id="f4b4c-132">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f4b4c-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f4b4c-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f4b4c-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4b4c-134"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f4b4c-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4b4c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f4b4c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4b4c-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4b4c-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4b4c-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4b4c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4b4c-138">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="f4b4c-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

