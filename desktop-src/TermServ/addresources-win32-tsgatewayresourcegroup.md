---
title: Adresssources-Methode der Win32_TSGatewayResourceGroup-Klasse
description: Fügt der Ressourcengruppe Ressourcen hinzu.
ms.assetid: 3210b468-6b82-4edb-ac8b-95f66a7b9328
ms.tgt_platform: multiple
keywords:
- Adresssources-Methode Remotedesktopdienste
- Adresssources-Methode Remotedesktopdienste, Win32_TSGatewayResourceGroup-Klasse
- Win32_TSGatewayResourceGroup-Klasse Remotedesktopdienste, adresssources-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.AddResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37498accf76b28f16e0de45565916c18ab8d9dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517462"
---
# <a name="addresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="bba23-106">Adresssources-Methode der Win32-Klasse "t- \_ gatewayresourcegroup"</span><span class="sxs-lookup"><span data-stu-id="bba23-106">AddResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="bba23-107">Fügt der Ressourcengruppe Ressourcen hinzu.</span><span class="sxs-lookup"><span data-stu-id="bba23-107">Adds resources to the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba23-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bba23-108">Syntax</span></span>


```mof
uint32 AddResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="bba23-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bba23-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bba23-110">*Ressourcen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bba23-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba23-111">Durch Semikolons getrennte Liste von Ressourcen, die der Ressourcengruppe hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bba23-111">Semicolon-separated list of resources to be added to the resource group.</span></span> <span data-ttu-id="bba23-112">Ein " \* " bedeutet alle Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="bba23-112">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bba23-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bba23-113">Return value</span></span>

<span data-ttu-id="bba23-114">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="bba23-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bba23-115">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bba23-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bba23-116">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bba23-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bba23-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bba23-117">Remarks</span></span>

<span data-ttu-id="bba23-118">Wenn sich mehrere Ressourcen im *Ressourcen* Parameter befinden und eine der Ressourcen nicht verarbeitet werden kann, wird keine der Ressourcen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="bba23-118">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="bba23-119">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="bba23-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="bba23-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="bba23-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bba23-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="bba23-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bba23-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bba23-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bba23-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bba23-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bba23-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bba23-124">Requirements</span></span>



| <span data-ttu-id="bba23-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bba23-125">Requirement</span></span> | <span data-ttu-id="bba23-126">Wert</span><span class="sxs-lookup"><span data-stu-id="bba23-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bba23-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bba23-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bba23-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bba23-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bba23-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bba23-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bba23-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bba23-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bba23-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="bba23-131">Namespace</span></span><br/>                | <span data-ttu-id="bba23-132">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="bba23-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bba23-133">MOF</span><span class="sxs-lookup"><span data-stu-id="bba23-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bba23-134"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="bba23-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bba23-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bba23-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bba23-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bba23-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bba23-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bba23-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba23-138">**Win32-Datei " \_ zgatewayresourcegroup"**</span><span class="sxs-lookup"><span data-stu-id="bba23-138">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

