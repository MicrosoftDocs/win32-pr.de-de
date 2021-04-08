---
title: Enablezugewonlysdrservers-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Wird verwendet, um die Eigenschaft "" der Eigenschaft "" zu wechseln.
ms.assetid: ec7f22bc-4e80-4ece-9567-5f405207480e
ms.tgt_platform: multiple
keywords:
- Enablezugewonlysdrservers-Methode Remotedesktopdienste
- Enablezugewonlysdrservers-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, enablezugewonlysdrservers-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.EnableAllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f031cff46e0fafdce80a995d2d4778875c1d56f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741256"
---
# <a name="enableallowonlysdrservers-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="52518-106">Enablezugewonlysdrservers-Methode der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="52518-106">EnableAllowOnlySDRServers method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="52518-107">Wird verwendet, **um die Eigenschaft** "" der Eigenschaft "" zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="52518-107">Used to toggle the **AllowOnlySDRServers** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="52518-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="52518-108">Syntax</span></span>


```mof
uint32 EnableAllowOnlySDRServers(
  [in] boolean AllowOnlySDRServers
);
```



## <a name="parameters"></a><span data-ttu-id="52518-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="52518-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52518-110">" *Zuweisung der Server* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="52518-110">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52518-111">Wenn diese Einstellung auf " **true**" festgelegt ist, werden Verbindungen nur zum Sichern von RDS-Servern (Geräte Umleitung) zugelassen.</span><span class="sxs-lookup"><span data-stu-id="52518-111">If set to **True**, connections will be allowed only to secure device redirection (SDR) RDS servers.</span></span> <span data-ttu-id="52518-112">Wenn diese Einstellung auf " **false**" festgelegt ist, werden Verbindungen auch älteren RDS-Servern gestattet.</span><span class="sxs-lookup"><span data-stu-id="52518-112">If set to **False**, connections will be allowed to older RDS servers also</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52518-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52518-113">Return value</span></span>

<span data-ttu-id="52518-114">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="52518-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="52518-115">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="52518-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="52518-116">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="52518-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52518-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52518-117">Requirements</span></span>



| <span data-ttu-id="52518-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52518-118">Requirement</span></span> | <span data-ttu-id="52518-119">Wert</span><span class="sxs-lookup"><span data-stu-id="52518-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="52518-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52518-120">Minimum supported client</span></span><br/> | <span data-ttu-id="52518-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="52518-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="52518-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52518-122">Minimum supported server</span></span><br/> | <span data-ttu-id="52518-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="52518-123">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="52518-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="52518-124">Namespace</span></span><br/>                | <span data-ttu-id="52518-125">ROOT \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="52518-125">ROOT\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="52518-126">MOF</span><span class="sxs-lookup"><span data-stu-id="52518-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52518-127"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="52518-127"><dt>TsGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="52518-128">DLL</span><span class="sxs-lookup"><span data-stu-id="52518-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52518-129"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52518-129"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="52518-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52518-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52518-131">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="52518-131">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

 





