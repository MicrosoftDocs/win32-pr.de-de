---
description: Die folgende Funktion wird mit anonymen Pipes verwendet.
ms.assetid: 9e80783e-9641-4cbd-9c28-a8efe6b9efaa
title: Pipefunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0ef895fe8b987f19f025b6a21ef4c3a5dc3cb24db5458595c25708066e8a78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481604"
---
# <a name="pipe-functions"></a>Pipefunktionen

Die folgende Funktion wird mit anonymen Pipes verwendet.



| Funktion                         | BESCHREIBUNG                |
|----------------------------------|----------------------------|
| [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) | Erstellt eine anonyme Pipe. |



 

Die folgenden Funktionen werden mit Named Pipes verwendet.



| Funktion                                                                 | BESCHREIBUNG                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea)                                   | Stellt eine Verbindung mit einer Nachrichtentyppipe her, schreibt in die Pipe und liest sie aus der Pipe und schließt dann die Pipe.                                                                                                                                       |
| [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)                             | Ermöglicht es einem Named Pipe-Serverprozess, zu warten, bis ein Clientprozess eine Verbindung mit einer Instanz einer benannten Pipe herstellt.                                                                                                                         |
| [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)                               | Erstellt eine Instanz einer benannten Pipe und gibt ein Handle für nachfolgende Pipevorgänge zurück. Ein Clientprozess stellt mithilfe der [**CreateFile-**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) oder [**CallNamedPipe-Funktion**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) eine Verbindung mit einer Named Pipe her. |
| [**DisconnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe)                       | Trennt das Serverende einer Named Pipe-Instanz von einem Clientprozess.                                                                                                                                                          |
| [**GetNamedPipeClientComputerName**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientcomputernamea) | Ruft den Clientcomputernamen für die angegebene Named Pipe ab.                                                                                                                                                                    |
| [**GetNamedPipeClientProcessId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientprocessid)       | Ruft den Clientprozessbezeichner für die angegebene Named Pipe ab.                                                                                                                                                               |
| [**GetNamedPipeClientSessionId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientsessionid)       | Ruft den Clientsitzungsbezeichner für die angegebene Named Pipe ab.                                                                                                                                                               |
| [**GetNamedPipeHandleState**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipehandlestatea)               | Ruft Informationen zu einer angegebenen Named Pipe ab.                                                                                                                                                                                 |
| [**GetNamedPipeInfo**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-getnamedpipeinfo)                             | Ruft Informationen zur angegebenen Named Pipe ab.                                                                                                                                                                               |
| [**GetNamedPipeServerProcessId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserverprocessid)       | Ruft den Serverprozessbezeichner für die angegebene Named Pipe ab.                                                                                                                                                               |
| [**GetNamedPipeServerSessionId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserversessionid)       | Ruft den Serversitzungsbezeichner für die angegebene Named Pipe ab.                                                                                                                                                               |
| [**ImpersonateNamedPipeClient**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient)    | Nimmt die Identität einer Named Pipe-Clientanwendung an.                                                                                                                                                                                       |
| [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe)                                   | Kopiert Daten aus einer benannten oder anonymen Pipe in einen Puffer, ohne sie aus der Pipe zu entfernen.                                                                                                                                         |
| [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate)               | Legt den Lesemodus und den Blockierungsmodus der angegebenen Named Pipe fest.                                                                                                                                                               |
| [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)                           | Kombiniert die Funktionen, die eine Nachricht in schreiben und eine Nachricht aus der angegebenen Named Pipe lesen, in einem einzigen Netzwerkvorgang.                                                                                                    |
| [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)                                   | Wartet, bis entweder ein Time out-Intervall verstrichen ist oder eine Instanz der angegebenen Named Pipe für eine Verbindung verfügbar ist.                                                                                                            |



 

 

 
