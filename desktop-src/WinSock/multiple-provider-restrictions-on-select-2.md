---
description: Die select-Funktion wird verwendet, um den Status eines oder mehrere Sockets in einer Gruppe zu bestimmen. Für jeden Socket kann der Aufrufer Informationen zum Lese-, Schreib- oder Fehlerstatus anfordern. Ein Satz von Sockets wird durch eine FD \_ SET-Struktur angegeben.
ms.assetid: 40354d8f-1e8b-48aa-888a-81a421568f23
title: Einschränkungen für mehrere Anbieter bei Auswahl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec5c89c6dd2db809a356f5b53212fd019e32fd9e348c298bcab7f567ee2d0fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569630"
---
# <a name="multiple-provider-restrictions-on-select"></a>Einschränkungen für mehrere Anbieter bei Auswahl

Die [**select-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-select) wird verwendet, um den Status eines oder mehrere Sockets in einer Gruppe zu bestimmen. Für jeden Socket kann der Aufrufer Informationen zum Lese-, Schreib- oder Fehlerstatus anfordern. Ein Satz von Sockets wird durch eine [**FD \_ SET-Struktur**](/windows/desktop/api/winsock/nf-winsock-fd_set) angegeben.

Windows Sockets 2 ermöglicht einer Anwendung die Verwendung von mehr als einem Dienstanbieter, aber die [**select-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-select) ist auf einen Satz von Sockets beschränkt, die einem einzelnen Dienstanbieter zugeordnet sind. Dies schränkt eine Anwendung nicht ein, dass mehrere Sockets über mehrere Anbieter geöffnet sind.

Es gibt zwei Möglichkeiten, den Status einer Gruppe von Sockets zu bestimmen, die sich über mehrere Dienstanbieter erstreckt:

-   Verwenden der [**WSAWaitForMultipleEvents-**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) oder [**WSAEventSelect-Funktionen,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) wenn blockierende Semantik verwendet wird.
-   Verwenden der [**WSAAsyncSelect-Funktion,**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) wenn nicht blockierende Vorgänge verwendet werden und die Anwendung bereits eine Windows verwendet.

Wenn eine Anwendung blockierende Semantik für eine Gruppe von Sockets verwenden muss, die mehrere Anbieter umfasst, wird [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) empfohlen. Die Anwendung kann auch die [**WSAEventSelect-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) verwenden, mit der die \_ FD XXX-Netzwerkereignisse (siehe [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)) einem Ereignisobjekt zuordnen und innerhalb des Ereignisobjektparadigmas behandelt werden können (beschrieben unter Überlappende E/A- und [Ereignisobjekte).](overlapped-i-o-and-event-objects-2.md)

Die [**WSAAsyncSelect-Funktion**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) ist nicht auf einen einzelnen Anbieter beschränkt, da sie einen einzelnen Socketdeskriptor als Eingabeparameter akzeptiert. Beachten Sie jedoch, dass die [**WSAEventSelect-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) gegenüber **WSAAsyncSelect** eine bessere Leistung und Skalierbarkeit bietet, da sich der Aufwand für die Verwaltung der Nachrichtenpump mit Winsock-Ereignismeldungen erhöht, wenn die Gesamtzahl der verwendeten Sockets zunimmt.

 

 



