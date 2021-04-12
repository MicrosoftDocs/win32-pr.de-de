---
title: MoveUp-Methode der Win32_TSGatewayRADIUSServer-Klasse
description: Verschiebt diesen Remote Authentication Dial-in User Service (RADIUS)-Server in der Prioritäts Reihenfolge eine Position nach oben.
ms.assetid: 060bb90d-72c0-4364-a44f-c6368434b174
ms.tgt_platform: multiple
keywords:
- MoveUp-Methode Remotedesktopdienste
- MoveUp-Methode Remotedesktopdienste, Win32_TSGatewayRADIUSServer-Klasse
- Win32_TSGatewayRADIUSServer-Klasse Remotedesktopdienste, moveUp-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca93eee44abd147576c6e678dce871ae4d49d921
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518929"
---
# <a name="moveup-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="41a46-106">MoveUp-Methode der Win32- \_ Klasse "zgatewayradiusserver"</span><span class="sxs-lookup"><span data-stu-id="41a46-106">MoveUp method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="41a46-107">Verschiebt diesen Remote Authentication Dial-in User Service (RADIUS)-Server in der Prioritäts Reihenfolge eine Position nach oben.</span><span class="sxs-lookup"><span data-stu-id="41a46-107">Moves this Remote Authentication Dial-In User Service (RADIUS) server one position up in the priority order.</span></span> <span data-ttu-id="41a46-108">Diese Methode verringert die **Priority** -Eigenschaft des aktuellen RADIUS-Servers und Inkremente die **Priority** -Eigenschaft des RADIUS-Servers, der dem aktuellen RADIUS-Server vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="41a46-108">This method decrements the **Priority** property of the current RADIUS server and increments the **Priority** property of the RADIUS server that precedes the current RADIUS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="41a46-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="41a46-109">Syntax</span></span>


```mof
uint32 MoveUp();
```



## <a name="parameters"></a><span data-ttu-id="41a46-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="41a46-110">Parameters</span></span>

<span data-ttu-id="41a46-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="41a46-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="41a46-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41a46-112">Return value</span></span>

<span data-ttu-id="41a46-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="41a46-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="41a46-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="41a46-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="41a46-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="41a46-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="41a46-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41a46-116">Remarks</span></span>

<span data-ttu-id="41a46-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="41a46-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="41a46-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="41a46-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="41a46-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="41a46-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="41a46-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="41a46-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="41a46-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="41a46-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="41a46-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41a46-122">Requirements</span></span>



| <span data-ttu-id="41a46-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41a46-123">Requirement</span></span> | <span data-ttu-id="41a46-124">Wert</span><span class="sxs-lookup"><span data-stu-id="41a46-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="41a46-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41a46-125">Minimum supported client</span></span><br/> | <span data-ttu-id="41a46-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="41a46-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="41a46-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41a46-127">Minimum supported server</span></span><br/> | <span data-ttu-id="41a46-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41a46-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="41a46-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="41a46-129">Namespace</span></span><br/>                | <span data-ttu-id="41a46-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="41a46-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="41a46-131">MOF</span><span class="sxs-lookup"><span data-stu-id="41a46-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41a46-132"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="41a46-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="41a46-133">DLL</span><span class="sxs-lookup"><span data-stu-id="41a46-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41a46-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41a46-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="41a46-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41a46-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41a46-136">**Win32-"t- \_ gatewayradiusserver"**</span><span class="sxs-lookup"><span data-stu-id="41a46-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

