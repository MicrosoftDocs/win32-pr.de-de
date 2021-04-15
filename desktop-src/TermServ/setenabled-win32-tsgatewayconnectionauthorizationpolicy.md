---
title: Die "stenabled"-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die aktivierte Eigenschaft fest, mit der die aktuelle Remotedesktopdienste Verbindungs Autorisierungs Richtlinie (RD \ 160; aktiviert oder deaktiviert wird. Cap).
ms.assetid: f8c0b39e-95d4-46cf-83fb-e91b650fbb4d
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode ""
- Remotedesktopdienste der Methode "" der Klasse "Win32_TSGatewayConnectionAuthorizationPolicy"
- Win32_TSGatewayConnectionAuthorizationPolicy Klasse Remotedesktopdienste, Methode "".
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6584e8916db2f8070def3904d0ece6ec0ee5ae34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517690"
---
# <a name="setenabled-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="61105-106">Die "stenabled"-Methode der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="61105-106">SetEnabled method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="61105-107">Legt die **aktivierte** Eigenschaft fest, die die aktuelle Remotedesktopdienste Verbindungs Autorisierungs Richtlinie (RD-CAP) aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="61105-107">Sets the **Enabled** property, which enables or disables the current Remote Desktop Services connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="61105-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="61105-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="61105-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="61105-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61105-110">*Aktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61105-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61105-111">**True** , wenn die RD-Obergrenze aktiviert werden soll, **false** , wenn die RD-Obergrenze deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="61105-111">**True** if the RD CAP is to be enabled, **False** if the RD CAP is to be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61105-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61105-112">Return value</span></span>

<span data-ttu-id="61105-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="61105-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="61105-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="61105-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="61105-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="61105-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="61105-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61105-116">Remarks</span></span>

<span data-ttu-id="61105-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="61105-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="61105-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="61105-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="61105-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="61105-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="61105-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="61105-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="61105-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="61105-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="61105-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61105-122">Requirements</span></span>



| <span data-ttu-id="61105-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61105-123">Requirement</span></span> | <span data-ttu-id="61105-124">Wert</span><span class="sxs-lookup"><span data-stu-id="61105-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="61105-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61105-125">Minimum supported client</span></span><br/> | <span data-ttu-id="61105-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="61105-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="61105-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61105-127">Minimum supported server</span></span><br/> | <span data-ttu-id="61105-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61105-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="61105-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="61105-129">Namespace</span></span><br/>                | <span data-ttu-id="61105-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="61105-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="61105-131">MOF</span><span class="sxs-lookup"><span data-stu-id="61105-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61105-132"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="61105-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="61105-133">DLL</span><span class="sxs-lookup"><span data-stu-id="61105-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61105-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61105-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="61105-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61105-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61105-136">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="61105-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

