---
description: Implementieren von IUnknown
ms.assetid: 4e363ccb-9725-4be6-bb31-283bf1d658f5
title: Implementieren von IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27c12e25d56adab1841a375ac6c1ce0857a73b5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520499"
---
# <a name="how-to-implement-iunknown"></a><span data-ttu-id="b9b0b-103">Implementieren von IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9b0b-103">How to Implement IUnknown</span></span>

<span data-ttu-id="b9b0b-104">Microsoft DirectShow basiert auf dem Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="b9b0b-104">Microsoft DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="b9b0b-105">Wenn Sie einen eigenen Filter schreiben, müssen Sie ihn als COM-Objekt implementieren.</span><span class="sxs-lookup"><span data-stu-id="b9b0b-105">If you write your own filter, you must implement it as a COM object.</span></span> <span data-ttu-id="b9b0b-106">Die DirectShow-Basisklassen stellen ein Framework bereit, aus dem dies zu tun ist.</span><span class="sxs-lookup"><span data-stu-id="b9b0b-106">The DirectShow base classes provide a framework from which to do this.</span></span> <span data-ttu-id="b9b0b-107">Die Verwendung der Basisklassen ist nicht erforderlich, kann jedoch den Entwicklungsprozess vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="b9b0b-107">Using the base classes is not required, but it can simplify the development process.</span></span> <span data-ttu-id="b9b0b-108">In diesem Artikel werden einige der internen Details von COM-Objekten und deren Implementierung in den DirectShow-Basisklassen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b9b0b-108">This article describes some of the internal details of COM objects and their implementation in the DirectShow base classes.</span></span>

<span data-ttu-id="b9b0b-109">In diesem Artikel wird davon ausgegangen, dass Sie wissen, wie Sie com-Client Anwendungen programmieren können – mit anderen Worten, dass Sie die Methoden in **IUnknown**– verstehen, aber keine vorherige Erfahrung bei der Entwicklung von COM-Objekten annimmt.</span><span class="sxs-lookup"><span data-stu-id="b9b0b-109">This article assumes that you know how to program COM client applications—in other words, that you understand the methods in **IUnknown**—but does not assume any prior experience developing COM objects.</span></span> <span data-ttu-id="b9b0b-110">DirectShow behandelt viele der Details der Entwicklung eines COM-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b9b0b-110">DirectShow handles many of the details of developing a COM object.</span></span> <span data-ttu-id="b9b0b-111">Wenn Sie mit der Entwicklung von COM-Objekten vertraut sind, sollten Sie den Abschnitt [mit cunknown](using-cunknown.md)lesen, in dem die [**cunknown**](cunknown.md) -Basisklasse beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b9b0b-111">If you have experience developing COM objects, you should read the section [Using CUnknown](using-cunknown.md), which describes the [**CUnknown**](cunknown.md) base class.</span></span>

<span data-ttu-id="b9b0b-112">COM ist eine Spezifikation und keine Implementierung.</span><span class="sxs-lookup"><span data-stu-id="b9b0b-112">COM is a specification, not an implementation.</span></span> <span data-ttu-id="b9b0b-113">Es definiert die Regeln, denen eine Komponente folgen muss. Diese Regeln werden dem Entwickler überlassen.</span><span class="sxs-lookup"><span data-stu-id="b9b0b-113">It defines the rules that a component must follow; putting those rules into effect is left to the developer.</span></span> <span data-ttu-id="b9b0b-114">In DirectShow werden alle Objekte von einem Satz von C++-Basisklassen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b9b0b-114">In DirectShow, all objects derive from a set of C++ base classes.</span></span> <span data-ttu-id="b9b0b-115">Die Basisklassenkonstruktoren und-Methoden führen die meisten com-Buchhaltungsaufgaben aus, z. b. die Beibehaltung einer konsistenten Verweis Anzahl.</span><span class="sxs-lookup"><span data-stu-id="b9b0b-115">The base class constructors and methods do most of the COM "bookkeeping" work, such as keeping a consistent reference count.</span></span> <span data-ttu-id="b9b0b-116">Durch Ableiten des Filters von einer Basisklasse erben Sie die Funktionalität der-Klasse.</span><span class="sxs-lookup"><span data-stu-id="b9b0b-116">By deriving your filter from a base class, you inherit the functionality of the class.</span></span> <span data-ttu-id="b9b0b-117">Um Basisklassen effektiv zu verwenden, benötigen Sie ein allgemeines Verständnis der Implementierung der com-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="b9b0b-117">To use base classes effectively, you need a general understanding of how they implement the COM specification.</span></span>

<span data-ttu-id="b9b0b-118">Dieser Artikel enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b9b0b-118">This article contains the following topics.</span></span>

-   [<span data-ttu-id="b9b0b-119">Funktionsweise von IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9b0b-119">How IUnknown Works</span></span>](how-iunknown-works.md)
-   [<span data-ttu-id="b9b0b-120">Verwenden von cunknown</span><span class="sxs-lookup"><span data-stu-id="b9b0b-120">Using CUnknown</span></span>](using-cunknown.md)

## <a name="related-topics"></a><span data-ttu-id="b9b0b-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b9b0b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9b0b-122">DirectShow und com</span><span class="sxs-lookup"><span data-stu-id="b9b0b-122">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



