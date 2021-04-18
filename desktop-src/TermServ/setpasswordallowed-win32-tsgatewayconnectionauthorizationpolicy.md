---
title: Setpasswordallowed-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Legt die passwordallowed-Eigenschaft fest, die die Unterstützung für die Verwendung eines Kennworts für die Verbindung mit dem Remotedesktop Gateway (RD-Gateway)-Server aktiviert oder deaktiviert.
ms.assetid: 2d2dfc45-ac2c-41dc-b2c1-4c8eab42c442
ms.tgt_platform: multiple
keywords:
- Setpasswordallowed-Methode Remotedesktopdienste
- Setpasswordallowed-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, setpasswordallowed-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetPasswordAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8bda5fde2fd79cc02697fd270fc307ef5f410f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392166"
---
# <a name="setpasswordallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="75be9-106">Setpasswordallowed-Methode der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="75be9-106">SetPasswordAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="75be9-107">Legt die **passwordallowed** -Eigenschaft fest, die die Unterstützung für die Verwendung eines Kennworts für die Verbindung mit dem Remotedesktop Gateway (RD-Gateway)-Server aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="75be9-107">Sets the **PasswordAllowed** property, which enables or disables support for using a password to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="75be9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="75be9-108">Syntax</span></span>


```mof
uint32 SetPasswordAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="75be9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="75be9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75be9-110">*Zulässig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75be9-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75be9-111">Neuer **passwordallowed** -Wert.</span><span class="sxs-lookup"><span data-stu-id="75be9-111">New **PasswordAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75be9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75be9-112">Return value</span></span>

<span data-ttu-id="75be9-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="75be9-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="75be9-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75be9-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="75be9-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="75be9-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="75be9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75be9-116">Remarks</span></span>

<span data-ttu-id="75be9-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="75be9-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="75be9-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="75be9-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="75be9-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="75be9-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="75be9-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="75be9-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="75be9-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="75be9-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="75be9-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75be9-122">Requirements</span></span>



| <span data-ttu-id="75be9-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75be9-123">Requirement</span></span> | <span data-ttu-id="75be9-124">Wert</span><span class="sxs-lookup"><span data-stu-id="75be9-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="75be9-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75be9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="75be9-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="75be9-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="75be9-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75be9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="75be9-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75be9-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="75be9-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="75be9-129">Namespace</span></span><br/>                | <span data-ttu-id="75be9-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="75be9-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="75be9-131">MOF</span><span class="sxs-lookup"><span data-stu-id="75be9-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75be9-132"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="75be9-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="75be9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="75be9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75be9-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75be9-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="75be9-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75be9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75be9-136">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="75be9-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

