---
title: Disconnect-Methode der Win32_TSGatewayConnection-Klasse
description: Trennt die Verbindung mit dem Remotedesktop Gateway-Server (RD-Gateway).
ms.assetid: 8c424e58-aa89-4ec6-acea-5b571d3f4c21
ms.tgt_platform: multiple
keywords:
- Disconnect-Methode Remotedesktopdienste
- Disconnect-Methode Remotedesktopdienste, Win32_TSGatewayConnection-Klasse
- Win32_TSGatewayConnection-Klasse Remotedesktopdienste, Disconnect-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.Disconnect
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53101e5ca3529c5033adc918f1f9ad11a3b45f7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740032"
---
# <a name="disconnect-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="46c3b-106">Disconnect-Methode der Win32-Klasse "t- \_ gatewayconnection"</span><span class="sxs-lookup"><span data-stu-id="46c3b-106">Disconnect method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="46c3b-107">Trennt die Verbindung mit dem Remotedesktop Gateway-Server (RD-Gateway).</span><span class="sxs-lookup"><span data-stu-id="46c3b-107">Disconnects the connection from the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="46c3b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="46c3b-108">Syntax</span></span>


```mof
uint32 Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="46c3b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="46c3b-109">Parameters</span></span>

<span data-ttu-id="46c3b-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="46c3b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46c3b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46c3b-111">Return value</span></span>

<span data-ttu-id="46c3b-112">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="46c3b-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="46c3b-113">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="46c3b-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="46c3b-114">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="46c3b-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="46c3b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46c3b-115">Remarks</span></span>

<span data-ttu-id="46c3b-116">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="46c3b-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="46c3b-117">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="46c3b-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="46c3b-118">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="46c3b-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="46c3b-119">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="46c3b-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="46c3b-120">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="46c3b-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="46c3b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46c3b-121">Requirements</span></span>



| <span data-ttu-id="46c3b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46c3b-122">Requirement</span></span> | <span data-ttu-id="46c3b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="46c3b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="46c3b-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46c3b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="46c3b-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="46c3b-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="46c3b-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46c3b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="46c3b-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46c3b-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="46c3b-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="46c3b-128">Namespace</span></span><br/>                | <span data-ttu-id="46c3b-129">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="46c3b-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="46c3b-130">MOF</span><span class="sxs-lookup"><span data-stu-id="46c3b-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46c3b-131"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="46c3b-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="46c3b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="46c3b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46c3b-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46c3b-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="46c3b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46c3b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46c3b-135">**Win32-"- \_ gatewayconnection"**</span><span class="sxs-lookup"><span data-stu-id="46c3b-135">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

