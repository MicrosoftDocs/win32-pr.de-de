---
title: Removecomputergroupnames-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Entfernt die angegebenen Computer Gruppennamen aus der computergroupnames-Eigenschaft.
ms.assetid: 5f4e566a-1a2e-459d-ab6c-53ffd42271d8
ms.tgt_platform: multiple
keywords:
- Removecomputergroupnames-Methode Remotedesktopdienste
- Removecomputergroupnames-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, removecomputergroupnames-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.RemoveComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988ec281798fba0257883eebfb60ac199b0f3c1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040383"
---
# <a name="removecomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="e7e88-106">Removecomputergroupnames-Methode der Win32- \_ Klasse "sgatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="e7e88-106">RemoveComputerGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="e7e88-107">Entfernt die angegebenen Computer Gruppennamen aus der **computergroupnames** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e7e88-107">Removes specified computer group names from the **ComputerGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7e88-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7e88-108">Syntax</span></span>


```mof
uint32 RemoveComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="e7e88-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7e88-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7e88-110">*Computer groupnames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7e88-110">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e88-111">Eine durch Semikolons getrennte Liste von Computer Gruppennamen, die aus der **computergroupnames** -Eigenschaft entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e7e88-111">Semicolon-separated list of computer group names to remove from the **ComputerGroupNames** property.</span></span> <span data-ttu-id="e7e88-112">Computer Gruppennamen müssen im Format " *Domäne \\ Computername*" vorliegen.</span><span class="sxs-lookup"><span data-stu-id="e7e88-112">Computer group names should be of the format *Domain\\ComputerGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7e88-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7e88-113">Return value</span></span>

<span data-ttu-id="e7e88-114">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="e7e88-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e7e88-115">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e7e88-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e7e88-116">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e7e88-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7e88-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7e88-117">Remarks</span></span>

<span data-ttu-id="e7e88-118">Wenn sich mehrere Computer Gruppennamen im *computergroupnames* -Parameter befinden und einer der Namen nicht verarbeitet werden kann, wird keiner der Namen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e7e88-118">If multiple computer group names are in the *ComputerGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="e7e88-119">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e7e88-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e7e88-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="e7e88-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e7e88-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="e7e88-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e7e88-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e7e88-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e7e88-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e7e88-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7e88-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7e88-124">Requirements</span></span>



| <span data-ttu-id="e7e88-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7e88-125">Requirement</span></span> | <span data-ttu-id="e7e88-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e7e88-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e88-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7e88-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e7e88-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e7e88-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e7e88-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7e88-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e7e88-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7e88-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e7e88-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7e88-131">Namespace</span></span><br/>                | <span data-ttu-id="e7e88-132">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e7e88-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e7e88-133">MOF</span><span class="sxs-lookup"><span data-stu-id="e7e88-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7e88-134"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="e7e88-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7e88-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e7e88-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7e88-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7e88-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e7e88-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7e88-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7e88-138">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="e7e88-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

