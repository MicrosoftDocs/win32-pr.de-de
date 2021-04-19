---
title: Explizite Bindungs Handles
description: Um die maximale Kontrolle über den Bindungsprozess zu erhalten, verwenden Client/Server-Anwendungen möglicherweise explizite Bindungs Handles.
ms.assetid: e711ce37-92f0-4e60-a126-148c27662c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b391c339ac3747928e3394152e9c0de7c1c7aa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341862"
---
# <a name="explicit-binding-handles"></a><span data-ttu-id="0603d-103">Explizite Bindungs Handles</span><span class="sxs-lookup"><span data-stu-id="0603d-103">Explicit Binding Handles</span></span>

<span data-ttu-id="0603d-104">Um die maximale Kontrolle über den Bindungsprozess zu erhalten, verwenden Client/Server-Anwendungen möglicherweise explizite Bindungs Handles.</span><span class="sxs-lookup"><span data-stu-id="0603d-104">For maximum control over the binding process, client/server applications may use explicit binding handles.</span></span> <span data-ttu-id="0603d-105">Wie implizite Handles ermöglichen explizite Bindungs Handles Ihrer Client Anwendung, einen Server für die Ausführung ihrer Aufrufe auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="0603d-105">Like implicit handles, explicit binding handles enable your client application to select a server to execute its calls.</span></span> <span data-ttu-id="0603d-106">Außerdem ermöglichen explizite Bindungs Handles Ihrer Client/Server-Anwendung das Erstellen einer authentifizierten RPC-Kommunikationssitzung.</span><span class="sxs-lookup"><span data-stu-id="0603d-106">In addition, explicit binding handles enable your client/server application to create an authenticated RPC communication session.</span></span> <span data-ttu-id="0603d-107">Mit expliziten Handles kann der Client eine Verbindung mit mehr als einem Server herstellen und Remote Prozeduren auf mehreren Servern ausführen.</span><span class="sxs-lookup"><span data-stu-id="0603d-107">With explicit handles, your client can connect to more than one server and execute remote procedures on multiple servers.</span></span> <span data-ttu-id="0603d-108">Multithread-und asynchrone Client Anwendungen können sogar eine Verbindung mit mehreren Servern herstellen und gleichzeitig mehrere Remote Prozeduren ausführen.</span><span class="sxs-lookup"><span data-stu-id="0603d-108">Multithreaded and asynchronous client applications can even connect to multiple servers and execute multiple remote procedures at the same time.</span></span>

<span data-ttu-id="0603d-109">Die Client Anwendung muss das explizite Handle als Parameter an jeden Remote Prozedur aufzurufen übergeben.</span><span class="sxs-lookup"><span data-stu-id="0603d-109">Your client application must pass the explicit handle as a parameter to each remote procedure call.</span></span> <span data-ttu-id="0603d-110">Um dem OSF-Standard zu entsprechen, sollte das Handle für jede Remote Prozedur als erster Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0603d-110">To conform to the OSF standard, the handle should be specified as the first parameter on each remote procedure.</span></span> <span data-ttu-id="0603d-111">Die Microsoft-Erweiterungen für RPC ermöglichen es Ihnen jedoch, das Bindungs Handle an anderen Positionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0603d-111">However, the Microsoft extensions to RPC enable you to specify the binding handle in other positions.</span></span> <span data-ttu-id="0603d-112">Weitere Informationen finden Sie unter [Microsoft RPC Binding-Handle Extensions](microsoft-rpc-binding-handle-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="0603d-112">For more information, see [Microsoft RPC Binding-Handle Extensions](microsoft-rpc-binding-handle-extensions.md).</span></span>

<span data-ttu-id="0603d-113">Zum Erstellen eines expliziten Handles deklarieren Sie das Handle als Parameter für die Remote Vorgänge in der IDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="0603d-113">To create an explicit handle, declare the handle as a parameter to the remote operations in the IDL file.</span></span> <span data-ttu-id="0603d-114">Das [Hello, World-Beispiel](tutorial.md) kann so neu definiert werden, dass ein explizites handle wie gezeigt verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="0603d-114">The [Hello, World example](tutorial.md) can be redefined to use an explicit handle as shown:</span></span>

``` syntax
/* IDL file for explicit handles */
 
[ 
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0) 
]
interface hello
{
  void HelloProc([in] handle_t h1,
                 [in, string] char *  pszString); 
}
```

<span data-ttu-id="0603d-115">Sie können explizite und implizite Handles in einer einzelnen Schnittstelle kombinieren.</span><span class="sxs-lookup"><span data-stu-id="0603d-115">You can combine explicit and implicit handles in a single interface.</span></span> <span data-ttu-id="0603d-116">Wenn eine Funktion einen expliziten Handle in der Parameterliste aufweist, wird dieses Handle verwendet.</span><span class="sxs-lookup"><span data-stu-id="0603d-116">If a function has an explicit handle in its parameter list, that handle will be used.</span></span> <span data-ttu-id="0603d-117">Wenn eine Funktion in einer Schnittstelle, die implizite Handles verwendet, kein explizites Handle angibt, wird das implizite Standard Handle verwendet.</span><span class="sxs-lookup"><span data-stu-id="0603d-117">If a function in an interface using implicit handles does not specify an explicit handle, then the default implicit handle will be used.</span></span>

 

 




