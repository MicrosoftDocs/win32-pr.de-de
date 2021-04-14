---
title: Die Methode "sstiessiontimeout" der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die Eigenschaften sessiontimeout und sessiontimeoutaction fest.
ms.assetid: 11491c97-3ef8-46c1-9504-696c613e374e
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "
- Methode Remotedesktopdienste der Methode "Win32_TSGatewayConnectionAuthorizationPolicy"
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, Methode "-Methode"
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSessionTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e544b59ae4fe0b74d0c120e6884ab81743cac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518161"
---
# <a name="setsessiontimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="738e3-106">Die Methode "stionessiontimeout" der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="738e3-106">SetSessionTimeout method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="738e3-107">Legt die Eigenschaften **sessiontimeout** und **sessiontimeoutaction** fest.</span><span class="sxs-lookup"><span data-stu-id="738e3-107">Sets the **SessionTimeout** and **SessionTimeoutAction** properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="738e3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="738e3-108">Syntax</span></span>


```mof
uint32 SetSessionTimeout(
  [in] uint32 SessionTimeout,
  [in] uint32 SessionTimeoutAction
);
```



## <a name="parameters"></a><span data-ttu-id="738e3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="738e3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="738e3-110">*Sessiontimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="738e3-110">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="738e3-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="738e3-111">Type: **uint32**</span></span>

<span data-ttu-id="738e3-112">Der neue Timeout Wert in Minuten.</span><span class="sxs-lookup"><span data-stu-id="738e3-112">The new timeout value, in minutes.</span></span> <span data-ttu-id="738e3-113">Der Wert 0 bedeutet, dass kein Timeout vorliegt.</span><span class="sxs-lookup"><span data-stu-id="738e3-113">A value of 0 means there is no timeout.</span></span>

</dd> <dt>

<span data-ttu-id="738e3-114">*Sessiontimeoutaction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="738e3-114">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="738e3-115">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="738e3-115">Type: **uint32**</span></span>

<span data-ttu-id="738e3-116">Gibt die Aktion an, die bei einem Sitzungs Timeout durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="738e3-116">Specifies the action to be taken in case of a session timeout.</span></span> <span data-ttu-id="738e3-117">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="738e3-117">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="738e3-118">0</span><span class="sxs-lookup"><span data-stu-id="738e3-118">0</span></span>
</dt> <dd>

<span data-ttu-id="738e3-119">Trennen Sie die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="738e3-119">Disconnect the session.</span></span>

</dd> <dt>

<span data-ttu-id="738e3-120">1</span><span class="sxs-lookup"><span data-stu-id="738e3-120">1</span></span>
</dt> <dd>

<span data-ttu-id="738e3-121">Versuchen Sie, die Sitzung erneut zu autorisieren.</span><span class="sxs-lookup"><span data-stu-id="738e3-121">Attempt to re-authorize the session.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="738e3-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="738e3-122">Return value</span></span>

<span data-ttu-id="738e3-123">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="738e3-123">Type: **uint32**</span></span>

<span data-ttu-id="738e3-124">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="738e3-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="738e3-125">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="738e3-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="738e3-126">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="738e3-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="738e3-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="738e3-127">Remarks</span></span>

<span data-ttu-id="738e3-128">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="738e3-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="738e3-129">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="738e3-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="738e3-130">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="738e3-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="738e3-131">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="738e3-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="738e3-132">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="738e3-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="738e3-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="738e3-133">Requirements</span></span>



| <span data-ttu-id="738e3-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="738e3-134">Requirement</span></span> | <span data-ttu-id="738e3-135">Wert</span><span class="sxs-lookup"><span data-stu-id="738e3-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="738e3-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="738e3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="738e3-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="738e3-137">None supported</span></span><br/>                                                                |
| <span data-ttu-id="738e3-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="738e3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="738e3-139">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="738e3-139">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="738e3-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="738e3-140">Namespace</span></span><br/>                | <span data-ttu-id="738e3-141">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="738e3-141">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="738e3-142">MOF</span><span class="sxs-lookup"><span data-stu-id="738e3-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="738e3-143"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="738e3-143"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="738e3-144">DLL</span><span class="sxs-lookup"><span data-stu-id="738e3-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="738e3-145"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="738e3-145"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="738e3-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="738e3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="738e3-147">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="738e3-147">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

