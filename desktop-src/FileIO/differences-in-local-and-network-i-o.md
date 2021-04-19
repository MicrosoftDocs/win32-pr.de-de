---
description: Unterschiede zwischen lokalem e/a und Netzwerk-e/a unter Windows.
ms.assetid: 8a8f20bd-fa41-4f1a-b9bf-5f09683cd46c
title: Unterschiede in lokalen und Netzwerk-e/a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30c4faf6b7358a1c7c134dccdeb12298309c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363544"
---
# <a name="differences-in-local-and-network-io"></a><span data-ttu-id="79298-103">Unterschiede in lokalen und Netzwerk-e/a</span><span class="sxs-lookup"><span data-stu-id="79298-103">Differences in Local and Network I/O</span></span>

<span data-ttu-id="79298-104">Es gibt einige wichtige Unterschiede zwischen lokalem e/a und Netzwerk-e/a unter Windows:</span><span class="sxs-lookup"><span data-stu-id="79298-104">There are some notable differences between local I/O and network I/O on Windows:</span></span>

-   <span data-ttu-id="79298-105">Die Netzwerk-e/a-Unterstützung ist abhängig vom Redirector und dem Netzwerkprotokoll.</span><span class="sxs-lookup"><span data-stu-id="79298-105">Network I/O support depends on the redirector and the network protocol.</span></span>
-   <span data-ttu-id="79298-106">Die Netzwerk-e/a-Leistung hängt von der Anzahl der Netzwerk-e/a-Vorgänge und der Geschwindigkeit der Netzwerkverbindung ab.</span><span class="sxs-lookup"><span data-stu-id="79298-106">Network I/O performance depends on how many network I/O operations are taking place and the speed of the network connection.</span></span> <span data-ttu-id="79298-107">Ihre Anwendung muss in der Lage sein, Netzwerk-e/a-Vorgänge mit Servern zu verarbeiten, die viel schneller oder langsamer als der lokale Computer sein können, sowie vorübergehende Änderungen an der Netzwerkkapazität.</span><span class="sxs-lookup"><span data-stu-id="79298-107">Your application must be able to handle network I/O operations with servers that may be much faster or slower than your local machine, as well as transient changes in network capacity.</span></span> <span data-ttu-id="79298-108">In diesen Fällen muss Ihre Anwendung möglicherweise mehr Zeit für den Abschluss des Vorgangs zulassen.</span><span class="sxs-lookup"><span data-stu-id="79298-108">In these cases, your application may need to allow more time for the operation to complete.</span></span>
-   <span data-ttu-id="79298-109">Die Funktionen, die Sie verwenden, um lokale Datei-e/a auszuführen, können sich über das Netzwerk anders Verhalten.</span><span class="sxs-lookup"><span data-stu-id="79298-109">The functions you use to perform local file I/O may behave differently over the network.</span></span> <span data-ttu-id="79298-110">Beispielsweise kann bei einem Netzwerk-e/a-Vorgang, der lange dauert, ein Timeout auftreten. In einigen Situationen kann es sein, dass Datei Handles unbegrenzt offen bleiben.</span><span class="sxs-lookup"><span data-stu-id="79298-110">For example, a network I/O operation that takes a long time to complete may time out. In some situations, file handles may be left open indefinitely because of this.</span></span> <span data-ttu-id="79298-111">Ein weiteres Beispiel ist, dass Functions Fehlercodes zurückgeben kann, die Ihre Anwendung für die Netzwerk-e/a-Vorgänge spezifisch verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="79298-111">Another example is that functions may return error codes for your application to process that are specific to network I/O.</span></span>

 

 



