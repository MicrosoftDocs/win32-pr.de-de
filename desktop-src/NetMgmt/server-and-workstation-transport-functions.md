---
title: Server-und Arbeitsstations Transport-Funktionen
description: Die Transportfunktionen für die Netzwerk Management Server und die Arbeitsstation verarbeiten die Bindung und das Aufheben der Bindung von Transportprotokollen an den Server und den Redirector.
ms.assetid: 64342e21-98f1-42d3-b541-46b826391fad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1ab4a4ce5dcc3b887eb9eb9d5759db89dfed55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337154"
---
# <a name="server-and-workstation-transport-functions"></a>Server-und Arbeitsstations Transport-Funktionen

Die Transportfunktionen für die Netzwerk Management Server und die Arbeitsstation verarbeiten die Bindung und das Aufheben der Bindung von Transportprotokollen an den Server und den Redirector. Die Server Transportfunktionen behandeln Transportprotokolle, die vom Server verwaltet werden. die Transportfunktionen der Arbeitsstation behandeln Transportprotokolle, die vom Redirector verwaltet werden.

Die Dateifreigabe zwischen einem Transportgerät und einem Server besteht aus zwei Komponenten:

-   Der Server Computer, auf dem sich die Dateien befinden.
-   Ein SMB-Client (Server Message Block), der auf die Dateien zugreift.

Der Client Computer kommuniziert mit dem Server Computer über ein lokales Netzwerk mithilfe eines Transport Protokolls. beispielsweise TCP oder XNS. Vom Client werden Anforderungen zum Abrufen von Daten an den Server gesendet. Die Software auf dem Client Computer, von dem die Datei Anforderungen generiert werden, wird als *Redirector* bezeichnet, da lokale Datei Anforderungen an den Server Computer umgeleitet werden. Die Software auf dem Computer, die die Datei Anforderungen empfängt und verarbeitet, wird als *Server* bezeichnet, da Sie die Clients bedient. Das für diese Anforderungen spezifische Format wird als SMB-Protokoll bezeichnet.

Die Server Transportfunktionen sind nachfolgend aufgeführt.



| Funktion                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Netservercomputernameadd**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernameadd) | Bindet einen emulierten Servernamen an jedes Transportprotokoll, für das ein Server aktiv ist. (Kombiniert die Funktionalität der [**netservertransportenum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum) -Funktion und der [**netservertransportaddex**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex) -Funktion.)                                            |
| [**Netservercomputernamedel**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernamedel) | Trennt jedes Netzwerk Transportprotokoll von einem emulierten Servernamen, der durch einen vorherigen-Befehl der **netservercomputernameadd** -Funktion festgelegt wurde.                                                                                                                                                                               |
| [**Netservertransportadd**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportadd)       | Bindet den angegebenen Server an das Transportprotokoll. (Diese Funktion unterstützt nur die Informationsebene " [**Server \_ Transport \_ Info \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0) ".)                                                                                                                                                |
| [**Netservertransportaddex**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex)   | Bindet den angegebenen Server an das Transportprotokoll. (Diese erweiterte Funktion unterstützt die Informationsebenen [**Server \_ Transport \_ Info \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1), [**Server \_ Transport \_ Info \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)und [**Server \_ Transport \_ Info \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3) .) |
| [**Netservertransportdel**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportdel)       | Trennt das Transportprotokoll vom Server.                                                                                                                                                                                                                                                                         |
| [**Netservertransportenum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum)     | Listet die vom Server verwalteten Transportprotokolle auf.                                                                                                                                                                                                                                                                   |



 

Server Transportfunktionen sind auf den folgenden Informationsebenen verfügbar:

-   [**Server \_ Transport \_ Informationen \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0)
-   [**Server \_ Transport \_ Informationen \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1)
-   [**Server \_ Transport \_ Informationen \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)
-   [**Server \_ Transport \_ Info \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3)

Die Transportfunktionen der Arbeitsstation führen äquivalente Vorgänge für die Arbeitsstation aus.

**Windows Server 2003 und Windows XP/2000:** Der Redirector bietet keine Unterstützung für die [**netwkstaturansport Add**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd) -Funktion oder die [**netwkstaturansportdel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel) -Funktion. Sie können die Standardeinstellungen für Transportprotokolle manuell über das Dialogfeld Eigenschaften von LAN- **Verbindung** im Ordner **Netzwerk-und DFÜ-Verbindungen** ändern.

Die Transportfunktionen der Arbeitsstation sind nachfolgend aufgeführt.



| Funktion                                               | BESCHREIBUNG                                                       |
|--------------------------------------------------------|-------------------------------------------------------------------|
| [**Netwkstaturansport**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd)   | Verbindet den Redirector mit dem Transportprotokoll.                |
| [**Netwkstaturansport**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel)   | Trennt das Transportprotokoll vom Redirector.           |
| [**Netwkstatus-Sportenum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstatransportenum) | Listet die Transportprotokolle auf, die vom Redirector verwaltet werden. |



 

Die Transportfunktionen für die Arbeitsstation sind auf einer Informationsebene verfügbar:

-   [**Wksta- \_ Transport \_ Info \_ 0**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_transport_info_0)

 

 




