---
description: Das Senden und empfangen von PGM-Daten ähnelt dem Senden und empfangen von Daten auf einem beliebigen Socket. In den folgenden Abschnitten werden spezifische Überlegungen zu PGM beschrieben.
ms.assetid: 51b447ad-b6da-424b-91df-e5be9ce225a5
title: Senden und empfangen von PGM-Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab73999c33c97c6ba528552af6d746d54fb605df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131168"
---
# <a name="sending-and-receiving-pgm-data"></a>Senden und empfangen von PGM-Daten

Das Senden und empfangen von PGM-Daten ähnelt dem Senden und empfangen von Daten auf einem beliebigen Socket. In den folgenden Abschnitten werden spezifische Überlegungen zu PGM beschrieben.

## <a name="sending-pgm-data"></a>Senden von PGM-Daten

Nachdem eine PGM-Sender Sitzung erstellt wurde, werden die Daten mithilfe der verschiedenen Windows Sockets Send-Funktionen gesendet: [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto), [**wsasend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)und [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto). Da Windows Sockets-Handles Dateisystem Handles sind, können auch andere Funktionen, wie z. b. " [**Write File**](/windows/win32/api/fileapi/nf-fileapi-writefile) " und CRT-Funktionen, Daten übertragen. Der folgende Code Ausschnitt veranschaulicht einen PGM-Absender Vorgang:


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



Bei der Verwendung des Nachrichten Modus (Sock \_ RDM) führt jeder Aufruf einer Sende Funktion zu einer diskreten Nachricht, was manchmal nicht wünschenswert ist. eine Anwendung möchte eine 2 Megabyte-Nachricht mit mehreren [**gesendeten**](/windows/desktop/api/Winsock2/nf-winsock2-send)aufrufen senden. Unter diesen Umständen kann der Absender die Option [RM \_ Set \_ Message \_ Border](socket-options.md) Socket festlegen, um die Größe der Nachrichten anzugeben, die nachverfolgt werden.

Wenn das Sendefenster voll ist, wird ein neues Send von der Anwendung erst dann akzeptiert, wenn das Fenster erweitert wurde. Der Versuch, einen nicht blockierenden Socket zu senden, schlägt mit "WSAEWOULDBLOCK;" fehl. ein blockierender Socket wird einfach blockiert, bis das Fenster bis zu dem Punkt wechselt, an dem die angeforderten Daten gepuffert und gesendet werden können. In überlappenden e/a-Vorgängen wird der Vorgang erst durchgeführt, wenn das Fenster genug erweitert, um die neuen Daten aufnehmen zu können.

## <a name="receiving-pgm-data"></a>Empfangen von PGM-Daten

Nachdem eine PGM-Empfänger Sitzung erstellt wurde, werden Daten mithilfe der verschiedenen Windows Sockets-Empfangsfunktionen empfangen: [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)und [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom). Da Windows Sockets-Handles auch Datei Handles sind, können die Funktionen " [**Infofile**](/windows/win32/api/fileapi/nf-fileapi-readfile) " und "CRT" auch zum Empfangen von PGM-Sitzungsdaten verwendet werden. Der Transport leitet Daten an den Empfänger weiter, sobald sie eintreffen, solange die Daten nacheinander sind. Der Transport gewährleistet, dass die zurückgegebenen Daten zusammenhängend und frei von Duplikaten sind. Der folgende Code Ausschnitt veranschaulicht einen PGM-Empfangsvorgang:


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



Wenn Sie den Nachrichten Modus (Sock \_ RDM) verwenden, gibt der Transport an, wann eine partielle Nachricht empfangen wird, entweder mit dem Fehler "wsaemsgsize", oder indem das Flag für die Nachrichten \_ Teilmenge bei Rückgabe von den Funktionen [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) und [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) festgelegt wird. Wenn das letzte Fragment der vollständigen Nachricht an den Client zurückgegeben wird, wird der Fehler oder das Flag nicht angezeigt.

Wenn die Sitzung ordnungsgemäß beendet wird, schlägt der Empfangsvorgang mit wsaediscon fehl. Wenn Datenverluste beim Transport auftreten, puffert PGM temporär die Out-of-Sequence-Pakete und versucht, die verlorenen Daten wiederherzustellen. Wenn der Datenverlust nicht wiederherstellbar ist, schlägt der Empfangsvorgang mit WSAECONNRESET fehl, und die Sitzung wird beendet. Die Sitzung kann aufgrund einer Vielzahl von Bedingungen zurückgesetzt werden, einschließlich der folgenden:

-   Der Empfänger oder die eingehende Verbindungs Rate ist zu langsam, um die Geschwindigkeit der eingehenden Daten Rate zu behalten.
-   Übermäßig viele Datenverluste treten auf, möglicherweise aufgrund vorübergehender Netzwerkbedingungen, z. b. Routing Probleme, Netzwerk Instabilität usw.
-   Ein nicht BEHEB barer Fehler tritt beim Absender auf.
-   Auf dem lokalen Computer ist eine übermäßige Ressourcenauslastung aufgetreten, z. b. das Überschreiten des maximal zulässigen internen Pufferspeichers oder das Auftreten einer Bedingung außerhalb der Ressourcen.
-   Ein Datenkonsistenz Prüfungs Fehler tritt auf.
-   Fehler in einer Komponente, von der PGM abhängig ist, wie z. b. TCP/IP oder Windows Sockets.

Sowohl das erste als auch das zweite Element in der obigen Liste können dazu führen, dass der Empfänger eine übermäßige Pufferung durchführt, bevor die Ressourcen nicht mehr ausgeführt werden, oder bevor das Absender Fenster überschritten wird.

## <a name="terminating-a-pgm-session"></a>Beenden einer PGM-Sitzung

Der PGM-Sender oder-Empfänger kann das Senden oder empfangen von Daten durch Aufrufen von [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)abbrechen. Der Empfänger muss **closesocket** für die Abhör-und empfangenden Sockets aufzurufen, um handle-Verluste zu verhindern. Durch den Aufruf von [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) für den Absender vor dem Aufruf von **closesocket** wird sichergestellt, dass alle Daten gesendet werden, und es wird sichergestellt, dass die Reparatur Daten beibehalten werden, bis das Sendefenster die letzte Datensequenz überschreitet.

 

 
