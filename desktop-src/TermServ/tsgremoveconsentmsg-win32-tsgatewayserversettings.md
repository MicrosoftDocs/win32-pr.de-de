---
title: Zgremuvegenehmimsg-Methode der Win32_TSGatewayServerSettings-Klasse
description: Entfernt die administrative Meldung für den Gatewayserver. | Zgremuvegenehmimsg-Methode der Win32_TSGatewayServerSettings-Klasse
ms.assetid: 626dc9ca-d6a1-48ab-84ec-cfccb8e720c2
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "zgremuvegenehmimsg"
- Methode Remotedesktopdienste der Methode "zgremuvegenehmimsg", Win32_TSGatewayServerSettings Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, zgremuvegenehmimsg-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGRemoveConsentMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24cd002ebb1a953d25cf129b4e5f3b4174842199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869952"
---
# <a name="tsgremoveconsentmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="7700b-107">Zgremuvegenehmimsg-Methode der Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="7700b-107">TSGRemoveConsentMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="7700b-108">Entfernt die administrative Meldung für den Gatewayserver.</span><span class="sxs-lookup"><span data-stu-id="7700b-108">Removes the administrative message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7700b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7700b-109">Syntax</span></span>


```mof
uint32 TSGRemoveConsentMsg();
```



## <a name="parameters"></a><span data-ttu-id="7700b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7700b-110">Parameters</span></span>

<span data-ttu-id="7700b-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7700b-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7700b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7700b-112">Return value</span></span>

<span data-ttu-id="7700b-113">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7700b-113">Type: **uint32**</span></span>

<span data-ttu-id="7700b-114">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="7700b-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7700b-115">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7700b-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7700b-116">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7700b-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7700b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7700b-117">Remarks</span></span>

<span data-ttu-id="7700b-118">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7700b-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="7700b-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="7700b-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7700b-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="7700b-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7700b-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7700b-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7700b-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7700b-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7700b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7700b-123">Requirements</span></span>



| <span data-ttu-id="7700b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7700b-124">Requirement</span></span> | <span data-ttu-id="7700b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7700b-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7700b-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7700b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7700b-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7700b-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7700b-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7700b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7700b-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7700b-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="7700b-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="7700b-130">Namespace</span></span><br/>                | <span data-ttu-id="7700b-131">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="7700b-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="7700b-132">MOF</span><span class="sxs-lookup"><span data-stu-id="7700b-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7700b-133"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="7700b-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="7700b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7700b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7700b-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7700b-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="7700b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7700b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7700b-137">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="7700b-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

