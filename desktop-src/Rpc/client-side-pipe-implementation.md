---
title: Client-Side Pipe-Implementierung
description: Client seitige Pipe-Implementierung in Remote Prozedur Aufruf (RPC).
ms.assetid: d790f859-47a9-4b6c-a218-8cbe05db21b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5666656f1f7296c252395255c17902a91cb32a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856684"
---
# <a name="client-side-pipe-implementation"></a><span data-ttu-id="9d1c6-103">Client-Side Pipe-Implementierung</span><span class="sxs-lookup"><span data-stu-id="9d1c6-103">Client-Side Pipe Implementation</span></span>

<span data-ttu-id="9d1c6-104">Die Client Anwendung muss die folgenden Prozeduren implementieren, die vom Clientstub während der Datenübertragung aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="9d1c6-104">The client application must implement the following procedures, which the client stub will call during data transfer:</span></span>

-   <span data-ttu-id="9d1c6-105">Eine Pull-Prozedur (für eine Eingabe Pipe)</span><span class="sxs-lookup"><span data-stu-id="9d1c6-105">A pull procedure (for an input pipe)</span></span>
-   <span data-ttu-id="9d1c6-106">Eine pushprozedur (für eine ausgabepipe)</span><span class="sxs-lookup"><span data-stu-id="9d1c6-106">A push procedure (for an output pipe)</span></span>
-   <span data-ttu-id="9d1c6-107">Eine Zuordnungs Prozedur, um einen Puffer für die Übertragungsdaten zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="9d1c6-107">An alloc procedure to allocate a buffer for the transfer data</span></span>

<span data-ttu-id="9d1c6-108">Alle diese Prozeduren müssen die Argumente verwenden, die von der von der Mittel l generierten Header Datei angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9d1c6-108">All of these procedures must use the arguments specified by the MIDL-generated header file.</span></span> <span data-ttu-id="9d1c6-109">Außerdem muss die Client Anwendung über eine Status Variable verfügen, um zu bestimmen, wo Daten gesucht oder platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9d1c6-109">In addition, the client application must have a state variable to identify where to locate or place data.</span></span>

<span data-ttu-id="9d1c6-110">Die zuordnungsprozedur kann auch so einfach oder so komplex sein, wie Sie benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="9d1c6-110">The alloc procedure can also be as simple or as complex as needed.</span></span> <span data-ttu-id="9d1c6-111">Sie kann z. b. jedes Mal, wenn der Stub die Funktion aufruft, einen Zeiger auf denselben Puffer zurückgeben, oder es kann jeweils eine andere Arbeitsspeicher Menge zuordnen.</span><span class="sxs-lookup"><span data-stu-id="9d1c6-111">For example, it can return a pointer to the same buffer every time the stub calls the function, or it can allocate a different amount of memory each time.</span></span> <span data-ttu-id="9d1c6-112">Wenn Ihre Daten bereits in der richtigen Form vorhanden sind (z. b. ein Array von Pipe-Elementen), können Sie die Zuordnungs Prozedur mit der Pull-Prozedur koordinieren, um einen Puffer zuzuordnen, der die Daten bereits enthält.</span><span class="sxs-lookup"><span data-stu-id="9d1c6-112">If your data is already in the proper form (an array of pipe elements, for example) you can coordinate the alloc procedure with the pull procedure to allocate a buffer that already contains the data.</span></span> <span data-ttu-id="9d1c6-113">In diesem Fall kann die Pull-Prozedur eine leere Routine sein.</span><span class="sxs-lookup"><span data-stu-id="9d1c6-113">In that case, your pull procedure could be an empty routine.</span></span>

<span data-ttu-id="9d1c6-114">Die Puffer Zuordnung muss in Bytes erfolgen.</span><span class="sxs-lookup"><span data-stu-id="9d1c6-114">The buffer allocation must be in bytes.</span></span> <span data-ttu-id="9d1c6-115">Die Push-und Pull-Prozeduren hingegen manipulieren Elemente, deren Größe in Bytes davon abhängt, wie Sie definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9d1c6-115">The push and pull procedures, on the other hand, manipulate elements, whose size in bytes depends on how they were defined.</span></span>

<span data-ttu-id="9d1c6-116">In diesem Abschnitt wird die Client Implementierung von Eingabe-und ausgabepipes in den folgenden Abschnitten erläutert:</span><span class="sxs-lookup"><span data-stu-id="9d1c6-116">This section discusses the client implementation of input and output pipes in the following sections:</span></span>

-   [<span data-ttu-id="9d1c6-117">Implementieren von Eingabe Pipes auf dem Client</span><span class="sxs-lookup"><span data-stu-id="9d1c6-117">Implementing Input Pipes on the Client</span></span>](implementing-input-pipes-on-the-client.md)
-   [<span data-ttu-id="9d1c6-118">Implementieren von Ausgabe Pipes auf dem Client</span><span class="sxs-lookup"><span data-stu-id="9d1c6-118">Implementing Output Pipes on the Client</span></span>](implementing-output-pipes-on-the-client.md)

 

 




