---
title: SetName-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt einen neuen Namen für diese Remotedesktop Verbindungs Autorisierungs Richtlinie fest (RD \ 160; Cap).
ms.assetid: 4a3b71d4-9b1c-46ea-b14a-fcbe32af37b5
ms.tgt_platform: multiple
keywords:
- SetName-Methode Remotedesktopdienste
- SetName-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, SetName-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15fa4c374f5686f8cddbe99b5a464e6f84b4a12a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741281"
---
# <a name="setname-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="a0a61-106">SetName-Methode der Win32- \_ Klasse "tgatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="a0a61-106">SetName method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="a0a61-107">Legt einen neuen Namen für diese Remotedesktop Verbindungs Autorisierungs Richtlinie (RD-CAP) fest.</span><span class="sxs-lookup"><span data-stu-id="a0a61-107">Sets a new name for this Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="a0a61-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0a61-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="a0a61-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0a61-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0a61-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0a61-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a61-111">Name der RD-Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="a0a61-111">Name of the RD CAP.</span></span> <span data-ttu-id="a0a61-112">Der Name muss 64 Zeichen oder kleiner, eindeutig (Groß-/Kleinschreibung wird ignoriert) sein und darf die folgenden reservierten Zeichen nicht enthalten:</span><span class="sxs-lookup"><span data-stu-id="a0a61-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="a0a61-113"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="a0a61-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="a0a61-114">\*\[Registerkarte\]</span><span class="sxs-lookup"><span data-stu-id="a0a61-114">\* \[TAB\]</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0a61-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0a61-115">Return value</span></span>

<span data-ttu-id="a0a61-116">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="a0a61-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a0a61-117">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a0a61-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a0a61-118">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a0a61-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a0a61-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0a61-119">Remarks</span></span>

<span data-ttu-id="a0a61-120">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a0a61-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a0a61-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="a0a61-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a0a61-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="a0a61-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a0a61-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a0a61-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a0a61-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a0a61-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0a61-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0a61-125">Requirements</span></span>



| <span data-ttu-id="a0a61-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0a61-126">Requirement</span></span> | <span data-ttu-id="a0a61-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a0a61-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a61-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0a61-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a0a61-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a0a61-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a0a61-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a0a61-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a0a61-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0a61-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a0a61-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="a0a61-132">Namespace</span></span><br/>                | <span data-ttu-id="a0a61-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a0a61-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a0a61-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a0a61-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0a61-135"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="a0a61-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0a61-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a0a61-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0a61-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0a61-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a0a61-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0a61-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0a61-139">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="a0a61-139">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

