---
title: Mehrere Ebenen von Zeigern
description: Verwenden mehrerer Zeiger Ebenen in Remote Prozedur Aufruf (RPC).
ms.assetid: d45b9b20-3b21-4d46-9097-8aacb4e4e921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61a917ee29c982505c601d7b0dd0721e94e4678
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948958"
---
# <a name="multiple-levels-of-pointers"></a><span data-ttu-id="f43d4-103">Mehrere Ebenen von Zeigern</span><span class="sxs-lookup"><span data-stu-id="f43d4-103">Multiple Levels of Pointers</span></span>

<span data-ttu-id="f43d4-104">Wenn mehrere Zeiger Ebenen vorhanden sind, werden die Attribute mit dem Zeiger verknüpft, der dem Variablennamen am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="f43d4-104">When there are multiple levels of pointers, the attributes are associated with the pointer closest to the variable name.</span></span> <span data-ttu-id="f43d4-105">Der Client ist nach wie vor für die Zuordnung von Arbeitsspeicher verantwortlich, der der Antwort zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f43d4-105">The client is still responsible for allocating any memory associated with the response.</span></span>

<span data-ttu-id="f43d4-106">Im folgenden Beispiel kann der Stub den Server anrufen, ohne im Voraus zu wissen, wie viele Daten zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="f43d4-106">The following example allows the stub to call the server without knowing in advance how much data will be returned:</span></span>

``` syntax
[
    uuid( ...),
    version(3.3),
]
interface AnInterface
{
    HRESULT GetBars([out] long * pSize,
             [out, size_is( , *pSize)]
             BAR ** ppBar);//BAR type defined elsewhere
}
```

<span data-ttu-id="f43d4-107">In diesem Beispiel übergibt der Stub dem Server einen eindeutigen Zeiger, der vom Server mit **null** initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f43d4-107">In this example, the stub passes the server a unique pointer, which the server initializes to **NULL**.</span></span> <span data-ttu-id="f43d4-108">Der Server ordnet dann einen Block von Balken zu, legt den Zeiger fest, legt das Größen Argument fest und gibt zurück.</span><span class="sxs-lookup"><span data-stu-id="f43d4-108">The server then allocates a block of BARs, sets the pointer, sets the size argument and returns.</span></span> <span data-ttu-id="f43d4-109">Beachten Sie, dass Sie einen Verweis \[ \] Zeiger an einen \[ [**eindeutigen**](/windows/desktop/Midl/unique) \] Zeiger auf Ihre Daten übergeben müssen, damit der Server Auswirkungen auf den Aufrufer hat.</span><span class="sxs-lookup"><span data-stu-id="f43d4-109">Note that in order for the server to have an effect on the caller you must pass a \[ref\] pointer to a \[[**unique**](/windows/desktop/Midl/unique)\] pointer to your data.</span></span> <span data-ttu-id="f43d4-110">Beachten Sie auch, dass das Komma in \[ [**size (, \_**](/windows/desktop/Midl/size-is) \* Psize) ist \] , das angibt, dass der Zeiger der obersten Ebene kein Größen Zeiger ist, aber dass der Zeiger auf der unteren Ebene ist.</span><span class="sxs-lookup"><span data-stu-id="f43d4-110">Also note the comma in \[[**size\_is**](/windows/desktop/Midl/size-is)( , \*pSize )\], which indicates that the top-level pointer is not a sized pointer, but that the lower-level pointer is.</span></span>

<span data-ttu-id="f43d4-111">Auf der Clientseite legt der Stub \* ppbar auf **null** fest, bevor die Remote Prozedur aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f43d4-111">On the client side, the stub sets \*ppBar to **NULL** before calling the remote procedure.</span></span> <span data-ttu-id="f43d4-112">Der Stub ordnet dann die Arrays von Bar-Objekten zu und löscht diese.</span><span class="sxs-lookup"><span data-stu-id="f43d4-112">The stub then allocates and unmarshals the arry of BAR objects.</span></span> <span data-ttu-id="f43d4-113">Das size-Argument gibt die Größe des Blocks an (und die Anzahl der nicht gemarshallten Balken).</span><span class="sxs-lookup"><span data-stu-id="f43d4-113">The size argument indicates the size of the block (and the number of unmarshaled BARs).</span></span> <span data-ttu-id="f43d4-114">Der Client muss das zurückgegebene Array von Balken Objekten freigeben, wenn es nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="f43d4-114">The client must free the returned array of BAR objects when it is no longer required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f43d4-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f43d4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f43d4-116">**Größe \_ :**</span><span class="sxs-lookup"><span data-stu-id="f43d4-116">**size\_is**</span></span>](/windows/desktop/Midl/size-is)
</dt> </dl>

 

 