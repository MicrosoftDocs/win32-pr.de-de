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
# <a name="essential-rpc-binding-terminology"></a>Wichtige RPC-Bindungs Terminologie

Um eine bessere Unterstützung für den Client/Server-Verbindungsprozess zu erhalten, ist es hilfreich, die folgenden Begriffe zu kennen.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Protokoll Sequenz
</dt> <dd>

Wenn Netzwerk Betriebssysteme miteinander kommunizieren, müssen Sie die gleiche Sprache lauschen und sprechen. Diese Sprachen werden als *Protokoll Sequenzen* bezeichnet. Client-und Serverprogramme müssen Protokoll Sequenzen verwenden, die vom verbundenen Netzwerk unterstützt werden. Microsoft RPC unterstützt eine Vielzahl von Protokoll Sequenzen. Weitere Informationen finden Sie unter [Auswählen einer Protokoll Sequenz](selecting-a-protocol-sequence.md), [Angeben von Protokoll Sequenzen](specifying-protocol-sequences.md)und [**Endpunkt**](/windows/desktop/Midl/endpoint).

</dd> <dt>

<span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Server Host Computer oder Server Host System
</dt> <dd>

Das Serverprogramm wird auf dem Server Host Computer ausgeführt. Viele Literatur zum Client-/Server-Computing bezieht sich jedoch sowohl auf das Serverprogramm als auch auf den Server Host Computer als "Server". Das Ergebnis ist, dass nicht immer klar ist, welche Themen behandelt werden.

</dd> <dt>

<span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher
</dt> <dd>

Serverprogramme lauschen an einem Port oder einer Gruppe von Ports auf dem Server Host Computer auf Client Anforderungen. Server Host Systeme behalten eine Datenbank dieser Ports bei, die als Endpunkte in RPC bezeichnet werden. Die Datenbank wird als Endpunkt Zuordnung bezeichnet.

</dd> <dt>

<span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Lichere
</dt> <dd>

Client Programme erstellen eine Bindung an den Server, um eine Kommunikationssitzung einzurichten. Eine Bindung enthält alle Informationen, die die Client Anwendungen zum Erstellen der Sitzung benötigen.

</dd> </dl>

 

 