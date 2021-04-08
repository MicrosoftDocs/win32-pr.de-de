---
description: TCP/IP verfügt über Eigenschaften, mit denen das Protokoll gemäß den Anforderungen der standardisierten Implementierung funktionieren kann.
ms.assetid: 6e9b3878-85f0-4572-9c00-a2e7647286ff
title: TCP/IP-Merkmale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561ab497d6f37c1c84b0203088b29e216ff0a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865960"
---
# <a name="tcpip-characteristics"></a><span data-ttu-id="56533-103">TCP/IP-Merkmale</span><span class="sxs-lookup"><span data-stu-id="56533-103">TCP/IP Characteristics</span></span>

<span data-ttu-id="56533-104">TCP/IP verfügt über Eigenschaften, mit denen das Protokoll gemäß den Anforderungen der standardisierten Implementierung funktionieren kann.</span><span class="sxs-lookup"><span data-stu-id="56533-104">TCP/IP has characteristics that enable the protocol to operate as its standardized implementation requirements dictate.</span></span> <span data-ttu-id="56533-105">Diese Merkmale können mit Entwicklungsoptionen kombiniert werden, die zu einer schlechten Leistung führen.</span><span class="sxs-lookup"><span data-stu-id="56533-105">These characteristics can combine with development choices that result in poor performance.</span></span> <span data-ttu-id="56533-106">Welche Auswirkung diese TCP/IP-Merkmale auf eine Anwendung haben, hängt davon ab, ob die Anwendung transaktional oder Streaming ist.</span><span class="sxs-lookup"><span data-stu-id="56533-106">The impact these TCP/IP characteristics have on an application depend on whether the application is transactional or streaming.</span></span>

<span data-ttu-id="56533-107">Transaktionale Anwendungen sind von dem Aufwand betroffen, der zum Einrichten und Beenden der Verbindung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="56533-107">Transactional applications are affected by the overhead required for connection establishment and termination.</span></span> <span data-ttu-id="56533-108">Wenn z. b. eine Verbindung in einem Ethernet-Netzwerk hergestellt wird, müssen jeweils drei Pakete mit ungefähr 60 Byte gesendet werden, und für den Austausch ist ungefähr eine RTT erforderlich.</span><span class="sxs-lookup"><span data-stu-id="56533-108">For example, each time a connection is established on an Ethernet network, three packets of approximately 60 bytes each must be sent, and approximately one RTT is required for the exchange.</span></span> <span data-ttu-id="56533-109">Wenn eine Verbindung beendet wird, werden vier Pakete ausgetauscht.</span><span class="sxs-lookup"><span data-stu-id="56533-109">When termination of a connection occurs, four packets are exchanged.</span></span> <span data-ttu-id="56533-110">Dies gilt für jede Verbindung. eine Anwendung, die Verbindungen öffnet und schließt, verursacht häufig den Aufwand für jedes Vorkommen.</span><span class="sxs-lookup"><span data-stu-id="56533-110">This is for each connection; an application that opens and closes connections often incurs this overhead on each occurrence.</span></span>

<span data-ttu-id="56533-111">Ein anderer Aspekt von TCP/IP ist ein *langsamer Start*, der immer dann stattfindet, wenn eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="56533-111">Another aspect of TCP/IP is *slow-start*, which takes place whenever a connection is established.</span></span> <span data-ttu-id="56533-112">Der langsame Start ist ein künstlicher Grenzwert für die Anzahl der Daten Segmente, die gesendet werden können, bevor die Bestätigung dieser Segmente empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="56533-112">Slow-start is an artificial limit on the number of data segments that can be sent before acknowledgment of those segments is received.</span></span> <span data-ttu-id="56533-113">Der langsame Start ist so konzipiert, dass die Überlastung des Netzwerks eingeschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="56533-113">Slow-start is designed to limit network congestion.</span></span> <span data-ttu-id="56533-114">Wenn eine Verbindung über Ethernet hergestellt wird, kann unabhängig von der Fenstergröße des Empfängers eine Übertragung von 4 KB bis zu 3-4 RTT dauern, da langsam begonnen wird.</span><span class="sxs-lookup"><span data-stu-id="56533-114">When a connection over Ethernet is established, regardless of the receiver's window size, a 4 KB transmission can take up to 3-4 RTT due to slow-start.</span></span>

<span data-ttu-id="56533-115">Eine TCP/IP-Optimierung, die als Nagle-Algorithmus bezeichnet wird, kann auch die Datenübertragungsgeschwindigkeit bei einer Verbindung einschränken.</span><span class="sxs-lookup"><span data-stu-id="56533-115">A TCP/IP optimization called the Nagle Algorithm can also limit data transfer speed on a connection.</span></span> <span data-ttu-id="56533-116">Der Nagle-Algorithmus ist so konzipiert, dass der Protokoll Mehraufwand für Anwendungen reduziert wird, die kleine Datenmengen senden, wie z. b. Telnet, die jeweils jeweils ein einzelnes Zeichen senden.</span><span class="sxs-lookup"><span data-stu-id="56533-116">The Nagle Algorithm is designed to reduce protocol overhead for applications that send small amounts of data, such as Telnet, which sends a single character at a time.</span></span> <span data-ttu-id="56533-117">Anstatt direkt ein Paket mit vielen Header-und kleinen Daten zu senden, wartet der Stapel auf weitere Daten von der Anwendung oder einer Bestätigung, bevor der Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="56533-117">Rather than immediately send a packet with lots of header and little data, the stack waits for more data from the application, or an acknowledgment, before proceeding.</span></span>

<span data-ttu-id="56533-118">Verzögerte Bestätigungen, die häufig als *verzögerte* Bestätigung bezeichnet werden, werden auch in TCP/IP integriert, um eine effizientere piggyunterstützung von Bestätigungen zu ermöglichen, wenn Rückgabe Daten von der empfangenden Anwendung empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="56533-118">Delayed acknowledgments, commonly referred to as *delayed ACK*, are also designed into TCP/IP to enable more efficient piggybacking of acknowledgments when return data is forthcoming from the receiving side application.</span></span> <span data-ttu-id="56533-119">Wenn diese Daten nicht in Kürze vorhanden sind und die Sendeseite auf eine Bestätigung wartet, können Verzögerungen von ungefähr 200 Millisekunden pro Sendevorgang auftreten.</span><span class="sxs-lookup"><span data-stu-id="56533-119">Unfortunately, if this data is not forthcoming and the sending side is waiting for an acknowledgment, delays of approximately 200 milliseconds per send can occur.</span></span>

<span data-ttu-id="56533-120">Wenn eine TCP-Verbindung geschlossen wird, werden Verbindungs Ressourcen an dem Knoten, der die Schließung initiiert hat, in einen Wartezustand versetzt, der als Zeit Wartezeit bezeichnet wird, um Schutz vor Daten Beschädigungen zu erhalten, wenn doppelte Pakete im Netzwerk gelinger werden.</span><span class="sxs-lookup"><span data-stu-id="56533-120">When a TCP connection is closed, connection resources at the node that initiated the close are put into a wait state, called TIME-WAIT, to guard against data corruption if duplicate packets linger in the network.</span></span> <span data-ttu-id="56533-121">Dadurch wird sichergestellt, dass beide Enden mit der Verbindung abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="56533-121">This ensures both ends are finished with the connection.</span></span> <span data-ttu-id="56533-122">Dies kann zu einem Mangel an Ressourcen, die pro Verbindung erforderlich sind, führen, z. b. RAM und Ports, wenn Anwendungen häufig Verbindungen öffnen und schließen.</span><span class="sxs-lookup"><span data-stu-id="56533-122">This can cause depletion of resources required per-connection, such as RAM and ports, when applications open and close connections frequently.</span></span>

<span data-ttu-id="56533-123">Neben der Auswirkung von verzögertem ACK und anderen Überlastungs Vermeidungs Schemas können Streaminganwendungen auch durch eine zu geringe standardmäßige Empfangs Fenstergröße auf dem empfangenden Ende beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="56533-123">Besides being affected by delayed ACK and other congestion avoidance schemes, streaming applications can also be affected by a too-small default receive window size on the receiving end.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56533-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56533-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56533-125">Anwendungsverhalten</span><span class="sxs-lookup"><span data-stu-id="56533-125">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="56533-126">Hochleistungsfähige Windows Sockets-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="56533-126">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="56533-127">Nagle-Algorithmus</span><span class="sxs-lookup"><span data-stu-id="56533-127">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



