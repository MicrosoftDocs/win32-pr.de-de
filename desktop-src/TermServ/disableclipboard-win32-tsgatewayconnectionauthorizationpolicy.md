---
title: Disableclipboard-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die clipboarddeaktiviert-Eigenschaft fest. Wenn die deviceredirectiontype-Eigenschaft den Wert \ 0034; 2 \ 0034; hat, steuert die clipboarddeaktiviert-Eigenschaft die Umleitung der Zwischenablage für Sitzungen, die über den Remotedesktop Gateway-Server (RD-Gateway) eingerichtet werden.
ms.assetid: c53fc802-958b-452d-9af9-0ce89ed46079
ms.tgt_platform: multiple
keywords:
- Disableclipboard-Methode Remotedesktopdienste
- Disableclipboard-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy Klasse Remotedesktopdienste, disableclipboard-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableClipboard
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ae2070a35fa31f1c9d9ad31e9e632e31c0193f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337495"
---
# <a name="disableclipboard-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="c9a90-107">Disableclipboard-Methode der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="c9a90-107">DisableClipboard method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="c9a90-108">Legt die **clipboarddeaktiviert** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="c9a90-108">Sets the **ClipboardDisabled** property.</span></span> <span data-ttu-id="c9a90-109">Wenn die **deviceredirectiontype** -Eigenschaft den Wert "2" hat, steuert die **clipboarddeaktiviert** -Eigenschaft die Umleitung der Zwischenablage für Sitzungen, die über den Remotedesktop Gateway-Server (RD-Gateway) eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="c9a90-109">If the **DeviceRedirectionType** property has a value of "2", the **ClipboardDisabled** property controls redirection of the clipboard for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a90-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9a90-110">Syntax</span></span>


```mof
uint32 DisableClipboard(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="c9a90-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9a90-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a90-112">*Deaktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9a90-112">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a90-113">Neuer Wert für die **clipboarddeaktiviert** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c9a90-113">New value for the **ClipboardDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9a90-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9a90-114">Return value</span></span>

<span data-ttu-id="c9a90-115">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c9a90-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c9a90-116">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c9a90-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c9a90-117">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c9a90-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c9a90-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9a90-118">Remarks</span></span>

<span data-ttu-id="c9a90-119">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c9a90-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c9a90-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="c9a90-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c9a90-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="c9a90-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c9a90-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c9a90-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c9a90-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c9a90-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9a90-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9a90-124">Requirements</span></span>



| <span data-ttu-id="c9a90-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9a90-125">Requirement</span></span> | <span data-ttu-id="c9a90-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c9a90-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a90-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9a90-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c9a90-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c9a90-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c9a90-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9a90-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c9a90-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9a90-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c9a90-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9a90-131">Namespace</span></span><br/>                | <span data-ttu-id="c9a90-132">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c9a90-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c9a90-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c9a90-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9a90-134"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="c9a90-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9a90-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c9a90-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9a90-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9a90-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c9a90-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9a90-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a90-138">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="c9a90-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

