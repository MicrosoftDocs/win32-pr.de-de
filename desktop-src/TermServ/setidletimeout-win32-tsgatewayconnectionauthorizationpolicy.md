---
title: Die Methode "stidletimeout" der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die IdleTimeout-Eigenschaft fest.
ms.assetid: 162224dd-e4d4-483f-9ec4-b87731bc5014
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "* tidletimeout"
- Methode Remotedesktopdienste Win32_TSGatewayConnectionAuthorizationPolicy Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, Methode "-Methode"
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetIdleTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c166311477dc9de94ca6c9614e14ac98907b406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345332"
---
# <a name="setidletimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="9227a-106">Die Methode "stidletimeout" der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="9227a-106">SetIdleTimeout method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="9227a-107">Legt die **IdleTimeout** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="9227a-107">Sets the **IdleTimeout** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9227a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9227a-108">Syntax</span></span>


```mof
uint32 SetIdleTimeout(
  [in] uint32 IdleTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="9227a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9227a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9227a-110">*IdleTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9227a-110">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9227a-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9227a-111">Type: **uint32**</span></span>

<span data-ttu-id="9227a-112">Der neue Timeout Wert in Minuten.</span><span class="sxs-lookup"><span data-stu-id="9227a-112">The new timeout value, in minutes.</span></span> <span data-ttu-id="9227a-113">Der Wert 0 bedeutet, dass kein Timeout vorliegt.</span><span class="sxs-lookup"><span data-stu-id="9227a-113">A value of 0 means there is no timeout.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9227a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9227a-114">Return value</span></span>

<span data-ttu-id="9227a-115">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9227a-115">Type: **uint32**</span></span>

<span data-ttu-id="9227a-116">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="9227a-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9227a-117">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9227a-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9227a-118">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9227a-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9227a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9227a-119">Remarks</span></span>

<span data-ttu-id="9227a-120">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9227a-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9227a-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="9227a-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9227a-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="9227a-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9227a-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9227a-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9227a-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9227a-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9227a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9227a-125">Requirements</span></span>



| <span data-ttu-id="9227a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9227a-126">Requirement</span></span> | <span data-ttu-id="9227a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9227a-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9227a-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9227a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9227a-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9227a-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9227a-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9227a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9227a-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9227a-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="9227a-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="9227a-132">Namespace</span></span><br/>                | <span data-ttu-id="9227a-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9227a-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9227a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9227a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9227a-135"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="9227a-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9227a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9227a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9227a-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9227a-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9227a-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9227a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9227a-139">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="9227a-139">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

