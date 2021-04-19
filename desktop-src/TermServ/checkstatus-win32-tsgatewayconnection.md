---
title: CheckStatus-Methode der Win32_TSGatewayConnection-Klasse
description: Hiermit wird der Status einer Remotedesktop Gateway-Server Verbindung (RD-Gateway) zu einem anderen Computer überprüft und ermittelt, ob der Bereitstellungs Zielcomputer für den Lastenausgleich konfiguriert ist.
ms.assetid: e8ee3d40-76eb-401f-b255-bccd7ba8c058
ms.tgt_platform: multiple
keywords:
- CheckStatus-Methode Remotedesktopdienste
- CheckStatus-Methode Remotedesktopdienste, Win32_TSGatewayConnection-Klasse
- Win32_TSGatewayConnection-Klasse Remotedesktopdienste, checkStatus-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.CheckStatus
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babb083af5c0581abe27d442a466c3d6114b957a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339545"
---
# <a name="checkstatus-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="5402e-106">CheckStatus-Methode der Win32- \_ Klasse "tgatewayconnection"</span><span class="sxs-lookup"><span data-stu-id="5402e-106">CheckStatus method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="5402e-107">Hiermit wird der Status einer Remotedesktop Gateway-Server Verbindung (RD-Gateway) zu einem anderen Computer überprüft und ermittelt, ob der Bereitstellungs Zielcomputer für den Lastenausgleich konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="5402e-107">Checks the status of a Remote Desktop Gateway (RD Gateway) server connection to another computer, and determines whether the target computer is configured for load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="5402e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5402e-108">Syntax</span></span>


```mof
uint32 CheckStatus(
  [in] string ServerName,
  [in] string EndPointName
);
```



## <a name="parameters"></a><span data-ttu-id="5402e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5402e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5402e-110">*Servername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5402e-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5402e-111">Der Name des Quell RD-Gateway Servers, von dem die Verbindung geprüft wird.</span><span class="sxs-lookup"><span data-stu-id="5402e-111">The name of the source RD Gateway server from which the connection is checked.</span></span>

</dd> <dt>

<span data-ttu-id="5402e-112">*EndpointName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5402e-112">*EndPointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5402e-113">Der Name des Zielservers (der Endpunkt), auf den der Zugriff vom Quell Server aus geprüft wird.</span><span class="sxs-lookup"><span data-stu-id="5402e-113">The name of the target server (the endpoint) to which access is checked from the source server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5402e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5402e-114">Return value</span></span>

<span data-ttu-id="5402e-115">Diese Methode gibt die folgenden möglichen Rückgabewerte zurück.</span><span class="sxs-lookup"><span data-stu-id="5402e-115">This method returns the following possible return values.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="5402e-116">0</span><span class="sxs-lookup"><span data-stu-id="5402e-116">0</span></span>

<span data-ttu-id="5402e-117">Der Verbindungsstatus lautet "OK".</span><span class="sxs-lookup"><span data-stu-id="5402e-117">The connection status is OK.</span></span> <span data-ttu-id="5402e-118">Der Endpunkt ist erreichbar und für den Lastenausgleich konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="5402e-118">The endpoint is reachable and is configured for load balancing.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5402e-119">1</span><span class="sxs-lookup"><span data-stu-id="5402e-119">1</span></span>

<span data-ttu-id="5402e-120">Der Verbindungsstatus ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="5402e-120">The connection status is unknown.</span></span> <span data-ttu-id="5402e-121">Höchstwahrscheinlich ist eine Ausnahme aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="5402e-121">Most likely, an exception occurred.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5402e-122">0x80075c34</span><span class="sxs-lookup"><span data-stu-id="5402e-122">0x80075c34</span></span>

<span data-ttu-id="5402e-123">Der Endpunkt ist entweder nicht erreichbar oder nicht für den Lastenausgleich konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="5402e-123">The endpoint is either not reachable, or it is not configured for load balancing.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5402e-124">0x80075c32</span><span class="sxs-lookup"><span data-stu-id="5402e-124">0x80075c32</span></span>

<span data-ttu-id="5402e-125">Status Fehler.</span><span class="sxs-lookup"><span data-stu-id="5402e-125">A status error occurred.</span></span> <span data-ttu-id="5402e-126">Der Endpunkt ist erreichbar, aber der RPC/HTTP-Lasten Ausgleichs Dienst (rpchttplsb) wurde auf dem Bereitstellungs Zielcomputer nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="5402e-126">The endpoint is reachable, but the RPC/HTTP Load Balancing Service (RPCHTTPLBS) service is not started on the target computer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5402e-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5402e-127">Remarks</span></span>

<span data-ttu-id="5402e-128">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="5402e-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5402e-129">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="5402e-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5402e-130">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5402e-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5402e-131">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5402e-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5402e-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5402e-132">Requirements</span></span>



| <span data-ttu-id="5402e-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5402e-133">Requirement</span></span> | <span data-ttu-id="5402e-134">Wert</span><span class="sxs-lookup"><span data-stu-id="5402e-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5402e-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5402e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5402e-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5402e-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5402e-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5402e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5402e-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5402e-138">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5402e-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="5402e-139">Namespace</span></span><br/>                | <span data-ttu-id="5402e-140">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5402e-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5402e-141">MOF</span><span class="sxs-lookup"><span data-stu-id="5402e-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5402e-142"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="5402e-142"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5402e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5402e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5402e-144"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5402e-144"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5402e-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5402e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5402e-146">**Win32-"- \_ gatewayconnection"**</span><span class="sxs-lookup"><span data-stu-id="5402e-146">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

