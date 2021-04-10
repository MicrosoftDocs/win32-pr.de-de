---
title: Zeiger und RPC
description: Es ist sehr effizient, Zeiger als C-Funktionsparameter zu verwenden.
ms.assetid: 5792bd45-9c2a-4dd2-b050-17082fd0c929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbacce89046e2808acad539d19bbdcfeb1bc99c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856636"
---
# <a name="pointers-and-rpc"></a><span data-ttu-id="b2097-103">Zeiger und RPC</span><span class="sxs-lookup"><span data-stu-id="b2097-103">Pointers and RPC</span></span>

<span data-ttu-id="b2097-104">Es ist sehr effizient, Zeiger als C-Funktionsparameter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2097-104">It is very efficient to use pointers as C-function parameters.</span></span> <span data-ttu-id="b2097-105">Der Zeiger kostet nur einige Bytes und kann verwendet werden, um auf eine große Menge an Arbeitsspeicher zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="b2097-105">The pointer costs only a few bytes and can be used to access a large amount of memory.</span></span> <span data-ttu-id="b2097-106">In einer verteilten Anwendung befinden sich die Client-und Server Prozeduren jedoch in unterschiedlichen Adressräumen – Sie können sich auf unterschiedlichen Computern befinden.</span><span class="sxs-lookup"><span data-stu-id="b2097-106">However, in a distributed application, the client and server procedures reside in different address spaces—they can be on different computers.</span></span> <span data-ttu-id="b2097-107">Daher haben der Client und der Server in der Regel keinen Zugriff auf denselben Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="b2097-107">Therefore, the client and the server usually do not have access to the same memory space.</span></span>

<span data-ttu-id="b2097-108">Wenn einer der Parameter der Remote Prozedur ein Zeiger auf ein Objekt ist, muss der Client eine Kopie des Objekts und dessen Zeiger auf den Server übertragen.</span><span class="sxs-lookup"><span data-stu-id="b2097-108">When one of the remote procedure's parameters is a pointer to an object, the client must transmit a copy of that object and its pointer to the server.</span></span> <span data-ttu-id="b2097-109">Wenn das Objekt durch die Remote Prozedur über seinen Zeiger geändert wird, gibt der Server den Zeiger und seine geänderte Kopie zurück.</span><span class="sxs-lookup"><span data-stu-id="b2097-109">If the remote procedure modifies the object through its pointer, the server returns the pointer and its modified copy.</span></span>

<span data-ttu-id="b2097-110">In der mittleren l werden Zeiger Attribute angeboten, um den erforderlichen mehr Aufwand und die Größe der Anwendung zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="b2097-110">MIDL offers pointer attributes to minimize the amount of required overhead and the size of your application.</span></span> <span data-ttu-id="b2097-111">In diesem Abschnitt werden der Zweck und die Verwendung von-Mittell-Zeiger Attributen erläutert.</span><span class="sxs-lookup"><span data-stu-id="b2097-111">This section discusses the purpose and uses of MIDL pointer attributes.</span></span> <span data-ttu-id="b2097-112">Außerdem werden Informationen zur Zeiger Behandlung in RPC-Anwendungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2097-112">It also presents information on pointer handling in RPC applications.</span></span> <span data-ttu-id="b2097-113">Es ist in die folgenden Themen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="b2097-113">It is divided into the following topics:</span></span>

-   [<span data-ttu-id="b2097-114">Arten von Zeigern</span><span class="sxs-lookup"><span data-stu-id="b2097-114">Kinds of Pointers</span></span>](kinds-of-pointers.md)
-   [<span data-ttu-id="b2097-115">Zeiger und Speicher Belegung</span><span class="sxs-lookup"><span data-stu-id="b2097-115">Pointers and Memory Allocation</span></span>](pointers-and-memory-allocation.md)
-   [<span data-ttu-id="b2097-116">Standard Zeiger Typen</span><span class="sxs-lookup"><span data-stu-id="b2097-116">Default Pointer Types</span></span>](default-pointer-types.md)
-   [<span data-ttu-id="b2097-117">Vererbung von Attributtypen</span><span class="sxs-lookup"><span data-stu-id="b2097-117">Pointer-Attribute Type Inheritance</span></span>](pointer-attribute-type-inheritance.md)

 

 




