---
title: Die Methode "* tresourcegroup" der Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Legt den Typ und den Namen der Ressourcengruppe fest.
ms.assetid: a3dd0ffa-a39b-46f9-8317-fcc90a8afcd1
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "* tresourcegroup"
- Methode Remotedesktopdienste der Methode "Win32_TSGatewayResourceAuthorizationPolicy"
- Win32_TSGatewayResourceAuthorizationPolicy Klasse Remotedesktopdienste, Methode "*"
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetResourceGroup
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22c2ceacbbbfc40372d0f0d084cf6525f754934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859062"
---
# <a name="setresourcegroup-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="193be-106">Die Methode "\* tresourcegroup" der Win32- \_ Klasse "zgatewayresourceauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="193be-106">SetResourceGroup method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="193be-107">Legt den Typ und den Namen der Ressourcengruppe fest.</span><span class="sxs-lookup"><span data-stu-id="193be-107">Sets the resource group type and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="193be-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="193be-108">Syntax</span></span>


```mof
uint32 SetResourceGroup(
  [in] string ResourceGroupName,
  [in] string ResourceGroupType
);
```



## <a name="parameters"></a><span data-ttu-id="193be-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="193be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="193be-110">*Resourcegroupname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="193be-110">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="193be-111">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="193be-111">Resource group name.</span></span> <span data-ttu-id="193be-112">Dieser Wert ersetzt die vorhandene **resourcegroupname** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="193be-112">This value replaces the existing **ResourceGroupName** property.</span></span>

</dd> <dt>

<span data-ttu-id="193be-113">*Resourcegrouptype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="193be-113">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="193be-114">Identifiziert den Typ der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="193be-114">Identifies the type of the resource group.</span></span> <span data-ttu-id="193be-115">Dieser Wert ersetzt die vorhandene **resourcegrouptype** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="193be-115">This value replaces the existing **ResourceGroupType** property.</span></span>

<dt>

<span data-ttu-id="193be-116">Sorgte</span><span class="sxs-lookup"><span data-stu-id="193be-116">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="193be-117">Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="193be-117">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="193be-118">Gewöhnt</span><span class="sxs-lookup"><span data-stu-id="193be-118">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="193be-119">Computer Gruppe, wie in Active Directory Domain Services gespeichert.</span><span class="sxs-lookup"><span data-stu-id="193be-119">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="193be-120">Allen</span><span class="sxs-lookup"><span data-stu-id="193be-120">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="193be-121">Alle Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="193be-121">All resources.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="193be-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="193be-122">Return value</span></span>

<span data-ttu-id="193be-123">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="193be-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="193be-124">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="193be-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="193be-125">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="193be-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="193be-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="193be-126">Remarks</span></span>

<span data-ttu-id="193be-127">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="193be-127">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="193be-128">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="193be-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="193be-129">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="193be-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="193be-130">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="193be-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="193be-131">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="193be-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="193be-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="193be-132">Requirements</span></span>



| <span data-ttu-id="193be-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="193be-133">Requirement</span></span> | <span data-ttu-id="193be-134">Wert</span><span class="sxs-lookup"><span data-stu-id="193be-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="193be-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="193be-135">Minimum supported client</span></span><br/> | <span data-ttu-id="193be-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="193be-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="193be-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="193be-137">Minimum supported server</span></span><br/> | <span data-ttu-id="193be-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="193be-138">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="193be-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="193be-139">Namespace</span></span><br/>                | <span data-ttu-id="193be-140">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="193be-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="193be-141">MOF</span><span class="sxs-lookup"><span data-stu-id="193be-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="193be-142"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="193be-142"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="193be-143">DLL</span><span class="sxs-lookup"><span data-stu-id="193be-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="193be-144"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="193be-144"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="193be-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="193be-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="193be-146">**Win32- \_ faigatewayresourceauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="193be-146">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

