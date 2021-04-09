---
description: Die SELECT-Funktion wird verwendet, um den Status einer oder mehrerer Sockets in einer Menge zu bestimmen. Der Aufrufer kann für jeden Socket Informationen zu Lese-, Schreib-oder Fehlerstatus anfordern. Ein Satz von Sockets wird durch eine FD- \_ Set-Struktur angegeben.
ms.assetid: 40354d8f-1e8b-48aa-888a-81a421568f23
title: Mehrere Anbieter Einschränkungen bei SELECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2556d98aea60e6fa822f9e3df57cc142c33491d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129156"
---
# <a name="multiple-provider-restrictions-on-select"></a>Mehrere Anbieter Einschränkungen bei SELECT

Die [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -Funktion wird verwendet, um den Status einer oder mehrerer Sockets in einer Menge zu bestimmen. Der Aufrufer kann für jeden Socket Informationen zu Lese-, Schreib-oder Fehlerstatus anfordern. Ein Satz von Sockets wird durch eine [**FD- \_ set**](/windows/desktop/api/winsock/nf-winsock-fd_set) -Struktur angegeben.

Windows Sockets 2 ermöglicht einer Anwendung die Verwendung von mehr als einem Dienstanbieter, aber die [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -Funktion ist auf einen Satz von Sockets beschränkt, die einem einzelnen Dienstanbieter zugeordnet sind. Dadurch wird verhindert, dass eine Anwendung mehrere Sockets durch mehrere Anbieter geöffnet hat.

Es gibt zwei Möglichkeiten, den Status eines Satzes von Sockets zu ermitteln, der mehr als einen Dienstanbieter umfasst:

-   Verwenden der [**wsawaitformultipleevents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) -oder [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) -Funktionen, wenn Blockierungs Semantik verwendet wird.
-   Verwenden der [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) -Funktion, wenn nicht blockierende Vorgänge verwendet werden und die Anwendung bereits eine Windows-nachrichtenpump verwendet.

Wenn eine Anwendung Blockierungs Semantik für einen Satz von Sockets verwenden muss, der mehrere Anbieter umfasst, wird [**wsawaitformultipleevents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) empfohlen. Die Anwendung kann auch die [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) -Funktion verwenden, die es den FD \_ xxx-Netzwerk Ereignissen (siehe [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)) ermöglicht, einem Ereignis Objekt zuzuordnen und innerhalb des ereignisobjektparadigmas behandelt zu werden (beschrieben in überlappenden e [/a-und Ereignis Objekten](overlapped-i-o-and-event-objects-2.md)).

Die [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) -Funktion ist nicht auf einen einzelnen Anbieter beschränkt, da Sie einen einzelnen socketdeskriptor als Eingabeparameter annimmt. Beachten Sie jedoch, dass die [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) -Funktion eine bessere Leistung und Skalierbarkeit gegenüber **WSAAsyncSelect** bietet, da der mehr Aufwand für die Wartung der Nachrichten Pumpe mit Winsock-Ereignis Nachrichten zunimmt, wenn sich die Gesamtzahl der verwendeten Sockets erhöht.

 

 



