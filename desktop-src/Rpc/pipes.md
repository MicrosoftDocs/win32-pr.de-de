---
title: Pipes (RPC)
description: Der pipetypkonstruktor ist ein sehr effizienter Mechanismus zum übergeben großer Datenmengen oder einer beliebigen Menge von Daten, die nicht alle gleichzeitig im Arbeitsspeicher verfügbar sind.
ms.assetid: 913d5e2a-00ad-4060-9274-a6db23fb2817
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, Pipes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6c670b51dfe634fb5b3318e0a0b8a796cfbf988
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474874"
---
# <a name="pipes-rpc"></a><span data-ttu-id="df825-104">Pipes (RPC)</span><span class="sxs-lookup"><span data-stu-id="df825-104">Pipes (RPC)</span></span>

<span data-ttu-id="df825-105">Der pipetypkonstruktor ist ein sehr effizienter Mechanismus zum übergeben großer Datenmengen oder einer beliebigen Menge von Daten, die nicht alle gleichzeitig im Arbeitsspeicher verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="df825-105">The pipe type constructor is a highly efficient mechanism for passing large amounts of data, or any quantity of data that is not all available in memory at one time.</span></span> <span data-ttu-id="df825-106">Durch die Verwendung einer Pipe verarbeitet die RPC-Laufzeit die tatsächliche Datenübertragung und entfällt so den Aufwand, der mit wiederholten Remote Prozedur aufrufen verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="df825-106">By using a pipe, RPC run time handles the actual data transfer, eliminating the overhead associated with repeated remote procedure calls.</span></span>

<span data-ttu-id="df825-107">Nachdem ein Client eine Remote Prozedur mit einem Pipe-Parameter aufgerufen hat, geben der Client und der Server Schleifen zum Übertragen von Daten ein.</span><span class="sxs-lookup"><span data-stu-id="df825-107">After a client invokes a remote procedure that has a pipe parameter, the client and server enter loops to transfer data.</span></span> <span data-ttu-id="df825-108">Die Daten können auf dem Client oder dem Server erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="df825-108">The data can be produced on the client or the server.</span></span> <span data-ttu-id="df825-109">In jedem Fall muss die Datenmenge (in Bytes) nicht im Voraus bekannt sein.</span><span class="sxs-lookup"><span data-stu-id="df825-109">Either way, the amount of data (in bytes) does not have to be known in advance.</span></span> <span data-ttu-id="df825-110">Die Daten können inkrementell erzeugt oder genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="df825-110">The data can be produced or consumed incrementally.</span></span> <span data-ttu-id="df825-111">In der Datenübertragungs Schleife ruft der Server Stub-Routinen auf, die einen Datenpuffer laden oder entladen.</span><span class="sxs-lookup"><span data-stu-id="df825-111">While in the data-transfer loop, the server calls stub routines that load or unload a buffer of data.</span></span> <span data-ttu-id="df825-112">Der Client ruft vom Programmierer definierte Prozeduren auf, um Puffer zuzuordnen, Daten in Daten zu laden und aus den Puffern zu entladen.</span><span class="sxs-lookup"><span data-stu-id="df825-112">The client calls programmer-defined procedures to allocate buffers, load data into and unload data from the buffers.</span></span>

<span data-ttu-id="df825-113">Dieser Abschnitt bietet eine Übersicht über die Verwendung von Pipes für Remote Prozedur Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="df825-113">This section provides an overview of using pipes for remote procedure calls.</span></span> <span data-ttu-id="df825-114">Sie finden die Übersicht in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="df825-114">It presents the overview in the following topics:</span></span>

-   [<span data-ttu-id="df825-115">Wichtige Pipe-Terminologie</span><span class="sxs-lookup"><span data-stu-id="df825-115">Essential Pipe Terminology</span></span>](essential-pipe-terminology.md)
-   [<span data-ttu-id="df825-116">Der Pipezustand</span><span class="sxs-lookup"><span data-stu-id="df825-116">The Pipe State</span></span>](the-pipe-state.md)
-   [<span data-ttu-id="df825-117">Definieren von Pipes in IDL-Dateien</span><span class="sxs-lookup"><span data-stu-id="df825-117">Defining Pipes in IDL Files</span></span>](defining-pipes-in-idl-files.md)
-   [<span data-ttu-id="df825-118">Client seitige Pipe-Implementierung</span><span class="sxs-lookup"><span data-stu-id="df825-118">Client-Side Pipe Implementation</span></span>](client-side-pipe-implementation.md)
-   [<span data-ttu-id="df825-119">Server seitige Pipe-Implementierung</span><span class="sxs-lookup"><span data-stu-id="df825-119">Server-Side Pipe Implementation</span></span>](server-side-pipe-implementation.md)
-   [<span data-ttu-id="df825-120">Regeln für mehrere Pipes</span><span class="sxs-lookup"><span data-stu-id="df825-120">Rules for Multiple Pipes</span></span>](rules-for-multiple-pipes.md)
-   [<span data-ttu-id="df825-121">Kombinieren von Pipe-und nonpipe-Parametern</span><span class="sxs-lookup"><span data-stu-id="df825-121">Combining Pipe and Nonpipe Parameters</span></span>](combining-pipe-and-nonpipe-parameters.md)

<span data-ttu-id="df825-122">Weitere Informationen zur Pipe-Syntax und zu Einschränkungen finden Sie unter [Pipe](/windows/desktop/Midl/pipe) in der Sprache der Mittel l-Sprache.</span><span class="sxs-lookup"><span data-stu-id="df825-122">For more information on pipe syntax and restrictions, see [pipe](/windows/desktop/Midl/pipe) in the MIDL Language Reference.</span></span> <span data-ttu-id="df825-123">Das Pipes-Beispielprogramm in der Platform Software Development Kit (SDK)-Beispiele \\ RPC-Verzeichnis veranschaulicht, wie Sie **\[ in, out \]** Pipes zum Übertragen von Daten zwischen einem Client und einem Server verwenden.</span><span class="sxs-lookup"><span data-stu-id="df825-123">The PIPES sample program in the Platform Software Development Kit (SDK) samples\\rpc directory demonstrates how to use **\[in,out\]** pipes to transfer data between a client and a server.</span></span>

 

 
