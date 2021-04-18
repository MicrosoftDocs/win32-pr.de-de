---
description: Windows Sockets 2 unterstützt überlappende e/a-Vorgänge, und alle Transportanbieter unterstützen diese Funktion.
ms.assetid: b36ab606-df1a-4254-b048-6d47eb366275
title: Überlappende e/a-und Ereignis Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed034f06243959d94a1ada7eaa71e33c84cd35ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368075"
---
# <a name="overlapped-io-and-event-objects"></a>Überlappende e/a-und Ereignis Objekte

Windows Sockets 2 unterstützt überlappende e/a-Vorgänge, und alle Transportanbieter unterstützen diese Funktion. Überlappende e/a-Vorgänge folgen dem in Windows eingerichteten Modell und können auf Sockets ausgeführt werden, die mit der [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) erstellt wurden, oder mit Sockets, die mit der [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) -Funktion erstellt wurden, wobei das überlappende Flag für das **WSA- \_ Flag \_** im Parameter *dwFlags*

> [!Note]  
> Das Erstellen eines Sockets mit dem überlappenden Attribut hat keine Auswirkung darauf, ob sich ein Socket derzeit im blockierenden oder nicht blockierenden Modus befindet. Sockets, die mit dem überlappenden Attribut erstellt werden, können verwendet werden, um überlappende e/a-Vorgänge auszuführen – dadurch wird der Blockierungs Modus eines Sockets nicht geändert. Da überlappende e/a-Vorgänge nicht blockiert werden, ist der Blockierungs Modus eines Sockets für diese Vorgänge irrelevant.

 

Für den Empfang verwenden Anwendungen die [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) -oder [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) -Funktionen, um Puffer anzugeben, in die Daten empfangen werden sollen. Wenn ein oder mehrere Puffer vor dem Zeitpunkt gepostet werden, zu dem die Daten vom Netzwerk empfangen wurden, können diese Daten sofort in die Puffer des Benutzers eingefügt werden, sobald sie eintreffen. Dadurch kann der Kopiervorgang vermieden werden, der andernfalls zum Zeitpunkt des aufgerufenen der [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) -oder der [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) -Funktion stattfindet. Wenn Daten bereits vorhanden sind, wenn Empfangs Puffer gepostet werden, werden Sie sofort in die Puffer des Benutzers kopiert.

Wenn Daten empfangen werden, wenn von der Anwendung keine Empfangs Puffer gepostet wurden, greift das Netzwerk auf den vertrauten synchronen Vorgangs Stil zu. Das heißt, die eingehenden Daten werden intern gepuffert, bis die Anwendung einen RECEIVE-Befehl ausgibt und somit einen Puffer bereitstellt, in den die Daten kopiert werden können. Eine Ausnahme besteht darin, dass die Anwendung [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) verwendet, um die Größe des Empfangspuffers auf NULL festzulegen. In dieser Instanz können zuverlässige Protokolle nur Daten empfangen, wenn Anwendungs Puffer gepostet wurden, und Daten zu unzuverlässigen Protokollen würden verloren gehen.

Auf der sendenden Seite verwenden Anwendungen [**wsasend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) oder [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) , um Zeiger auf gefüllte Puffer bereitzustellen, und dann erklären Sie sich damit einverstanden, die Puffer in irgendeiner Weise zu stören, bis das Netzwerk den Inhalt des Puffers verbraucht hat.

Überlappende Sende-und Empfangs Aufrufe werden sofort zurückgegeben. Der Rückgabewert 0 (null) gibt an, dass der e/a-Vorgang sofort abgeschlossen wurde und dass die entsprechende Vervollständigungs Angabe bereits erfolgt ist. Das heißt, das zugeordnete Ereignis Objekt wurde signalisiert, oder eine Vervollständigungs Routine wurde in die Warteschlange eingereiht und wird ausgeführt, wenn der aufrufende Thread in den Wartezustand der Warn Tabelle wechselt.

Ein Rückgabewert von Socketfehler, der \_ mit einem Fehlercode von [WSA \_ \_ ](windows-sockets-error-codes-2.md) -e/a-Vorgängen gekoppelt ist, weist darauf hin, dass der überlappende Vorgang erfolgreich initiiert wurde und dass ein weiterer Hinweis bereitgestellt wird, wenn Sendepuffer verarbeitet wurden oder wenn ein Empfangsvorgang abgeschlossen wurde. Bei Sockets, bei denen es sich um einen Byte Datenstrom Stil handelt, wird der Abschluss Hinweis immer dann angezeigt, wenn die eingehenden Daten erschöpft sind, unabhängig davon, ob die Puffer voll sind. Jeder andere Fehlercode gibt an, dass der überlappende Vorgang nicht erfolgreich initiiert wurde und keine Vervollständigungs Angabe erfolgt.

Sende-und Empfangs Vorgänge können überlappen. Die Empfangsfunktionen können mehrmals aufgerufen werden, um Empfangs Puffer zur Vorbereitung eingehender Daten bereitzustellen. die Sende Funktionen können mehrmals aufgerufen werden, um mehrere Puffer in die Warteschlange zu senden. Obwohl die Anwendung sich auf eine Reihe von überlappenden Sende Puffern verlassen kann, die in der angegebenen Reihenfolge gesendet werden, können die entsprechenden Vervollständigungs Hinweise in einer anderen Reihenfolge auftreten. Ebenso können Puffer auf der Empfangsseite in der Reihenfolge ausgefüllt werden, in der Sie bereitgestellt werden, aber die Abschluss Hinweise können in einer anderen Reihenfolge auftreten.

In vielen Fällen können überlappende Winsock-Vorgänge mit " [**Accept tex**](/windows/win32/api/mswsock/nf-mswsock-acceptex)", " [**connectex**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)", " [**wsasend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)", " [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)", " [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile)" und ähnlichen Funktionen abgebrochen werden. Allerdings ist das Verhalten für die fortgesetzte Verwendung eines Sockets, der ausstehende Vorgänge abgebrochen hat, nicht definiert. Die [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) -Funktion sollte aufgerufen werden, nachdem ein überlappende Vorgang abgebrochen wurde. Daher sollte die **closesocket** -Funktion zum Schließen des Sockets aufgerufen werden, um die besten Ergebnisse zu erzielen, anstatt die e/a direkt abzubrechen. Dadurch werden alle ausstehenden Vorgänge abgebrochen.

Die verzögerte Vervollständigungsfunktion der überlappenden e/a ist auch für [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)verfügbar. Dies ist eine erweiterte Version von [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket).

 

 
