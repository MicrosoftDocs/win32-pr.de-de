---
description: Metriken werden verwendet, um Aspekte der Netzwerk-und Protokoll Leistung zu messen.
ms.assetid: ee5faaf6-e230-4084-9829-e8cae8759587
title: Netzwerkterminologie (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04e84621cdaec2638762d54f67e5aca7e3d55ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751417"
---
# <a name="network-terminology-windows-sockets-2"></a><span data-ttu-id="8c3e6-103">Netzwerkterminologie (Windows Sockets 2)</span><span class="sxs-lookup"><span data-stu-id="8c3e6-103">Network Terminology (Windows Sockets 2)</span></span>

<span data-ttu-id="8c3e6-104">Metriken werden verwendet, um Aspekte der Netzwerk-und Protokoll Leistung zu messen.</span><span class="sxs-lookup"><span data-stu-id="8c3e6-104">Metrics are used to measure aspects of network and protocol performance.</span></span> <span data-ttu-id="8c3e6-105">Die Werte für solche Metriken in verschiedenen Szenarien geben die Leistungs Ebene einer Netzwerk Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="8c3e6-105">The values for such metrics in various scenarios indicate the level of performance of a network application.</span></span> <span data-ttu-id="8c3e6-106">In diesem Abschnitt werden Begriffe und Metriken definiert, die branchenweit zum Messen der Leistung von Netzwerkanwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c3e6-106">This section defines terms and metrics used industry-wide for measuring network application performance.</span></span> <span data-ttu-id="8c3e6-107">Diese Begriffe werden im weiteren Verlauf dieses Handbuchs verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c3e6-107">These terms are used throughout the rest of this guide.</span></span>

-   <span data-ttu-id="8c3e6-108">Roundtripzeit (RTT)</span><span class="sxs-lookup"><span data-stu-id="8c3e6-108">Round Trip Time (RTT)</span></span>

    <span data-ttu-id="8c3e6-109">Zeit (in Millisekunden) für eine Anforderung, eine Fahrt von einem Quellcomputer zu einem Zielcomputer durchführen zu können, und wieder zurück.</span><span class="sxs-lookup"><span data-stu-id="8c3e6-109">Time, in milliseconds, for a request to make a trip from a source computer to a destination computer, and back again.</span></span> <span data-ttu-id="8c3e6-110">Niedrigere Werte weisen auf eine bessere Leistung hin.</span><span class="sxs-lookup"><span data-stu-id="8c3e6-110">Lower values indicate better performance.</span></span> <span data-ttu-id="8c3e6-111">Vorwärts-und Rückgabe Pfad Zeiten sind nicht notwendigerweise gleich.</span><span class="sxs-lookup"><span data-stu-id="8c3e6-111">Forward and return path times are not necessarily equal.</span></span>

    <span data-ttu-id="8c3e6-112">RTT-Werte sind von der Netzwerkinfrastruktur, der Entfernung zwischen Knoten, den Netzwerkbedingungen und der Paketgröße betroffen.</span><span class="sxs-lookup"><span data-stu-id="8c3e6-112">RTT values are affected by network infrastructure, distance between nodes, network conditions, and packet size.</span></span> <span data-ttu-id="8c3e6-113">Die Paketgröße, die Überlastung und die Nutzlast der Nutzlast beeinflussen RTT, wenn Sie auf langsamen Verknüpfungen wie DFÜ-Verbindungen gemessen werden.</span><span class="sxs-lookup"><span data-stu-id="8c3e6-113">Packet size, congestion and payload compressibility impact RTT when measured on slow links, such as dial-up connections.</span></span> <span data-ttu-id="8c3e6-114">Andere Faktoren wirken sich auf RTT aus, einschließlich der Forward-Fehlerkorrektur und der Datenkomprimierung, durch die Puffer und Warteschlangen eingeführt werden, die RTT erhöhen</span><span class="sxs-lookup"><span data-stu-id="8c3e6-114">Other factors affect RTT, including forward error correction and data compression, which introduce buffers and queues that increase RTT, and therefore decrease performance.</span></span>

-   <span data-ttu-id="8c3e6-115">Goodput</span><span class="sxs-lookup"><span data-stu-id="8c3e6-115">Goodput</span></span>

    <span data-ttu-id="8c3e6-116">Das Measure der nützlichen Anwendungsdaten, die vom Empfänger erfolgreich verarbeitet wurden (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="8c3e6-116">Measure of useful application data successfully processed by the receiver, in bits-per-second.</span></span> <span data-ttu-id="8c3e6-117">Goodput ermöglicht die Messung des effektiven oder nützlichen Durchsatzes und umfasst nur Anwendungsdaten. Paket-, Protokoll-und Medien Header werden als mehr Aufwand angesehen und sind nicht Teil von goodput.</span><span class="sxs-lookup"><span data-stu-id="8c3e6-117">Goodput enables the measurement of effective or useful throughput and includes only application data; packet, protocol, and media headers are considered overhead, and are not part of goodput.</span></span>

-   <span data-ttu-id="8c3e6-118">Protokoll Aufwand</span><span class="sxs-lookup"><span data-stu-id="8c3e6-118">Protocol Overhead</span></span>

    <span data-ttu-id="8c3e6-119">Nicht Anwendungs bytes, einschließlich Protokoll und Medien Rahmen, dividiert durch die Gesamtzahl der übertragenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="8c3e6-119">Nonapplication bytes, including protocol and media framing, divided by the total number of bytes transmitted.</span></span> <span data-ttu-id="8c3e6-120">Der Wert wird als Prozentsatz ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="8c3e6-120">The value is expressed as a percentage.</span></span> <span data-ttu-id="8c3e6-121">Höhere Werte weisen auf eine schlechtere Leistung hin.</span><span class="sxs-lookup"><span data-stu-id="8c3e6-121">Higher values indicate poorer performance.</span></span>

    <span data-ttu-id="8c3e6-122">Der Aufwand wird in diesem Handbuch für beide Richtungen berechnet, kann jedoch für jede Richtung separat berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="8c3e6-122">Overhead is calculated for both directions in this guide, but can be calculated for each direction separately.</span></span>

-   <span data-ttu-id="8c3e6-123">Bandwidth-Delay Produkt</span><span class="sxs-lookup"><span data-stu-id="8c3e6-123">Bandwidth-Delay Product</span></span>

    <span data-ttu-id="8c3e6-124">Produkt der Bits-pro-Sekunde-Bandbreite des Netzwerks und RTT (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="8c3e6-124">Product of the bits-per-second bandwidth of the network, and the RTT (in seconds).</span></span> <span data-ttu-id="8c3e6-125">Dieser Wert entspricht der Anzahl von Bits, die benötigt wird, um die verfügbare Netzwerkbandbreite auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="8c3e6-125">This value equates to the number of bits it takes to fill available network bandwidth.</span></span> <span data-ttu-id="8c3e6-126">Wenn der Wert für das Produkt "Bandbreiten Verzögerung" hoch ist, muss der TCP/IP-Stapel große Mengen nicht bestätigter Daten verarbeiten, um die Pipeline vollständig zu halten.</span><span class="sxs-lookup"><span data-stu-id="8c3e6-126">When the value for bandwidth-delay product is high, the TCP/IP stack must handle large amounts of unacknowledged data in order to keep the pipeline full.</span></span> <span data-ttu-id="8c3e6-127">Das Produkt für die Bandbreiten Verzögerung ist eine zentrale End-to-End-Metrik für Streaminganwendungen.</span><span class="sxs-lookup"><span data-stu-id="8c3e6-127">Bandwidth-delay product is a key end-to-end metric for streaming applications.</span></span>

 

 



