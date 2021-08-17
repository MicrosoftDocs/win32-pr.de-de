---
description: Die Einführung überlappende E/A erfordert einen Mechanismus, mit dem Anwendungen Sende- und Empfangsanforderungen eindeutig ihren nachfolgenden Vervollständigungsanzeigen zuordnen können.
ms.assetid: 944d87bd-388f-420d-ac7d-69c4a28f8a5c
title: Ereignisobjekte (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34820d7df92704d86f7dbdc100816789488426e2fdd553456be94da921811c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132593"
---
# <a name="event-objects-windows-sockets-2"></a>Ereignisobjekte (Windows Sockets 2)

Die Einführung überlappende E/A erfordert einen Mechanismus, mit dem Anwendungen Sende- und Empfangsanforderungen eindeutig ihren nachfolgenden Vervollständigungsanzeigen zuordnen können. In Windows Sockets 2 wird dies mit Ereignisobjekten erreicht, die nach Windows werden. Windows Sockets-Ereignisobjekte sind recht einfache Konstrukte, die erstellt und geschlossen, festgelegt und entsperrt sowie auf gewartet und abgewartet werden können. Ihr Hauptprogramm ist die Fähigkeit einer Anwendung, zu blockieren und zu warten, bis ein oder mehrere Ereignisobjekte festgelegt werden.

Anwendungen verwenden [**WSACreateEvent,**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) um ein Ereignisobjekthandl zu erhalten, das dann als erforderlicher Parameter für die überlappenden Versionen von Sende- und Empfangsaufrufen [**(WSASend,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) [**WSASendTo,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) [**WSARecv,**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) [**WSARecvFrom)**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)bereitgestellt werden kann. Das Ereignisobjekt, das bei der ersten Erstellt wird, wird von den Transportanbietern festgelegt, wenn der zugeordnete überlappende E/A-Vorgang abgeschlossen wurde (entweder erfolgreich oder mit Fehlern). Jedes von **WSACreateEvent** erstellte Ereignisobjekt sollte über ein entsprechendes [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent) verfügen, um es zu zerstören.

Ereignisobjekte werden auch in [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) verwendet, um ein oder mehrere \_ FD XXX-Netzwerkereignisse einem Ereignisobjekt zu zuordnen. Dies wird unter [Asynchrone Benachrichtigung mithilfe von Ereignisobjekten beschrieben.](asynchronous-notification-using-event-objects-2.md)

In 32-Bit-Umgebungen werden ereignisobjektbezogene Funktionen, einschließlich [**WSACreateEvent,**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) [**WSACloseEvent,**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent) [**WSASetEvent,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent) [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)und [**WSAWaitForMultipleEvents,**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) direkt den entsprechenden nativen Windows-Funktionen zugeordnet, die denselben Funktionsnamen verwenden, jedoch ohne das WSA-Präfix.

 

 



