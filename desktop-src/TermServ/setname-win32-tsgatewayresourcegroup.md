---
title: SetName-Methode der Win32_TSGatewayResourceGroup-Klasse
description: Legt die Name-Eigenschaft für die Ressourcengruppe fest.
ms.assetid: 2c2fe1b6-5826-490e-aec2-479a0191e215
ms.tgt_platform: multiple
keywords:
- SetName-Methode Remotedesktopdienste
- SetName-Methode Remotedesktopdienste, Win32_TSGatewayResourceGroup-Klasse
- Win32_TSGatewayResourceGroup-Klasse Remotedesktopdienste, SetName-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac9ea16eb82896bb8fad67fff7ed849308100726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858898"
---
# <a name="setname-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="b7824-106">SetName-Methode der Win32- \_ Klasse "tgatewayresourcegroup"</span><span class="sxs-lookup"><span data-stu-id="b7824-106">SetName method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="b7824-107">Legt die **Name** -Eigenschaft für die Ressourcengruppe fest.</span><span class="sxs-lookup"><span data-stu-id="b7824-107">Sets the **Name** property for the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7824-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7824-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="b7824-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7824-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7824-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7824-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7824-111">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b7824-111">Name of the resource group.</span></span> <span data-ttu-id="b7824-112">Der Name muss 64 Zeichen oder kleiner, eindeutig (Groß-/Kleinschreibung wird ignoriert) sein und darf die folgenden reservierten Zeichen nicht enthalten:</span><span class="sxs-lookup"><span data-stu-id="b7824-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="b7824-113"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="b7824-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="b7824-114">\*\[Registerkarte\]</span><span class="sxs-lookup"><span data-stu-id="b7824-114">\* \[TAB\]</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7824-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7824-115">Return value</span></span>

<span data-ttu-id="b7824-116">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="b7824-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b7824-117">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b7824-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b7824-118">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b7824-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b7824-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7824-119">Remarks</span></span>

<span data-ttu-id="b7824-120">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b7824-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b7824-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="b7824-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b7824-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="b7824-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b7824-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7824-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b7824-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b7824-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7824-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7824-125">Requirements</span></span>



| <span data-ttu-id="b7824-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7824-126">Requirement</span></span> | <span data-ttu-id="b7824-127">Wert</span><span class="sxs-lookup"><span data-stu-id="b7824-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7824-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7824-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b7824-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b7824-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b7824-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7824-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b7824-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7824-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b7824-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7824-132">Namespace</span></span><br/>                | <span data-ttu-id="b7824-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b7824-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b7824-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b7824-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7824-135"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="b7824-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7824-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b7824-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7824-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7824-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b7824-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7824-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7824-139">**Win32-Datei " \_ zgatewayresourcegroup"**</span><span class="sxs-lookup"><span data-stu-id="b7824-139">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

