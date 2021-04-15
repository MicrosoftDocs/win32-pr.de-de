---
title: Die Methode "szmartcardallowed" der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die smartcardallowed-Eigenschaft fest, die Unterstützung für die Verwendung einer Smartcard für die Verbindung mit dem Remotedesktop Gateway (RD-Gateway)-Server aktiviert oder deaktiviert.
ms.assetid: 9fe1c7a9-2bab-439f-8dc2-421ed876fcf7
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "* zmartcardallowed"
- Methode Remotedesktopdienste der Methode "Win32_TSGatewayConnectionAuthorizationPolicy" der Methode ""
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, Methode "-Methode"
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSmartcardAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022b5461086ae05f198cbce4faaee0e9c36bf77e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392065"
---
# <a name="setsmartcardallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="da1da-106">Die Methode "\* zmartcardallowed" der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="da1da-106">SetSmartcardAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="da1da-107">Legt die **smartcardallowed** -Eigenschaft fest, die Unterstützung für die Verwendung einer Smartcard für die Verbindung mit dem Remotedesktop Gateway (RD-Gateway)-Server aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="da1da-107">Sets the **SmartcardAllowed** property, which enables or disables support for using a smart card to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="da1da-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="da1da-108">Syntax</span></span>


```mof
uint32 SetSmartcardAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="da1da-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="da1da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da1da-110">*Zulässig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da1da-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da1da-111">Neuer **smartcardzulässiger** Wert.</span><span class="sxs-lookup"><span data-stu-id="da1da-111">New **SmartcardAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da1da-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da1da-112">Return value</span></span>

<span data-ttu-id="da1da-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="da1da-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="da1da-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="da1da-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="da1da-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="da1da-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="da1da-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da1da-116">Remarks</span></span>

<span data-ttu-id="da1da-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="da1da-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="da1da-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="da1da-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="da1da-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="da1da-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="da1da-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="da1da-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="da1da-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="da1da-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="da1da-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da1da-122">Requirements</span></span>



| <span data-ttu-id="da1da-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da1da-123">Requirement</span></span> | <span data-ttu-id="da1da-124">Wert</span><span class="sxs-lookup"><span data-stu-id="da1da-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="da1da-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da1da-125">Minimum supported client</span></span><br/> | <span data-ttu-id="da1da-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="da1da-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="da1da-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da1da-127">Minimum supported server</span></span><br/> | <span data-ttu-id="da1da-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da1da-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="da1da-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="da1da-129">Namespace</span></span><br/>                | <span data-ttu-id="da1da-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="da1da-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="da1da-131">MOF</span><span class="sxs-lookup"><span data-stu-id="da1da-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da1da-132"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="da1da-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="da1da-133">DLL</span><span class="sxs-lookup"><span data-stu-id="da1da-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da1da-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da1da-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="da1da-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da1da-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da1da-136">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="da1da-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

