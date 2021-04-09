---
title: Wichtige RPC-Bindungs Terminologie
description: Um eine bessere Unterstützung für den Client/Server-Verbindungsprozess zu erhalten, ist es hilfreich, die folgenden Begriffe zu kennen.
ms.assetid: 05aca325-87ee-4581-9152-a8a2ff7fb490
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, binden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b18b8d3872c830d90079ad740505fead14c1b3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039440"
---
# <a name="essential-rpc-binding-terminology"></a><span data-ttu-id="6333a-104">Wichtige RPC-Bindungs Terminologie</span><span class="sxs-lookup"><span data-stu-id="6333a-104">Essential RPC Binding Terminology</span></span>

<span data-ttu-id="6333a-105">Um eine bessere Unterstützung für den Client/Server-Verbindungsprozess zu erhalten, ist es hilfreich, die folgenden Begriffe zu kennen.</span><span class="sxs-lookup"><span data-stu-id="6333a-105">To better aid in a discussion of the client/server connection process, it is helpful to know the following terms.</span></span>

## <a name="parameters"></a><span data-ttu-id="6333a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6333a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6333a-107"><span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Protokoll Sequenz</span><span class="sxs-lookup"><span data-stu-id="6333a-107"><span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Protocol Sequence</span></span>
</dt> <dd>

<span data-ttu-id="6333a-108">Wenn Netzwerk Betriebssysteme miteinander kommunizieren, müssen Sie die gleiche Sprache lauschen und sprechen.</span><span class="sxs-lookup"><span data-stu-id="6333a-108">When network operating systems communicate with each other, they must listen and speak the same language.</span></span> <span data-ttu-id="6333a-109">Diese Sprachen werden als *Protokoll Sequenzen* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6333a-109">These languages are called *protocol sequences*.</span></span> <span data-ttu-id="6333a-110">Client-und Serverprogramme müssen Protokoll Sequenzen verwenden, die vom verbundenen Netzwerk unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6333a-110">Client and server programs must use protocol sequences that the network connecting them supports.</span></span> <span data-ttu-id="6333a-111">Microsoft RPC unterstützt eine Vielzahl von Protokoll Sequenzen.</span><span class="sxs-lookup"><span data-stu-id="6333a-111">Microsoft RPC supports a variety of protocol sequences.</span></span> <span data-ttu-id="6333a-112">Weitere Informationen finden Sie unter [Auswählen einer Protokoll Sequenz](selecting-a-protocol-sequence.md), [Angeben von Protokoll Sequenzen](specifying-protocol-sequences.md)und [**Endpunkt**](/windows/desktop/Midl/endpoint).</span><span class="sxs-lookup"><span data-stu-id="6333a-112">For details, see [Selecting a Protocol Sequence](selecting-a-protocol-sequence.md), [Specifying Protocol Sequences](specifying-protocol-sequences.md), and [**endpoint**](/windows/desktop/Midl/endpoint).</span></span>

</dd> <dt>

<span data-ttu-id="6333a-113"><span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Server Host Computer oder Server Host System</span><span class="sxs-lookup"><span data-stu-id="6333a-113"><span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Server Host Computer or Server Host System</span></span>
</dt> <dd>

<span data-ttu-id="6333a-114">Das Serverprogramm wird auf dem Server Host Computer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6333a-114">The server program runs on the server host computer.</span></span> <span data-ttu-id="6333a-115">Viele Literatur zum Client-/Server-Computing bezieht sich jedoch sowohl auf das Serverprogramm als auch auf den Server Host Computer als "Server".</span><span class="sxs-lookup"><span data-stu-id="6333a-115">However, much literature on client/server computing refers to both the server program and the server host computer as the "server."</span></span> <span data-ttu-id="6333a-116">Das Ergebnis ist, dass nicht immer klar ist, welche Themen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="6333a-116">The result is that it is not always clear which is being discussed.</span></span>

</dd> <dt>

<span data-ttu-id="6333a-117"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6333a-117"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span>
</dt> <dd>

<span data-ttu-id="6333a-118">Serverprogramme lauschen an einem Port oder einer Gruppe von Ports auf dem Server Host Computer auf Client Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="6333a-118">Server programs listen to a port or a group of ports on the server host computer for client requests.</span></span> <span data-ttu-id="6333a-119">Server Host Systeme behalten eine Datenbank dieser Ports bei, die als Endpunkte in RPC bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="6333a-119">Server host systems maintain a database of these ports, which are called endpoints in RPC.</span></span> <span data-ttu-id="6333a-120">Die Datenbank wird als Endpunkt Zuordnung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6333a-120">The database is called the endpoint map.</span></span>

</dd> <dt>

<span data-ttu-id="6333a-121"><span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Lichere</span><span class="sxs-lookup"><span data-stu-id="6333a-121"><span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Binding</span></span>
</dt> <dd>

<span data-ttu-id="6333a-122">Client Programme erstellen eine Bindung an den Server, um eine Kommunikationssitzung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="6333a-122">Client programs create a binding to the server to establish a communication session.</span></span> <span data-ttu-id="6333a-123">Eine Bindung enthält alle Informationen, die die Client Anwendungen zum Erstellen der Sitzung benötigen.</span><span class="sxs-lookup"><span data-stu-id="6333a-123">A binding contains all of the information the client applications needs to create the session.</span></span>

</dd> </dl>

 

 