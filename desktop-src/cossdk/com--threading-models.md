---
description: Com+-Threading Modelle werden um eine Objektsammlung entworfen, die als Apartment bezeichnet wird. Ein Apartment ist eine Sammlung von Kontexten, die in einem Prozess enthalten sind.
ms.assetid: c73fb4c5-20ae-4873-afd2-4f40eb47bade
title: Com+-Threading Modelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f07b065861c042e68add633368a9c8b8ba41b2
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "103761115"
---
# <a name="com-threading-models"></a><span data-ttu-id="01ea8-104">Com+-Threading Modelle</span><span class="sxs-lookup"><span data-stu-id="01ea8-104">COM+ Threading Models</span></span>

<span data-ttu-id="01ea8-105">Com+-Threading Modelle werden um eine Objektsammlung entworfen, die als Apartment bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="01ea8-105">COM+ threading models are designed around an object collection called an apartment.</span></span> <span data-ttu-id="01ea8-106">Ein Apartment ist eine Auflistung von Kontexten, die in einem Prozess enthalten sind, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="01ea8-106">An apartment is a collection of contexts contained in a process, as shown in the following illustration.</span></span>

![Diagramm, das eine Auflistung von Kontexten in einer Aktivität in einem Apartment innerhalb eines Prozesses anzeigt.](images/6b86fe3b-262a-483a-a418-67d60f9a5d68.png)

<span data-ttu-id="01ea8-108">Aufrufe innerhalb eines Apartment sind direkt, während Aufrufe über mehrere Apartments hinweg (Prozess übergreifend) indirekt sind und Proxy-und Stub-Code erfordern.</span><span class="sxs-lookup"><span data-stu-id="01ea8-108">Calls within an apartment are direct, while calls across apartments (out-of-process) are indirect and require proxy and stub code.</span></span> <span data-ttu-id="01ea8-109">Apartments lassen Objekte mit unterschiedlichen Synchronisierungs-und Eintritts Eigenschaften zu und haben zwei Kategorien: Single Thread und Multithreaded.</span><span class="sxs-lookup"><span data-stu-id="01ea8-109">Apartments allow for objects with different synchronization and reentrancy properties and have two categories: single-threaded and multithreaded.</span></span> <span data-ttu-id="01ea8-110">Objekte in einem Single Thread-Apartment (STA) werden auf dem jeweiligen Thread ausgeführt, in dem Sie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="01ea8-110">Objects in a single-threaded apartment (STA) execute on the particular thread in which they were created.</span></span> <span data-ttu-id="01ea8-111">Mit Stas kann jeweils nur eine Methode gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="01ea8-111">STAs allow only one method to execute at a time.</span></span> <span data-ttu-id="01ea8-112">Sie sind auf Benutzeroberflächen ausgelegt und verlassen sich auf die Microsoft Windows-Nachrichten Warteschlange, um eingehende Aufrufe zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="01ea8-112">They are designed for user interfaces and rely on the Microsoft Windows message queue to process incoming calls.</span></span>

<span data-ttu-id="01ea8-113">Objekte in einem Multithread-Apartment (MTA) werden in einem beliebigen Thread ausgeführt, sodass eine beliebige Anzahl von Methoden gleichzeitig erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="01ea8-113">Objects in a multithreaded apartment (MTA) execute on any thread and allow any number of methods to occur simultaneously.</span></span> <span data-ttu-id="01ea8-114">MTAs unterstützen implizit den erneuten Zutritt.</span><span class="sxs-lookup"><span data-stu-id="01ea8-114">MTAs support reentrance implicitly.</span></span>

<span data-ttu-id="01ea8-115">Com+-Klassen sind mit einer **ThreadingModel** -Eigenschaft gekennzeichnet, mit der com+ das Objekt im richtigen Apartment erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="01ea8-115">COM+ classes are marked with a **ThreadingModel** property that allows COM+ to create the object in the proper apartment.</span></span> <span data-ttu-id="01ea8-116">Um zu ermitteln, in welchem Apartment ein Objekt erstellt wird, verwendet [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) die **ThreadingModel** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="01ea8-116">To determine which apartment an object is created in, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) uses the **ThreadingModel** property.</span></span>

<span data-ttu-id="01ea8-117">Threads müssen [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) aufrufen, bevor Sie com+ verwenden können.</span><span class="sxs-lookup"><span data-stu-id="01ea8-117">Threads must call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) before they can use COM+.</span></span> <span data-ttu-id="01ea8-118">Dadurch werden Sie im richtigen Apartment und Kontext erstellt.</span><span class="sxs-lookup"><span data-stu-id="01ea8-118">This creates them inside the correct apartment and context.</span></span> <span data-ttu-id="01ea8-119">Das Haupt Thread Apartment wird als erster von **CoInitializeEx** aufgerufener STA festgelegt.</span><span class="sxs-lookup"><span data-stu-id="01ea8-119">The main thread apartment is determined to be the first STA called by **CoInitializeEx**.</span></span> <span data-ttu-id="01ea8-120">Dies ist normalerweise dem Haupt Thread eines Prozesses zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="01ea8-120">This is usually associated with the main thread of a process.</span></span> <span data-ttu-id="01ea8-121">**CoInitializeEx** gibt den Typ des Apartment an, das für den Thread erforderlich ist, indem die folgenden Flags festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="01ea8-121">**CoInitializeEx** indicates the type of apartment required by the thread by setting the following flags:</span></span>

-   <span data-ttu-id="01ea8-122">**Coinit \_ Multithread**– der Thread wird im einzelnen Multithread-Apartment lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="01ea8-122">**COINIT\_MULTITHREADED**—Locates the thread in the single multithreaded apartment.</span></span>
-   <span data-ttu-id="01ea8-123">**Coinit \_ Apartmentthreaded**– platziert den Thread in einem neuen Sta.</span><span class="sxs-lookup"><span data-stu-id="01ea8-123">**COINIT\_APARTMENTTHREADED**—Places the thread into a new STA.</span></span>

<span data-ttu-id="01ea8-124">Die folgenden Themen in diesem Abschnitt enthalten weitere Informationen zur Verwendung von Threading Modellen und-Apartments in com+:</span><span class="sxs-lookup"><span data-stu-id="01ea8-124">The following topics in this section provide more information about using threading models and apartments in COM+:</span></span>

-   [<span data-ttu-id="01ea8-125">Threading Modell-Attribut</span><span class="sxs-lookup"><span data-stu-id="01ea8-125">Threading Model Attribute</span></span>](threading-model-attribute.md)
-   [<span data-ttu-id="01ea8-126">Neutrale Apartments</span><span class="sxs-lookup"><span data-stu-id="01ea8-126">Neutral Apartments</span></span>](neutral-apartments.md)

## <a name="related-topics"></a><span data-ttu-id="01ea8-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="01ea8-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01ea8-128">Prozesse, Threads und Apartments</span><span class="sxs-lookup"><span data-stu-id="01ea8-128">Processes, Threads, and Apartments</span></span>](/windows/desktop/com/processes--threads--and-apartments)
</dt> <dt>

[<span data-ttu-id="01ea8-129">**Threading Model**</span><span class="sxs-lookup"><span data-stu-id="01ea8-129">**ThreadingModel**</span></span>](components.md)
</dt> </dl>

 

 
