---
title: MoveUp-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Verschiebt die aktuelle Remotedesktop Verbindungs Autorisierungs Richtlinie (RD \ 160; Cap) eine Position nach oben in der Reihenfolge, in der RD \ 160; Caps werden ausgewertet.
ms.assetid: 5c9ff18d-e019-4a52-af0b-75fa61d77b7a
ms.tgt_platform: multiple
keywords:
- MoveUp-Methode Remotedesktopdienste
- MoveUp-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, moveUp-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81973261d156328aa1f306c26dd8bd9bdd20511f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479095"
---
# <a name="moveup-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="bca62-106">MoveUp-Methode der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="bca62-106">MoveUp method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="bca62-107">Verschiebt den aktuellen Remotedesktop Verbindungs Autorisierungs Richtlinie (RD-CAP) eine Position nach oben in der Reihenfolge, in der die RD-CAPs ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="bca62-107">Moves the current Remote Desktop connection authorization policy (RD CAP) one position up in the order that RD CAPs are evaluated.</span></span> <span data-ttu-id="bca62-108">Mit dieser Methode wird die **Order** -Eigenschaft der aktuellen RD-Obergrenze verringert und die **Order** -Eigenschaft der RD-Obergrenze erhöht, die der aktuellen RD-Obergrenze vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="bca62-108">This method decrements the **Order** property of the current RD CAP and increments the **Order** property of the RD CAP that preceded the current RD CAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="bca62-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bca62-109">Syntax</span></span>


```mof
uint32 MoveUp();
```



## <a name="parameters"></a><span data-ttu-id="bca62-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bca62-110">Parameters</span></span>

<span data-ttu-id="bca62-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="bca62-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bca62-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bca62-112">Return value</span></span>

<span data-ttu-id="bca62-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="bca62-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bca62-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bca62-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bca62-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bca62-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bca62-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bca62-116">Remarks</span></span>

<span data-ttu-id="bca62-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="bca62-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="bca62-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="bca62-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bca62-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="bca62-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bca62-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bca62-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bca62-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bca62-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bca62-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bca62-122">Requirements</span></span>



| <span data-ttu-id="bca62-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bca62-123">Requirement</span></span> | <span data-ttu-id="bca62-124">Wert</span><span class="sxs-lookup"><span data-stu-id="bca62-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bca62-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bca62-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bca62-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bca62-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bca62-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bca62-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bca62-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bca62-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bca62-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="bca62-129">Namespace</span></span><br/>                | <span data-ttu-id="bca62-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="bca62-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bca62-131">MOF</span><span class="sxs-lookup"><span data-stu-id="bca62-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bca62-132"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="bca62-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bca62-133">DLL</span><span class="sxs-lookup"><span data-stu-id="bca62-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bca62-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bca62-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bca62-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bca62-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bca62-136">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="bca62-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="bca62-137">**Nach unten**</span><span class="sxs-lookup"><span data-stu-id="bca62-137">**MoveDown**</span></span>](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

