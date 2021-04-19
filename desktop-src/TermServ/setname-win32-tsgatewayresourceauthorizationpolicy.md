---
title: SetName-Methode der Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Legt die Name-Eigenschaft für die Remotedesktop-Ressourcen Autorisierungs Richtlinie fest (RD \ 160; Rap).
ms.assetid: 3a652ece-11fe-4aa7-913d-39ef96ab1633
ms.tgt_platform: multiple
keywords:
- SetName-Methode Remotedesktopdienste
- SetName-Methode Remotedesktopdienste, Win32_TSGatewayResourceAuthorizationPolicy-Klasse
- Win32_TSGatewayResourceAuthorizationPolicy-Klasse Remotedesktopdienste, SetName-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7e595472302d97e91026b3a84dc466e248ef5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342432"
---
# <a name="setname-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="870cd-106">SetName-Methode der Win32- \_ Klasse "tgatewayresourceauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="870cd-106">SetName method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="870cd-107">Legt die **Name** -Eigenschaft für die Remotedesktop-Ressourcen Autorisierungs Richtlinie (RD-RAP) fest.</span><span class="sxs-lookup"><span data-stu-id="870cd-107">Sets the **Name** property for the Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="870cd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="870cd-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="870cd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="870cd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="870cd-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="870cd-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="870cd-111">Name der RD-RAP.</span><span class="sxs-lookup"><span data-stu-id="870cd-111">Name of the RD RAP.</span></span> <span data-ttu-id="870cd-112">Der Name muss 64 Zeichen oder kleiner, eindeutig (Groß-/Kleinschreibung wird ignoriert) sein und darf die folgenden reservierten Zeichen nicht enthalten:</span><span class="sxs-lookup"><span data-stu-id="870cd-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="870cd-113"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="870cd-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="870cd-114">\*\[Registerkarte\]</span><span class="sxs-lookup"><span data-stu-id="870cd-114">\* \[TAB\]</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="870cd-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="870cd-115">Return value</span></span>

<span data-ttu-id="870cd-116">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="870cd-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="870cd-117">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="870cd-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="870cd-118">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="870cd-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="870cd-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="870cd-119">Remarks</span></span>

<span data-ttu-id="870cd-120">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="870cd-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="870cd-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="870cd-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="870cd-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="870cd-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="870cd-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="870cd-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="870cd-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="870cd-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="870cd-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="870cd-125">Requirements</span></span>



| <span data-ttu-id="870cd-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="870cd-126">Requirement</span></span> | <span data-ttu-id="870cd-127">Wert</span><span class="sxs-lookup"><span data-stu-id="870cd-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="870cd-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="870cd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="870cd-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="870cd-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="870cd-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="870cd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="870cd-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="870cd-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="870cd-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="870cd-132">Namespace</span></span><br/>                | <span data-ttu-id="870cd-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="870cd-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="870cd-134">MOF</span><span class="sxs-lookup"><span data-stu-id="870cd-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="870cd-135"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="870cd-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="870cd-136">DLL</span><span class="sxs-lookup"><span data-stu-id="870cd-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="870cd-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="870cd-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="870cd-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="870cd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="870cd-139">**Win32- \_ faigatewayresourceauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="870cd-139">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

