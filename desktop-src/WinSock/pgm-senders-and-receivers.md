---
description: Das Einrichten einer PGM-Sitzung ähnelt der Verbindung, die mit einer TCP-Sitzung verknüpft ist.
ms.assetid: 777e0106-0314-4ec8-b064-88ceb694614b
title: PGM-Absender und-Empfänger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e300a0c9de199e1f836e71407caf6487812cf7b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526120"
---
# <a name="pgm-senders-and-receivers"></a><span data-ttu-id="13231-103">PGM-Absender und-Empfänger</span><span class="sxs-lookup"><span data-stu-id="13231-103">PGM Senders and Receivers</span></span>

<span data-ttu-id="13231-104">Das Einrichten einer PGM-Sitzung ähnelt der Verbindung, die mit einer TCP-Sitzung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="13231-104">Establishing a PGM session is similar to the connection establishment routine associated with a TCP session.</span></span> <span data-ttu-id="13231-105">Der bedeutende Abbruch von einer TCP-Sitzung ist jedoch, dass die Client-und Server Semantik umgekehrt ist. der Server (der PGM-Sender) stellt eine Verbindung mit einer Multicast Gruppe her, während der Client (der PGM-Empfänger) darauf wartet, eine Verbindung zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="13231-105">The significant departure from a TCP session, however, is that the client and server semantics are reversed; the server (the PGM sender) connects to a multicast group, while the client (the PGM receiver) waits to accept a connection.</span></span> <span data-ttu-id="13231-106">In den folgenden Abschnitten werden die programmgesteuerten Schritte erläutert, die zum Erstellen eines PGM-Senders und eines PGM-Empfängers erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="13231-106">The following paragraphs detail programmatic steps necessary for creating a PGM sender and a PGM receiver.</span></span> <span data-ttu-id="13231-107">Auf dieser Seite werden auch die verfügbaren Daten Modi für PGM-Sitzungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="13231-107">This page also describes the available data modes for PGM sessions.</span></span>

## <a name="pgm-sender"></a><span data-ttu-id="13231-108">PGM-Absender</span><span class="sxs-lookup"><span data-stu-id="13231-108">PGM Sender</span></span>

<span data-ttu-id="13231-109">**Führen Sie die folgenden Schritte aus, um einen PGM-Sender zu erstellen:**</span><span class="sxs-lookup"><span data-stu-id="13231-109">**To create a PGM sender, perform the following steps**</span></span>

1.  <span data-ttu-id="13231-110">Erstellen Sie einen PGM-Socket.</span><span class="sxs-lookup"><span data-stu-id="13231-110">Create a PGM socket.</span></span>
2.  <span data-ttu-id="13231-111">[**binden**](/windows/desktop/api/winsock/nf-winsock-bind) Sie den Socket an inaddr \_ any.</span><span class="sxs-lookup"><span data-stu-id="13231-111">[**bind**](/windows/desktop/api/winsock/nf-winsock-bind) the socket to INADDR\_ANY.</span></span>
3.  <span data-ttu-id="13231-112">Stellen Sie eine [**Verbindung**](/windows/desktop/api/Winsock2/nf-winsock2-connect) mit der Multicast Gruppen-Übertragungs Adresse her.</span><span class="sxs-lookup"><span data-stu-id="13231-112">[**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) to the multicast group transmission address.</span></span>

<span data-ttu-id="13231-113">Es werden keine formellen Sitzungs Handler für Clients ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="13231-113">No formal session handshaking is performed with any clients.</span></span> <span data-ttu-id="13231-114">Der Verbindungsprozess ähnelt einer UDP- [**Verbindung**](/windows/desktop/api/Winsock2/nf-winsock2-connect), da er eine Endpunkt Adresse (die Multicast Gruppe) dem Socket zuordnet.</span><span class="sxs-lookup"><span data-stu-id="13231-114">The connection process is similar to a UDP [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), in that it associates an endpoint address (the multicast group) with the socket.</span></span> <span data-ttu-id="13231-115">Nach Abschluss des Vorgangs können Daten auf dem Socket gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="13231-115">Once completed, data may be sent on the socket.</span></span>

<span data-ttu-id="13231-116">Wenn ein Absender einen PGM-Socket erstellt und ihn mit einer Multicast Adresse verbindet, wird eine PGM-Sitzung erstellt.</span><span class="sxs-lookup"><span data-stu-id="13231-116">When a sender creates a PGM socket and connects it to a multicast address, a PGM session is created.</span></span> <span data-ttu-id="13231-117">Eine zuverlässige Multicast Sitzung wird durch eine Kombination aus dem Globally Unique Identifier (GUID) und dem Quellport definiert.</span><span class="sxs-lookup"><span data-stu-id="13231-117">A reliable multicast session is defined by a combination of the globally unique identifier (GUID) and the source port.</span></span> <span data-ttu-id="13231-118">Die GUID wird vom Transport generiert.</span><span class="sxs-lookup"><span data-stu-id="13231-118">The GUID is generated by the transport.</span></span> <span data-ttu-id="13231-119">Der sSource-Port wird vom Transport festgelegt, und es wird kein Steuerelement bereitgestellt, über den der Quellport verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="13231-119">The sSource port is specified by the transport, and no control is provided over which source port is used.</span></span>

> [!Note]  
> <span data-ttu-id="13231-120">Das Empfangen von Daten auf einem Absender Socket ist nicht zulässig und führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="13231-120">Receiving data on a sender socket is not allowed, and results in an error.</span></span>

 

<span data-ttu-id="13231-121">Der folgende Code Ausschnitt veranschaulicht das Einrichten eines PGM-Senders:</span><span class="sxs-lookup"><span data-stu-id="13231-121">The following code snippet illustrates setting up a PGM sender:</span></span>


```C++

SOCKET        s;
SOCKADDR_IN   salocal, sasession;
int           dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

salocal.sin_family = AF_INET;
salocal.sin_port   = htons (0);    // Port is ignored here
salocal.sin_addr.s_addr = htonl (INADDR_ANY);

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant sender socket options here
//

//
// Now, connect <entity type="hellip"/>
// Setting the connection port (dwSessionPort) has relevance, and
// can be used to multiplex multiple sessions to the same
// multicast group address over different ports
//
dwSessionPort = 0;
sasession.sin_family = AF_INET;
sasession.sin_port   = htons (dwSessionPort);
sasession.sin_addr.s_addr = inet_addr ("234.5.6.7");

connect (s, (SOCKADDR *)&sasession, sizeof(sasession));

//
// We're now ready to send data!
//



```



## <a name="pgm-receiver"></a><span data-ttu-id="13231-122">PGM-Empfänger</span><span class="sxs-lookup"><span data-stu-id="13231-122">PGM Receiver</span></span>

<span data-ttu-id="13231-123">**Führen Sie die folgenden Schritte aus, um einen PGM-Empfänger zu erstellen.**</span><span class="sxs-lookup"><span data-stu-id="13231-123">**To create a PGM receiver, perform the following steps**</span></span>

1.  <span data-ttu-id="13231-124">Erstellen Sie einen PGM-Socket.</span><span class="sxs-lookup"><span data-stu-id="13231-124">Create a PGM socket.</span></span>
2.  <span data-ttu-id="13231-125">[**binden**](/windows/desktop/api/winsock/nf-winsock-bind) Sie den Socket an die Multicast Gruppen Adresse, über die der Absender überträgt.</span><span class="sxs-lookup"><span data-stu-id="13231-125">[**bind**](/windows/desktop/api/winsock/nf-winsock-bind) the socket to the multicast group address on which the sender is transmitting.</span></span>
3.  <span data-ttu-id="13231-126">Ruft die Funktion " [**lauschen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) " im Socket auf, um den Socket in den Empfangsmodus zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="13231-126">Call the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function on the socket to put the socket in listening mode.</span></span> <span data-ttu-id="13231-127">Die Funktion "lauschen" gibt zurück, wenn eine PGM-Sitzung für die angegebene Multicast Gruppen Adresse und den Port erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="13231-127">The listen function returns when a PGM session is detected on the specified multicast group address and port.</span></span>
4.  <span data-ttu-id="13231-128">Rufen Sie die [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) -Funktion auf, um ein neues Sockethandle zu erhalten, das der Sitzung entspricht.</span><span class="sxs-lookup"><span data-stu-id="13231-128">Call the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) function to obtain a new socket handle corresponding to the session.</span></span>

<span data-ttu-id="13231-129">Nur ursprüngliche PGM-Daten (odata) lösen die Annahme einer neuen Sitzung aus.</span><span class="sxs-lookup"><span data-stu-id="13231-129">Only original PGM data (ODATA) triggers the acceptance of a new session.</span></span> <span data-ttu-id="13231-130">Daher kann ein anderer PGM-Datenverkehr (z. b. SPM-oder rdata-Pakete) vom Transport empfangen werden, dies führt jedoch nicht dazu, dass die Funktion " [**lauschen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) " zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="13231-130">As such, other PGM traffic (such as SPM or RDATA packets) may be received by the transport, but do not result in the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function returning.</span></span>

<span data-ttu-id="13231-131">Nachdem eine Sitzung akzeptiert wurde, wird das zurückgegebene Sockethandle zum Empfangen von Daten verwendet.</span><span class="sxs-lookup"><span data-stu-id="13231-131">Once a session is accepted, the returned socket handle is used for receiving data.</span></span>

> [!Note]  
> <span data-ttu-id="13231-132">Das Senden von Daten in einem Empfangs Socket ist nicht zulässig und führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="13231-132">Sending data on a receive socket is not allowed, and results in an error.</span></span>

 

<span data-ttu-id="13231-133">Der folgende Code Ausschnitt veranschaulicht das Einrichten eines PGM-Empfängers:</span><span class="sxs-lookup"><span data-stu-id="13231-133">The following code snippet illustrates setting up a PGM receiver:</span></span>


```C++

SOCKET        s,
              sclient;
SOCKADDR_IN   salocal,
              sasession;
int           sasessionsz, dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

//
// The bind port (dwSessionPort) specified should match that
// which the sender specified in the connect call
//
dwSessionPort = 0;
salocal.sin_family = AF_INET;
salocal.sin_port   = htons (dwSessionPort);    
salocal.sin_addr.s_addr = inet_addr ("234.5.6.7");

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant receiver socket options here
//

listen (s, 10);

sasessionsz = sizeof(sasession);
sclient = accept (s, (SOCKADDR *)&sasession, &sasessionsz);

//
// accept will return the client socket and we are now ready
// to receive data on the new socket!
//



```



## <a name="data-modes"></a><span data-ttu-id="13231-134">Daten Modi</span><span class="sxs-lookup"><span data-stu-id="13231-134">Data Modes</span></span>

<span data-ttu-id="13231-135">PGM-Sitzungen verfügen über zwei Optionen für Daten Modi: Nachrichten Modus und Streammodus.</span><span class="sxs-lookup"><span data-stu-id="13231-135">PGM sessions have two options for data modes: message mode and stream mode.</span></span>

<span data-ttu-id="13231-136">Der Nachrichten Modus ist für Anwendungen geeignet, die diskrete Nachrichten senden müssen, und wird durch den Sockettyp Sock \_ RDM angegeben.</span><span class="sxs-lookup"><span data-stu-id="13231-136">Message mode is appropriate for applications that need to send discrete messages, and is specified by a socket type of SOCK\_RDM.</span></span> <span data-ttu-id="13231-137">Der Streammodus eignet sich für Anwendungen, die Streamingdaten an Empfänger (z. b. Video-oder Sprachanwendungen) senden müssen, und die durch einen Sockettyp von Sock Stream angegeben werden \_ .</span><span class="sxs-lookup"><span data-stu-id="13231-137">Stream mode is appropriate for applications that need to send streaming data to receivers, such as video or voice applications, and is specified by a socket type of SOCK\_STREAM.</span></span> <span data-ttu-id="13231-138">Die Auswahl des Modus hat Auswirkungen auf die Verarbeitung von Daten durch Winsock.</span><span class="sxs-lookup"><span data-stu-id="13231-138">The choice of mode effects how Winsock processes data.</span></span>

<span data-ttu-id="13231-139">Sehen Sie sich das folgende Beispiel an: ein PGM-Absender im Nachrichten Modus führt drei Aufrufe an die [**wsasend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) -Funktion mit jeweils einem 100-Byte-Puffer aus.</span><span class="sxs-lookup"><span data-stu-id="13231-139">Consider the following example: A message mode PGM sender makes three calls to the [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) function, each with a 100-byte buffer.</span></span> <span data-ttu-id="13231-140">Dieser Vorgang wird im Netzwerk als drei diskrete PGM-Pakete angezeigt.</span><span class="sxs-lookup"><span data-stu-id="13231-140">This operation appears on the wire as three discrete PGM packets.</span></span> <span data-ttu-id="13231-141">Auf der Empfängerseite gibt jeder Aufrufe der [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) -Funktion nur 100 Bytes zurück, auch wenn ein größerer Empfangs Puffer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="13231-141">On the receiver side, each call to the [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) function returns only 100 bytes, even if a larger receive buffer is provided.</span></span> <span data-ttu-id="13231-142">Im Gegensatz dazu können bei einem PGM-Absender im Streammodus diese 3 100-Byte-Übertragungen in weniger als drei physische Pakete übertragen werden (oder in ein BLOB von Daten auf der Empfängerseite zusammen geschrieben werden).</span><span class="sxs-lookup"><span data-stu-id="13231-142">In contrast, with a stream mode PGM sender those three 100 byte transmissions could be coalesced into less than three physical packets on the wire (or coalesced into one blob of data on the receiver side).</span></span> <span data-ttu-id="13231-143">Wenn der Empfänger z. b. eine der Windows Sockets-Empfangsfunktionen aufruft, kann jede Menge von Daten, die vom PGM-Transport empfangen wurde, an die Anwendung zurückgegeben werden, ohne dass dabei berücksichtigt wird, wie die Daten physisch übertragen oder empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="13231-143">As such, when the receiver calls one of the Windows Sockets receive functions, any amount of data that has been received by the PGM transport may be returned to the application without regard to how the data was physically transmitted or received.</span></span>

 

 



