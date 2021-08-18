---
description: Das Senden und Empfangen von PGM-Daten ähnelt dem Senden oder Empfangen von Daten auf einem Socket. In den folgenden Abschnitten werden PGM-spezifische Aspekte erläutert.
ms.assetid: 51b447ad-b6da-424b-91df-e5be9ce225a5
title: Senden und Empfangen von PGM-Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 130b38ea52e5d0679b988e55f8292b9752a4bf15d0514a8277a2e0b3b2327001
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740571"
---
# <a name="sending-and-receiving-pgm-data"></a>Senden und Empfangen von PGM-Daten

Das Senden und Empfangen von PGM-Daten ähnelt dem Senden oder Empfangen von Daten auf einem Socket. In den folgenden Abschnitten werden PGM-spezifische Aspekte erläutert.

## <a name="sending-pgm-data"></a>Senden von PGM-Daten

Sobald eine PGM-Sendersitzung erstellt wurde, werden Daten mithilfe der verschiedenen sendefunktionen von Windows Sockets gesendet: [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)und [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto). Da Windows Sockets-Handles Dateisystemhandles sind, können auch andere Funktionen wie [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) und CRT-Funktionen Daten übertragen. Der folgende Codeausschnitt veranschaulicht einen PGM-Sendervorgang:


```C++
LONG        error;
    //:
error = send (s, pSendBuffer, SendLength, 0);
if (error == SOCKET_ERROR)
{
    fprintf (stderr, "send() failed: Error = %d\n",
             WSAGetLastError());
}
```



Bei Verwendung des Nachrichtenmodus (SOCK RDM) führt jeder Aufruf einer Sendefunktion zu einer diskreten Nachricht, die manchmal nicht wünschenswert ist. Eine Anwendung möchte möglicherweise eine \_ 2-Megabyte-Nachricht mit mehreren Aufrufen zum Senden von [](/windows/desktop/api/Winsock2/nf-winsock2-send)senden. In solchen Fällen kann der Absender die [RM \_ SET MESSAGE \_ \_ BOUNDARY-Socketoption](socket-options.md) festlegen, um die Größe der folgenden Nachricht anzugeben.

Wenn das Sendefenster voll ist, wird ein neues Senden von der Anwendung erst akzeptiert, wenn das Fenster erweitert wurde. Der Versuch, an einem nicht blockierenden Socket zu senden, schlägt mit WSAEWOULDBLOCK fehl. Ein blockierende Socket wird einfach blockiert, bis das Fenster an den Punkt vorüber geht, an dem die angeforderten Daten gepuffert und gesendet werden können. Bei überlappenden E/A-Daten wird der Vorgang erst abgeschlossen, wenn das Fenster so weit geöffnet ist, dass die neuen Daten berücksichtigt werden.

## <a name="receiving-pgm-data"></a>Empfangen von PGM-Daten

Sobald eine PGM-Empfängersitzung erstellt wurde, werden Daten mithilfe der verschiedenen Windows Sockets-Empfangsfunktionen empfangen: [**recv,**](/windows/desktop/api/winsock/nf-winsock-recv) [**recvfrom,**](/windows/desktop/api/winsock/nf-winsock-recvfrom) [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)und [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom). Da Windows Sockets-Handles auch Dateihandles sind, können die [**ReadFile-**](/windows/win32/api/fileapi/nf-fileapi-readfile) und CRT-Funktionen auch zum Empfangen von PGM-Sitzungsdaten verwendet werden. Der Transport gibt Daten an den Empfänger weiter, solange die Daten nacheinander empfangen werden. Der Transport stellt sicher, dass die zurückgegebenen Daten zusammenhängend und frei von Duplikaten sind. Der folgende Codeausschnitt veranschaulicht einen PGM-Empfangsvorgang:


```C++
LONG        BytesRead;
    //:
BytesRead = recv (sockR, pTestBuffer, MaxBufferSize, 0);
if (BytesRead == 0)
{
    fprintf(stdout, "Session was terminated\n");
}
else if (BytesRead == SOCKET_ERROR)
{
    fprintf(stderr, "recv() failed: Error = %d\n",
            WSAGetLastError());
}
```



Bei Verwendung des Nachrichtenmodus (SOCK RDM) gibt der Transport an, wann eine Teilnachricht empfangen wird, entweder mit dem WSAEMSGSIZE-Fehler oder durch Festlegen des MSG PARTIAL-Flags bei rückgabe der \_ \_ [**WSARecv-**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) und [**WSARecvFrom-Funktionen.**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) Wenn das letzte Fragment der vollständigen Nachricht an den Client zurückgegeben wird, wird der Fehler oder das Flag nicht angegeben.

Wenn die Sitzung ordnungsgemäß beendet wird, schlägt der Empfangsvorgang mit WSAEDISCON fehl. Wenn im Transport Datenverlust auftritt, puffert PGM vorübergehend die Out-of-Sequence-Pakete und versucht, die verlorenen Daten wiederhergestellt zu haben. Wenn der Datenverlust nicht wiederhergestellt werden kann, ist der Empfangsvorgang mit WSAECONNRESET nicht möglich, und die Sitzung wird beendet. Die Sitzung kann aufgrund einer Vielzahl von Bedingungen zurückgesetzt werden, einschließlich der folgenden:

-   Der Empfänger oder die eingehende Verbindungsrate ist zu langsam, um mit der eingehenden Datenrate Schritt zu halten.
-   Übermäßiger Datenverlust tritt auf, möglicherweise aufgrund vorübergehender Netzwerkbedingungen, z. B. Routingprobleme, Netzwerkinstabilität usw.
-   Ein nicht behebbarer Fehler tritt beim Absender auf.
-   Eine übermäßige Ressourcenauslastung tritt auf dem lokalen Computer auf, z. B. das Überschreiten des maximal zulässigen internen Pufferspeichers oder das Auftreten einer Bedingung, bei der keine Ressourcen verfügbar sind.
-   Ein Fehler bei der Datenkonsistenzprüfung tritt auf.
-   Fehler in einer PGM-Komponente hängen von ab, z. B. TCP/IP oder Windows Sockets.

Sowohl das erste als auch das zweite Ergebnis in der obigen Liste können dazu führen, dass der Empfänger eine übermäßige Pufferung vor dem Aussenden der Ressourcen oder vor dem letztendlichen Wechsel über das Fenster des Absenders durchführen kann.

## <a name="terminating-a-pgm-session"></a>Beenden einer PGM-Sitzung

Der PGM-Absender oder -Empfänger kann das Senden oder Empfangen von Daten beenden, indem [**er closesocket aufruft.**](/windows/desktop/api/winsock/nf-winsock-closesocket) Der Empfänger muss **closesocket sowohl** auf den lauschenden als auch auf den empfangenden Sockets aufrufen, um Handlelecks zu verhindern. Das [**Herunterfahren**](/windows/desktop/api/winsock/nf-winsock-shutdown) des Absenders vor dem Aufruf von **closesocket** stellt sicher, dass alle Daten gesendet werden, und stellt sicher, dass Reparaturdaten beibehalten werden, bis das Sendefenster über die letzte Datensequenz hinaus geschaltet wird, auch wenn die Anwendung selbst beendet wird.

 

 
