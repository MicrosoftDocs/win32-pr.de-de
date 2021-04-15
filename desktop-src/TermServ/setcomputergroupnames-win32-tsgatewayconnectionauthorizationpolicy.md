---
title: Setcomputergroupnames-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die computergroupnames-Eigenschaft fest.
ms.assetid: dd6747df-140f-4eeb-857b-d14f8713586c
ms.tgt_platform: multiple
keywords:
- Setcomputergroupnames-Methode Remotedesktopdienste
- Setcomputergroupnames-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, setcomputergroupnames-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99c29ce37aeb8bfad0ae77197c7364b0135fa99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391865"
---
# <a name="setcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="5ecc6-106">Setcomputergroupnames-Methode der Win32- \_ Klasse "sgatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="5ecc6-106">SetComputerGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="5ecc6-107">Legt die **computergroupnames** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="5ecc6-107">Sets the **ComputerGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ecc6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ecc6-108">Syntax</span></span>


```mof
uint32 SetComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="5ecc6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ecc6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ecc6-110">*Computer groupnames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ecc6-110">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ecc6-111">Liste von durch Semikolons getrennten Computer Gruppennamen.</span><span class="sxs-lookup"><span data-stu-id="5ecc6-111">List of semicolon-separated computer group names.</span></span> <span data-ttu-id="5ecc6-112">Dieser Wert kann leer sein.</span><span class="sxs-lookup"><span data-stu-id="5ecc6-112">This value can be empty.</span></span> <span data-ttu-id="5ecc6-113">Die Namen weisen das Format *Domäne \\ computergroupname* auf.</span><span class="sxs-lookup"><span data-stu-id="5ecc6-113">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="5ecc6-114">Wenn ein Wert angegeben wird, muss der Client Computer zu einer dieser Computer Gruppen gehören, damit der Benutzer auf den RD-Gateway Server zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="5ecc6-114">If a value is specified, the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ecc6-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ecc6-115">Return value</span></span>

<span data-ttu-id="5ecc6-116">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="5ecc6-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5ecc6-117">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5ecc6-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5ecc6-118">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5ecc6-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5ecc6-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ecc6-119">Remarks</span></span>

<span data-ttu-id="5ecc6-120">Wenn sich mehrere Computer Gruppennamen im *computergroupnames* -Parameter befinden und einer der Namen nicht verarbeitet werden kann, wird keiner der Namen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="5ecc6-120">If multiple computer group names are in the *ComputerGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="5ecc6-121">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="5ecc6-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5ecc6-122">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="5ecc6-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5ecc6-123">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="5ecc6-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5ecc6-124">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5ecc6-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5ecc6-125">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5ecc6-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ecc6-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ecc6-126">Requirements</span></span>



| <span data-ttu-id="5ecc6-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ecc6-127">Requirement</span></span> | <span data-ttu-id="5ecc6-128">Wert</span><span class="sxs-lookup"><span data-stu-id="5ecc6-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ecc6-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ecc6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5ecc6-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5ecc6-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5ecc6-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ecc6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5ecc6-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ecc6-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5ecc6-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ecc6-133">Namespace</span></span><br/>                | <span data-ttu-id="5ecc6-134">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5ecc6-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5ecc6-135">MOF</span><span class="sxs-lookup"><span data-stu-id="5ecc6-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ecc6-136"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="5ecc6-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ecc6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5ecc6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ecc6-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ecc6-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5ecc6-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ecc6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ecc6-140">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="5ecc6-140">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

