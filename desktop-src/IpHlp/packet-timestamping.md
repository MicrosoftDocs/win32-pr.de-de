---
title: Paketzeitstempel
description: Die APIs für IP-Hilfspakete mit Zeitstempeln bieten die Möglichkeit, die Zeitstempelfunktion eines Netzwerkadapters zu bestimmen und Zeitstempel vom Netzwerkadapter in Form von zeitstempelübergreifenden Zeitstempeln abzufragen.
ms.topic: article
ms.date: 01/19/2021
ms.openlocfilehash: 12da7189dbae5f38085cdf4ad5f8e9ac1214cff7ddd0b683ecd97b70b2786c51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146633"
---
# <a name="packet-timestamping"></a>Paketzeitstempel

## <a name="introduction"></a>Einführung

Viele Netzwerkschnittstellenkarten (NICs oder Netzwerkadapter) können einen Zeitstempel auf ihrer Hardware generieren, wenn ein Paket empfangen oder übertragen wird. Der Zeitstempel wird mithilfe der eigenen Hardwareuhr der NIC generiert. Dieses Feature wird insbesondere vom Precision Time Protocol (PTP) verwendet, einem Zeitsynchronisierungsprotokoll. PTP stellt die Verwendung solcher Hardwarezeitstempel innerhalb des Protokolls selbst bereit.

Die Zeitstempel können z. B. verwendet werden, um die Zeit zu berechnen, die ein Paket innerhalb des Netzwerkstapels des Computers aufgewendet hat, bevor es an das Netzwerk gesendet oder von diesem empfangen wird. Diese Berechnungen können dann von PTP verwendet werden, um die Genauigkeit der Zeitsynchronisierung zu verbessern. Die Paketzeitstempelunterstützung von Netzwerkadaptern ist manchmal speziell auf das PTP-Protokoll ausgerichtet. In anderen Fällen wird eine allgemeinere Unterstützung bereitgestellt.

Zeitstempel-APIs bieten Windows die Möglichkeit, die Hardware-Zeitstempelfunktion von Netzwerkadaptern für das PTP Version 2-Protokoll zu unterstützen. Insgesamt umfassen die Features die Bereitstellung der Möglichkeit für Treiber von Netzwerkadaptern zur Unterstützung von Zeitstempeln und für Anwendungen im Benutzermodus die Nutzung von Zeitstempeln, die Paketen über [Windows Sockets](/windows/win32/winsock/windows-sockets-start-page-2) zugeordnet sind (siehe [Winsock-Zeitstempel).](/windows/win32/winsock/winsock-timestamping) Darüber hinaus ist die Möglichkeit zum Generieren von Softwarezeitstempeln verfügbar, wodurch ein Netzwerktreiber Zeitstempel in Software generieren kann. Solche Softwarezeitstempel werden von NIC-Treibern mithilfe der Kernelmodusentsprechung von [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) generiert. Die gleichzeitige Aktivierung von Hardware- *und* Softwarezeitstempeln wird jedoch nicht unterstützt.

Insbesondere bieten die in diesem Thema beschriebenen PAKETzeitstempel-APIs des Internetprotokollhilfs -Pakets die Möglichkeit für Benutzermodusanwendungen, die Zeitstempelfunktion eines Netzwerkadapters zu bestimmen und Zeitstempel vom Netzwerkadapter in Form von Kreuzzeitstempeln abzufragen (siehe unten).

## <a name="supporting-precision-time-protocol-version-2"></a>Unterstützung von Precision Time Protocol, Version 2

Wie bereits erwähnt, besteht das Hauptziel der Zeitstempelunterstützung in Windows darin, das PTPv2-Protokoll (Precision Time Protocol, Version 2) zu unterstützen. In PTPv2 benötigen nicht alle Nachrichten einen Zeitstempel. Insbesondere ptp-Ereignismeldungen verwenden Zeitstempel. Derzeit ist die Unterstützung auf PTPv2 über das User Datagram-Protokoll (User Datagram Protocol, UDP) festgelegt. PTP über Unformatiertes Ethernet wird nicht unterstützt.

Zeitstempel werden für PTPv2 im *2-Schritt-Modus* unterstützt. *2 Schritt* bezieht sich auf den Modus, in dem die tatsächlichen Zeitstempel in den PTP-Paketen nicht im Echtzeitmodus in der Hardware generiert werden, sondern stattdessen von der Hardware abgerufen und als separate Nachrichten übermittelt werden (z. B. mithilfe einer Folgenachricht).

Zusammenfassend lässt sich die Zeitstempel-APIs des Ip-Hilfsdiensts (Internet Protocol Helper) zusammen mit der Zeitstempelunterstützung von Winsock in einer PTPv2-Anwendung verwenden, um die Genauigkeit der Zeitsynchronisierung zu verbessern.

## <a name="retrieving-the-timestamping-capabilities-of-a-network-adapter"></a>Abrufen der Zeitstempelfunktionen eines Netzwerkadapters

Eine Anwendung wie ein PTP-Zeitsynchronisierungsdienst muss die Zeitstempelfunktion eines Netzwerkadapters bestimmen. Mithilfe der abgerufenen Funktionen kann die Anwendung dann entscheiden, ob sie Zeitstempel verwenden möchte.

Auch wenn ein *Netzwerkadapter* Zeitstempel unterstützt, muss die Funktion standardmäßig deaktiviert bleiben. Ein Adapter aktiviert das Zeitstempeln, wenn er dazu aufgefordert wird. Windows stellt APIs für eine Anwendung bereit, um die Hardwarefunktionen abzurufen und welche Funktionen aktiviert sind.

Um die unterstützten Zeitstempelfunktionen eines Netzwerkadapters abzurufen, rufen Sie die [**GetInterfaceSupportedTimestampCapabilities-Funktion**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) auf, stellen den lokal eindeutigen Bezeichner (LUID) des Netzwerkadapters bereit und rufen als Rückgabe die unterstützten Zeitstempelfunktionen in Form eines [**INTERFACE_TIMESTAMP_CAPABILITIES-Objekts**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) ab.

Der von **GetInterfaceSupportedTimestampCapabilities zurückgegebene** Code gibt an, ob der Aufruf erfolgreich war und ob ein aufgefüllter **INTERFACE_TIMESTAMP_CAPABILITIES** Wert abgerufen wurde.

Um die derzeit aktivierten Zeitstempelfunktionen eines Netzwerkadapters abzurufen, rufen Sie die [**GetInterfaceActiveTimestampCapabilities-Funktion**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) auf, stellen den lokal eindeutigen Bezeichner (LUID) des Netzwerkadapters bereit und rufen als Rückgabe die aktivierten Zeitstempelfunktionen in Form eines [**INTERFACE_TIMESTAMP_CAPABILITIES-Objekts**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) ab.

Auch hier gibt der von **GetInterfaceActiveTimestampCapabilities** zurückgegebene Code einen Erfolg oder Fehler an und gibt an, ob ein gültiger **INTERFACE_TIMESTAMP_CAPABILITIES** Wert abgerufen wurde.

Netzwerkadapter können eine Vielzahl von Zeitstempelfunktionen unterstützen. Einige Adapter können beispielsweise beim Senden und Empfangen zeitstempeln, während andere nur PTPv2-Pakete unterstützen. Die [**INTERFACE_TIMESTAMP_CAPABILITIES-Struktur**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) beschreibt die genauen Funktionen, die ein Netzwerkadapter unterstützt.

## <a name="retrieving-cross-timestamps-from-a-network-adapter"></a>Abrufen von Zeitstempeln von einem Netzwerkadapter

Bei Verwendung von Hardwarezeitstempeln muss eine PTP-Anwendung eine Beziehung zwischen der Hardwareuhr des Netzwerkadapters und einer Systemuhr herstellen (z. B. mit geeigneten mathematischen Techniken). Dies ist erforderlich, damit ein Wert, der eine Uhrzeit in der Einheit einer Uhr darstellt, in die Einheit einer anderen Uhr konvertiert werden kann. Zu diesem Zweck werden zeitstempelübergreifende Zeitstempel bereitgestellt, und Ihre Anwendung kann in regelmäßigen Abständen Eine Stichprobe von Zeitstempeln erstellen, um eine solche Beziehung herzustellen.

Rufen Sie hierzu die [**CaptureInterfaceHardwareCrossTimestamp-Funktion**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp) auf, und geben Sie dabei den lokal eindeutigen Bezeichner (LUID) des Netzwerkadapters an, und rufen Sie als Rückgabe den Zeitstempel vom Netzwerkadapter in Form eines [**INTERFACE_HARDWARE_CROSSTIMESTAMP-Objekts**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_hardware_crosstimestamp) ab.

## <a name="timestamp-capability-change-notifications"></a>Änderungsbenachrichtigungen zur Zeitstempelfunktion

Um benachrichtigt zu werden, wenn sich die Zeitstempelfunktionen für einen Netzwerkadapter ändern, rufen Sie die [**RegisterInterfaceTimestampConfigChange-Funktion**](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange) auf und stellen einen Zeiger auf die von Ihnen implementierte Rückruffunktion zusammen mit einem optionalen Kontext bereit, der dem Aufrufer zugeordnet ist.

**RegisterInterfaceTimestampConfigChange** gibt ein Handle zurück, das Sie anschließend an [**UnregisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-unregisterinterfacetimestampconfigchange) übergeben können, um die Registrierung Ihrer Rückruffunktion zu aufheben.

## <a name="code-example-1mdashretrieving-timestamp-capabilities-and-cross-timestamps"></a>Codebeispiel &mdash; 1: Abrufen von Zeitstempelfunktionen und zeitstempelübergreifenden Zeitstempeln

```c
// main.cpp in a Console App project.

#include <stdio.h>
#include <winsock2.h>
#include <iphlpapi.h>
#pragma comment(lib, "Iphlpapi")

BOOL
IsPTPv2HardwareTimestampingSupportedForIPv4(PINTERFACE_TIMESTAMP_CAPABILITIES timestampCapabilities)
{
    // Supported if both receive and transmit side support is present
    if (((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4EventMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4AllMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.AllReceive))
         &&
        ((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4EventMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4AllMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.TaggedTransmit) ||
         (timestampCapabilities->HardwareCapabilities.AllTransmit)))
    {
        return TRUE;
    }

    return FALSE;
}

BOOL
IsPTPv2HardwareTimestampingSupportedForIPv6(PINTERFACE_TIMESTAMP_CAPABILITIES timestampCapabilities)
{
    // Supported if both receive and transmit side support is present
    if (((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6EventMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6AllMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.AllReceive))
         &&
        ((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6EventMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6AllMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.TaggedTransmit) ||
         (timestampCapabilities->HardwareCapabilities.AllTransmit)))
    {
        return TRUE;
    }

    return FALSE;
}

enum SupportedTimestampType
{
    TimestampTypeNone = 0,
    TimestampTypeSoftware = 1,
    TimestampTypeHardware = 2
};

// This function checks and returns the supported timestamp capabilities for an interface for
// a PTPv2 application
SupportedTimestampType
CheckActiveTimestampCapabilitiesForPtpv2(NET_LUID interfaceLuid)
{
    DWORD result = NO_ERROR;
    INTERFACE_TIMESTAMP_CAPABILITIES timestampCapabilities;
    SupportedTimestampType supportedType = TimestampTypeNone;

    result = GetInterfaceActiveTimestampCapabilities(
                 &interfaceLuid,
                 &timestampCapabilities);
    if (result != NO_ERROR)
    {
        printf("Error retrieving hardware timestamp capabilities: %d\n", result);
        goto Exit;
    }

    if (IsPTPv2HardwareTimestampingSupportedForIPv4(&timestampCapabilities) &&
        IsPTPv2HardwareTimestampingSupportedForIPv6(&timestampCapabilities))
    {
        supportedType = TimestampTypeHardware;
        goto Exit;
    }
    else
    {
        if ((timestampCapabilities.SoftwareCapabilities.AllReceive) &&
            ((timestampCapabilities.SoftwareCapabilities.AllTransmit) ||
             (timestampCapabilities.SoftwareCapabilities.TaggedTransmit)))
        {
            supportedType = TimestampTypeSoftware;
        }
    }

Exit:
    return supportedType;
}

// Helper function which does the correlation between hardware and system clock
// using mathematical techniques
void ComputeCorrelationOfHardwareAndSystemTimestamps(INTERFACE_HARDWARE_CROSSTIMESTAMP *crossTimestamp);

// An application would call this function periodically to gather a set 
// of matching timestamps for use in converting hardware timestamps to
// system timestamps
DWORD
RetrieveAndProcessCrossTimestamp(NET_LUID interfaceLuid)
{
    DWORD result = NO_ERROR;
    INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp;

    result = CaptureInterfaceHardwareCrossTimestamp(
                 &interfaceLuid,
                 &crossTimestamp);
    if (result != NO_ERROR)
    {
        printf("Error retrieving cross timestamp for the interface: %d\n", result);
        goto Exit;
    }

    // Process crossTimestamp further to create a relation between the hardware clock
    // of the NIC and the QPC values using appropriate mathematical techniques
    ComputeCorrelationOfHardwareAndSystemTimestamps(&crossTimestamp);

Exit:
    return result;
}

int main()
{
}
```

## <a name="code-example-2mdashregistering-for-timestamp-capability-change-notifications"></a>Codebeispiel &mdash; 2: Registrierung für Zeitstempelfunktionsänderungsbenachrichtigungen

Dieses Beispiel zeigt, wie Ihre Anwendung End-to-End-Zeitstempel verwenden kann.

```c
// main.cpp in a Console App project.

#include <stdlib.h>
#include <stdio.h>
#include <winsock2.h>
#include <mswsock.h>
#include <iphlpapi.h>
#include <mstcpip.h>
#pragma comment(lib, "Ws2_32")
#pragma comment(lib, "Iphlpapi")

// Globals and function declarations used by the application.
// The sample functions and skeletons demonstrate:
// - Checking timestamp configuration for an interface to determine if timestamping can be used
// - If timestamping is enabled, starts tracking changes in timestamp configuration
// - Performing correlation between hardware and system timestamps using cross timestamps
//   on a separate thread depending on the timestamp type configured
// - Receiving a packet and computing the latency between when the timestamp
//   was generated on packet reception, and when the packet was received by
//   the application through the socket
// The sample tries to demonstrate how an application could use timestamps. It is not thread safe 
// and does not do exhaustive error checking.
// Lot of the functions are provided as skeletons, or only declared and invoked
// but are not defined. It is up to
// the application to implement these suitably.

// An application could use the functions below by e.g.
// - Call InitializeTimestampingForInterface for the interface it wants to track for timestamping capability.
// - Call EstimateReceiveLatency to estimate the receive latency of a packet depending on the timestamp 
//   type configured for the interface.

enum SupportedTimestampType
{
    TimestampTypeNone = 0,
    TimestampTypeSoftware = 1,
    TimestampTypeHardware = 2
};

// interfaceBeingTracked is the interface the PTPv2 application
// intends to use for timestamping purpose.
wchar_t* interfaceBeingTracked;

// The active timestamping type determined for
// interfaceBeingTracked.
SupportedTimestampType timestampTypeEnabledForInterface;

HANDLE correlationThread;
HANDLE threadStopEvent;
HIFTIMESTAMPCHANGE TimestampChangeNotificationHandle = NULL;

// Function from sample above to check if an interface supports timestamping for PTPv2.
SupportedTimestampType CheckActiveTimestampCapabilitiesForPtpv2(NET_LUID interfaceLuid);

// Function from sample above to retrieve cross timestamps and process them further.
DWORD RetrieveAndProcessCrossTimestamp(NET_LUID interfaceLuid);

// Helper function which registers for timestamp configuration changes.
DWORD RegisterTimestampChangeNotifications();

// Callback function which is invoked when timestamp configuration changes
// for some network interface.
INTERFACE_TIMESTAMP_CONFIG_CHANGE_CALLBACK TimestampConfigChangeCallback;

// Function which does the correlation between hardware and system clock
// using mathematical techniques. It is periodically invoked and provided
// a sample of cross timestamp to compute a correlation.
void ComputeCorrelationOfHardwareAndSystemTimestamps(INTERFACE_HARDWARE_CROSSTIMESTAMP *crossTimestamp);

// Helper function which converts a hardware timestamp from the NIC clock
// to system timestamp (QPC) values. It is assumed that this works together
// with the ComputeCorrelationOfHardwareAndSystemTimestamps function
// to derive the correlation.
ULONG64 ConvertHardwareTimestampToQpc(ULONG64 HardwareTimestamp);

// Start function of thread which periodically samples
// cross timestamps to correlate hardware and software timestamps.
DWORD WINAPI CorrelateHardwareAndSystemTimestamps(LPVOID);

// Helper function which starts a new thread at CorrelateHardwareAndSystemTimestamps.
DWORD StartCorrelatingHardwareAndSytemTimestamps();

// Helper function which restarts correlation when some change is detected.
DWORD RestartCorrelatingHardwareAndSystemTimestamps();

// Stops the correlation thread.
DWORD StopCorrelatingHardwareAndSystemTimestamps();

DWORD
FindInterfaceFromFriendlyName(wchar_t* friendlyName, NET_LUID* interfaceLuid)
{
    DWORD result = 0;
    ULONG flags = 0;
    ULONG outBufLen = 0;
    PIP_ADAPTER_ADDRESSES pAddresses = NULL;
    PIP_ADAPTER_ADDRESSES currentAddresses = NULL;

    result = GetAdaptersAddresses(0,
        flags,
        NULL,
        pAddresses,
        &outBufLen);
    if (result == ERROR_BUFFER_OVERFLOW)
    {
        pAddresses = (PIP_ADAPTER_ADDRESSES)malloc(outBufLen);

        result = GetAdaptersAddresses(0,
            flags,
            NULL,
            pAddresses,
            &outBufLen);
        if (result != NO_ERROR)
        {
            goto Done;
        }
    }
    else if (result != NO_ERROR)
    {
        goto Done;
    }

    currentAddresses = pAddresses;
    while (currentAddresses != NULL)
    {
        if (wcscmp(friendlyName, currentAddresses->FriendlyName) == 0)
        {
            result = ConvertInterfaceIndexToLuid(currentAddresses->IfIndex, interfaceLuid);
            goto Done;
        }

        currentAddresses = currentAddresses->Next;
    }

    result = ERROR_NOT_FOUND;

Done:

    if (pAddresses != NULL)
    {
        free(pAddresses);
    }

    return result;
}

// This function checks if an interface is suitable for
// timestamping for PTPv2. If so, it registers for timestamp
// configuration changes and initializes some globals.
// If hardware  timestamping is enabled it also starts
// correlation thread.
DWORD
InitializeTimestampingForInterface(wchar_t* friendlyName)
{
    DWORD error;
    SupportedTimestampType supportedType = TimestampTypeNone;

    NET_LUID interfaceLuid;

    error = FindInterfaceFromFriendlyName(friendlyName, &interfaceLuid);
    if (error != 0)
    {
        return error;
    }

    supportedType = CheckActiveTimestampCapabilitiesForPtpv2(interfaceLuid);

    if (supportedType != TimestampTypeNone)
    {
        error = RegisterTimestampChangeNotifications();
        if (error != NO_ERROR)
        {
            return error;
        }

        if (supportedType == TimestampTypeHardware)
        {
            threadStopEvent = CreateEvent(
                NULL,
                FALSE,
                FALSE,
                NULL
            );
            if (threadStopEvent == NULL)
            {
                return GetLastError();
            }            

            error = StartCorrelatingHardwareAndSytemTimestamps();
            if (error != 0)
            {
                return error;
            }
        }

        interfaceBeingTracked = friendlyName;
        timestampTypeEnabledForInterface = supportedType;

        return error;
    }

    return ERROR_NOT_SUPPORTED;
}

DWORD
RegisterTimestampChangeNotifications()
{
    DWORD retcode = NO_ERROR;

    // Register with NULL context
    retcode = RegisterInterfaceTimestampConfigChange(TimestampConfigChangeCallback, NULL, &TimestampChangeNotificationHandle);
    if (retcode != NO_ERROR)
    {
        printf("Error when calling RegisterIfTimestampConfigChange %d\n", retcode);
    }

    return retcode;
}

// The callback invoked when change in some interface’s timestamping configuration
// happens. The callback takes appropriate action based on the new capability of the
// interface. The callback assumes that there is only 1 NIC. If multiple NICs are being
// tracked for timestamping then the application would need to check all of them.
VOID
WINAPI
TimestampConfigChangeCallback(
    _In_ PVOID /*CallerContext*/
    )
{
    SupportedTimestampType supportedType;

    NET_LUID interfaceLuid;
    DWORD error;

    error = FindInterfaceFromFriendlyName(interfaceBeingTracked, &interfaceLuid);
    if (error != NO_ERROR)
    {
        if (timestampTypeEnabledForInterface == TimestampTypeHardware)
        {
            StopCorrelatingHardwareAndSystemTimestamps();
            timestampTypeEnabledForInterface = TimestampTypeNone;
        }
        return;
    }

    supportedType = CheckActiveTimestampCapabilitiesForPtpv2(interfaceLuid);

    if ((supportedType == TimestampTypeHardware) &&
        (timestampTypeEnabledForInterface == TimestampTypeHardware))
    {
        // NIC could have been restarted, restart the correlation between hardware and 
        // system timestamps.
        RestartCorrelatingHardwareAndSystemTimestamps();
    }
    else if (supportedType == TimestampTypeHardware)
    {
        // Start thread correlating hardware and software timestamps
        StartCorrelatingHardwareAndSytemTimestamps();
    }
    else if (supportedType != TimestampTypeHardware)
    {
        // Hardware timestamps are not enabled, stop correlation
        StopCorrelatingHardwareAndSystemTimestamps();
    }

    timestampTypeEnabledForInterface = supportedType;
}

DWORD 
StartCorrelatingHardwareAndSytemTimestamps()
{
    // Create a new thread which starts at CorrelateHardwareAndSoftwareTimestamps
    correlationThread = CreateThread(
        NULL,
        0,
        CorrelateHardwareAndSystemTimestamps,
        NULL,
        0,
        NULL); 

    if (correlationThread == NULL)
    {
        return GetLastError();
    }
}

// Thread which periodically invokes functions to 
// sample cross timestamps and use them to compute
// correlation between hardware and system timestamps.
DWORD WINAPI
CorrelateHardwareAndSystemTimestamps(LPVOID /*lpParameter*/)
{
    DWORD error;
    NET_LUID interfaceLuid;
    DWORD result;

    result = FindInterfaceFromFriendlyName(interfaceBeingTracked, &interfaceLuid);
    if (result != 0)
    {
        return result;
    }

    while (TRUE)
    {
        error = RetrieveAndProcessCrossTimestamp(interfaceLuid);

        // Sleep and repeat till the thread gets a signal to stop
        result = WaitForSingleObject(threadStopEvent, 5000);
        if (result != WAIT_TIMEOUT)
        {
            if (result == WAIT_OBJECT_0)
            {
                return 0;
            }
            else if (result == WAIT_FAILED)            
            {
                return GetLastError();
            }

            return result;
        }
    }
}

DWORD
StopCorrelatingHardwareAndSystemTimestamps()
{
    SetEvent(threadStopEvent);
    return 0;
}

// Function which receives a packet and estimates the latency between the 
// point at which receive timestamp (of appropriate type) was generated
// and when the packet was received in the app through the socket.
// The sample assumes that there is only 1 NIC in the system. This is the NIC which is tracked through
// interfaceBeingTracked for correlation purpose, and through which packets are being
// received by the socket.
// The recvmsg parameter is of type LPFN_WSARECVMSG and an application can
// retrieve it by issuing WSAIoctl
// with SIO_GET_EXTENSION_FUNCTION_POINTER control
// and WSAID_WSARECVMSG. Please refer to msdn.
void EstimateReceiveLatency(SOCKET sock, LPFN_WSARECVMSG recvmsg)
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
    ULONG64 packetReceivedTimestamp;

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
    config.Flags |= TIMESTAMPING_FLAG_RX;
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
    if (error == SOCKET_ERROR)
    {
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
    if (error == SOCKET_ERROR)
    {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return;
    }

    if (timestampTypeEnabledForInterface != TimestampTypeNone)
    {
        // Capture system timestamp (QPC) upon message reception.
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;

        printf("received packet\n");

        // Look for socket rx timestamp returned via control message.
        BOOLEAN retrievedTimestamp = FALSE;
        PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
        while (cmsg != NULL)
        {
            if (cmsg->cmsg_level == SOL_SOCKET && cmsg->cmsg_type == SO_TIMESTAMP)
            {
                socketTimestamp = *(PUINT64)WSA_CMSG_DATA(cmsg);
                retrievedTimestamp = TRUE;
                break;
            }
            cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
        }

        if (retrievedTimestamp)
        {
            // Compute socket receive path latency.
            LARGE_INTEGER clockFrequency;
            ULONG64 elapsedMicroseconds;

            if (timestampTypeEnabledForInterface == TimestampTypeHardware)
            {
                packetReceivedTimestamp = ConvertHardwareTimestampToQpc(socketTimestamp);
            }
            else
            {
                packetReceivedTimestamp = socketTimestamp;
            }
        
            QueryPerformanceFrequency(&clockFrequency);

            // Compute socket receive path latency.
            elapsedMicroseconds = appLevelTimestamp - packetReceivedTimestamp;
            elapsedMicroseconds *= 1000000;
            elapsedMicroseconds /= clockFrequency.QuadPart;
            printf("RX latency estimation: %lld microseconds\n",
                 elapsedMicroseconds);
        }
        else
        {
            printf("failed to retrieve RX timestamp\n");
        }
    }
}

int main()
{
}
```
