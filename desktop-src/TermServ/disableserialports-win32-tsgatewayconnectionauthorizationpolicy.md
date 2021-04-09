---
title: Disableserialports-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die serialportsdeaktiviert-Eigenschaft fest.
ms.assetid: 95c027e3-f76d-4335-84ac-93a1c3718e66
ms.tgt_platform: multiple
keywords:
- Disableserialports-Methode Remotedesktopdienste
- Disableserialports-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, disableserialports-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableSerialPorts
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a4f6941f8bc98d7f8e424a984922ad1f6631c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740416"
---
# <a name="disableserialports-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="33993-106">Disableserialports-Methode der Win32- \_ Klasse "tgatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="33993-106">DisableSerialPorts method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="33993-107">Legt die **serialportsdeaktiviert** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="33993-107">Sets the **SerialPortsDisabled** property.</span></span> <span data-ttu-id="33993-108">Wenn die **deviceredirectiontype** -Eigenschaft den Wert "2" hat, steuert die **serialportsdeaktiviert** -Eigenschaft die Umleitung der seriellen Anschlüsse für Sitzungen, die über den Remotedesktop Gateway-Server (RD-Gateway) eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="33993-108">If the **DeviceRedirectionType** property has a value of "2", the **SerialPortsDisabled** property controls redirection of the serial ports for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="33993-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="33993-109">Syntax</span></span>


```mof
uint32 DisableSerialPorts(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="33993-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="33993-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33993-111">*Deaktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33993-111">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33993-112">Neuer Wert für die **serialportsdeaktiviert** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="33993-112">New value for the **SerialPortsDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33993-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33993-113">Return value</span></span>

<span data-ttu-id="33993-114">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="33993-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="33993-115">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="33993-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="33993-116">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="33993-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="33993-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33993-117">Remarks</span></span>

<span data-ttu-id="33993-118">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="33993-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="33993-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="33993-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="33993-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="33993-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="33993-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="33993-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="33993-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="33993-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="33993-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33993-123">Requirements</span></span>



| <span data-ttu-id="33993-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33993-124">Requirement</span></span> | <span data-ttu-id="33993-125">Wert</span><span class="sxs-lookup"><span data-stu-id="33993-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="33993-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33993-126">Minimum supported client</span></span><br/> | <span data-ttu-id="33993-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="33993-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="33993-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33993-128">Minimum supported server</span></span><br/> | <span data-ttu-id="33993-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33993-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="33993-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="33993-130">Namespace</span></span><br/>                | <span data-ttu-id="33993-131">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="33993-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="33993-132">MOF</span><span class="sxs-lookup"><span data-stu-id="33993-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33993-133"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="33993-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="33993-134">DLL</span><span class="sxs-lookup"><span data-stu-id="33993-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33993-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33993-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="33993-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33993-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33993-137">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="33993-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

