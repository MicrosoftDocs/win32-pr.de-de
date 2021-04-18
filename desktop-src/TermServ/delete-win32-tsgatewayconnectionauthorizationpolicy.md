---
title: Delete-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Löscht die aktuelle Remotedesktop Verbindungs Autorisierungs Richtlinie (RD \ 160; Cap).
ms.assetid: aef7216a-4459-492b-95cb-87ea760dcde9
ms.tgt_platform: multiple
keywords:
- Delete-Methode Remotedesktopdienste
- Delete-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, DELETE-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Delete
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26b99cf7856c31f2e45f026631beb974e61c481f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338123"
---
# <a name="delete-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="a8315-106">Delete-Methode der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="a8315-106">Delete method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="a8315-107">Löscht die aktuelle Remotedesktop Verbindungs Autorisierungs Richtlinie (RD-CAP).</span><span class="sxs-lookup"><span data-stu-id="a8315-107">Deletes the current Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="a8315-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8315-108">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="a8315-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8315-109">Parameters</span></span>

<span data-ttu-id="a8315-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a8315-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8315-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8315-111">Return value</span></span>

<span data-ttu-id="a8315-112">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="a8315-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a8315-113">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a8315-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a8315-114">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a8315-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a8315-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8315-115">Remarks</span></span>

<span data-ttu-id="a8315-116">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a8315-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a8315-117">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="a8315-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a8315-118">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="a8315-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a8315-119">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a8315-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a8315-120">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a8315-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8315-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8315-121">Requirements</span></span>



| <span data-ttu-id="a8315-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8315-122">Requirement</span></span> | <span data-ttu-id="a8315-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a8315-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8315-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8315-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a8315-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a8315-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a8315-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8315-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a8315-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8315-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a8315-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8315-128">Namespace</span></span><br/>                | <span data-ttu-id="a8315-129">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a8315-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a8315-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a8315-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8315-131"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="a8315-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8315-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a8315-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8315-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8315-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a8315-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8315-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8315-135">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="a8315-135">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

