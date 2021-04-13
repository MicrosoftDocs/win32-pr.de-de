---
title: Update-Methode der Win32_TSGatewayResourceGroup-Klasse
description: Aktualisiert die Ressourcengruppe.
ms.assetid: b5927046-f461-41cd-861b-0fd77f2008e5
ms.tgt_platform: multiple
keywords:
- Update-Methode Remotedesktopdienste
- Update-Methode Remotedesktopdienste, Win32_TSGatewayResourceGroup-Klasse
- Win32_TSGatewayResourceGroup-Klasse Remotedesktopdienste, Update-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a7b1610fc14aa522fa4d8b7caf03fccd7b37375
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391962"
---
# <a name="update-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="a35b0-106">Update-Methode der Win32-Klasse "t- \_ gatewayresourcegroup"</span><span class="sxs-lookup"><span data-stu-id="a35b0-106">Update method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="a35b0-107">Aktualisiert die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a35b0-107">Updates the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="a35b0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a35b0-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="a35b0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a35b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a35b0-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a35b0-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a35b0-111">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a35b0-111">Name of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="a35b0-112">*Beschreibung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a35b0-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a35b0-113">Beschreibung der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a35b0-113">Description of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="a35b0-114">*Ressourcen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a35b0-114">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a35b0-115">Durch Semikolons getrennte Liste von Ressourcen in dieser Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a35b0-115">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="a35b0-116">Ein " \* " bedeutet alle Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a35b0-116">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a35b0-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a35b0-117">Return value</span></span>

<span data-ttu-id="a35b0-118">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="a35b0-118">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a35b0-119">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a35b0-119">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a35b0-120">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a35b0-120">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a35b0-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a35b0-121">Remarks</span></span>

<span data-ttu-id="a35b0-122">Wenn sich mehrere Ressourcen im *Ressourcen* Parameter befinden und eine der Ressourcen nicht verarbeitet werden kann, wird keine der Ressourcen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a35b0-122">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="a35b0-123">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a35b0-123">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a35b0-124">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="a35b0-124">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a35b0-125">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="a35b0-125">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a35b0-126">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a35b0-126">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a35b0-127">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a35b0-127">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a35b0-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a35b0-128">Requirements</span></span>



| <span data-ttu-id="a35b0-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a35b0-129">Requirement</span></span> | <span data-ttu-id="a35b0-130">Wert</span><span class="sxs-lookup"><span data-stu-id="a35b0-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a35b0-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a35b0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a35b0-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a35b0-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a35b0-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a35b0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a35b0-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a35b0-134">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a35b0-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="a35b0-135">Namespace</span></span><br/>                | <span data-ttu-id="a35b0-136">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a35b0-136">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a35b0-137">MOF</span><span class="sxs-lookup"><span data-stu-id="a35b0-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a35b0-138"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="a35b0-138"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a35b0-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a35b0-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a35b0-140"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a35b0-140"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a35b0-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a35b0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a35b0-142">**Win32-Datei " \_ zgatewayresourcegroup"**</span><span class="sxs-lookup"><span data-stu-id="a35b0-142">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

