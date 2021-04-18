---
title: Wieder verwenden von Objekten
description: Wieder verwenden von Objekten
ms.assetid: 07055fea-bdfe-4c7a-be07-2edcbf609dd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a830eb539823b0350c9ce41a096cda821bb0cb
ms.sourcegitcommit: 917c90b6ed4af323fedada331211b40396876424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2020
ms.locfileid: "104516695"
---
# <a name="reusing-objects"></a><span data-ttu-id="2a11b-103">Wieder verwenden von Objekten</span><span class="sxs-lookup"><span data-stu-id="2a11b-103">Reusing Objects</span></span>

<span data-ttu-id="2a11b-104">Ein wichtiges Ziel eines Objektmodells besteht darin, Objekt Autoren die Wiederverwendung und Erweiterung von Objekten zu ermöglichen, die von anderen Benutzern als Teile ihrer eigenen Implementierungen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2a11b-104">An important goal of any object model is to enable object authors to reuse and extend objects provided by others as pieces of their own implementations.</span></span> <span data-ttu-id="2a11b-105">Eine Möglichkeit, dies in Microsoft Visual C++ und anderen Sprachen zu erreichen, ist die Verwendung der *Implementierungsvererbung*, mit der ein Objekt einige seiner Funktionen von einem anderen Objekt erben kann, während andere Funktionen außer Kraft gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="2a11b-105">One way to do this in Microsoft Visual C++ and other languages is by using *implementation inheritance*, which allows an object to inherit ("subclass") some of its functions from another object while overriding other functions.</span></span>

<span data-ttu-id="2a11b-106">Das Problem bei der systemweiten Objekt Interaktion mit herkömmlicher Implementierungs Vererbung besteht darin, dass der Vertrag (die Schnittstelle) zwischen Objekten in einer Implementierungs Hierarchie nicht eindeutig definiert ist.</span><span class="sxs-lookup"><span data-stu-id="2a11b-106">The problem for systemwide object interaction using traditional implementation inheritance is that the contract (the interface) between objects in an implementation hierarchy is not clearly defined.</span></span> <span data-ttu-id="2a11b-107">Tatsächlich ist Sie implizit und mehrdeutig.</span><span class="sxs-lookup"><span data-stu-id="2a11b-107">In fact, it is implicit and ambiguous.</span></span> <span data-ttu-id="2a11b-108">Wenn das übergeordnete oder untergeordnete Objekt seine Implementierung ändert, kann das Verhalten verwandter Komponenten nicht definiert oder nicht dauerhaft implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="2a11b-108">When the parent or child object changes its implementation, the behavior of related components might become undefined or unstably implemented.</span></span> <span data-ttu-id="2a11b-109">In jeder einzelnen Anwendung, in der die Implementierung von einem einzelnen Engineering-Team verwaltet werden kann, das alle Komponenten gleichzeitig aktualisiert, ist dies nicht immer ein wichtiger Grund.</span><span class="sxs-lookup"><span data-stu-id="2a11b-109">In any single application, where the implementation can be managed by a single engineering team that updates all of the components at the same time, this is not always a major concern.</span></span> <span data-ttu-id="2a11b-110">In einer Umgebung, in der die Komponenten eines Teams durch die Wiederverwendung durch Blackbox anderer von anderen Teams erstellter Komponenten erstellt werden, gefährdet diese Art von Instabilität die Wiederverwendung.</span><span class="sxs-lookup"><span data-stu-id="2a11b-110">In an environment where the components of one team are built through black-box reuse of other components built by other teams, this type of instability jeopardizes reuse.</span></span> <span data-ttu-id="2a11b-111">Außerdem funktioniert die Implementierungs Vererbung in der Regel nur innerhalb der Prozess Grenzen.</span><span class="sxs-lookup"><span data-stu-id="2a11b-111">Additionally, implementation inheritance usually works only within process boundaries.</span></span> <span data-ttu-id="2a11b-112">Dadurch wird die herkömmliche Implementierungs Vererbung für große, sich entwickelnde Systeme, die aus den von vielen Engineering Teams erstellten Softwarekomponenten bestehen, nicht praktikabel.</span><span class="sxs-lookup"><span data-stu-id="2a11b-112">This makes traditional implementation inheritance impractical for large, evolving systems composed of software components built by many engineering teams.</span></span>

<span data-ttu-id="2a11b-113">Der Schlüssel zum Aufbau wiederverwendbarer Komponenten ist, dass das Objekt als undurchsichtiges Feld behandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2a11b-113">The key to building reusable components is to be able to treat the object as an opaque box.</span></span> <span data-ttu-id="2a11b-114">Dies bedeutet, dass der Code Abschnitt, der versucht, ein anderes Objekt wiederzuverwenden, nichts kennt und nichts über die interne Struktur oder Implementierung der verwendeten Komponente wissen muss.</span><span class="sxs-lookup"><span data-stu-id="2a11b-114">This means that the piece of code attempting to reuse another object knows nothing, and needs to know nothing, about the internal structure or implementation of the component being used.</span></span> <span data-ttu-id="2a11b-115">Anders ausgedrückt: der Code, der versucht, eine Komponente wiederzuverwenden, hängt vom Verhalten des Objekts und nicht von der exakten Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="2a11b-115">In other words, the code attempting to reuse a component depends on the behavior of the object and not its exact implementation.</span></span>

<span data-ttu-id="2a11b-116">Um die Wiederverwendbarkeit von Blackbox zu erreichen, übernimmt com andere bewährte Mechanismen für die Wiederverwendbarkeit *, wie z* *. b*</span><span class="sxs-lookup"><span data-stu-id="2a11b-116">To achieve black-box reusability, COM adopts other established reusability mechanisms such as *containment/delegation* and *aggregation*.</span></span>

> [!NOTE]  
> <span data-ttu-id="2a11b-117">Der Zweck wird das Objekt, das wieder verwendet wird, als internes *Objekt* bezeichnet, und das Objekt, das dieses innere Objekt verwendet, ist das *äußere Objekt*.</span><span class="sxs-lookup"><span data-stu-id="2a11b-117">For convenience, the object being reused is called the *inner object* and the object making use of that inner object is the *outer object*.</span></span>

 

<span data-ttu-id="2a11b-118">Es ist wichtig, sich in beiden Mechanismen daran zu erinnern, wie das äußere Objekt seinen Clients angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2a11b-118">It is important to remember in both these mechanisms how the outer object appears to its clients.</span></span> <span data-ttu-id="2a11b-119">Wenn die Clients betroffen sind, implementieren beide Objekte alle Schnittstellen, auf die der Client einen Zeiger erhalten kann.</span><span class="sxs-lookup"><span data-stu-id="2a11b-119">As far as the clients are concerned, both objects implement any interfaces to which the client can get a pointer.</span></span> <span data-ttu-id="2a11b-120">Der Client behandelt das äußere Objekt als ein undurchsichtiges Feld und ist daher nicht relevant, und es muss sich nicht um die interne Struktur des äußeren Objekts kümmern. "der Client kümmert sich nur um das Verhalten.</span><span class="sxs-lookup"><span data-stu-id="2a11b-120">The client treats the outer object as an opaque box and therefore does not care, nor does it need to care, about the internal structure of the outer objectâ€”the client cares only about behavior.</span></span>

<span data-ttu-id="2a11b-121">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="2a11b-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="2a11b-122">Einschluss/Delegierung</span><span class="sxs-lookup"><span data-stu-id="2a11b-122">Containment/Delegation</span></span>](containment-delegation.md)
-   [<span data-ttu-id="2a11b-123">Aggregation</span><span class="sxs-lookup"><span data-stu-id="2a11b-123">Aggregation</span></span>](aggregation.md)

 

 




