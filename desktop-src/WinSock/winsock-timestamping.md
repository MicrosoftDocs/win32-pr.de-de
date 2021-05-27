---
title: Winsock-Zeitstempel
description: Paketzeitstempel sind ein wichtiges Feature für viele Zeitsynchronisierungsanwendungen, z. &mdash; B. Precision Time Protocol. Je näher die Zeitstempelgenerierung an dem Zeitpunkt liegt, an dem ein Paket von der Netzwerkadapterhardware empfangen/gesendet wird, desto genauer kann die Synchronisierungsanwendung sein.
ms.topic: article
ms.date: 10/22/2020
ms.openlocfilehash: eae0dce8c2c16bc187ef5522f323e7f36d7fc0b4
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110559957"
---
# <a name="winsock-timestamping"></a><span data-ttu-id="f22ff-104">Winsock-Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="f22ff-104">Winsock timestamping</span></span>

## <a name="introduction"></a><span data-ttu-id="f22ff-105">Einführung</span><span class="sxs-lookup"><span data-stu-id="f22ff-105">Introduction</span></span>

<span data-ttu-id="f22ff-106">Paketzeitstempel sind ein wichtiges Feature für viele Zeitsynchronisierungsanwendungen, z. &mdash; B. Precision Time Protocol.</span><span class="sxs-lookup"><span data-stu-id="f22ff-106">Packet timestamps are a crucial feature to many clock synchronization applications&mdash;for example, Precision Time Protocol.</span></span> <span data-ttu-id="f22ff-107">Je näher die Zeitstempelgenerierung an dem Zeitpunkt liegt, an dem ein Paket von der Netzwerkadapterhardware empfangen/gesendet wird, desto genauer kann die Synchronisierungsanwendung sein.</span><span class="sxs-lookup"><span data-stu-id="f22ff-107">The closer the timestamp generation is to when a packet is received/sent by the network adapter hardware, the more accurate the synchronization application can be.</span></span>

<span data-ttu-id="f22ff-108">Die in diesem Thema beschriebenen Zeitstempel-APIs bieten Ihrer Anwendung einen Mechanismus zum Melden von Zeitstempeln, die weit unterhalb der Anwendungsschicht generiert werden.</span><span class="sxs-lookup"><span data-stu-id="f22ff-108">So the timestamping APIs described in this topic provide your application with a mechanism to report timestamps that are generated well below the application layer.</span></span> <span data-ttu-id="f22ff-109">Insbesondere ein Softwarezeitstempel an der Schnittstelle zwischen dem Miniport und NDIS und ein Hardwarezeitstempel in der NIC-Hardware.</span><span class="sxs-lookup"><span data-stu-id="f22ff-109">Specifically, a software timestamp at the interface between the miniport and NDIS, and a hardware timestamp in the NIC hardware.</span></span> <span data-ttu-id="f22ff-110">Die Zeitstempel-API kann die Genauigkeit der Uhrsynchronisierung stark verbessern.</span><span class="sxs-lookup"><span data-stu-id="f22ff-110">The timestamping API can greatly improve clock synchronization accuracy.</span></span> <span data-ttu-id="f22ff-111">Derzeit ist die Unterstützung auf UDP-Sockets (User Datagram Protocol) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f22ff-111">Currently, support is scoped to User Datagram Protocol (UDP) sockets.</span></span>

## <a name="receive-timestamps"></a><span data-ttu-id="f22ff-112">Empfangszeitstempel</span><span class="sxs-lookup"><span data-stu-id="f22ff-112">Receive timestamps</span></span>

<span data-ttu-id="f22ff-113">Sie konfigurieren den Empfangszeitstempelempfang über [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span><span class="sxs-lookup"><span data-stu-id="f22ff-113">You configure receive timestamp reception through the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span></span> <span data-ttu-id="f22ff-114">Verwenden Sie diese IOCTL, um den Empfang des Zeitstempelempfangs zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f22ff-114">Use that IOCTL to enable receive timestamp reception.</span></span> <span data-ttu-id="f22ff-115">Wenn Sie ein Datagramm mithilfe der [**LPFN_WSARECVMSG-Funktion (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) erhalten, ist sein  Zeitstempel (sofern verfügbar) in der SO_TIMESTAMP steuerbar.</span><span class="sxs-lookup"><span data-stu-id="f22ff-115">When you receive a datagram using the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function, its timestamp (if available) is contained in the **SO_TIMESTAMP** control message.</span></span>

<span data-ttu-id="f22ff-116">**SO_TIMESTAMP** (0x300A) ist in `mstcpip.h` definiert.</span><span class="sxs-lookup"><span data-stu-id="f22ff-116">**SO_TIMESTAMP** (0x300A) is defined in `mstcpip.h`.</span></span> <span data-ttu-id="f22ff-117">Die Steuermeldungsdaten werden als **UINT64 zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="f22ff-117">The control message data is returned as a **UINT64**.</span></span>

## <a name="transmit-timestamps"></a><span data-ttu-id="f22ff-118">Übertragen von Zeitstempeln</span><span class="sxs-lookup"><span data-stu-id="f22ff-118">Transmit timestamps</span></span>

<span data-ttu-id="f22ff-119">Der Empfang des Sendezeitstempels wird auch über [**die**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) SIO_TIMESTAMPING IOCTL konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="f22ff-119">Transmit timestamp reception is also configured through the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span></span> <span data-ttu-id="f22ff-120">Verwenden Sie diese IOCTL, um den Empfang des Sendezeitstempels zu aktivieren, und geben Sie die Anzahl der Übertragungszeitstempel an, die das System puffert.</span><span class="sxs-lookup"><span data-stu-id="f22ff-120">Use that IOCTL to enable transmit timestamp reception, and specify the number of transmit timestamps that the system will buffer.</span></span> <span data-ttu-id="f22ff-121">Wenn Übertragungszeitstempel generiert werden, werden sie dem Puffer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f22ff-121">As transmit timestamps are generated, they are added to the buffer.</span></span> <span data-ttu-id="f22ff-122">Wenn der Puffer voll ist, werden neue Übertragungszeitstempel verworfen.</span><span class="sxs-lookup"><span data-stu-id="f22ff-122">If the buffer is full, new transmit timestamps are discarded.</span></span>

<span data-ttu-id="f22ff-123">Ordnen Sie beim Senden eines Datagramms das Datagramm einer  SO_TIMESTAMP_ID-Steuermeldung zu.</span><span class="sxs-lookup"><span data-stu-id="f22ff-123">When sending a datagram, associate the datagram with an **SO_TIMESTAMP_ID** control message.</span></span> <span data-ttu-id="f22ff-124">Dieser sollte einen eindeutigen Bezeichner enthalten.</span><span class="sxs-lookup"><span data-stu-id="f22ff-124">This should contain a unique identifier.</span></span> <span data-ttu-id="f22ff-125">Senden Sie das Datagramm zusammen mit der **SO_TIMESTAMP_ID** Mithilfe von [**WSASendMsg.**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg)</span><span class="sxs-lookup"><span data-stu-id="f22ff-125">Send the datagram, along with its **SO_TIMESTAMP_ID** control message, using [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg).</span></span> <span data-ttu-id="f22ff-126">Übertragungszeitstempel sind nach der Rückgabe von **WSASendMsg möglicherweise nicht sofort** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f22ff-126">Transmit timestamps might not be immediately available after **WSASendMsg** returns.</span></span> <span data-ttu-id="f22ff-127">Wenn Übertragungszeitstempel verfügbar werden, werden sie in einen Puffer pro Socket platziert.</span><span class="sxs-lookup"><span data-stu-id="f22ff-127">As transmit timestamps become available, they are placed into a per-socket buffer.</span></span> <span data-ttu-id="f22ff-128">Verwenden Sie den [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL, um den Zeitstempel nach seiner ID zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f22ff-128">Use the [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL to poll for the timestamp by its ID.</span></span> <span data-ttu-id="f22ff-129">Wenn der Zeitstempel verfügbar ist, wird er aus dem Puffer entfernt und zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f22ff-129">If the timestamp is available, then it is removed from the buffer and returned.</span></span> <span data-ttu-id="f22ff-130">Wenn der Zeitstempel nicht verfügbar ist, gibt [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) **WSAEWOULDBLOCK zurück.**</span><span class="sxs-lookup"><span data-stu-id="f22ff-130">If the timestamp is not available, then [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) returns **WSAEWOULDBLOCK**.</span></span> <span data-ttu-id="f22ff-131">Wenn ein Übertragungszeitstempel generiert wird, während der Puffer voll ist, wird der neue Zeitstempel verworfen.</span><span class="sxs-lookup"><span data-stu-id="f22ff-131">If a transmit timestamp is generated while the buffer is full, the new timestamp is discarded.</span></span>

<span data-ttu-id="f22ff-132">**SO_TIMESTAMP_ID** (0x300B) ist in `mstcpip.h` definiert.</span><span class="sxs-lookup"><span data-stu-id="f22ff-132">**SO_TIMESTAMP_ID** (0x300B) is defined in `mstcpip.h`.</span></span> <span data-ttu-id="f22ff-133">Sie sollten die Steuermeldungsdaten als **UINT32 -Wert () verwenden.**</span><span class="sxs-lookup"><span data-stu-id="f22ff-133">You should supply the control message data as a **UINT32**.</span></span>

<span data-ttu-id="f22ff-134">Zeitstempel werden als 64-Bit-Indikatorwert dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f22ff-134">Timestamps are represented as a 64-bit counter value.</span></span> <span data-ttu-id="f22ff-135">Die Häufigkeit des Leistungsindikators hängt von der Quelle des Zeitstempels ab.</span><span class="sxs-lookup"><span data-stu-id="f22ff-135">The frequency of the counter depends on the source of the timestamp.</span></span> <span data-ttu-id="f22ff-136">Bei Softwarezeitstempeln ist der Zähler ein [**QueryPerformanceCounter-Wert**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC), und Sie können seine Häufigkeit über [**QueryPerformanceFrequency bestimmen.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)</span><span class="sxs-lookup"><span data-stu-id="f22ff-136">For software timestamps, the counter is a [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) value, and you can determine its frequency via [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).</span></span> <span data-ttu-id="f22ff-137">Bei NIC-Hardwarezeitstempeln hängt die Zählerhäufigkeit von der NIC-Hardware ab, und Sie können sie mit zusätzlichen Informationen ermitteln, die von [**CaptureInterfaceHardwareCrossTimestamp angegeben werden.**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp)</span><span class="sxs-lookup"><span data-stu-id="f22ff-137">For NIC hardware timestamps, the counter frequency is dependent on the NIC hardware, and you can determine it with additional information given by [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp).</span></span> <span data-ttu-id="f22ff-138">Um die Quelle von Zeitstempeln zu bestimmen, verwenden Sie die [**Funktionen GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) und [**GetInterfaceSupportedTimestampCapabilities.**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities)</span><span class="sxs-lookup"><span data-stu-id="f22ff-138">To determine the source of timestamps, use the [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) and [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) functions.</span></span>

<span data-ttu-id="f22ff-139">Zusätzlich zur Konfiguration auf Socketebene mithilfe SIO_TIMESTAMPING Socketoption zum Aktivieren des Zeitstempelempfangs für einen Socket ist auch eine Konfiguration auf Systemebene erforderlich. [](/windows/win32/winsock/winsock-ioctls#sio_timestamping)</span><span class="sxs-lookup"><span data-stu-id="f22ff-139">In addition to socket-level configuration using the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) socket option to enable timestamp reception for a socket, system-level configuration is also needed.</span></span>

## <a name="estimating-latency-of-socket-send-path"></a><span data-ttu-id="f22ff-140">Schätzen der Latenz des Socketsendepfads</span><span class="sxs-lookup"><span data-stu-id="f22ff-140">Estimating latency of socket send path</span></span>

<span data-ttu-id="f22ff-141">In diesem Abschnitt verwenden wir Übertragungszeitstempel, um die Latenz des Sockets-Sendepfads zu schätzen.</span><span class="sxs-lookup"><span data-stu-id="f22ff-141">In this section, we'll use transmit timestamps to estimate the latency of the socket send path.</span></span> <span data-ttu-id="f22ff-142">Wenn Sie über eine vorhandene Anwendung verfügen, die E/A-Zeitstempel auf Anwendungsebene &mdash; nutzt, wobei der Zeitstempel so nah wie möglich am tatsächlichen Übertragungspunkt liegen &mdash; muss, enthält dieses Beispiel eine quantitative Beschreibung, wie viel die Winsock-Zeitstempel-APIs die Genauigkeit Ihrer Anwendung verbessern können.</span><span class="sxs-lookup"><span data-stu-id="f22ff-142">If you have an existing application that consumes application-level IO timestamps&mdash;where the timestamp needs to be as close as possible to the actual point of transmission&mdash;then this sample provides a quantitative description as to how much the Winsock timestamping APIs can improve the accuracy of your application.</span></span>

<span data-ttu-id="f22ff-143">Im Beispiel wird davon ausgegangen, dass nur eine Netzwerkschnittstellenkarte (Network Interface Card, NIC) im System vorhanden ist, und dass *interfaceLuid* die LUID dieses Adapters ist.</span><span class="sxs-lookup"><span data-stu-id="f22ff-143">The example assumes that there's only one network interface card (NIC) in the system, and that *interfaceLuid* is the LUID of that adapter.</span></span>

```c
void QueryHardwareClockFrequency(LARGE_INTEGER* clockFrequency)
{
    // Returns the hardware clock frequency. This can be calculated by
    // collecting crosstimestamps via CaptureInterfaceHardwareCrossTimestamp
    // and forming a linear regression model.
}

void estimate_send_latency(SOCKET sock,
    PSOCKADDR_STORAGE addr,
    NET_LUID* interfaceLuid,
    BOOLEAN hardwareTimestampSource)
{
    DWORD numBytes;
    INT error;
    CHAR data[512];
    CHAR control[WSA_CMSG_SPACE(sizeof(UINT32))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    ULONG64 appLevelTimestamp;

    dataBuf.buf = data;
    dataBuf.len = sizeof(data);
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)addr;
    wsaMsg.namelen = (INT)INET_SOCKADDR_LENGTH(addr->ss_family);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    // Configure tx timestamp reception.
    TIMESTAMPING_CONFIG config = { 0 };
    config.flags |= TIMESTAMPING_FLAG_TX;
    config.txTimestampsBuffered = 1;
    error =
        WSAIoctl(
            sock,
            SIO_TIMESTAMPING,
            &config,
            sizeof(config),
            NULL,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("WSAIoctl failed %d\n", WSAGetLastError());
        return;
    }

    // Assign a tx timestamp ID to this datagram.
    UINT32 txTimestampId = 123;
    PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    cmsg->cmsg_len = WSA_CMSG_LEN(sizeof(UINT32));
    cmsg->cmsg_level = SOL_SOCKET;
    cmsg->cmsg_type = SO_TIMESTAMP_ID;
    *(PUINT32)WSA_CMSG_DATA(cmsg) = txTimestampId;

    // Capture app-layer timestamp prior to send call.
    if (hardwareTimestampSource) {
        INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp = { 0 };
        crossTimestamp.Version = INTERFACE_HARDWARE_CROSSTIMESTAMP_VERSION_1;
        error = CaptureInterfaceHardwareCrossTimestamp(interfaceLuid, &crossTimestamp);
        if (error != NO_ERROR) {
            printf("CaptureInterfaceHardwareCrossTimestamp failed %d\n", error);
            return;
        }
        appLevelTimestamp = crossTimestamp.HardwareClockTimestamp;
    }
    else { // software source
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;
    }

    error =
        sendmsg(
            sock,
            &wsaMsg,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("sendmsg failed %d\n", WSAGetLastError());
        return;
    }

    printf("sent packet\n");

    // Poll for the socket tx timestamp value. The timestamp may not be available
    // immediately.
    UINT64 socketTimestamp;
    ULONG maxTimestampPollAttempts = 6;
    ULONG txTstampRetrieveIntervalMs = 1;
    BOOLEAN retrievedTimestamp = FALSE;
    for (ULONG i = 0; i < maxTimestampPollAttempts; i++) {
        error =
            WSAIoctl(
                sock,
                SIO_GET_TX_TIMESTAMP,
                &txTimestampId,
                sizeof(txTimestampId),
                &socketTimestamp,
                sizeof(socketTimestamp),
                &numBytes,
                NULL,
                NULL);
        if (error != SOCKET_ERROR) {
            ASSERT(numBytes == sizeof(timestamp));
            ASSERT(timestamp != 0);
            retrievedTimestamp = TRUE;
            break;
        }

        error = WSAGetLastError();
        if (error != WSAEWOULDBLOCK) {
            printf(“WSAIoctl failed % d\n”, error);
            break;
        }

        Sleep(txTstampRetrieveIntervalMs);
        txTstampRetrieveIntervalMs *= 2;
    }

    if (retrievedTimestamp) {
        LARGE_INTEGER clockFrequency;
        ULONG64 elapsedMicroseconds;

        if (hardwareTimestampSource) {
            QueryHardwareClockFrequency(&clockFrequency);
        }
        else { // software source
            QueryPerformanceFrequency(&clockFrequency);
        }

        // Compute socket send path latency.
        elapsedMicroseconds = socketTimestamp - appLevelTimestamp;
        elapsedMicroseconds *= 1000000;
        elapsedMicroseconds /= clockFrequency.QuadPart;
        printf("socket send path latency estimation: %lld microseconds\n",
            elapsedMicroseconds);
    }
    else {
        printf("failed to retrieve TX timestamp\n");
    }
}
```

## <a name="estimating-latency-of-socket-receive-path"></a><span data-ttu-id="f22ff-144">Schätzen der Latenz des Socket-Empfangspfads</span><span class="sxs-lookup"><span data-stu-id="f22ff-144">Estimating latency of socket receive path</span></span>

<span data-ttu-id="f22ff-145">Hier ist ein ähnliches Beispiel für den Empfangspfad.</span><span class="sxs-lookup"><span data-stu-id="f22ff-145">Here's a similar sample for the receive path.</span></span> <span data-ttu-id="f22ff-146">Im Beispiel wird davon ausgegangen, dass nur eine Netzwerkschnittstellenkarte (Network Interface Card, NIC) im System vorhanden ist, und dass *interfaceLuid* die LUID dieses Adapters ist.</span><span class="sxs-lookup"><span data-stu-id="f22ff-146">The example assumes that there's only one network interface card (NIC) in the system, and that *interfaceLuid* is the LUID of that adapter.</span></span>

```c
void QueryHardwareClockFrequency(LARGE_INTEGER* clockFrequency)
{
    // Returns the hardware clock frequency. This can be calculated by
    // collecting crosstimestamps via CaptureInterfaceHardwareCrossTimestamp
    // and forming a linear regression model.
}

void estimate_receive_latency(SOCKET sock,
    NET_LUID* interfaceLuid,
    BOOLEAN hardwareTimestampSource)
{
    DWORD numBytes;
    INT error;
    CHAR data[512];
    CHAR control[WSA_CMSG_SPACE(sizeof(UINT64))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    UINT64 socketTimestamp = 0;
    ULONG64 appLevelTimestamp;

    dataBuf.buf = data;
    dataBuf.len = sizeof(data);
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = NULL;
    wsaMsg.namelen = 0;
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    // Configure rx timestamp reception.
    TIMESTAMPING_CONFIG config = { 0 };
    config.flags |= TIMESTAMPING_FLAG_RX;
    error =
        WSAIoctl(
            sock,
            SIO_TIMESTAMPING,
            &config,
            sizeof(config),
            NULL,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("WSAIoctl failed %d\n", WSAGetLastError());
        return;
    }

    error =
        recvmsg(
            sock,
            &wsaMsg,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return;
    }

    // Capture app-layer timestamp upon message reception.
    if (hardwareTimestampSource) {
        INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp = { 0 };
        crossTimestamp.Version = INTERFACE_HARDWARE_CROSSTIMESTAMP_VERSION_1;
        error = CaptureInterfaceHardwareCrossTimestamp(interfaceLuid, &crossTimestamp);
        if (error != NO_ERROR) {
            printf("CaptureInterfaceHardwareCrossTimestamp failed %d\n", error);
            return;
        }
        appLevelTimestamp = crossTimestamp.HardwareClockTimestamp;
    }
    else { // software source
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;
    }

    printf("received packet\n");

    // Look for socket rx timestamp returned via control message.
    BOOLEAN retrievedTimestamp = FALSE;
    PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    while (cmsg != NULL) {
        if (cmsg->cmsg_level == SOL_SOCKET && cmsg->cmsg_type == SO_TIMESTAMP) {
            socketTimestamp = *(PUINT64)WSA_CMSG_DATA(cmsg);
            retrievedTimestamp = TRUE;
            break;
        }
        cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
    }

    if (retrievedTimestamp) {
        // Compute socket receive path latency.
        LARGE_INTEGER clockFrequency;
        ULONG64 elapsedMicroseconds;

        if (hardwareTimestampSource) {
            QueryHardwareClockFrequency(&clockFrequency);
        }
        else { // software source
            QueryPerformanceFrequency(&clockFrequency);
        }

        // Compute socket send path latency.
        elapsedMicroseconds = appLevelTimestamp - socketTimestamp;
        elapsedMicroseconds *= 1000000;
        elapsedMicroseconds /= clockFrequency.QuadPart;
        printf("RX latency estimation: %lld microseconds\n",
            elapsedMicroseconds);
    }
    else {
        printf("failed to retrieve RX timestamp\n");
    }
}
```

## <a name="a-limitation"></a><span data-ttu-id="f22ff-147">Eine Einschränkung</span><span class="sxs-lookup"><span data-stu-id="f22ff-147">A limitation</span></span>

<span data-ttu-id="f22ff-148">Eine Einschränkung der Winsock-Zeitstempel-APIs besteht darin, dass das Aufrufen [**von SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) immer ein nicht blockierender Vorgang ist.</span><span class="sxs-lookup"><span data-stu-id="f22ff-148">One limitation of the Winsock timestamping APIs is that calling [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) is always a non-blocking operation.</span></span> <span data-ttu-id="f22ff-149">Selbst das Aufrufen von IOCTL auf überlappende Weise führt zu einer sofortigen Rückgabe von **WSAEWULEDBLOCK,** wenn derzeit keine Übertragungszeitstempel verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f22ff-149">Even calling the IOCTL in an OVERLAPPED fashion results in an immediate return of **WSAEWOULDBLOCK** if there are currently no available transmit timestamps.</span></span> <span data-ttu-id="f22ff-150">Da Übertragungszeitstempel nach der Rückgabe von [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) möglicherweise nicht sofort verfügbar sind, muss Ihre Anwendung die IOCTL abfragen, bis der Zeitstempel verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f22ff-150">Since transmit timestamps might not be immediately available after [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) returns, your application must poll the IOCTL until the timestamp is available.</span></span> <span data-ttu-id="f22ff-151">Ein Übertragungszeitstempel ist nach einem **erfolgreichen WSASendMsg-Aufruf** garantiert verfügbar, da der Zeitstempelpuffer für die Übertragung nicht voll ist.</span><span class="sxs-lookup"><span data-stu-id="f22ff-151">A transmit timestamp is guaranteed to be available after a successful **WSASendMsg** call given that the transmit timestamp buffer is not full.</span></span>
