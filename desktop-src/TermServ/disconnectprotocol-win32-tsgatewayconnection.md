---
title: Disconnectprotocol-Methode der Win32_TSGatewayConnection-Klasse
description: Trennt alle Verbindungen des angegebenen Protokolls vom Remotedesktop Gateway-Server (RD-Gateway).
ms.assetid: 0ca3f478-dfdc-404e-ac17-43b6873b7256
ms.tgt_platform: multiple
keywords:
- Disconnectprotocol-Methode Remotedesktopdienste
- Disconnectprotocol-Methode Remotedesktopdienste, Win32_TSGatewayConnection-Klasse
- Win32_TSGatewayConnection-Klasse Remotedesktopdienste, disconnectprotocol-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectProtocol
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a37050cbd622c6fea14b8b4e5dc6a414eaad85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340827"
---
# <a name="disconnectprotocol-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="2c896-106">Disconnectprotocol-Methode der Win32- \_ Klasse "tgatewayconnection"</span><span class="sxs-lookup"><span data-stu-id="2c896-106">DisconnectProtocol method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="2c896-107">Trennt alle Verbindungen des angegebenen Protokolls vom Remotedesktop Gateway-Server (RD-Gateway).</span><span class="sxs-lookup"><span data-stu-id="2c896-107">Disconnects all connections of the specified protocol from the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c896-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c896-108">Syntax</span></span>


```mof
uint32 DisconnectProtocol(
  [in] string ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="2c896-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c896-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c896-110">*ProtocolName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c896-110">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c896-111">Der Protokoll Name für eine bestimmte Verbindung.</span><span class="sxs-lookup"><span data-stu-id="2c896-111">The protocol name for a specific connection.</span></span> <span data-ttu-id="2c896-112">Dies kann über die **ProtocolName** -Eigenschaft der Win32-Klasse " **\_ tgatewayconnection** " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2c896-112">This can be retrieved from the **ProtocolName** property of the **Win32\_TSGatewayConnection** class.</span></span>

<dt>

<span data-ttu-id="2c896-113">TS</span><span class="sxs-lookup"><span data-stu-id="2c896-113">"TS"</span></span>
</dt> <dd>

<span data-ttu-id="2c896-114">Das Protokoll für den RD-Gateway Server.</span><span class="sxs-lookup"><span data-stu-id="2c896-114">The protocol for the RD Gateway server.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c896-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c896-115">Return value</span></span>

<span data-ttu-id="2c896-116">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="2c896-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2c896-117">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2c896-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2c896-118">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2c896-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2c896-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c896-119">Remarks</span></span>

<span data-ttu-id="2c896-120">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2c896-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2c896-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="2c896-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2c896-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="2c896-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2c896-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c896-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2c896-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2c896-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c896-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c896-125">Requirements</span></span>



| <span data-ttu-id="2c896-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c896-126">Requirement</span></span> | <span data-ttu-id="2c896-127">Wert</span><span class="sxs-lookup"><span data-stu-id="2c896-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c896-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c896-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2c896-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2c896-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2c896-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c896-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2c896-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c896-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2c896-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c896-132">Namespace</span></span><br/>                | <span data-ttu-id="2c896-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2c896-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2c896-134">MOF</span><span class="sxs-lookup"><span data-stu-id="2c896-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c896-135"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="2c896-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c896-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2c896-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c896-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c896-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2c896-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c896-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c896-139">**Win32-"- \_ gatewayconnection"**</span><span class="sxs-lookup"><span data-stu-id="2c896-139">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

