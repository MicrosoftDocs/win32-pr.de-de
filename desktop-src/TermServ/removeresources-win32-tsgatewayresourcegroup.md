---
title: Removeresources-Methode der Win32_TSGatewayResourceGroup-Klasse
description: Entfernt Ressourcen aus der Ressourcengruppe.
ms.assetid: 5f339990-8273-4658-843e-b6b7a85808e1
ms.tgt_platform: multiple
keywords:
- Removeresources-Methode Remotedesktopdienste
- Removeresources-Methode Remotedesktopdienste, Win32_TSGatewayResourceGroup-Klasse
- Win32_TSGatewayResourceGroup-Klasse Remotedesktopdienste, removeresources-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.RemoveResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e3d1cc1e39d8c96833fc6a371741493457a28b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392212"
---
# <a name="removeresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="a6cab-106">Removeresources-Methode der Win32-Klasse "t- \_ gatewayresourcegroup"</span><span class="sxs-lookup"><span data-stu-id="a6cab-106">RemoveResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="a6cab-107">Entfernt Ressourcen aus der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a6cab-107">Removes resources from the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6cab-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6cab-108">Syntax</span></span>


```mof
uint32 RemoveResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="a6cab-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6cab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6cab-110">*Ressourcen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6cab-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6cab-111">Durch Semikolons getrennte Liste der zu entfernenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a6cab-111">Semicolon-separated list of resources to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6cab-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6cab-112">Return value</span></span>

<span data-ttu-id="a6cab-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="a6cab-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a6cab-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a6cab-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a6cab-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a6cab-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a6cab-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6cab-116">Remarks</span></span>

<span data-ttu-id="a6cab-117">Wenn sich mehrere Ressourcen im *Ressourcen* Parameter befinden und eine der Ressourcen nicht verarbeitet werden kann, wird keine der Ressourcen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a6cab-117">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="a6cab-118">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a6cab-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a6cab-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="a6cab-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a6cab-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="a6cab-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a6cab-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a6cab-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a6cab-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a6cab-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6cab-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6cab-123">Requirements</span></span>



| <span data-ttu-id="a6cab-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6cab-124">Requirement</span></span> | <span data-ttu-id="a6cab-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a6cab-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6cab-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6cab-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a6cab-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a6cab-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a6cab-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6cab-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a6cab-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6cab-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a6cab-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="a6cab-130">Namespace</span></span><br/>                | <span data-ttu-id="a6cab-131">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a6cab-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a6cab-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a6cab-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6cab-133"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="a6cab-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6cab-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a6cab-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6cab-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6cab-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a6cab-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6cab-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6cab-137">**Win32-Datei " \_ zgatewayresourcegroup"**</span><span class="sxs-lookup"><span data-stu-id="a6cab-137">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

