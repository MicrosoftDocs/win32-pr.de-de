---
title: Paketzeitstempel
description: Die IP-Hilfspaketzeitstempel-APIs bieten die Möglichkeit, die Zeitstempelfunktion eines Netzwerkadapters zu bestimmen und Zeitstempel vom Netzwerkadapter in Form von Zeitstempeln abfragt.
ms.topic: article
ms.date: 01/19/2021
ms.openlocfilehash: 07743473bcb606ccdb86c55f14a3413adf10d73a
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110559983"
---
# <a name="packet-timestamping"></a><span data-ttu-id="ff91f-103">Paketzeitstempel</span><span class="sxs-lookup"><span data-stu-id="ff91f-103">Packet timestamping</span></span>

## <a name="introduction"></a><span data-ttu-id="ff91f-104">Einführung</span><span class="sxs-lookup"><span data-stu-id="ff91f-104">Introduction</span></span>

<span data-ttu-id="ff91f-105">Viele Netzwerkschnittstellenkarten (NICs oder Netzwerkadapter) können bei jedem Empfangen oder Übertragen eines Pakets einen Zeitstempel in ihrer Hardware generieren.</span><span class="sxs-lookup"><span data-stu-id="ff91f-105">Many network interface cards (NICs, or network adapters) can generate a timestamp in their hardware whenever a packet is received or transmitted.</span></span> <span data-ttu-id="ff91f-106">Der Zeitstempel wird mithilfe der eigenen Hardwareuhr der NIC generiert.</span><span class="sxs-lookup"><span data-stu-id="ff91f-106">The timestamp is generated using the NIC's own hardware clock.</span></span> <span data-ttu-id="ff91f-107">Dieses Feature wird insbesondere vom Precision Time Protocol (PTP) verwendet, bei dem es sich um ein Zeitsynchronisierungsprotokoll handelt.</span><span class="sxs-lookup"><span data-stu-id="ff91f-107">This feature is used in particular by the Precision Time Protocol (PTP), which is a time synchronization protocol.</span></span> <span data-ttu-id="ff91f-108">PTP stellt die Verwendung solcher Hardwarezeitstempel innerhalb des Protokolls selbst zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ff91f-108">PTP makes provision to use such hardware timestamps within the protocol itself.</span></span>

<span data-ttu-id="ff91f-109">Die Zeitstempel können beispielsweise verwendet werden, um die Zeit zu berechnen, die von einem Paket im Netzwerkstapel des Computers verbracht wird, bevor es an das Netzwerk gesendet oder vom Netzwerk empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="ff91f-109">The timestamps can, for example, be used to compute the time spent by a packet within the network stack of the machine before being sent to or received from the wire.</span></span> <span data-ttu-id="ff91f-110">Diese Berechnungen können dann von PTP verwendet werden, um die Genauigkeit der Zeitsynchronisierung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="ff91f-110">Those calculations can then be used by PTP to improve the accuracy of time synchronization.</span></span> <span data-ttu-id="ff91f-111">Die Unterstützung des Paketzeitstempels von Netzwerkadaptern ist manchmal speziell auf das PTP-Protokoll ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="ff91f-111">The packet timestamping support of network adapters is geared sometimes specifically for the PTP protocol.</span></span> <span data-ttu-id="ff91f-112">In anderen Fällen wird eine allgemeinere Unterstützung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ff91f-112">In other cases, a more general support is provided.</span></span>

<span data-ttu-id="ff91f-113">Zeitstempel-APIs bieten Windows die Möglichkeit, die Hardwarezeitstempelfunktion von Netzwerkadaptern für das PTP-Protokoll version 2 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ff91f-113">Timestamping APIs give Windows the ability to support the hardware timestamping capability of network adapters for the PTP version 2 protocol.</span></span> <span data-ttu-id="ff91f-114">Insgesamt umfassen die Features die Bereitstellung der Möglichkeit für Treiber von Netzwerkadaptern, Zeitstempel zu unterstützen, und für Benutzermodusanwendungen die Nutzung von Zeitstempeln, die Paketen über [Windows Sockets](/windows/win32/winsock/windows-sockets-start-page-2) zugeordnet sind (siehe Winsock-Zeitstempel). [](/windows/win32/winsock/winsock-timestamping)</span><span class="sxs-lookup"><span data-stu-id="ff91f-114">Overall, the features include providing the ability to drivers of network adapters to support timestamps, and for user-mode applications to consume timestamps associated with packets through [Windows Sockets](/windows/win32/winsock/windows-sockets-start-page-2) (see [Winsock timestamping](/windows/win32/winsock/winsock-timestamping)).</span></span> <span data-ttu-id="ff91f-115">Darüber hinaus ist auch die Möglichkeit verfügbar, Softwarezeitstempel zu generieren, die es einem Netzwerktreiber ermöglichen, Zeitstempel in Software zu generieren.</span><span class="sxs-lookup"><span data-stu-id="ff91f-115">In addition, the ability to generate software timestamps is also available, which allows a network driver to generate timestamps in software.</span></span> <span data-ttu-id="ff91f-116">Solche Softwarezeitstempel werden von NIC-Treibern mithilfe der Kernelmodusentsprechung von [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) generiert.</span><span class="sxs-lookup"><span data-stu-id="ff91f-116">Such software timestamps are generated by NIC drivers using the kernel-mode equivalent of [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC).</span></span> <span data-ttu-id="ff91f-117">Die gemeinsame Aktivierung von *Hardware-* und Softwarezeitstempeln wird jedoch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ff91f-117">However, having both hardware *and* software timestamps enabled together isn't supported.</span></span>

<span data-ttu-id="ff91f-118">Insbesondere bieten die in diesem Thema beschriebenen PAKETzeitstempel-APIs des Internetprotokollhilfs -Pakets die Möglichkeit für Benutzermodusanwendungen, die Zeitstempelfunktion eines Netzwerkadapters zu bestimmen und Zeitstempel vom Netzwerkadapter in Form von Kreuzzeitstempeln abzufragen (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="ff91f-118">In particular, the Internet Protocol Helper (IP Helper) packet timestamping APIs described in this topic provide the ability for user-mode applications to determine the timestamping capability of a network adapter, and to query timestamps from the network adapter in the form of cross timestamps (described below).</span></span>

## <a name="supporting-precision-time-protocol-version-2"></a><span data-ttu-id="ff91f-119">Unterstützung von Precision Time Protocol, Version 2</span><span class="sxs-lookup"><span data-stu-id="ff91f-119">Supporting Precision Time Protocol version 2</span></span>

<span data-ttu-id="ff91f-120">Wie bereits erwähnt, besteht das Hauptziel der Unterstützung von Zeitstempeln in Windows darin, das PTPv2-Protokoll (Precision Time Protocol, Version 2) zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ff91f-120">As mentioned, the main goal of timestamping support in Windows is to support the Precision Time Protocol version 2 (PTPv2) protocol.</span></span> <span data-ttu-id="ff91f-121">In PTPv2 benötigen nicht alle Nachrichten einen Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="ff91f-121">Within PTPv2, not all messages need a timestamp.</span></span> <span data-ttu-id="ff91f-122">Ptp-Ereignismeldungen verwenden insbesondere Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="ff91f-122">In particular, PTP event messages do use timestamps.</span></span> <span data-ttu-id="ff91f-123">Derzeit ist die Unterstützung auf PTPv2 über das User Datagram-Protokoll (User Datagram Protocol, UDP) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ff91f-123">Currently, support is scoped to PTPv2 over User Datagram Protocol (UDP).</span></span> <span data-ttu-id="ff91f-124">PTP über Unformatiertes Ethernet wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ff91f-124">PTP over raw ethernet isn't supported.</span></span>

<span data-ttu-id="ff91f-125">Zeitstempel werden für PTPv2 im *2-Schritt-Modus* unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ff91f-125">Timestamping is supported for PTPv2 operating in *2 step* mode.</span></span> <span data-ttu-id="ff91f-126">*2 Schritt* bezieht sich auf den Modus, in dem die tatsächlichen Zeitstempel in den PTP-Paketen nicht während der Übertragung in der Hardware generiert werden, sondern stattdessen von der Hardware abgerufen und als separate Nachrichten übermittelt werden (z. B. mithilfe einer Folgemeldung).</span><span class="sxs-lookup"><span data-stu-id="ff91f-126">*2 step* refers to the mode in which the actual timestamps in the PTP packets aren't generated on the fly in the hardware, but are instead retrieved from the hardware and conveyed as separate messages (for example, using a follow-up message).</span></span>

<span data-ttu-id="ff91f-127">Zusammenfassend lässt sich die Zeitstempel-APIs des Ip-Hilfsdiensts (Internet Protocol Helper) zusammen mit der Zeitstempelunterstützung von Winsock in einer PTPv2-Anwendung verwenden, um die Genauigkeit der Zeitsynchronisierung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="ff91f-127">In summary, you can use the Internet Protocol Helper (IP Helper) packet timestamping APIs, together with Winsock's timestamping support, in a PTPv2 application to improve its time synchronization accuracy.</span></span>

## <a name="retrieving-the-timestamping-capabilities-of-a-network-adapter"></a><span data-ttu-id="ff91f-128">Abrufen der Zeitstempelfunktionen eines Netzwerkadapters</span><span class="sxs-lookup"><span data-stu-id="ff91f-128">Retrieving the timestamping capabilities of a network adapter</span></span>

<span data-ttu-id="ff91f-129">Eine Anwendung wie ein PTP-Zeitsynchronisierungsdienst muss die Zeitstempelfunktion eines Netzwerkadapters bestimmen.</span><span class="sxs-lookup"><span data-stu-id="ff91f-129">An application such as a PTP time synchronization service needs to determine the timestamping capability of a network adapter.</span></span> <span data-ttu-id="ff91f-130">Mithilfe der abgerufenen Funktionen kann die Anwendung dann entscheiden, ob sie Zeitstempel verwenden möchte.</span><span class="sxs-lookup"><span data-stu-id="ff91f-130">Using the retrieved capabilities, the application can then decide whether or not it wants to use timestamps.</span></span>

<span data-ttu-id="ff91f-131">Auch wenn ein *Netzwerkadapter* Zeitstempel unterstützt, muss die Funktion standardmäßig deaktiviert bleiben.</span><span class="sxs-lookup"><span data-stu-id="ff91f-131">Even if a network adapter *does* support timestamps, it's required to keep the ability turned off by default.</span></span> <span data-ttu-id="ff91f-132">Ein Adapter aktiviert das Zeitstempeln, wenn er dazu aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="ff91f-132">An adapter turns on timestamping when instructed to do so.</span></span> <span data-ttu-id="ff91f-133">Windows stellt APIs für eine Anwendung bereit, um die Funktionalität der Hardware abzurufen und welche Funktionen aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="ff91f-133">Windows provides APIs for an application to retrieve the hardware's capability, as well as which capabilities are turned on.</span></span>

<span data-ttu-id="ff91f-134">Um die unterstützten Zeitstempelfunktionen eines Netzwerkadapters abzurufen, rufen Sie die [**GetInterfaceSupportedTimestampCapabilities-Funktion**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) auf, geben den lokal eindeutigen Bezeichner (LUID) des Netzwerkadapters an und rufen im Gegenzug die unterstützten Zeitstempelfunktionen in Form eines [**INTERFACE_TIMESTAMP_CAPABILITIES-Objekts ab.**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities)</span><span class="sxs-lookup"><span data-stu-id="ff91f-134">To retrieve the supported timestamp capabilities of a network adapter, you call the [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) function, providing the locally unique identifier (LUID) of the network adapter, and in return retrieving the supported timestamping capabilities in the form of an [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) object.</span></span>

<span data-ttu-id="ff91f-135">Der von **GetInterfaceSupportedTimestampCapabilities** zurückgegebene Code gibt an, ob der Aufruf  erfolgreich war und ob ein aufgefüllter INTERFACE_TIMESTAMP_CAPABILITIES abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ff91f-135">The code returned from **GetInterfaceSupportedTimestampCapabilities** indicates whether or not the call succeeded, and whether or not a populated **INTERFACE_TIMESTAMP_CAPABILITIES** value was retrieved.</span></span>

<span data-ttu-id="ff91f-136">Um die derzeit aktivierten Zeitstempelfunktionen eines Netzwerkadapters abzurufen, rufen Sie die [**GetInterfaceActiveTimestampCapabilities-Funktion**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) auf, geben den lokal eindeutigen Bezeichner (LUID) des Netzwerkadapters an und rufen im Gegenzug die aktivierten Zeitstempelfunktionen in Form eines [**INTERFACE_TIMESTAMP_CAPABILITIES-Objekts**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) ab.</span><span class="sxs-lookup"><span data-stu-id="ff91f-136">To retrieve the currently enabled timestamp capabilities of a network adapter, you call the [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) function, providing the locally unique identifier (LUID) of the network adapter, and in return retrieving the enabled timestamping capabilities in the form of an [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) object.</span></span>

<span data-ttu-id="ff91f-137">Auch hier gibt der von **GetInterfaceActiveTimestampCapabilities** zurückgegebene Code einen  Erfolg oder Fehler an und gibt an, ob ein gültiger INTERFACE_TIMESTAMP_CAPABILITIES abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ff91f-137">Again, the code returned from **GetInterfaceActiveTimestampCapabilities** indicates success or failure, and whether or not a valid **INTERFACE_TIMESTAMP_CAPABILITIES** value was retrieved.</span></span>

<span data-ttu-id="ff91f-138">Netzwerkadapter können eine Vielzahl von Zeitstempelfunktionen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ff91f-138">Network adapters can support a variety of timestamping capabilities.</span></span> <span data-ttu-id="ff91f-139">Beispielsweise können einige Adapter jedes Paket beim Senden und Empfangen mit einem Zeitstempel versehen, während andere nur PTPv2-Pakete unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ff91f-139">For example, some adapters can timestamp every packet during send and receive, while others support only PTPv2 packets.</span></span> <span data-ttu-id="ff91f-140">Die [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) beschreibt die genauen Funktionen, die ein Netzwerkadapter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ff91f-140">The [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) structure describes the exact capabilities that a network adapter supports.</span></span>

## <a name="retrieving-cross-timestamps-from-a-network-adapter"></a><span data-ttu-id="ff91f-141">Abrufen von Zeitstempeln von einem Netzwerkadapter</span><span class="sxs-lookup"><span data-stu-id="ff91f-141">Retrieving cross timestamps from a network adapter</span></span>

<span data-ttu-id="ff91f-142">Bei Verwendung von Hardwarezeitstempeln muss eine PTP-Anwendung eine Beziehung zwischen der Hardwareuhr des Netzwerkadapters und einer Systemuhr herstellen (z. B. mithilfe geeigneter mathematischer Techniken).</span><span class="sxs-lookup"><span data-stu-id="ff91f-142">When using hardware timestamps, a PTP application needs to establish a relation (for example, by using appropriate mathematical techniques) between the hardware clock of the network adapter and a system clock.</span></span> <span data-ttu-id="ff91f-143">Dies ist erforderlich, damit ein Wert, der eine Uhrzeit in der Einheit einer Uhr darstellt, in eine Einheit einer anderen Uhr konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ff91f-143">This is necessary so that a value representing a time in one clock's unit can be converted into another clock's unit.</span></span> <span data-ttu-id="ff91f-144">Für diesen Zweck werden Zeitstempel bereitgestellt, und Ihre Anwendung kann regelmäßig Zeitstempelstichproben erstellen, um eine solche Beziehung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ff91f-144">Cross timestamps are provided for this purpose, and your application can sample cross timestamps periodically in order to establish such a relation.</span></span>

<span data-ttu-id="ff91f-145">Rufen Sie hierzu die [**CaptureInterfaceHardwareCrossTimestamp-Funktion**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp) auf, geben Sie den lokal eindeutigen Bezeichner (LUID) des Netzwerkadapters an, und rufen Sie als Rückgabe den Zeitstempel vom Netzwerkadapter in Form eines [**INTERFACE_HARDWARE_CROSSTIMESTAMP-Objekts**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_hardware_crosstimestamp) ab.</span><span class="sxs-lookup"><span data-stu-id="ff91f-145">To do that, call the [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp) function, providing the locally unique identifier (LUID) of the network adapter, and in return retrieving the timestamp from the network adapter in the form of an [**INTERFACE_HARDWARE_CROSSTIMESTAMP**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_hardware_crosstimestamp) object.</span></span>

## <a name="timestamp-capability-change-notifications"></a><span data-ttu-id="ff91f-146">Änderungsbenachrichtigungen zur Zeitstempelfunktion</span><span class="sxs-lookup"><span data-stu-id="ff91f-146">Timestamp capability change notifications</span></span>

<span data-ttu-id="ff91f-147">Um benachrichtigt zu werden, wenn sich die Zeitstempelfunktionen für einen Netzwerkadapter ändern, rufen Sie die [**RegisterInterfaceTimestampConfigChange-Funktion**](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange) auf und stellen einen Zeiger auf die von Ihnen implementierte Rückruffunktion zusammen mit einem optionalen Kontext bereit, der dem Aufrufer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ff91f-147">To be notified should the timestamp capabilities for a network adapter change, call the [**RegisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange) function, providing a pointer to the callback function that you've implemented, together with an optional caller-allocated context.</span></span>

<span data-ttu-id="ff91f-148">**RegisterInterfaceTimestampConfigChange** gibt ein Handle zurück, das Sie anschließend an [**UnregisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-unregisterinterfacetimestampconfigchange) übergeben können, um die Registrierung Ihrer Rückruffunktion zu aufheben.</span><span class="sxs-lookup"><span data-stu-id="ff91f-148">**RegisterInterfaceTimestampConfigChange** returns a handle that you can subsequently pass to [**UnregisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-unregisterinterfacetimestampconfigchange) in order to unregister your callback function.</span></span>

## <a name="code-example-1mdashretrieving-timestamp-capabilities-and-cross-timestamps"></a><span data-ttu-id="ff91f-149">Codebeispiel &mdash; 1: Abrufen von Zeitstempelfunktionen und zeitstempelübergreifenden Zeitstempeln</span><span class="sxs-lookup"><span data-stu-id="ff91f-149">Code example 1&mdash;retrieving timestamp capabilities and cross timestamps</span></span>

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

## <a name="code-example-2mdashregistering-for-timestamp-capability-change-notifications"></a><span data-ttu-id="ff91f-150">Codebeispiel &mdash; 2: Registrierung für Änderungsbenachrichtigungen für Zeitstempelfunktionen</span><span class="sxs-lookup"><span data-stu-id="ff91f-150">Code example 2&mdash;registering for timestamp capability change notifications</span></span>

<span data-ttu-id="ff91f-151">Dieses Beispiel zeigt, wie Ihre Anwendung End-to-End-Zeitstempel verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="ff91f-151">This example shows how your application could use timestamps end to end.</span></span>

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
