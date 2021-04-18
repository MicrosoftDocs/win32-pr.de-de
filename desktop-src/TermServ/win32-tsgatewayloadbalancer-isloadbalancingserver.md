---
title: Isloadbalancingserver-Methode der Win32_TSGatewayLoadBalancer-Klasse
description: Bestimmt, ob der Remotedesktop Gateway-Server (RD-Gateway) einen Lastenausgleich durchführen kann.
ms.assetid: ae1a91c1-0b8b-4bd0-83f9-41c973247f27
ms.tgt_platform: multiple
keywords:
- Isloadbalancingserver-Methode Remotedesktopdienste
- Isloadbalancingserver-Methode Remotedesktopdienste, Win32_TSGatewayLoadBalancer-Klasse
- Win32_TSGatewayLoadBalancer-Klasse Remotedesktopdienste, isloadbalancingserver-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.IsLoadBalancingServer
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eae909df4074c8129a1b49eb0d5c3b336fed5d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344684"
---
# <a name="isloadbalancingserver-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="b73ee-106">Isloadbalancingserver-Methode der Win32- \_ Klasse "segatewayloadbalancer"</span><span class="sxs-lookup"><span data-stu-id="b73ee-106">IsLoadBalancingServer method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="b73ee-107">Bestimmt, ob der Remotedesktop Gateway-Server (RD-Gateway) einen Lastenausgleich durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="b73ee-107">Determines whether the Remote Desktop Gateway (RD Gateway) server can perform load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="b73ee-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b73ee-108">Syntax</span></span>


```mof
uint32 IsLoadBalancingServer(
  [out] boolean LoadBalancing
);
```



## <a name="parameters"></a><span data-ttu-id="b73ee-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b73ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b73ee-110">*Loadbalancing* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b73ee-110">*LoadBalancing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b73ee-111">**True** , wenn der Server einen Lastenausgleich durchführen kann, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="b73ee-111">**TRUE** if the server can perform load balancing, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b73ee-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b73ee-112">Return value</span></span>

<span data-ttu-id="b73ee-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="b73ee-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b73ee-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b73ee-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b73ee-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b73ee-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b73ee-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b73ee-116">Remarks</span></span>

<span data-ttu-id="b73ee-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b73ee-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b73ee-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="b73ee-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b73ee-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="b73ee-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b73ee-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b73ee-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b73ee-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b73ee-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b73ee-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b73ee-122">Requirements</span></span>



| <span data-ttu-id="b73ee-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b73ee-123">Requirement</span></span> | <span data-ttu-id="b73ee-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b73ee-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b73ee-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b73ee-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b73ee-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b73ee-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b73ee-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b73ee-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b73ee-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b73ee-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b73ee-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="b73ee-129">Namespace</span></span><br/>                | <span data-ttu-id="b73ee-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b73ee-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b73ee-131">MOF</span><span class="sxs-lookup"><span data-stu-id="b73ee-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b73ee-132"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="b73ee-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b73ee-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b73ee-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b73ee-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b73ee-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b73ee-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b73ee-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b73ee-136">**Win32-"t- \_ gatewayloadbalancer"**</span><span class="sxs-lookup"><span data-stu-id="b73ee-136">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

