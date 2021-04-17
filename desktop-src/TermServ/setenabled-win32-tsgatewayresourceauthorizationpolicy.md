---
title: Die "stenabled"-Methode der Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Aktiviert oder deaktiviert die Remotedesktop-Ressourcen Autorisierungs Richtlinie (RD \ 160; Rap) durch Festlegen der aktivierten Eigenschaft.
ms.assetid: ee5830ba-36a1-4f28-a902-be5867439ada
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode ""
- Remotedesktopdienste der Methode "" der Klasse "Win32_TSGatewayResourceAuthorizationPolicy"
- Win32_TSGatewayResourceAuthorizationPolicy Klasse Remotedesktopdienste, Methode "".
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de7c4e013690a5d5e8ffd6b235a42ea43c445ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478861"
---
# <a name="setenabled-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="68b0a-106">Die "stenabled"-Methode der Win32-Klasse "t- \_ gatewayresourceauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="68b0a-106">SetEnabled method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="68b0a-107">Aktiviert oder deaktiviert die Remotedesktop-Ressourcen Autorisierungs Richtlinie (RD-RAP) durch Festlegen der **aktivierten** Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="68b0a-107">Enables or disables the Remote Desktop resource authorization policy (RD RAP) by setting the **Enabled** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="68b0a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="68b0a-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="68b0a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="68b0a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68b0a-110">*Aktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68b0a-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68b0a-111">**True** gibt an, dass die RD-RAP aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="68b0a-111">If **True**, the RD RAP will be enabled.</span></span> <span data-ttu-id="68b0a-112">Wenn der Wert **false** ist, wird die RD-RAP deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="68b0a-112">If **False**, the RD RAP will be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68b0a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68b0a-113">Return value</span></span>

<span data-ttu-id="68b0a-114">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="68b0a-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="68b0a-115">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="68b0a-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="68b0a-116">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="68b0a-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="68b0a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68b0a-117">Remarks</span></span>

<span data-ttu-id="68b0a-118">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="68b0a-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="68b0a-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="68b0a-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="68b0a-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="68b0a-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="68b0a-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="68b0a-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="68b0a-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="68b0a-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="68b0a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68b0a-123">Requirements</span></span>



| <span data-ttu-id="68b0a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68b0a-124">Requirement</span></span> | <span data-ttu-id="68b0a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="68b0a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="68b0a-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68b0a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="68b0a-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="68b0a-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="68b0a-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68b0a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="68b0a-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68b0a-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="68b0a-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="68b0a-130">Namespace</span></span><br/>                | <span data-ttu-id="68b0a-131">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="68b0a-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="68b0a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="68b0a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68b0a-133"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="68b0a-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="68b0a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="68b0a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68b0a-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68b0a-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="68b0a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68b0a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68b0a-137">**Win32- \_ faigatewayresourceauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="68b0a-137">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

