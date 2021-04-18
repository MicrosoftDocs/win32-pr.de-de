---
description: Die folgende Funktion wird mit anonymen Pipes verwendet.
ms.assetid: 9e80783e-9641-4cbd-9c28-a8efe6b9efaa
title: Pipe-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2413157ca76af56b5344327e1d3a9e93f86253f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347525"
---
# <a name="pipe-functions"></a>Pipe-Funktionen

Die folgende Funktion wird mit anonymen Pipes verwendet.



| Funktion                         | BESCHREIBUNG                |
|----------------------------------|----------------------------|
| [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) | Erstellt eine anonyme Pipe. |



 

Die folgenden Funktionen werden mit Named Pipes verwendet.



| Funktion                                                                 | BESCHREIBUNG                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Callnamedpipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea)                                   | Stellt eine Verbindung mit einer Pipe des Nachrichten Typs her, schreibt in die Pipe und liest Sie aus der Pipe und schließt dann die Pipe.                                                                                                                                       |
| [**Connectnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)                             | Ermöglicht einem Named Pipe Server-Prozess zu warten, bis ein Client Prozess eine Verbindung mit einer Instanz eines Named Pipe herstellt.                                                                                                                         |
| [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)                               | Erstellt eine Instanz eines Named Pipe und gibt ein Handle für nachfolgende Pipe-Vorgänge zurück. Ein Client Prozess stellt eine Verbindung mit einem Named Pipe mithilfe [**der Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "Funktion" oder " [**callnamedpipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) " her. |
| [**Disconnectnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe)                       | Trennt das Server Ende einer Named Pipe-Instanz von einem Client Prozess.                                                                                                                                                          |
| [**Getnamedpipeclientcomputername**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientcomputernamea) | Ruft den Namen des Client Computers für den angegebenen Named Pipe ab.                                                                                                                                                                    |
| [**Getnamedpipeclientprocessid**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientprocessid)       | Ruft den Client Prozess Bezeichner für die angegebene Named Pipe ab.                                                                                                                                                               |
| [**Getnamedpipeclientsessionid**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientsessionid)       | Ruft den Client Sitzungs Bezeichner für die angegebene Named Pipe ab.                                                                                                                                                               |
| [**Getnamedpipelenker State**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipehandlestatea)               | Ruft Informationen zu einem angegebenen Named Pipe ab.                                                                                                                                                                                 |
| [**Getnamedpipeinfo**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-getnamedpipeinfo)                             | Ruft Informationen über die angegebene Named Pipe ab.                                                                                                                                                                               |
| [**Getnamedpipeserverprocessid**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserverprocessid)       | Ruft den Server Prozess Bezeichner für die angegebene Named Pipe ab.                                                                                                                                                               |
| [**Getnamedpipeserversessionid**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserversessionid)       | Ruft den Server Sitzungs Bezeichner für die angegebene Named Pipe ab.                                                                                                                                                               |
| [**Identität-Identitäts-amedpipeclient**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient)    | Nimmt die Identität einer Named Pipe-Client Anwendung an.                                                                                                                                                                                       |
| [**"Peer Name"**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe)                                   | Kopiert Daten aus einer benannten oder anonymen Pipe in einen Puffer, ohne Sie aus der Pipe zu entfernen.                                                                                                                                         |
| [**Setnamedpipelenker State**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate)               | Legt den Lesemodus und den Blockierungs Modus der angegebenen Named Pipe fest.                                                                                                                                                               |
| [**Transactnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)                           | Kombiniert die Funktionen, die eine Meldung schreiben, und liest eine Meldung aus dem angegebenen Named Pipe in einem einzelnen Netzwerk Vorgang.                                                                                                    |
| [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)                                   | Wartet, bis entweder ein Timeout Intervall abläuft oder eine Instanz des angegebenen Named Pipe für eine Verbindung verfügbar ist.                                                                                                            |



 

 

 
