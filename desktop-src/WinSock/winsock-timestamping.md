---
title: Winsock-Zeitstempel
description: Paketzeitstempel sind ein wichtiges Feature für viele Zeitsynchronisierungsanwendungen, z. &mdash; B. Precision Time Protocol. Je näher die Zeitstempelgenerierung an dem Zeitpunkt liegt, an dem ein Paket von der Netzwerkadapterhardware empfangen/gesendet wird, desto genauer kann die Synchronisierungsanwendung sein.
ms.topic: article
ms.date: 10/22/2020
ms.openlocfilehash: 329c13d76fc0c4ce0d87550623e7419af14bfdd268bf359a8f50729e0b0596e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568990"
---
# <a name="winsock-timestamping"></a>Winsock-Zeitstempel

## <a name="introduction"></a>Einführung

Paketzeitstempel sind ein wichtiges Feature für viele Zeitsynchronisierungsanwendungen, z. &mdash; B. Precision Time Protocol. Je näher die Zeitstempelgenerierung an dem Zeitpunkt liegt, an dem ein Paket von der Netzwerkadapterhardware empfangen/gesendet wird, desto genauer kann die Synchronisierungsanwendung sein.

Die in diesem Thema beschriebenen Zeitstempel-APIs bieten Ihrer Anwendung einen Mechanismus zum Melden von Zeitstempeln, die weit unterhalb der Anwendungsschicht generiert werden. Insbesondere ein Softwarezeitstempel an der Schnittstelle zwischen dem Miniport und NDIS und ein Hardwarezeitstempel in der NIC-Hardware. Die Zeitstempel-API kann die Genauigkeit der Uhrsynchronisierung stark verbessern. Derzeit ist die Unterstützung auf UDP-Sockets (User Datagram Protocol) festgelegt.

## <a name="receive-timestamps"></a>Empfangszeitstempel

Sie konfigurieren den Empfangszeitstempelempfang [**über**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) SIO_TIMESTAMPING IOCTL. Verwenden Sie diese IOCTL, um den Empfang des Zeitstempelempfangs zu aktivieren. Wenn Sie ein Datagramm mithilfe der [**funktion LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) erhalten, ist sein Zeitstempel **(sofern verfügbar)** in der SO_TIMESTAMP Steuerelementmeldung enthalten.

**SO_TIMESTAMP** (0x300A) ist in `mstcpip.h` definiert. Die Steuermeldungsdaten werden als **UINT64 zurückgegeben.**

## <a name="transmit-timestamps"></a>Übertragen von Zeitstempeln

Der Empfang des Sendezeitstempels wird auch über [**die**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) SIO_TIMESTAMPING IOCTL konfiguriert. Verwenden Sie diese IOCTL, um den Empfang des Sendezeitstempels zu aktivieren, und geben Sie die Anzahl der Übertragungszeitstempel an, die das System puffert. Wenn Übertragungszeitstempel generiert werden, werden sie dem Puffer hinzugefügt. Wenn der Puffer voll ist, werden neue Übertragungszeitstempel verworfen.

Ordnen Sie beim Senden eines Datagramms das Datagramm einer  SO_TIMESTAMP_ID-Steuermeldung zu. Dieser sollte einen eindeutigen Bezeichner enthalten. Senden Sie das Datagramm zusammen mit **der** SO_TIMESTAMP_ID Mithilfe von [**WSASendMsg.**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) Übertragungszeitstempel sind möglicherweise nicht sofort verfügbar, nachdem **WSASendMsg zurückgegeben** wurde. Wenn Übertragungszeitstempel verfügbar werden, werden sie in einen Puffer pro Socket platziert. Verwenden Sie den [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL, um den Zeitstempel nach seiner ID zu erhalten. Wenn der Zeitstempel verfügbar ist, wird er aus dem Puffer entfernt und zurückgegeben. Wenn der Zeitstempel nicht verfügbar ist, gibt [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) **WSAEWOULDBLOCK zurück.** Wenn ein Übertragungszeitstempel generiert wird, während der Puffer voll ist, wird der neue Zeitstempel verworfen.

**SO_TIMESTAMP_ID** (0x300B) ist in `mstcpip.h` definiert. Sie sollten die Steuermeldungsdaten als **UINT32 -Wert () verwenden.**

Zeitstempel werden als 64-Bit-Indikatorwert dargestellt. Die Häufigkeit des Leistungsindikators hängt von der Quelle des Zeitstempels ab. Bei Softwarezeitstempeln ist der Zähler ein [**QueryPerformanceCounter-Wert**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC), und Sie können seine Häufigkeit über [**QueryPerformanceFrequency bestimmen.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) Bei NIC-Hardwarezeitstempeln hängt die Zählerhäufigkeit von der NIC-Hardware ab, und Sie können sie mit zusätzlichen Informationen ermitteln, die von [**CaptureInterfaceHardwareCrossTimestamp angegeben werden.**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp) Um die Quelle von Zeitstempeln zu bestimmen, verwenden Sie die [**Funktionen GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) und [**GetInterfaceSupportedTimestampCapabilities.**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities)

Zusätzlich zur Konfiguration auf Socketebene mithilfe SIO_TIMESTAMPING Socketoption zum Aktivieren des Zeitstempelempfangs für einen Socket ist auch eine Konfiguration auf Systemebene erforderlich. [](/windows/win32/winsock/winsock-ioctls#sio_timestamping)

## <a name="estimating-latency-of-socket-send-path"></a>Schätzen der Latenz des Socketsendepfads

In diesem Abschnitt verwenden wir Übertragungszeitstempel, um die Latenz des Sockets-Sendepfads zu schätzen. Wenn Sie über eine vorhandene Anwendung verfügen, die E/A-Zeitstempel auf Anwendungsebene verwendet, bei denen der Zeitstempel so nah wie möglich am tatsächlichen Übertragungspunkt sein muss, enthält dieses Beispiel eine quantitative Beschreibung, um wie viel die Winsock-Zeitstempel-APIs die Genauigkeit Ihrer Anwendung verbessern &mdash; &mdash; können.

Im Beispiel wird davon ausgegangen, dass nur eine Netzwerkschnittstellenkarte (NIC) im System enthalten ist und *dass interfaceLuid* die LUID dieses Adapters ist.

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

## <a name="estimating-latency-of-socket-receive-path"></a>Schätzen der Latenz des Socket-Empfangspfads

Hier ist ein ähnliches Beispiel für den Empfangspfad. Im Beispiel wird davon ausgegangen, dass nur eine Netzwerkschnittstellenkarte (NIC) im System enthalten ist und *dass interfaceLuid* die LUID dieses Adapters ist.

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

## <a name="a-limitation"></a>Eine Einschränkung

Eine Einschränkung der Winsock-Zeitstempel-APIs ist, dass das Aufrufen SIO_GET_TX_TIMESTAMP immer ein nicht blockierende Vorgang ist. [](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) Selbst das Aufrufen von IOCTL auf OVERLAPPED-Weise führt zu einer sofortigen Rückgabe von **WSAEWOULDBLOCK,** wenn derzeit keine Übertragungszeitstempel verfügbar sind. Da Übertragungszeitstempel nach der Rückgabe von [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) möglicherweise nicht sofort verfügbar sind, muss Ihre Anwendung die IOCTL-Datei abrufen, bis der Zeitstempel verfügbar ist. Ein Übertragungszeitstempel ist nach einem erfolgreichen **WSASendMsg-Aufruf** garantiert verfügbar, wenn der Übertragungszeitstempelpuffer nicht voll ist.
