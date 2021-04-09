---
title: Setcookieauthenticationallowed-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die cookieauthenticationallowed-Eigenschaft fest.
ms.assetid: 481b89cb-d73b-4dae-941c-a629c2ae5ac4
ms.tgt_platform: multiple
keywords:
- Setcookieauthenticationallowed-Methode Remotedesktopdienste
- Setcookieauthenticationallowed-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, setcookieauthenticationallowed-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetCookieAuthenticationAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9293123ab6ce5b1ddcdb172f9258ba73b23fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103154"
---
# <a name="setcookieauthenticationallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="9f23f-106">Setcookieauthenticationallowed-Methode der Win32- \_ Klasse "sgatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="9f23f-106">SetCookieAuthenticationAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="9f23f-107">Legt die **cookieauthenticationallowed** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="9f23f-107">Sets the **CookieAuthenticationAllowed** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f23f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f23f-108">Syntax</span></span>


```mof
uint32 SetCookieAuthenticationAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="9f23f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f23f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f23f-110">*Zulässig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f23f-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f23f-111">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="9f23f-111">Type: **boolean**</span></span>

<span data-ttu-id="9f23f-112">Der neue Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="9f23f-112">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f23f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f23f-113">Return value</span></span>

<span data-ttu-id="9f23f-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f23f-114">Type: **uint32**</span></span>

<span data-ttu-id="9f23f-115">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="9f23f-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9f23f-116">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9f23f-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9f23f-117">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9f23f-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f23f-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f23f-118">Remarks</span></span>

<span data-ttu-id="9f23f-119">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9f23f-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9f23f-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="9f23f-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9f23f-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="9f23f-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9f23f-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9f23f-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9f23f-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9f23f-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f23f-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f23f-124">Requirements</span></span>



| <span data-ttu-id="9f23f-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f23f-125">Requirement</span></span> | <span data-ttu-id="9f23f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="9f23f-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f23f-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f23f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9f23f-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9f23f-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9f23f-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f23f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9f23f-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9f23f-130">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="9f23f-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f23f-131">Namespace</span></span><br/>                | <span data-ttu-id="9f23f-132">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9f23f-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9f23f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="9f23f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f23f-134"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="9f23f-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f23f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9f23f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f23f-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f23f-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9f23f-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f23f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f23f-138">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="9f23f-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

