---
title: Create-Methode der Win32_TSGatewayResourceGroup-Klasse
description: Erstellt eine Ressourcengruppe.
ms.assetid: 715e6086-1c7d-4b20-983a-3ab98e875ca5
ms.tgt_platform: multiple
keywords:
- Create-Methode Remotedesktopdienste
- Create Method Remotedesktopdienste, Win32_TSGatewayResourceGroup-Klasse
- Win32_TSGatewayResourceGroup Klasse Remotedesktopdienste, Methode erstellen
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9c5179967c143faa36763b7a2aabb8849d2f13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040272"
---
# <a name="create-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="0b8a6-106">Create-Methode der Win32-Klasse "t- \_ gatewayresourcegroup"</span><span class="sxs-lookup"><span data-stu-id="0b8a6-106">Create method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="0b8a6-107">Erstellt eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0b8a6-107">Creates a resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b8a6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b8a6-108">Syntax</span></span>


```mof
uint32 Create(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="0b8a6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b8a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b8a6-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b8a6-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b8a6-111">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0b8a6-111">Name of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="0b8a6-112">*Beschreibung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b8a6-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b8a6-113">Beschreibung der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0b8a6-113">Description of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="0b8a6-114">*Ressourcen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b8a6-114">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b8a6-115">Durch Semikolons getrennte Liste von Ressourcen in dieser Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0b8a6-115">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="0b8a6-116">Ein " \* " bedeutet alle Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="0b8a6-116">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b8a6-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b8a6-117">Return value</span></span>

<span data-ttu-id="0b8a6-118">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="0b8a6-118">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0b8a6-119">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0b8a6-119">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0b8a6-120">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0b8a6-120">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0b8a6-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b8a6-121">Remarks</span></span>

<span data-ttu-id="0b8a6-122">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="0b8a6-122">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0b8a6-123">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="0b8a6-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0b8a6-124">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="0b8a6-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0b8a6-125">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0b8a6-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0b8a6-126">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0b8a6-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b8a6-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b8a6-127">Requirements</span></span>



| <span data-ttu-id="0b8a6-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b8a6-128">Requirement</span></span> | <span data-ttu-id="0b8a6-129">Wert</span><span class="sxs-lookup"><span data-stu-id="0b8a6-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b8a6-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b8a6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0b8a6-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0b8a6-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0b8a6-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b8a6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0b8a6-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b8a6-133">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0b8a6-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b8a6-134">Namespace</span></span><br/>                | <span data-ttu-id="0b8a6-135">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0b8a6-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0b8a6-136">MOF</span><span class="sxs-lookup"><span data-stu-id="0b8a6-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b8a6-137"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="0b8a6-137"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b8a6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0b8a6-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b8a6-139"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b8a6-139"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0b8a6-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b8a6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b8a6-141">**Win32-Datei " \_ zgatewayresourcegroup"**</span><span class="sxs-lookup"><span data-stu-id="0b8a6-141">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

