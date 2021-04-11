---
title: Win32_TSGatewayConnection-Klasse
description: Stellt eine Verbindung zwischen einem Client Computer und einem Remotedesktop Gateway-Server (RD-Gateway) dar.
ms.assetid: 6e76ae25-409d-436a-8eef-8f047194c29c
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnection-Klasse Remotedesktopdienste
- Win32_TSGatewayConnection Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection
- Win32_TSGatewayConnection.ConnectionKey
- Win32_TSGatewayConnection.TunnelId
- Win32_TSGatewayConnection.ChannelId
- Win32_TSGatewayConnection.UserName
- Win32_TSGatewayConnection.FullUserName
- Win32_TSGatewayConnection.ClientAddress
- Win32_TSGatewayConnection.ConnectedTime
- Win32_TSGatewayConnection.IdleTime
- Win32_TSGatewayConnection.ConnectedResource
- Win32_TSGatewayConnection.ProtocolName
- Win32_TSGatewayConnection.ConnectedPort
- Win32_TSGatewayConnection.NumberOfKilobytesSent
- Win32_TSGatewayConnection.NumberOfKilobytesReceived
- Win32_TSGatewayConnection.ConnectionDuration
- Win32_TSGatewayConnection.TransportProtocol
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dbaa79213282a70b2f29e6bee9f94901700dddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105831"
---
# <a name="win32_tsgatewayconnection-class"></a><span data-ttu-id="11c5a-105">Win32-Klasse "t- \_ gatewayconnection"</span><span class="sxs-lookup"><span data-stu-id="11c5a-105">Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="11c5a-106">Stellt eine Verbindung zwischen einem Client Computer und einem Remotedesktop Gateway-Server (RD-Gateway) dar.</span><span class="sxs-lookup"><span data-stu-id="11c5a-106">Represents a connection from a client computer to a Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="11c5a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="11c5a-107">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnection
{
  string ConnectionKey;
  uint64 TunnelId;
  uint32 ChannelId;
  string UserName;
  string FullUserName;
  string ClientAddress;
  string ConnectedTime;
  string IdleTime;
  string ConnectedResource;
  string ProtocolName;
  uint32 ConnectedPort;
  uint64 NumberOfKilobytesSent;
  uint64 NumberOfKilobytesReceived;
  string ConnectionDuration;
  uint32 TransportProtocol;
};
```

## <a name="members"></a><span data-ttu-id="11c5a-108">Member</span><span class="sxs-lookup"><span data-stu-id="11c5a-108">Members</span></span>

<span data-ttu-id="11c5a-109">Die Win32-Klasse " **\_ zgatewayconnection** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="11c5a-109">The **Win32\_TSGatewayConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="11c5a-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="11c5a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="11c5a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11c5a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="11c5a-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="11c5a-112">Methods</span></span>

<span data-ttu-id="11c5a-113">Die Win32-Klasse " **\_ zgatewayconnection** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="11c5a-113">The **Win32\_TSGatewayConnection** class has these methods.</span></span>



| <span data-ttu-id="11c5a-114">Methode</span><span class="sxs-lookup"><span data-stu-id="11c5a-114">Method</span></span>                                                                     | <span data-ttu-id="11c5a-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11c5a-115">Description</span></span>                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11c5a-116">**Check Status**</span><span class="sxs-lookup"><span data-stu-id="11c5a-116">**CheckStatus**</span></span>](checkstatus-win32-tsgatewayconnection.md)               | <span data-ttu-id="11c5a-117">Überprüft den Status einer RD-Gateway Server-Verbindung und gibt an, ob der Zielserver für den Lastenausgleich konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="11c5a-117">Checks the status of an RD Gateway server connection, and whether the target server is configured for load balancing.</span></span><br/> |
| [<span data-ttu-id="11c5a-118">**Trennen**</span><span class="sxs-lookup"><span data-stu-id="11c5a-118">**Disconnect**</span></span>](disconnect-win32-tsgatewayconnection.md)                 | <span data-ttu-id="11c5a-119">Beendet die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="11c5a-119">Ends the connection.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="11c5a-120">**Disconnectprotocol**</span><span class="sxs-lookup"><span data-stu-id="11c5a-120">**DisconnectProtocol**</span></span>](disconnectprotocol-win32-tsgatewayconnection.md) | <span data-ttu-id="11c5a-121">Beendet alle Verbindungen, die das angegebene Protokoll verwenden.</span><span class="sxs-lookup"><span data-stu-id="11c5a-121">Ends all connections that use the specified protocol.</span></span><br/>                                                                 |
| [<span data-ttu-id="11c5a-122">**Disconnectuser**</span><span class="sxs-lookup"><span data-stu-id="11c5a-122">**DisconnectUser**</span></span>](disconnectuser-win32-tsgatewayconnection.md)         | <span data-ttu-id="11c5a-123">Beendet alle Verbindungen des angegebenen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="11c5a-123">Ends all connections of the specified user.</span></span><br/>                                                                           |



 

### <a name="properties"></a><span data-ttu-id="11c5a-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11c5a-124">Properties</span></span>

<span data-ttu-id="11c5a-125">Die Win32-Klasse "t- **\_ gatewayconnection** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="11c5a-125">The **Win32\_TSGatewayConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11c5a-126">**ChannelId**</span><span class="sxs-lookup"><span data-stu-id="11c5a-126">**ChannelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11c5a-127">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11c5a-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11c5a-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11c5a-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11c5a-129">Kanal Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="11c5a-129">Channel identifier.</span></span>

</dd> <dt>

<span data-ttu-id="11c5a-130">**Clientaddress**</span><span class="sxs-lookup"><span data-stu-id="11c5a-130">**ClientAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11c5a-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11c5a-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11c5a-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11c5a-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11c5a-133">Client-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="11c5a-133">Client IP address.</span></span>

</dd> <dt>

<span data-ttu-id="11c5a-134">**Connectedport**</span><span class="sxs-lookup"><span data-stu-id="11c5a-134">**ConnectedPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11c5a-135">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11c5a-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11c5a-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11c5a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11c5a-137">Port für die verbundene Ressource, mit der der Benutzer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="11c5a-137">Port on the connected resource to which the user is connected.</span></span>

</dd> <dt>

<span data-ttu-id="11c5a-138">**Connectedresource**</span><span class="sxs-lookup"><span data-stu-id="11c5a-138">**ConnectedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11c5a-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11c5a-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11c5a-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11c5a-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11c5a-141">Der Name des Computers (oder Clusters), mit dem der Client verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="11c5a-141">Name of the computer (or cluster) to which the client is connected.</span></span>

</dd> <dt>

<span data-ttu-id="11c5a-142">**Connectedtime**</span><span class="sxs-lookup"><span data-stu-id="11c5a-142">**ConnectedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11c5a-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11c5a-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11c5a-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11c5a-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11c5a-145">Der Zeitstempel, zu dem die Verbindung hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="11c5a-145">The time stamp for when the connection was established.</span></span> <span data-ttu-id="11c5a-146">Diese Zeit wird zurückgesetzt, wenn die Verbindung zurückgesetzt wird, auch wenn die Verbindung automatisch wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="11c5a-146">This time is reset when the connection is reset, even if it is automatically reconnected.</span></span>

</dd> <dt>

<span data-ttu-id="11c5a-147">**Connectionduration**</span><span class="sxs-lookup"><span data-stu-id="11c5a-147">**ConnectionDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11c5a-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11c5a-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11c5a-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11c5a-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11c5a-150">Die Zeit, die seit der verbundenen Zeit verstrichen ist.</span><span class="sxs-lookup"><span data-stu-id="11c5a-150">The time that has elapsed since the connected time.</span></span>

</dd> <dt>

<span data-ttu-id="11c5a-151">**Connectionkey**</span><span class="sxs-lookup"><span data-stu-id="11c5a-151">**ConnectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11c5a-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11c5a-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11c5a-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11c5a-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11c5a-154">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="11c5a-154">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="11c5a-155">Der Verbindungs Bezeichner im Format "tunnelid: channelid".</span><span class="sxs-lookup"><span data-stu-id="11c5a-155">Connection identifier in the format "tunnelId:channelID".</span></span>

</dd> <dt>

<span data-ttu-id="11c5a-156">**Fullusername**</span><span class="sxs-lookup"><span data-stu-id="11c5a-156">**FullUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11c5a-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11c5a-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11c5a-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11c5a-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11c5a-159">Vollständiger Benutzername des verbundenen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="11c5a-159">Full user name of the connected user.</span></span>

</dd> <dt>

<span data-ttu-id="11c5a-160">**IdleTime**</span><span class="sxs-lookup"><span data-stu-id="11c5a-160">**IdleTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11c5a-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11c5a-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11c5a-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11c5a-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11c5a-163">Leerlaufzeit der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="11c5a-163">Idle time of the connection.</span></span>

</dd> <dt>

<span data-ttu-id="11c5a-164">**Anzahl der empfangenen Anzahlen**</span><span class="sxs-lookup"><span data-stu-id="11c5a-164">**NumberOfKilobytesReceived**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11c5a-165">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="11c5a-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="11c5a-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11c5a-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11c5a-167">Anzahl der Kilobyte, die vom RD-Gateway Server vom Client Computer empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="11c5a-167">Number of kilobytes received from the client computer by the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="11c5a-168">**Numofkilobytess**</span><span class="sxs-lookup"><span data-stu-id="11c5a-168">**NumberOfKilobytesSent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11c5a-169">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="11c5a-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="11c5a-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11c5a-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11c5a-171">Anzahl der Kilobyte, die vom RD-Gateway Server an den Client Computer gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="11c5a-171">Number of kilobytes sent to the client computer by the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="11c5a-172">**ProtocolName**</span><span class="sxs-lookup"><span data-stu-id="11c5a-172">**ProtocolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11c5a-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11c5a-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11c5a-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11c5a-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11c5a-175">Protokoll, das verwendet wird, um eine Verbindung mit dem RD-Gateway-Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="11c5a-175">Protocol that is used to connect to the RD Gateway server.</span></span>

<dt>

<span data-ttu-id="11c5a-176">RDP</span><span class="sxs-lookup"><span data-stu-id="11c5a-176">"RDP"</span></span>
</dt> <dd>

<span data-ttu-id="11c5a-177">Das Protokoll für den RD-Gateway Server.</span><span class="sxs-lookup"><span data-stu-id="11c5a-177">The protocol for the RD Gateway server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="11c5a-178">**Transportprotocol**</span><span class="sxs-lookup"><span data-stu-id="11c5a-178">**TransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11c5a-179">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11c5a-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11c5a-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11c5a-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11c5a-181">Gibt den Transporttyp für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="11c5a-181">Specifies the transport type for the connection.</span></span> <span data-ttu-id="11c5a-182">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="11c5a-182">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="11c5a-183">0</span><span class="sxs-lookup"><span data-stu-id="11c5a-183">0</span></span>
</dt> <dd>

<span data-ttu-id="11c5a-184">RPC-über-HTTP-Transport.</span><span class="sxs-lookup"><span data-stu-id="11c5a-184">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="11c5a-185">1</span><span class="sxs-lookup"><span data-stu-id="11c5a-185">1</span></span>
</dt> <dd>

<span data-ttu-id="11c5a-186">HTTP-Transport.</span><span class="sxs-lookup"><span data-stu-id="11c5a-186">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="11c5a-187">2</span><span class="sxs-lookup"><span data-stu-id="11c5a-187">2</span></span>
</dt> <dd>

<span data-ttu-id="11c5a-188">UDP-Transport.</span><span class="sxs-lookup"><span data-stu-id="11c5a-188">UDP transport.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="11c5a-189">**Tunnelid**</span><span class="sxs-lookup"><span data-stu-id="11c5a-189">**TunnelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11c5a-190">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="11c5a-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="11c5a-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11c5a-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11c5a-192">Tunnel Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="11c5a-192">Tunnel identifier.</span></span>

</dd> <dt>

<span data-ttu-id="11c5a-193">**UserName**</span><span class="sxs-lookup"><span data-stu-id="11c5a-193">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11c5a-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11c5a-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11c5a-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11c5a-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11c5a-196">Benutzername, der mit dem RD-Gateway-Server verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="11c5a-196">User name connected to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11c5a-197">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11c5a-197">Remarks</span></span>

<span data-ttu-id="11c5a-198">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="11c5a-198">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="11c5a-199">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="11c5a-199">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="11c5a-200">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="11c5a-200">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="11c5a-201">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="11c5a-201">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="11c5a-202">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="11c5a-202">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="11c5a-203">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11c5a-203">Requirements</span></span>



| <span data-ttu-id="11c5a-204">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11c5a-204">Requirement</span></span> | <span data-ttu-id="11c5a-205">Wert</span><span class="sxs-lookup"><span data-stu-id="11c5a-205">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c5a-206">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11c5a-206">Minimum supported client</span></span><br/> | <span data-ttu-id="11c5a-207">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="11c5a-207">None supported</span></span><br/>                                                                |
| <span data-ttu-id="11c5a-208">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11c5a-208">Minimum supported server</span></span><br/> | <span data-ttu-id="11c5a-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11c5a-209">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="11c5a-210">Namespace</span><span class="sxs-lookup"><span data-stu-id="11c5a-210">Namespace</span></span><br/>                | <span data-ttu-id="11c5a-211">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="11c5a-211">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="11c5a-212">MOF</span><span class="sxs-lookup"><span data-stu-id="11c5a-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11c5a-213"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="11c5a-213"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="11c5a-214">DLL</span><span class="sxs-lookup"><span data-stu-id="11c5a-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11c5a-215"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11c5a-215"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="11c5a-216">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11c5a-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11c5a-217">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="11c5a-217">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="11c5a-218">**Win32-"t- \_ gatewayloadbalancer"**</span><span class="sxs-lookup"><span data-stu-id="11c5a-218">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="11c5a-219">**Win32-"t- \_ gatewayradiusserver"**</span><span class="sxs-lookup"><span data-stu-id="11c5a-219">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="11c5a-220">**Win32- \_ faigatewayresourceauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="11c5a-220">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="11c5a-221">**Win32-Datei " \_ zgatewayresourcegroup"**</span><span class="sxs-lookup"><span data-stu-id="11c5a-221">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="11c5a-222">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="11c5a-222">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

