---
description: Dieser Abschnitt beschreibt die pragmatische allgemeine Multicast-Protokoll Implementierung (PGM) in Windows, häufig als zuverlässiges Multicast bezeichnet. Zuverlässiges Multicast wird durch Windows Sockets in Windows Server 2003 und höher implementiert.
ms.assetid: 81c203ed-739f-4a06-99a1-9a99c6164edc
title: Zuverlässige Multicast Programmierung (PGM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce57fcce7bf2faf471604bed97d345971801ca1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343441"
---
# <a name="reliable-multicast-programming-pgm"></a><span data-ttu-id="4c2dc-104">Zuverlässige Multicast Programmierung (PGM)</span><span class="sxs-lookup"><span data-stu-id="4c2dc-104">Reliable Multicast Programming (PGM)</span></span>

<span data-ttu-id="4c2dc-105">Dieser Abschnitt beschreibt die pragmatische allgemeine Multicast-Protokoll Implementierung (PGM) in Windows, häufig als zuverlässiges Multicast bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4c2dc-105">This section describes the Pragmatic General Multicast (PGM) multicast protocol implementation in Windows, often referred to as reliable multicast.</span></span> <span data-ttu-id="4c2dc-106">Zuverlässiges Multicast wird durch Windows Sockets in Windows Server 2003 und höher implementiert.</span><span class="sxs-lookup"><span data-stu-id="4c2dc-106">Reliable multicast is implemented through Windows Sockets in Windows Server 2003 and later.</span></span>

<span data-ttu-id="4c2dc-107">**Windows XP:** PGM wird nur unterstützt, wenn Microsoft Message Queuing (MSMQ) 3,0 installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4c2dc-107">**Windows XP:** PGM is only supported when Microsoft Message Queuing (MSMQ) 3.0 is installed.</span></span>

<span data-ttu-id="4c2dc-108">PGM ist ein zuverlässiges und skalierbares Multicast Protokoll, das es Empfängern ermöglicht, Verluste zu erkennen, eine erneute Übertragung verlorener Daten anzufordern oder eine Anwendung mit nicht BEHEB barem Verlust zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="4c2dc-108">PGM is a reliable and scalable multicast protocol that enables receivers to detect loss, request retransmission of lost data, or notify an application of unrecoverable loss.</span></span> <span data-ttu-id="4c2dc-109">Bei PGM handelt es sich um ein zuverlässiges Empfänger Protokoll. Dies bedeutet, dass der Empfänger dafür verantwortlich ist, sicherzustellen, dass alle Daten empfangen werden, sodass er den Absender der Empfangs Verantwortung übernimmt.</span><span class="sxs-lookup"><span data-stu-id="4c2dc-109">PGM is a receiver-reliable protocol, which means the receiver is responsible for ensuring all data is received, absolving the sender of reception responsibility.</span></span>

<span data-ttu-id="4c2dc-110">PGM eignet sich für Anwendungen, die eine duplizierte Multicast-Datenübermittlung von mehreren Quellen an mehrere Empfänger benötigen.</span><span class="sxs-lookup"><span data-stu-id="4c2dc-110">PGM is appropriate for applications that require duplicate-free multicast data delivery from multiple sources to multiple receivers.</span></span> <span data-ttu-id="4c2dc-111">PGM unterstützt weder eine bestätigte Übermittlung noch die Reihenfolge von Paketen mehrerer Absender.</span><span class="sxs-lookup"><span data-stu-id="4c2dc-111">PGM does not support acknowledged delivery, nor does it guarantee ordering of packets from multiple senders.</span></span>

<span data-ttu-id="4c2dc-112">Weitere Informationen zu PGM finden Sie 3208 unter [www.ietf.org](https://www.ietf.org/).</span><span class="sxs-lookup"><span data-stu-id="4c2dc-112">For more information about PGM, refer to RFC 3208 available at [www.ietf.org](https://www.ietf.org/).</span></span>

<span data-ttu-id="4c2dc-113">In diesem Abschnitt wird beschrieben, wie Sie zuverlässiges Multicast unter Windows verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c2dc-113">This section describes how to use reliable multicast on Windows.</span></span> <span data-ttu-id="4c2dc-114">In den folgenden Themen werden die verschiedenen Aspekte der Erstellung einer zuverlässigen Multicast Anwendung mithilfe von Windows Sockets erläutert:</span><span class="sxs-lookup"><span data-stu-id="4c2dc-114">The following topics explain the various aspects of creating a reliable multicast application using Windows Sockets:</span></span>

-   [<span data-ttu-id="4c2dc-115">PGM-Absender und-Empfänger</span><span class="sxs-lookup"><span data-stu-id="4c2dc-115">PGM Senders and Receivers</span></span>](pgm-senders-and-receivers.md)
-   [<span data-ttu-id="4c2dc-116">PGM-Sender Optionen</span><span class="sxs-lookup"><span data-stu-id="4c2dc-116">PGM Sender Options</span></span>](pgm-sender-options.md)
-   [<span data-ttu-id="4c2dc-117">Senden und empfangen von PGM-Daten</span><span class="sxs-lookup"><span data-stu-id="4c2dc-117">Sending and Receiving PGM Data</span></span>](sending-and-receiving-pgm-data.md)
-   [<span data-ttu-id="4c2dc-118">Multihosting und PGM</span><span class="sxs-lookup"><span data-stu-id="4c2dc-118">Multihoming and PGM</span></span>](multihoming-and-pgm.md)
-   [<span data-ttu-id="4c2dc-119">PGM-Socketoptionen</span><span class="sxs-lookup"><span data-stu-id="4c2dc-119">PGM Socket Options</span></span>](pgm-socket-options.md)

 

 



