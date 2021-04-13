---
title: Disableplugandplaydevices-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die plugandplaydevicesdeaktiviert-Eigenschaft fest.
ms.assetid: 0cfe9fea-da93-47fa-a9ea-868c78890a53
ms.tgt_platform: multiple
keywords:
- Disableplugandplaydevices-Methode Remotedesktopdienste
- Disableplugandplaydevices-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, disableplugandplaydevices-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisablePlugAndPlayDevices
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7432d69fc8cd088af5d5a44a07b90f9d697348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391613"
---
# <a name="disableplugandplaydevices-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="92299-106">Disableplugandplaydevices-Methode der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="92299-106">DisablePlugAndPlayDevices method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="92299-107">Legt die **plugandplaydevicesdeaktiviert** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="92299-107">Sets the **PlugAndPlayDevicesDisabled** property.</span></span> <span data-ttu-id="92299-108">Wenn die **deviceredirectiontype** -Eigenschaft den Wert "2" hat, steuert die **plugandplaydevicesdeaktiviert** -Eigenschaft die Umleitung von Plug & Play Geräten für Sitzungen, die über den Remotedesktop Gateway (RD-Gateway)-Server eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="92299-108">If the **DeviceRedirectionType** property has a value of "2", the **PlugAndPlayDevicesDisabled** property controls redirection of Plug and Play devices for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="92299-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="92299-109">Syntax</span></span>


```mof
uint32 DisablePlugAndPlayDevices(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="92299-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="92299-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92299-111">*Deaktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92299-111">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92299-112">Neuer Wert für die **plugandplaydevicesdeaktiviert** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="92299-112">New value for the **PlugAndPlayDevicesDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92299-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92299-113">Return value</span></span>

<span data-ttu-id="92299-114">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="92299-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="92299-115">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="92299-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="92299-116">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="92299-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="92299-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92299-117">Remarks</span></span>

<span data-ttu-id="92299-118">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="92299-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="92299-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="92299-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="92299-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="92299-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="92299-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="92299-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="92299-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="92299-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="92299-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92299-123">Requirements</span></span>



| <span data-ttu-id="92299-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92299-124">Requirement</span></span> | <span data-ttu-id="92299-125">Wert</span><span class="sxs-lookup"><span data-stu-id="92299-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="92299-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92299-126">Minimum supported client</span></span><br/> | <span data-ttu-id="92299-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="92299-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="92299-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92299-128">Minimum supported server</span></span><br/> | <span data-ttu-id="92299-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92299-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="92299-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="92299-130">Namespace</span></span><br/>                | <span data-ttu-id="92299-131">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="92299-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="92299-132">MOF</span><span class="sxs-lookup"><span data-stu-id="92299-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92299-133"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="92299-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="92299-134">DLL</span><span class="sxs-lookup"><span data-stu-id="92299-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92299-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92299-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="92299-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92299-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92299-137">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="92299-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

