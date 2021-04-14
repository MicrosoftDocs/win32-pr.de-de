---
title: Die Methode "Methode" der Win32_TSGatewayResourceGroup Klasse
description: Legt die Ressourcen Eigenschaft für diese Ressourcengruppe fest.
ms.assetid: 0043ee04-26d1-4907-87cc-a15f72cb0b93
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode ""
- Methoden Remotedesktopdienste der Methode "Win32_TSGatewayResourceGroup"
- Win32_TSGatewayResourceGroup-Klasse Remotedesktopdienste, Methode "-Methode"
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f2ca14597fc7d6ce3660e6e180bf93dfd86cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391720"
---
# <a name="setresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="ba172-106">Die ""-Methode der Win32- \_ Klasse "Klasse-gatewayresourcegroup"</span><span class="sxs-lookup"><span data-stu-id="ba172-106">SetResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="ba172-107">Legt die **Ressourcen** Eigenschaft für diese Ressourcengruppe fest.</span><span class="sxs-lookup"><span data-stu-id="ba172-107">Sets the **Resources** property for this resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba172-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba172-108">Syntax</span></span>


```mof
uint32 SetResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="ba172-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba172-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba172-110">*Ressourcen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba172-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba172-111">Durch Semikolons getrennte Liste von Ressourcen in dieser Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ba172-111">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="ba172-112">Ein " \* " bedeutet alle Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="ba172-112">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba172-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba172-113">Return value</span></span>

<span data-ttu-id="ba172-114">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="ba172-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ba172-115">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ba172-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ba172-116">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ba172-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ba172-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba172-117">Remarks</span></span>

<span data-ttu-id="ba172-118">Wenn sich mehrere Ressourcen im *Ressourcen* Parameter befinden und eine der Ressourcen nicht verarbeitet werden kann, wird keine der Ressourcen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ba172-118">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="ba172-119">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ba172-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ba172-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="ba172-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ba172-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="ba172-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ba172-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ba172-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ba172-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ba172-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba172-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba172-124">Requirements</span></span>



| <span data-ttu-id="ba172-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba172-125">Requirement</span></span> | <span data-ttu-id="ba172-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ba172-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba172-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba172-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ba172-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ba172-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ba172-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba172-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ba172-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba172-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ba172-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba172-131">Namespace</span></span><br/>                | <span data-ttu-id="ba172-132">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ba172-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="ba172-133">MOF</span><span class="sxs-lookup"><span data-stu-id="ba172-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba172-134"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="ba172-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba172-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ba172-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba172-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba172-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ba172-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba172-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba172-138">**Win32-Datei " \_ zgatewayresourcegroup"**</span><span class="sxs-lookup"><span data-stu-id="ba172-138">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

