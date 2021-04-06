---
title: Setservers-Methode der Win32_TSGatewayLoadBalancer-Klasse
description: Legt die Server-Eigenschaft mit der Liste der Remotedesktop Gateway-Server (RD-Gateway) für den Lastenausgleich fest.
ms.assetid: c82de8e2-301b-465d-b375-038b8a480cde
ms.tgt_platform: multiple
keywords:
- Setservers-Methode Remotedesktopdienste
- Setservers-Methode Remotedesktopdienste, Win32_TSGatewayLoadBalancer-Klasse
- Win32_TSGatewayLoadBalancer-Klasse Remotedesktopdienste, setservers-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.SetServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b28d1123ce82844fb501f3562014b93337502b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742369"
---
# <a name="setservers-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="b4321-106">Setservers-Methode der Win32- \_ Klasse "segatewayloadbalancer"</span><span class="sxs-lookup"><span data-stu-id="b4321-106">SetServers method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="b4321-107">Legt die **Server** -Eigenschaft mit der Liste der Remotedesktop Gateway-Server (RD-Gateway) für den Lastenausgleich fest.</span><span class="sxs-lookup"><span data-stu-id="b4321-107">Sets the **Servers** property with the list of Remote Desktop Gateway (RD Gateway) load-balancing servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4321-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4321-108">Syntax</span></span>


```mof
uint32 SetServers(
  [in] string Servers
);
```



## <a name="parameters"></a><span data-ttu-id="b4321-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4321-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4321-110">*Server* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4321-110">*Servers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4321-111">Durch Semikolons getrennte Liste der RD-Gateway Lasten Ausgleichs Server.</span><span class="sxs-lookup"><span data-stu-id="b4321-111">Semicolon-separated list of RD Gateway load-balancing servers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4321-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4321-112">Return value</span></span>

<span data-ttu-id="b4321-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="b4321-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b4321-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b4321-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b4321-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b4321-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b4321-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4321-116">Remarks</span></span>

<span data-ttu-id="b4321-117">Wenn sich mehrere Server im *Server* -Parameter befinden und einer der Server nicht verarbeitet werden kann, wird keiner der Server verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b4321-117">If multiple servers are in the *Servers* parameter and one of the servers cannot be processed, none of the servers will be processed.</span></span>

<span data-ttu-id="b4321-118">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b4321-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b4321-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="b4321-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b4321-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="b4321-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b4321-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b4321-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b4321-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b4321-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4321-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4321-123">Requirements</span></span>



| <span data-ttu-id="b4321-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4321-124">Requirement</span></span> | <span data-ttu-id="b4321-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b4321-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4321-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4321-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b4321-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b4321-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b4321-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4321-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b4321-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4321-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b4321-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="b4321-130">Namespace</span></span><br/>                | <span data-ttu-id="b4321-131">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b4321-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b4321-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b4321-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4321-133"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="b4321-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4321-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b4321-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4321-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4321-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b4321-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4321-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4321-137">**Win32-"t- \_ gatewayloadbalancer"**</span><span class="sxs-lookup"><span data-stu-id="b4321-137">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

