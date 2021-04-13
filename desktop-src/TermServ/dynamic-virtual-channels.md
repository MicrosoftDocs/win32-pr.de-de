---
title: Dynamische virtuelle Kanäle
description: Die APIs des dynamischen virtuellen Kanals (DVC) erweitern die vorhandenen virtuellen Channel-APIs für Remotedesktopdienste, die als statische virtuelle Kanal-APIs bezeichnet werden.
ms.assetid: bddf0048-482d-40f3-a973-9d7bc15be8fa
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3181c0960b50289846018c3ace773a8351cb20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388264"
---
# <a name="dynamic-virtual-channels"></a><span data-ttu-id="4b6a8-103">Dynamische virtuelle Kanäle</span><span class="sxs-lookup"><span data-stu-id="4b6a8-103">Dynamic Virtual Channels</span></span>

<span data-ttu-id="4b6a8-104">Die APIs des dynamischen virtuellen Kanals (DVC) erweitern die vorhandenen virtuellen Channel-APIs für Remotedesktopdienste, die als statische virtuelle Kanal-APIs bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-104">Dynamic virtual channel (DVC) APIs extend the existing virtual channel APIs for Remote Desktop Services, known as static virtual channel (SVC) APIs.</span></span> <span data-ttu-id="4b6a8-105">DVC-APIs erfüllen mehrere Einschränkungen, die in SVC-APIs zwischen Client und Server vorhanden waren, wie z. b.:</span><span class="sxs-lookup"><span data-stu-id="4b6a8-105">DVC APIs address several limitations that existed in SVC APIs between the client and server, such as:</span></span>

-   <span data-ttu-id="4b6a8-106">Eine begrenzte Anzahl von Kanälen</span><span class="sxs-lookup"><span data-stu-id="4b6a8-106">A limited number of channels</span></span>
-   <span data-ttu-id="4b6a8-107">Paket-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="4b6a8-107">Packet reconstruction</span></span>

<span data-ttu-id="4b6a8-108">DVC-APIs unterstützen Sie bei der Implementierung von Modulen auf Server-und Clientseite einer Remotedesktopdienste Verbindung, die miteinander kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-108">DVC APIs will help you to implement modules on the server and client side of a Remote Desktop Services connection that communicate with each other.</span></span>

<span data-ttu-id="4b6a8-109">Wie viele andere Client/Server-Architekturen wird eine Verbindung auf Grundlage eines häufig vereinbarten Daten Abschnitts hergestellt, der als Endpunkt bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-109">Like many other client/server architectures, a connection is established based on a commonly agreed upon piece of data, referred to as an endpoint.</span></span> <span data-ttu-id="4b6a8-110">Ein ähnliches Beispiel ist TCP/IP, bei dem ein Endpunkt durch eine Kombination aus Server-IP-Adresse und dem Portnamen festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-110">A similar example is TCP/IP, where an endpoint is established through a combination of server IP address and the port name.</span></span> <span data-ttu-id="4b6a8-111">Ein weiteres Beispiel sind Named Pipes, bei denen ein Endpunkt eine Kombination aus dem Servernamen und dem Pipenamen ist.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-111">Another example is named pipes, where an endpoint is a combination of the server name and the pipe name.</span></span> <span data-ttu-id="4b6a8-112">In einer Remotedesktopdienste Verbindung sind nur zwei Seiten beteiligt.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-112">In a Remote Desktop Services connection there are only two sides involved.</span></span> <span data-ttu-id="4b6a8-113">Daher besteht der Endpunkt aus einer einfachen beliebigen Zeichenfolge, die die Verbindung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-113">Therefore, the endpoint consists of a simple arbitrary string that uniquely identifies the connection.</span></span> <span data-ttu-id="4b6a8-114">Ähnlich wie bei TCP/IP und Named Pipes können mehrere Verbindungen über denselben Endpunkt Namen initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-114">Much like TCP/IP and named pipes, multiple connections can initiate from the same endpoint name.</span></span> <span data-ttu-id="4b6a8-115">In diesem Sinne haben Verbindungen keine Namen. nur ein Listener, der auf eingehende Anforderungen für den Endpunkt wartet.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-115">In that sense, connections do not have names; just a listener that waits for incoming requests on the endpoint.</span></span>

<span data-ttu-id="4b6a8-116">Die DVC-APIs bestehen aus folgendem:</span><span class="sxs-lookup"><span data-stu-id="4b6a8-116">The DVC APIs consist of the following:</span></span>

-   <span data-ttu-id="4b6a8-117">Client-APIs</span><span class="sxs-lookup"><span data-stu-id="4b6a8-117">Client APIs</span></span>

    <span data-ttu-id="4b6a8-118">Diese APIs sind im Remotedesktopverbindung-Client (RDC) als Plug-in verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-118">These APIs are available in the Remote Desktop Connection (RDC) client as a plug-in.</span></span> <span data-ttu-id="4b6a8-119">Die Clientseite befindet sich im passiven Modus, in dem Sie auf eingehende Verbindungen lauscht, aber keine aktive Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-119">The client side is in passive mode, where it listens for incoming connections but does not actively establish a connection.</span></span>

-   <span data-ttu-id="4b6a8-120">Server-APIs</span><span class="sxs-lookup"><span data-stu-id="4b6a8-120">Server APIs</span></span>

    <span data-ttu-id="4b6a8-121">Diese APIs initiieren die Verbindung aktiv.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-121">These APIs actively initiate the connection.</span></span>

<span data-ttu-id="4b6a8-122">Weitere Informationen zum Schreiben eines Moduls für einen dynamischen virtuellen Kanal (DVC) finden Sie unter [DVC-Implementierungs Details](dvc-implementation-details.md).</span><span class="sxs-lookup"><span data-stu-id="4b6a8-122">For information about how to write a dynamic virtual channel (DVC) module, see [DVC Implementation Details](dvc-implementation-details.md).</span></span>

 

 




