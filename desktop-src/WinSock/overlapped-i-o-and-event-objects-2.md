---
description: Windows Sockets 2 unterstützt überlappende E/A- und alle Transportanbieter unterstützen diese Funktion.
ms.assetid: b36ab606-df1a-4254-b048-6d47eb366275
title: Überlappende E/A- und Ereignisobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca6ae2ee17036275183518bfd444b9317bcdc05145a9fcb327ad48388618a66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741053"
---
# <a name="overlapped-io-and-event-objects"></a>Überlappende E/A- und Ereignisobjekte

Windows Sockets 2 unterstützt überlappende E/A- und alle Transportanbieter unterstützen diese Funktion. Überlappende E/A-Funktionen folgen dem in Windows eingerichteten Modell und [](/windows/desktop/api/Winsock2/nf-winsock2-socket) können für Sockets ausgeführt werden, die mit der Socketfunktion oder sockets erstellt wurden, die mit der [**WSASocket-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) mit dem im *dwFlags-Parameter* festgelegten **Flag WSA \_ FLAG \_ OVERLAPPED** erstellt wurden.

> [!Note]  
> Das Erstellen eines Sockets mit dem überlappenden Attribut hat keine Auswirkungen darauf, ob sich ein Socket derzeit im blockierenden oder nicht blockierenden Modus befindet. Sockets, die mit dem überlappenden Attribut erstellt wurden, können verwendet werden, um überlappende E/A-Aktionen durchzuführen. Dadurch wird der Blockierungsmodus eines Sockets nicht geändert. Da überlappende E/A-Vorgänge nicht blockiert werden, ist der Blockierungsmodus eines Sockets für diese Vorgänge irrelevant.

 

Für den Empfang verwenden Anwendungen die [**WSARecv-**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) oder [**WSARecvFrom-Funktionen,**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) um Puffer zu liefern, in die Daten empfangen werden sollen. Wenn vor dem Zeitpunkt, zu dem Daten vom Netzwerk empfangen wurden, ein oder mehrere Puffer gesendet werden, können diese Daten sofort beim Eintreffen in den Puffern des Benutzers platziert werden. Dadurch kann der Kopiervorgang vermieden werden, der andernfalls zu dem Zeitpunkt auftritt, zu dem die [**recv-**](/windows/desktop/api/winsock/nf-winsock-recv) oder [**recvfrom-Funktion**](/windows/desktop/api/winsock/nf-winsock-recvfrom) aufgerufen wird. Wenn beim Posten von Empfangspuffern bereits Daten vorhanden sind, werden sie sofort in die Puffer des Benutzers kopiert.

Wenn Daten empfangen werden, wenn von der Anwendung keine Empfangspuffer gesendet wurden, greift das Netzwerk auf die vertraute synchrone Betriebsart zurück. Das heißt, die eingehenden Daten werden intern gepuffert, bis die Anwendung einen Empfangsaufruf aus gibt und dadurch einen Puffer liefert, in den die Daten kopiert werden können. Eine Ausnahme ist, wenn die Anwendung [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) verwendet, um die Größe des Empfangspuffers auf 0 (null) zu setzen. In diesem Fall lassen zuverlässige Protokolle nur den Daten empfangen, wenn Anwendungspuffer gepostet wurden und Daten in unzuverlässigen Protokollen verloren gehen würden.

Auf der Sendeseite verwenden Anwendungen [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) oder [**WSASendTo,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) um Zeiger auf gefüllte Puffer zu liefern, und stimmen dann zu, die Puffer in irgendeiner Weise zu stören, bis das Netzwerk den Inhalt des Puffers verbraucht hat.

Überlappende Sende- und Empfangsaufrufe werden sofort zurück. Der Rückgabewert 0 (null) gibt an, dass der E/A-Vorgang sofort abgeschlossen wurde und dass die entsprechende Vervollständigungsanzeige bereits aufgetreten ist. Das heißt, das zugeordnete Ereignisobjekt wurde signalisiert, oder eine Abschlussroutine wurde in die Warteschlange eingereiht und wird ausgeführt, wenn der aufrufende Thread in den wartbaren Wartezustand versetzt wird.

Der Rückgabewert SOCKET ERROR in Verbindung mit einem Fehlercode von \_ [WSA \_ IO \_ PENDING](windows-sockets-error-codes-2.md) gibt an, dass der überlappende Vorgang erfolgreich initiiert wurde und dass eine nachfolgende Angabe angezeigt wird, wenn Sendepuffer verbraucht wurden oder ein Empfangsvorgang abgeschlossen wurde. Bei Sockets im Bytestream-Format tritt die Vervollständigungsanzeige jedoch immer dann auf, wenn die eingehenden Daten erschöpft sind, unabhängig davon, ob die Puffer voll sind. Jeder andere Fehlercode gibt an, dass der überlappende Vorgang nicht erfolgreich initiiert wurde und keine Vervollständigungsanzeige anstehender ist.

Sowohl Sende- als auch Empfangsvorgänge können überlappen. Die Empfangsfunktionen können mehrmals aufgerufen werden, um Empfangspuffer als Vorbereitung auf eingehende Daten zu senden, und die Sendefunktionen können mehrmals aufgerufen werden, um mehrere zu sendende Puffer in die Warteschlange zu stellen. Während die Anwendung davon abhängig sein kann, dass eine Reihe von überlappenden Sendepuffern in der angegebenen Reihenfolge gesendet wird, können die entsprechenden Vervollständigungsanzeigen in einer anderen Reihenfolge auftreten. Auf der empfangenden Seite können Puffer in der Reihenfolge gefüllt werden, in der sie bereitgestellt werden, aber die Vervollständigungsanzeigen können in einer anderen Reihenfolge auftreten.

In vielen Fällen überlappen sich Winsock-Vorgänge mit [**AcceptEx,**](/windows/win32/api/mswsock/nf-mswsock-acceptex) [**ConnectEx,**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) [**WSASend,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) [**WSARecv,**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile)und ähnlichen Funktionen. Das Verhalten ist jedoch für die weitere Verwendung eines Sockets, der ausstehende Vorgänge abgebrochen hat, nicht definiert. Die [**closesocket-Funktion**](/windows/desktop/api/winsock/nf-winsock-closesocket) sollte nach dem Abbrechen eines überlappenden Vorgangs aufgerufen werden. Um optimale Ergebnisse zu erzielen, sollte daher anstelle des direkten Abbrechens der E/A die **closesocket-Funktion** aufgerufen werden, um den Socket zu schließen, der schließlich alle ausstehenden Vorgänge beendet.

Das Feature für verzögerte Vervollständigung überlappende E/A ist auch für [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)verfügbar, eine erweiterte Version von [**ioctlsocket.**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)

 

 
