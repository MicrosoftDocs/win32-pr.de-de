---
title: Die muvedown-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse.
description: Verschiebt die aktuelle Remotedesktop Verbindungs Autorisierungs Richtlinie (RD \ 160; Cap) eine Position unten in der Reihenfolge, in der RD \ 160; Caps werden ausgewertet.
ms.assetid: 57349e59-e200-4789-bbcb-d474eacde39d
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der
- Remotedesktopdienste-Methode, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste,-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveDown
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e5b2e2b56a60d78f827f8989c0317cb003e511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342480"
---
# <a name="movedown-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="1570e-106">Die Methode "Pfad" der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="1570e-106">MoveDown method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="1570e-107">Verschiebt den aktuellen Remotedesktop Verbindungs Autorisierungs Richtlinie (RD-CAP) eine Position nach unten in der Reihenfolge, in der die RD-CAPs ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="1570e-107">Moves the current Remote Desktop connection authorization policy (RD CAP) one position down in the order that RD CAPs are evaluated.</span></span> <span data-ttu-id="1570e-108">Mit dieser Methode wird die **Order** -Eigenschaft der aktuellen RD-Obergrenze erhöht und die **Order** -Eigenschaft der RD-Obergrenze verringert, die der aktuellen RD-Obergrenze folgt.</span><span class="sxs-lookup"><span data-stu-id="1570e-108">This method increments the **Order** property of the current RD CAP and decrements the **Order** property of the RD CAP that followed the current RD CAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="1570e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1570e-109">Syntax</span></span>


```mof
uint32 MoveDown();
```



## <a name="parameters"></a><span data-ttu-id="1570e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1570e-110">Parameters</span></span>

<span data-ttu-id="1570e-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1570e-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1570e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1570e-112">Return value</span></span>

<span data-ttu-id="1570e-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="1570e-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1570e-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1570e-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1570e-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1570e-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1570e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1570e-116">Remarks</span></span>

<span data-ttu-id="1570e-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1570e-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1570e-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="1570e-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1570e-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="1570e-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1570e-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1570e-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1570e-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1570e-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1570e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1570e-122">Requirements</span></span>



| <span data-ttu-id="1570e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1570e-123">Requirement</span></span> | <span data-ttu-id="1570e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1570e-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1570e-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1570e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1570e-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1570e-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1570e-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1570e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1570e-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1570e-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1570e-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="1570e-129">Namespace</span></span><br/>                | <span data-ttu-id="1570e-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1570e-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1570e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="1570e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1570e-132"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="1570e-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1570e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1570e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1570e-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1570e-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1570e-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1570e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1570e-136">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="1570e-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="1570e-137">**MoveUp**</span><span class="sxs-lookup"><span data-stu-id="1570e-137">**MoveUp**</span></span>](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

