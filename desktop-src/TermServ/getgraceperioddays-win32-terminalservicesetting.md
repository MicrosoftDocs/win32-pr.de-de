---
title: Getgraceperioddays-Methode der Win32_TerminalServiceSetting-Klasse
description: Ruft die Anzahl der Tage ab, die in der Remotedesktopdienste-Lizenzierungs Frist für einen Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server verbleiben. Ein NULL-Wert gibt an, dass die Toleranz Periode abgelaufen ist.
ms.assetid: d84d7815-ee09-43d9-a370-993d23f14898
ms.tgt_platform: multiple
keywords:
- Getgraceperioddays-Methode Remotedesktopdienste
- Getgraceperioddays-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, getgraceperioddays-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetGracePeriodDays
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0faaf525bb74a8ac4b0164c181e5a20cfb215d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340477"
---
# <a name="getgraceperioddays-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="32b3e-107">Getgraceperioddays-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="32b3e-107">GetGracePeriodDays method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="32b3e-108">Ruft die Anzahl der Tage ab, die in der Remotedesktopdienste-Lizenzierungs Frist für einen Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server verbleiben.</span><span class="sxs-lookup"><span data-stu-id="32b3e-108">Retrieves the number of days that are remaining in the Remote Desktop Services licensing grace period for a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="32b3e-109">Ein NULL-Wert gibt an, dass die Toleranz Periode abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="32b3e-109">A zero value indicates that the grace period is over.</span></span>

## <a name="syntax"></a><span data-ttu-id="32b3e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="32b3e-110">Syntax</span></span>


```mof
uint32 GetGracePeriodDays(
  [out] uint32 DaysLeft
);
```



## <a name="parameters"></a><span data-ttu-id="32b3e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="32b3e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32b3e-112">*DaysLeft* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="32b3e-112">*DaysLeft* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32b3e-113">Die Anzahl der Tage, die in der Toleranz Periode verbleiben.</span><span class="sxs-lookup"><span data-stu-id="32b3e-113">The number of days that are remaining in the grace period.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32b3e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32b3e-114">Remarks</span></span>

<span data-ttu-id="32b3e-115">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="32b3e-115">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="32b3e-116">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**.</span><span class="sxs-lookup"><span data-stu-id="32b3e-116">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="32b3e-117">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="32b3e-117">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="32b3e-118">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="32b3e-118">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="32b3e-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="32b3e-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="32b3e-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="32b3e-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="32b3e-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="32b3e-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="32b3e-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="32b3e-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="32b3e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32b3e-123">Requirements</span></span>



| <span data-ttu-id="32b3e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32b3e-124">Requirement</span></span> | <span data-ttu-id="32b3e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="32b3e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32b3e-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32b3e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="32b3e-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32b3e-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32b3e-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32b3e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="32b3e-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32b3e-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32b3e-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="32b3e-130">Namespace</span></span><br/>                | <span data-ttu-id="32b3e-131">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="32b3e-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="32b3e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="32b3e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32b3e-133"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="32b3e-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="32b3e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="32b3e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32b3e-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32b3e-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32b3e-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32b3e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b3e-137">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="32b3e-137">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

