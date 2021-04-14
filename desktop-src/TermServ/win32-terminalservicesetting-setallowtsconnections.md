---
title: Die Methode "-Methode" der Win32_TerminalServiceSetting-Klasse
description: Mit der Methode "*" können neue Remote Desktop Verbindungen zugelassen oder verweigert werden. Mit dieser Methode wird die allowtconnections-Eigenschaft für die-Klasse entsprechend geändert.
ms.assetid: 6cbaea62-ced0-4788-99fb-5b36816b80a1
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "
- Methode Remotedesktopdienste der Methode "Win32_TerminalServiceSetting"
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, Methode "*"
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetAllowTSConnections
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e800f1a47567f16d916563d4d1e62c767016329a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478834"
---
# <a name="setallowtsconnections-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="58ef9-107">Die Methode "Setup-lowtconnections" der Win32- \_ Klasse "terminalservicesetts"</span><span class="sxs-lookup"><span data-stu-id="58ef9-107">SetAllowTSConnections method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="58ef9-108">Mit **der Methode** "\*" können neue Remote Desktop Verbindungen zugelassen oder verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="58ef9-108">The **SetAllowTSConnections** method allows or denies new remote desktop connections.</span></span> <span data-ttu-id="58ef9-109">Mit dieser Methode wird die **allowtconnections** -Eigenschaft für die-Klasse entsprechend geändert.</span><span class="sxs-lookup"><span data-stu-id="58ef9-109">This method will modify the **AllowTSConnections** property for the class accordingly.</span></span>

## <a name="syntax"></a><span data-ttu-id="58ef9-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="58ef9-110">Syntax</span></span>


```mof
uint32 SetAllowTSConnections(
  [in] uint32 AllowTSConnections,
  [in] uint32 ModifyFirewallException
);
```



## <a name="parameters"></a><span data-ttu-id="58ef9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="58ef9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58ef9-112">*Allow-connections* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58ef9-112">*AllowTSConnections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ef9-113">Gibt an, ob neue Remote Desktop Verbindungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="58ef9-113">Specifies whether new remote desktop connections are allowed.</span></span> <span data-ttu-id="58ef9-114">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="58ef9-114">This must be one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="58ef9-115"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="58ef9-115"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="58ef9-116">Neue Verbindungen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="58ef9-116">New connections are not allowed.</span></span> <span data-ttu-id="58ef9-117">Wenn der *modifyfirewallexception* -Parameter 1 ist, wird die Remotedesktop Firewallausnahme deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="58ef9-117">If the *ModifyFirewallException* parameter is 1, then the Remote Desktop firewall exception is disabled.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="58ef9-118"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="58ef9-118"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="58ef9-119">Neue Verbindungen sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="58ef9-119">New connections are allowed.</span></span> <span data-ttu-id="58ef9-120">Wenn der *modifyfirewallexception* -Parameter 1 ist, wird die Remotedesktop Firewallausnahme aktiviert.</span><span class="sxs-lookup"><span data-stu-id="58ef9-120">If the *ModifyFirewallException* parameter is 1, then the Remote Desktop firewall exception is enabled.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="58ef9-121">*Modifyfirewallexception* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58ef9-121">*ModifyFirewallException* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ef9-122">Gibt an, ob die firewallausnahmeeinstellung für Remotedesktop in den durch den *allowzconnections* -Parameter angegebenen Zustand geändert wird.</span><span class="sxs-lookup"><span data-stu-id="58ef9-122">Specifies if the firewall exception setting for Remote Desktop will be modified to the state specified by the *AllowTSConnections* parameter.</span></span> <span data-ttu-id="58ef9-123">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="58ef9-123">This must be one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="58ef9-124"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="58ef9-124"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="58ef9-125">Ändern Sie die Einstellung für die Firewallausnahme nicht.</span><span class="sxs-lookup"><span data-stu-id="58ef9-125">Do not modify the firewall exception setting.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="58ef9-126"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="58ef9-126"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="58ef9-127">Ändern Sie die Einstellung für die Firewallausnahme.</span><span class="sxs-lookup"><span data-stu-id="58ef9-127">Modify the firewall exception setting.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58ef9-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58ef9-128">Return value</span></span>

<span data-ttu-id="58ef9-129">Gibt bei Erfolg Erfolg zurück. Andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="58ef9-129">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="58ef9-130">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="58ef9-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="58ef9-131">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="58ef9-131">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="58ef9-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58ef9-132">Remarks</span></span>

<span data-ttu-id="58ef9-133">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="58ef9-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="58ef9-134">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="58ef9-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="58ef9-135">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="58ef9-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="58ef9-136">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="58ef9-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="58ef9-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58ef9-137">Requirements</span></span>



| <span data-ttu-id="58ef9-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58ef9-138">Requirement</span></span> | <span data-ttu-id="58ef9-139">Wert</span><span class="sxs-lookup"><span data-stu-id="58ef9-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58ef9-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58ef9-140">Minimum supported client</span></span><br/> | <span data-ttu-id="58ef9-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58ef9-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58ef9-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58ef9-142">Minimum supported server</span></span><br/> | <span data-ttu-id="58ef9-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58ef9-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58ef9-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="58ef9-144">Namespace</span></span><br/>                | <span data-ttu-id="58ef9-145">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="58ef9-145">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="58ef9-146">MOF</span><span class="sxs-lookup"><span data-stu-id="58ef9-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58ef9-147"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="58ef9-147"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="58ef9-148">DLL</span><span class="sxs-lookup"><span data-stu-id="58ef9-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58ef9-149"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58ef9-149"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58ef9-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58ef9-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ef9-151">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="58ef9-151">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

