---
title: Implementieren von IClassFactory
description: Implementieren von IClassFactory
ms.assetid: 96466756-c135-4ee5-a48c-f31129878473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b057657508b3060506c15c68308ea6a5332e5099
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391044"
---
# <a name="implementing-iclassfactory"></a><span data-ttu-id="67d14-103">Implementieren von IClassFactory</span><span class="sxs-lookup"><span data-stu-id="67d14-103">Implementing IClassFactory</span></span>

<span data-ttu-id="67d14-104">Wenn ein Client eine CLSID verwendet, um die Erstellung einer Objektinstanz anzufordern, besteht der erste Schritt in der Erstellung eines Klassen Objekts, einem zwischen Objekt, das eine Implementierung der Methoden der [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) -Schnittstelle enthält.</span><span class="sxs-lookup"><span data-stu-id="67d14-104">When a client uses a CLSID to request the creation of an object instance, the first step is creation of a class object, an intermediate object that contains an implementation of the methods of the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface.</span></span> <span data-ttu-id="67d14-105">Während com mehrere Instanzen Erstellungs Funktionen bereitstellt, ist der erste Schritt bei der Implementierung dieser Funktionen die Erstellung eines Klassen Objekts.</span><span class="sxs-lookup"><span data-stu-id="67d14-105">While COM provides several instance creation functions, the first step in the implementation of these functions is the creation of a class object.</span></span>

<span data-ttu-id="67d14-106">Daher müssen alle Server die Methoden der [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) -Schnittstelle implementieren, die zwei Methoden enthält:</span><span class="sxs-lookup"><span data-stu-id="67d14-106">As a result, all servers must implement the methods of the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface, which contains two methods:</span></span>

-   <span data-ttu-id="67d14-107">" [**Kreatabstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance)".</span><span class="sxs-lookup"><span data-stu-id="67d14-107">[**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance).</span></span> <span data-ttu-id="67d14-108">Diese Methode muss eine nicht initialisierte Instanz des-Objekts erstellen und einen Zeiger auf eine angeforderte Schnittstelle für das-Objekt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="67d14-108">This method must create an uninitialized instance of the object and return a pointer to a requested interface on the object.</span></span>
-   <span data-ttu-id="67d14-109">[**Lock Server**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver).</span><span class="sxs-lookup"><span data-stu-id="67d14-109">[**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver).</span></span> <span data-ttu-id="67d14-110">Diese Methode erhöht lediglich den Verweis Zähler für das Klassenobjekt, um sicherzustellen, dass der Server im Arbeitsspeicher bleibt und nicht heruntergefahren wird, bevor der Client dafür bereit ist.</span><span class="sxs-lookup"><span data-stu-id="67d14-110">This method just increments the reference count on the class object to ensure that the server stays in memory and does not shut down before the client is ready for it to do so.</span></span>

<span data-ttu-id="67d14-111">Damit ein Server für seine eigene Lizenzierung verantwortlich ist, definiert com [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), das seine Definition von [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)erbt.</span><span class="sxs-lookup"><span data-stu-id="67d14-111">To enable a server to be responsible for its own licensing, COM defines [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), which inherits its definition from [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="67d14-112">Daher muss ein Server, der **IClassFactory2** implementiert, definitionsgemäß die Methoden von **IClassFactory** implementieren.</span><span class="sxs-lookup"><span data-stu-id="67d14-112">Thus, a server implementing **IClassFactory2** must, by definition, implement the methods of **IClassFactory**.</span></span>

<span data-ttu-id="67d14-113">COM bietet auch Hilfsfunktionen zum Implementieren von Prozess externen Servern.</span><span class="sxs-lookup"><span data-stu-id="67d14-113">COM also provides helper functions for implementing out-of-process servers.</span></span> <span data-ttu-id="67d14-114">Weitere Informationen finden Sie unter [Implementierung von Out-of-Process-Server Implementierungen](out-of-process-server-implementation-helpers.md).</span><span class="sxs-lookup"><span data-stu-id="67d14-114">For more information, see [Out-of-Process Server Implementation Helpers](out-of-process-server-implementation-helpers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="67d14-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="67d14-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67d14-116">Zuständigkeiten von com-Servern</span><span class="sxs-lookup"><span data-stu-id="67d14-116">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> <dt>

[<span data-ttu-id="67d14-117">Lizenzierung und IClassFactory2</span><span class="sxs-lookup"><span data-stu-id="67d14-117">Licensing and IClassFactory2</span></span>](licensing-and-iclassfactory2.md)
</dt> </dl>

 

 