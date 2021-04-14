---
description: Die Einführung von überlappenden e/a-Vorgängen erfordert einen Mechanismus, damit Anwendungen Sende-und Empfangs Anforderungen mit ihren nachfolgenden Vervollständigungs hinweisen eindeutig zuordnen können.
ms.assetid: 944d87bd-388f-420d-ac7d-69c4a28f8a5c
title: Ereignis Objekte (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e72b60442f9c56ae2c8e9af905bd14b6536b8e10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343519"
---
# <a name="event-objects-windows-sockets-2"></a>Ereignis Objekte (Windows Sockets 2)

Die Einführung von überlappenden e/a-Vorgängen erfordert einen Mechanismus, damit Anwendungen Sende-und Empfangs Anforderungen mit ihren nachfolgenden Vervollständigungs hinweisen eindeutig zuordnen können. In Windows Sockets 2 wird dies mit Ereignis Objekten erreicht, die nach Windows-Ereignissen modelliert werden. Bei Windows Sockets-Ereignis Objekten handelt es sich um relativ einfache Konstrukte, die erstellt, geschlossen, festgelegt, gelöscht und gewartet werden können. Das Haupt Dienstprogramm ist die Fähigkeit einer Anwendung, blockiert zu werden, und zu warten, bis ein oder mehrere Ereignis Objekte festgelegt werden.

Anwendungen verwenden [**wsacreateevent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) zum Abrufen eines Ereignis Objekt Handles, das dann als erforderlicher Parameter für die überlappenden Versionen von Sende-und Empfangs aufrufen ( [**wsasend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)) bereitgestellt werden kann. Das Ereignis Objekt, das bei der ersten Erstellung gelöscht wird, wird von den Transportanbietern festgelegt, wenn die zugeordnete überlappende e/a-Operation abgeschlossen wurde (entweder erfolgreich oder mit Fehlern). Jedes Ereignis Objekt, das von **wsacreateevent** erstellt wurde, sollte ein entsprechendes [**wsacloseevent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent) aufweisen, um es zu zerstören.

Ereignis Objekte werden auch in [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) verwendet, um einem Ereignis Objekt ein oder mehrere FD \_ xxx-Netzwerkereignisse zuzuordnen. Dies wird in [asynchroner Benachrichtigung mithilfe von Ereignis Objekten](asynchronous-notification-using-event-objects-2.md)beschrieben.

In 32-Bit-Umgebungen werden Ereignisobjekt– zugehörige Funktionen (einschließlich [**wsacreateevent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**wsacloseevent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**wsasetevent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**wsaresetevent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)und [**wsawaitformultipleevents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) ) direkt den entsprechenden nativen Windows-Funktionen zugeordnet. dabei wird der gleiche Funktionsname verwendet, jedoch ohne das WSA-Präfix.

 

 



