---
title: Setsecureidallowed-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Diese Methode ist für eine spätere Verwendung vorgesehen.
ms.assetid: 9f49e69a-c004-4e3e-b238-69865e3bf00b
ms.tgt_platform: multiple
keywords:
- Setsecureidallowed-Methode Remotedesktopdienste
- Setsecureidallowed-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, setsecureidallowed-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSecureIdAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e61c158a7dfcafb6d1d5ac66833e42284b818d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344071"
---
# <a name="setsecureidallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="e9001-106">Setsecureidallowed-Methode der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="e9001-106">SetSecureIdAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="e9001-107">Diese Methode ist für eine spätere Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="e9001-107">This method is reserved for future use.</span></span>

<span data-ttu-id="e9001-108">Legt die **secureidallowed** -Eigenschaft fest, die für die zukünftige Verwendung reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="e9001-108">Sets the **SecureIdAllowed** property, which is reserved for future use.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9001-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9001-109">Syntax</span></span>


```mof
uint32 SetSecureIdAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="e9001-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9001-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9001-111">*Zulässig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9001-111">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9001-112">Neuer **secureidzulässiger** Wert.</span><span class="sxs-lookup"><span data-stu-id="e9001-112">New **SecureIdAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9001-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9001-113">Return value</span></span>

<span data-ttu-id="e9001-114">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="e9001-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e9001-115">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e9001-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e9001-116">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e9001-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e9001-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9001-117">Remarks</span></span>

<span data-ttu-id="e9001-118">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e9001-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e9001-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="e9001-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e9001-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="e9001-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e9001-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e9001-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e9001-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e9001-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9001-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9001-123">Requirements</span></span>



| <span data-ttu-id="e9001-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9001-124">Requirement</span></span> | <span data-ttu-id="e9001-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e9001-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9001-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9001-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e9001-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e9001-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e9001-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9001-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e9001-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9001-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e9001-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9001-130">Namespace</span></span><br/>                | <span data-ttu-id="e9001-131">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e9001-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e9001-132">MOF</span><span class="sxs-lookup"><span data-stu-id="e9001-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9001-133"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="e9001-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9001-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e9001-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9001-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9001-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e9001-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9001-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9001-137">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="e9001-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

