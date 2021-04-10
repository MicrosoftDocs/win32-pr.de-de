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
# <a name="sending-and-receiving-pgm-data"></a><span data-ttu-id="32e49-104">Senden und empfangen von PGM-Daten</span><span class="sxs-lookup"><span data-stu-id="32e49-104">Sending and Receiving PGM Data</span></span>

<span data-ttu-id="32e49-105">Das Senden und empfangen von PGM-Daten ähnelt dem Senden und empfangen von Daten auf einem beliebigen Socket.</span><span class="sxs-lookup"><span data-stu-id="32e49-105">Sending and receiving PGM data is similar to sending or receiving data on any socket.</span></span> <span data-ttu-id="32e49-106">In den folgenden Abschnitten werden spezifische Überlegungen zu PGM beschrieben.</span><span class="sxs-lookup"><span data-stu-id="32e49-106">There are considerations specific to PGM, outlined in the following paragraphs.</span></span>

## <a name="sending-pgm-data"></a><span data-ttu-id="32e49-107">Senden von PGM-Daten</span><span class="sxs-lookup"><span data-stu-id="32e49-107">Sending PGM Data</span></span>

<span data-ttu-id="32e49-108">Nachdem eine PGM-Sender Sitzung erstellt wurde, werden die Daten mithilfe der verschiedenen Windows Sockets Send-Funktionen gesendet: [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto), [**wsasend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)und [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto).</span><span class="sxs-lookup"><span data-stu-id="32e49-108">Once a PGM sender session is created, data is sent using the various Windows Sockets send functions: [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), and [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto).</span></span> <span data-ttu-id="32e49-109">Da Windows Sockets-Handles Dateisystem Handles sind, können auch andere Funktionen, wie z. b. " [**Write File**](/windows/win32/api/fileapi/nf-fileapi-writefile) " und CRT-Funktionen, Daten übertragen.</span><span class="sxs-lookup"><span data-stu-id="32e49-109">Since Windows Sockets handles are file system handles, other functions such as [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) and CRT functions can also transmit data.</span></span> <span data-ttu-id="32e49-110">Der folgende Code Ausschnitt veranschaulicht einen PGM-Absender Vorgang:</span><span class="sxs-lookup"><span data-stu-id="32e49-110">The following code snippet illustrates a PGM sender operation:</span></span>


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



<span data-ttu-id="32e49-111">Bei der Verwendung des Nachrichten Modus (Sock \_ RDM) führt jeder Aufruf einer Sende Funktion zu einer diskreten Nachricht, was manchmal nicht wünschenswert ist. eine Anwendung möchte eine 2 Megabyte-Nachricht mit mehreren [**gesendeten**](/windows/desktop/api/Winsock2/nf-winsock2-send)aufrufen senden.</span><span class="sxs-lookup"><span data-stu-id="32e49-111">When using message mode (SOCK\_RDM), each call to a send function results in a discrete message, which sometimes isn't desirable; an application may want to send a 2 megabyte message with multiple calls to [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send).</span></span> <span data-ttu-id="32e49-112">Unter diesen Umständen kann der Absender die Option [RM \_ Set \_ Message \_ Border](socket-options.md) Socket festlegen, um die Größe der Nachrichten anzugeben, die nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="32e49-112">In such circumstances, the sender can set the [RM\_SET\_MESSAGE\_BOUNDARY](socket-options.md) socket option to indicate the size of the message that followings.</span></span>

<span data-ttu-id="32e49-113">Wenn das Sendefenster voll ist, wird ein neues Send von der Anwendung erst dann akzeptiert, wenn das Fenster erweitert wurde.</span><span class="sxs-lookup"><span data-stu-id="32e49-113">If the send window is full, a new send from the application is not accepted until window has been advanced.</span></span> <span data-ttu-id="32e49-114">Der Versuch, einen nicht blockierenden Socket zu senden, schlägt mit "WSAEWOULDBLOCK;" fehl. ein blockierender Socket wird einfach blockiert, bis das Fenster bis zu dem Punkt wechselt, an dem die angeforderten Daten gepuffert und gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="32e49-114">Attempting to send on a non-blocking socket fails with WSAEWOULDBLOCK; a blocking socket simply blocks until the window advances to the point where the requested data can be buffered and sent.</span></span> <span data-ttu-id="32e49-115">In überlappenden e/a-Vorgängen wird der Vorgang erst durchgeführt, wenn das Fenster genug erweitert, um die neuen Daten aufnehmen zu können.</span><span class="sxs-lookup"><span data-stu-id="32e49-115">In overlapped I/O, the operation does not complete until the window advances enough to accommodate the new data.</span></span>

## <a name="receiving-pgm-data"></a><span data-ttu-id="32e49-116">Empfangen von PGM-Daten</span><span class="sxs-lookup"><span data-stu-id="32e49-116">Receiving PGM Data</span></span>

<span data-ttu-id="32e49-117">Nachdem eine PGM-Empfänger Sitzung erstellt wurde, werden Daten mithilfe der verschiedenen Windows Sockets-Empfangsfunktionen empfangen: [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)und [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom).</span><span class="sxs-lookup"><span data-stu-id="32e49-117">Once a PGM receiver session is created, data is received using the various Windows Sockets receive functions: [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), and [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom).</span></span> <span data-ttu-id="32e49-118">Da Windows Sockets-Handles auch Datei Handles sind, können die Funktionen " [**Infofile**](/windows/win32/api/fileapi/nf-fileapi-readfile) " und "CRT" auch zum Empfangen von PGM-Sitzungsdaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32e49-118">Since Windows Sockets handles are also file handles, the [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) and CRT functions can also be used to receive PGM session data.</span></span> <span data-ttu-id="32e49-119">Der Transport leitet Daten an den Empfänger weiter, sobald sie eintreffen, solange die Daten nacheinander sind.</span><span class="sxs-lookup"><span data-stu-id="32e49-119">The transport forwards data up to the receiver as it arrives as long as the data is in sequence.</span></span> <span data-ttu-id="32e49-120">Der Transport gewährleistet, dass die zurückgegebenen Daten zusammenhängend und frei von Duplikaten sind.</span><span class="sxs-lookup"><span data-stu-id="32e49-120">The transport guarantees that the data returned is contiguous and free of duplicates.</span></span> <span data-ttu-id="32e49-121">Der folgende Code Ausschnitt veranschaulicht einen PGM-Empfangsvorgang:</span><span class="sxs-lookup"><span data-stu-id="32e49-121">The following code snippet illustrates a PGM receive operation:</span></span>


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



<span data-ttu-id="32e49-122">Wenn Sie den Nachrichten Modus (Sock \_ RDM) verwenden, gibt der Transport an, wann eine partielle Nachricht empfangen wird, entweder mit dem Fehler "wsaemsgsize", oder indem das Flag für die Nachrichten \_ Teilmenge bei Rückgabe von den Funktionen [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) und [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="32e49-122">When using message mode (SOCK\_RDM), the transport indicates when a partial message is received, either with the WSAEMSGSIZE error, or by setting the MSG\_PARTIAL flag upon return from the [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) and [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) functions.</span></span> <span data-ttu-id="32e49-123">Wenn das letzte Fragment der vollständigen Nachricht an den Client zurückgegeben wird, wird der Fehler oder das Flag nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="32e49-123">When the last fragment of the full message is returned to the client, the error or flag is not indicated.</span></span>

<span data-ttu-id="32e49-124">Wenn die Sitzung ordnungsgemäß beendet wird, schlägt der Empfangsvorgang mit wsaediscon fehl.</span><span class="sxs-lookup"><span data-stu-id="32e49-124">When the session is terminated gracefully, the receive operation fails with WSAEDISCON.</span></span> <span data-ttu-id="32e49-125">Wenn Datenverluste beim Transport auftreten, puffert PGM temporär die Out-of-Sequence-Pakete und versucht, die verlorenen Daten wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="32e49-125">When data loss occurs in the transport, PGM temporarily buffers the out-of-sequence packets and attempts to recover the lost data.</span></span> <span data-ttu-id="32e49-126">Wenn der Datenverlust nicht wiederherstellbar ist, schlägt der Empfangsvorgang mit WSAECONNRESET fehl, und die Sitzung wird beendet.</span><span class="sxs-lookup"><span data-stu-id="32e49-126">If the data-loss is unrecoverable, the receive operation fail with WSAECONNRESET, and the session is terminated.</span></span> <span data-ttu-id="32e49-127">Die Sitzung kann aufgrund einer Vielzahl von Bedingungen zurückgesetzt werden, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="32e49-127">The session can be reset due to a variety of conditions, including the following:</span></span>

-   <span data-ttu-id="32e49-128">Der Empfänger oder die eingehende Verbindungs Rate ist zu langsam, um die Geschwindigkeit der eingehenden Daten Rate zu behalten.</span><span class="sxs-lookup"><span data-stu-id="32e49-128">The receiver or the incoming connection rate is too slow to keep pace with the incoming data rate.</span></span>
-   <span data-ttu-id="32e49-129">Übermäßig viele Datenverluste treten auf, möglicherweise aufgrund vorübergehender Netzwerkbedingungen, z. b. Routing Probleme, Netzwerk Instabilität usw.</span><span class="sxs-lookup"><span data-stu-id="32e49-129">Excessive data loss occurs, possibly due to transient network conditions, such as routing problems, network instability, and so forth.</span></span>
-   <span data-ttu-id="32e49-130">Ein nicht BEHEB barer Fehler tritt beim Absender auf.</span><span class="sxs-lookup"><span data-stu-id="32e49-130">An unrecoverable error occurs on the sender.</span></span>
-   <span data-ttu-id="32e49-131">Auf dem lokalen Computer ist eine übermäßige Ressourcenauslastung aufgetreten, z. b. das Überschreiten des maximal zulässigen internen Pufferspeichers oder das Auftreten einer Bedingung außerhalb der Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="32e49-131">Excessive resource utilization occurs on the local computer, such as exceeding the maximum allowed internal buffer storage, or encountering an out-of-resources condition.</span></span>
-   <span data-ttu-id="32e49-132">Ein Datenkonsistenz Prüfungs Fehler tritt auf.</span><span class="sxs-lookup"><span data-stu-id="32e49-132">A data consistency check error occurs.</span></span>
-   <span data-ttu-id="32e49-133">Fehler in einer Komponente, von der PGM abhängig ist, wie z. b. TCP/IP oder Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="32e49-133">Failure in a component PGM depends on, such as TCP/IP or Windows Sockets.</span></span>

<span data-ttu-id="32e49-134">Sowohl das erste als auch das zweite Element in der obigen Liste können dazu führen, dass der Empfänger eine übermäßige Pufferung durchführt, bevor die Ressourcen nicht mehr ausgeführt werden, oder bevor das Absender Fenster überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="32e49-134">Both the first and second items in the above list could result in the receiver performing excessive buffering before running out of resources, or before ultimately moving beyond the sender's window.</span></span>

## <a name="terminating-a-pgm-session"></a><span data-ttu-id="32e49-135">Beenden einer PGM-Sitzung</span><span class="sxs-lookup"><span data-stu-id="32e49-135">Terminating A PGM Session</span></span>

<span data-ttu-id="32e49-136">Der PGM-Sender oder-Empfänger kann das Senden oder empfangen von Daten durch Aufrufen von [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)abbrechen.</span><span class="sxs-lookup"><span data-stu-id="32e49-136">The PGM sender or receiver can stop sending or receiving data by calling [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).</span></span> <span data-ttu-id="32e49-137">Der Empfänger muss **closesocket** für die Abhör-und empfangenden Sockets aufzurufen, um handle-Verluste zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="32e49-137">The receiver must call **closesocket** on both the listening and receiving sockets to prevent handle leaks.</span></span> <span data-ttu-id="32e49-138">Durch den Aufruf von [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) für den Absender vor dem Aufruf von **closesocket** wird sichergestellt, dass alle Daten gesendet werden, und es wird sichergestellt, dass die Reparatur Daten beibehalten werden, bis das Sendefenster die letzte Datensequenz überschreitet.</span><span class="sxs-lookup"><span data-stu-id="32e49-138">Calling [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) on the sender before calling **closesocket** ensures all data gets sent, and ensures repair data is maintained until the send window advances past the last data sequence, even if the application itself terminates.</span></span>

 

 
