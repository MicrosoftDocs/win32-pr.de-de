---
title: Deleteallservers-Methode der Win32_TSGatewayLoadBalancer-Klasse
description: Löscht alle Remotedesktop Gateway (RD-Gateway)-Lasten Ausgleichs Server, die Teil der Lastenausgleichs-Farm sind.
ms.assetid: 091ed866-8f2b-47b8-990b-e9a6d7e1194c
ms.tgt_platform: multiple
keywords:
- Deleteallservers-Methode Remotedesktopdienste
- Deleteallservers-Methode Remotedesktopdienste, Win32_TSGatewayLoadBalancer-Klasse
- Win32_TSGatewayLoadBalancer-Klasse Remotedesktopdienste, deleteallservers-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.DeleteAllServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8004b4cfe811394acb328938775fcc9947bbbd19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517453"
---
# <a name="deleteallservers-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="f06e8-106">Deleteallservers-Methode der Win32-Klasse "t- \_ gatewayloadbalancer"</span><span class="sxs-lookup"><span data-stu-id="f06e8-106">DeleteAllServers method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="f06e8-107">Löscht alle Remotedesktop Gateway (RD-Gateway)-Lasten Ausgleichs Server, die Teil der Lastenausgleichs-Farm sind.</span><span class="sxs-lookup"><span data-stu-id="f06e8-107">Deletes all Remote Desktop Gateway (RD Gateway) load-balancing servers that are participating in the load-balancing farm.</span></span>

## <a name="syntax"></a><span data-ttu-id="f06e8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f06e8-108">Syntax</span></span>


```mof
uint32 DeleteAllServers();
```



## <a name="parameters"></a><span data-ttu-id="f06e8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f06e8-109">Parameters</span></span>

<span data-ttu-id="f06e8-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f06e8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f06e8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f06e8-111">Return value</span></span>

<span data-ttu-id="f06e8-112">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="f06e8-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f06e8-113">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f06e8-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f06e8-114">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f06e8-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f06e8-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f06e8-115">Remarks</span></span>

<span data-ttu-id="f06e8-116">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f06e8-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f06e8-117">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="f06e8-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f06e8-118">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="f06e8-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f06e8-119">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f06e8-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f06e8-120">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f06e8-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f06e8-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f06e8-121">Requirements</span></span>



| <span data-ttu-id="f06e8-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f06e8-122">Requirement</span></span> | <span data-ttu-id="f06e8-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f06e8-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f06e8-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f06e8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f06e8-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f06e8-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f06e8-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f06e8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f06e8-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f06e8-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f06e8-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="f06e8-128">Namespace</span></span><br/>                | <span data-ttu-id="f06e8-129">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f06e8-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f06e8-130">MOF</span><span class="sxs-lookup"><span data-stu-id="f06e8-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f06e8-131"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="f06e8-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="f06e8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f06e8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f06e8-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f06e8-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f06e8-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f06e8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f06e8-135">**Win32-"t- \_ gatewayloadbalancer"**</span><span class="sxs-lookup"><span data-stu-id="f06e8-135">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

