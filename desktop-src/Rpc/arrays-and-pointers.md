---
title: Arrays und Zeiger
description: Der Remote Prozedur Aufruf (RPC) ist so konzipiert, dass er für Entwickler größtenteils transparent ist.
ms.assetid: 5ad5a51d-a821-44a5-bbc3-14409cb42cb4
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, Arrays und Zeiger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb6bc3f4a2ec4af85156bf15160b0ce7d1efc33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711334"
---
# <a name="arrays-and-pointers"></a><span data-ttu-id="e4970-104">Arrays und Zeiger</span><span class="sxs-lookup"><span data-stu-id="e4970-104">Arrays and Pointers</span></span>

<span data-ttu-id="e4970-105">Der Remote Prozedur Aufruf (RPC) ist so konzipiert, dass er für Entwickler größtenteils transparent ist.</span><span class="sxs-lookup"><span data-stu-id="e4970-105">Remote Procedure Call (RPC) is designed to be mostly transparent to developers.</span></span> <span data-ttu-id="e4970-106">Um diese Transparenz zu erreichen, überträgt der Clientstub sowohl den Zeiger als auch das Datenobjekt, auf das er verweist, an den Server.</span><span class="sxs-lookup"><span data-stu-id="e4970-106">To achieve this transparency, the client stub transmits to the server both the pointer and the data object to which it points.</span></span> <span data-ttu-id="e4970-107">Wenn die Daten von der Remote Prozedur geändert werden, muss der Server die neuen Daten an den Client zurücksenden, damit der Client die neuen Daten über die ursprünglichen Daten kopieren kann.</span><span class="sxs-lookup"><span data-stu-id="e4970-107">If the remote procedure changes the data, the server must transmit the new data back to the client so that the client can copy the new data over the original data.</span></span>

<span data-ttu-id="e4970-108">Im allgemeinen verhält sich ein Remote Prozedur aufrufsverhalten wie ein lokaler Prozedur Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="e4970-108">In general, a remote procedure call behaves just like a local procedure call.</span></span> <span data-ttu-id="e4970-109">Das heißt, wenn ein Zeiger ein Parameter ist, kann die Remote Prozedur auf das Datenobjekt zugreifen, auf das der Zeiger auf die gleiche Weise wie eine lokale Prozedur verweist.</span><span class="sxs-lookup"><span data-stu-id="e4970-109">That is, when a pointer is a parameter, the remote procedure can access the data object the pointer refers to in the same way that a local procedure can.</span></span>

<span data-ttu-id="e4970-110">Da Client-und Serverprogramme in unterschiedlichen Adressbereichen ausgeführt werden, müssen Entwickler Microsoft Interface Definition Language-Attribute (Mittelwert) verwenden, um zu beschreiben, wie Array-und Zeiger Daten zwischen dem Client und dem Server übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="e4970-110">Since client and server programs run in different address spaces, developers must use Microsoft Interface Definition Language (MIDL) attributes to describe how array and pointer data is transmitted between the client and the server.</span></span> <span data-ttu-id="e4970-111">Dieser Abschnitt enthält eine Übersicht über die Verwendung von Arrays und Zeigern in verteilten Anwendungen in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="e4970-111">This section presents an overview of how to use arrays and pointers in distributed applications, in the following topics:</span></span>

-   [<span data-ttu-id="e4970-112">Arrays und RPC</span><span class="sxs-lookup"><span data-stu-id="e4970-112">Arrays and RPC</span></span>](arrays-and-rpc.md)
-   [<span data-ttu-id="e4970-113">Zeiger und RPC</span><span class="sxs-lookup"><span data-stu-id="e4970-113">Pointers and RPC</span></span>](pointers-and-rpc.md)
-   [<span data-ttu-id="e4970-114">Verwenden von Arrays, Zeichen folgen und Zeigern</span><span class="sxs-lookup"><span data-stu-id="e4970-114">Using Arrays, Strings, and Pointers</span></span>](using-arrays-strings-and-pointers.md)

 

 




