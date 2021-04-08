---
title: Setdeviceredirectiontype-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die deviceredirectiontype-Eigenschaft fest, die steuert, welche Geräte umgeleitet werden.
ms.assetid: d97a0a7d-a08e-4703-b0f0-ba5d20688dc8
ms.tgt_platform: multiple
keywords:
- Setdeviceredirectiontype-Methode Remotedesktopdienste
- Setdeviceredirectiontype-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, setdeviceredirectiontype-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetDeviceRedirectionType
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98b369e0b6031aa503e2f7f55860d004f63b7f93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949795"
---
# <a name="setdeviceredirectiontype-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="6ea48-106">Setdeviceredirectiontype-Methode der Win32- \_ Klasse "tgatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="6ea48-106">SetDeviceRedirectionType method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="6ea48-107">Legt die **deviceredirectiontype** -Eigenschaft fest, die steuert, welche Geräte umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="6ea48-107">Sets the **DeviceRedirectionType** property, which controls which devices will be redirected.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ea48-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ea48-108">Syntax</span></span>


```mof
uint32 SetDeviceRedirectionType(
  [in] uint32 DeviceRedirectionType
);
```



## <a name="parameters"></a><span data-ttu-id="6ea48-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ea48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ea48-110">*Deviceredirectiontype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ea48-110">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ea48-111">Der Geräte Umleitungstyp.</span><span class="sxs-lookup"><span data-stu-id="6ea48-111">The device redirection type.</span></span>

<dt>

<span data-ttu-id="6ea48-112">0</span><span class="sxs-lookup"><span data-stu-id="6ea48-112">0</span></span>
</dt> <dd>

<span data-ttu-id="6ea48-113">Alle Geräte werden umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6ea48-113">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="6ea48-114">1</span><span class="sxs-lookup"><span data-stu-id="6ea48-114">1</span></span>
</dt> <dd>

<span data-ttu-id="6ea48-115">Keine Geräte werden umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6ea48-115">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="6ea48-116">2</span><span class="sxs-lookup"><span data-stu-id="6ea48-116">2</span></span>
</dt> <dd>

<span data-ttu-id="6ea48-117">Angegebene Geräte werden nicht umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6ea48-117">Specified devices will not be redirected.</span></span> <span data-ttu-id="6ea48-118">Die Eigenschaften **diskdrivesdeaktiviert**, **printersdeaktiviert**, **serialportsdeaktiviert**, **clipboarddeaktiviert** und **plugandplaydevicesdeaktiviert** steuern, welche Geräte nicht umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="6ea48-118">The **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled**, and **PlugAndPlayDevicesDisabled** properties control which devices will not be redirected.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ea48-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ea48-119">Return value</span></span>

<span data-ttu-id="6ea48-120">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="6ea48-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6ea48-121">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ea48-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6ea48-122">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6ea48-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6ea48-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ea48-123">Remarks</span></span>

<span data-ttu-id="6ea48-124">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="6ea48-124">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6ea48-125">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="6ea48-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6ea48-126">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="6ea48-126">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6ea48-127">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6ea48-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6ea48-128">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6ea48-128">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ea48-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ea48-129">Requirements</span></span>



| <span data-ttu-id="6ea48-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ea48-130">Requirement</span></span> | <span data-ttu-id="6ea48-131">Wert</span><span class="sxs-lookup"><span data-stu-id="6ea48-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ea48-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ea48-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6ea48-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6ea48-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6ea48-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ea48-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6ea48-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ea48-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6ea48-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ea48-136">Namespace</span></span><br/>                | <span data-ttu-id="6ea48-137">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6ea48-137">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6ea48-138">MOF</span><span class="sxs-lookup"><span data-stu-id="6ea48-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ea48-139"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="6ea48-139"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ea48-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6ea48-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ea48-141"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ea48-141"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6ea48-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ea48-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ea48-143">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="6ea48-143">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

