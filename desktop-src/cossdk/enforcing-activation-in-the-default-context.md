---
description: Eine konfigurierte COM-Komponente wird normalerweise in einem eigenen Kontext aktiviert; Das heißt, com+ verweist auf die Komponenten Katalog Informationen, um konfigurierte Dienste bereitzustellen.
ms.assetid: 09dc7165-22b1-4eca-9591-d83e85556f3f
title: Erzwingen der Aktivierung im Standardkontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41599f71dc37c37c1a9a574d274ca2858835e2df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524363"
---
# <a name="enforcing-activation-in-the-default-context"></a><span data-ttu-id="5dcae-103">Erzwingen der Aktivierung im Standardkontext</span><span class="sxs-lookup"><span data-stu-id="5dcae-103">Enforcing Activation in the Default Context</span></span>

<span data-ttu-id="5dcae-104">Eine konfigurierte COM-Komponente wird normalerweise in einem eigenen Kontext aktiviert; Das heißt, com+ verweist auf die Katalog Informationen der Komponente, um konfigurierte Dienste bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5dcae-104">A configured COM component is usually activated in its own context; that is, COM+ references the component's catalog information to provide any configured services.</span></span> <span data-ttu-id="5dcae-105">Sie können jedoch festlegen, dass eine konfigurierte Komponente im Standardkontext aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5dcae-105">However, you can choose to activate a configured component in the default context.</span></span> <span data-ttu-id="5dcae-106">Eine Basis-COM-Komponente – eine registrierte Komponente ohne com+-Katalog Informationen – wird normalerweise im Standardkontext aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5dcae-106">A base COM component—a registered component that has no COM+ catalog information—is usually activated in the default context.</span></span>

<span data-ttu-id="5dcae-107">Das Aktivieren einer COM-Komponente im Standardkontext bietet wie folgt drei wichtige Leistungsvorteile:</span><span class="sxs-lookup"><span data-stu-id="5dcae-107">Activating a COM component in the default context provides three major performance benefits, as follows:</span></span>

-   <span data-ttu-id="5dcae-108">Sie speichern Systemressourcen, indem Sie die Anzahl der erstellten Kontexte begrenzen.</span><span class="sxs-lookup"><span data-stu-id="5dcae-108">You save system resources by limiting the number of contexts that are created.</span></span>
-   <span data-ttu-id="5dcae-109">Sie erhöhen die Leistung, indem Sie die Anzahl von Kontext übergreifenden aufrufen einschränken.</span><span class="sxs-lookup"><span data-stu-id="5dcae-109">You increase performance by limiting the number of cross-context calls.</span></span> <span data-ttu-id="5dcae-110">Da Aufrufe zwischen Kontexten Marshalling erfordern, ist es für ein COM-Objekt, das im Standardkontext aktiviert ist, viel schneller, Aufrufe an andere Objekte im Standardkontext vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="5dcae-110">Because calls across contexts require marshaling, it is much faster for a COM object activated in the default context to make calls to other objects in the default context.</span></span> <span data-ttu-id="5dcae-111">Die Leistung in diesem Fall (von aufrufen innerhalb desselben Kontexts) ähnelt der des Aufrufs einer Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="5dcae-111">The performance in this case (of calls within the same context) is similar to that of calling a subroutine.</span></span>
-   <span data-ttu-id="5dcae-112">Ältere COM-Anwendungen können in com+ importiert und ohne Probleme ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5dcae-112">You can import older COM applications into COM+ and run them without a problem.</span></span> <span data-ttu-id="5dcae-113">Beispielsweise können mehrere ältere COM-Anwendungen unter der Annahme implementiert werden, dass es zulässig ist, Objekt Verweise innerhalb eines Apartment zu übergeben, ohne dass die Verweise gemarshallt werden.</span><span class="sxs-lookup"><span data-stu-id="5dcae-113">For example, you may have several older COM applications implemented under the assumption that it was allowable to pass object references within an apartment without marshaling the references.</span></span> <span data-ttu-id="5dcae-114">Diese com-Anwendungen funktionieren nicht, wenn Sie in com+ importiert werden, da die Objekt Verweise über Kontext Grenzen hinweg übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="5dcae-114">These COM applications do not work when imported into COM+ because the object references are passed across context boundaries.</span></span> <span data-ttu-id="5dcae-115">Sie können diese Art von COM-Anwendung jedoch beim Importieren ausführen, wenn Sie das Verwaltungs Programmkomponenten Dienste verwenden, um alle Klassen in der Anwendung zu markieren, die **im Standardkontext aktiviert werden müssen**.</span><span class="sxs-lookup"><span data-stu-id="5dcae-115">However, you can make this type of COM application run when imported if you use the Component Services administrative tool to mark all the classes in the application as **Must be activated in the default context**.</span></span>

<span data-ttu-id="5dcae-116">Der größte Nachteil beim Aktivieren einer konfigurierten Komponente im Standardkontext ist, dass com+ keinen der konfigurierten Dienste der Komponente bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="5dcae-116">The major disadvantage to activating a configured component in the default context is that COM+ does not provide any of the component's configured services.</span></span> <span data-ttu-id="5dcae-117">Es gibt einen Kompromiss zwischen verbesserter Leistung und der Möglichkeit, com+-Dienste zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5dcae-117">There is a trade-off between enhanced performance and the ability to use COM+ services.</span></span>

<span data-ttu-id="5dcae-118">Nehmen Sie beispielsweise an, dass für eine COM-Komponente keine COM+-Dienste erforderlich sind (z. b. [Transaktionen](com--transactions.md), [Just-in-Time-Aktivierung](com--just-in-time-activation.md), [Ereignisse](com--events.md), in der [Warteschlange befindliche Komponenten](com--queued-components.md), [Synchronisierung](com--synchronization.md)oder [Objekt Pooling](com--object-pooling.md)) und dass die Komponente eine Reihe von Aufrufen an andere COM-Komponenten ausführt, die möglicherweise im Standardkontext aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="5dcae-118">For example, assume that a COM component does not require any COM+ services (such as [Transactions](com--transactions.md), [Just-in-Time Activation](com--just-in-time-activation.md), [Events](com--events.md), [Queued Components](com--queued-components.md), [Synchronization](com--synchronization.md), or [Object Pooling](com--object-pooling.md)) and that the component makes a number of calls to other COM components that may be activated in the default context.</span></span> <span data-ttu-id="5dcae-119">In diesem Fall empfiehlt es sich, die aufrufende Komponente im Standardkontext zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5dcae-119">In this case, it would be a good idea to activate the calling component in the default context.</span></span>

<span data-ttu-id="5dcae-120">Wenn für die COM-Komponente com+-Dienste erforderlich sind, kann Sie nicht als markiert werden, da Sie **im Standardkontext aktiviert werden muss**.</span><span class="sxs-lookup"><span data-stu-id="5dcae-120">If the COM component requires COM+ services, it cannot be marked as **Must be activated in the default context**.</span></span> <span data-ttu-id="5dcae-121">Außerdem gibt es keine wirkliche Leistungssteigerung, wenn ein im Standardkontext aktiviertes com-Objekt eine Reihe von Aufrufen an Objekte in anderen Kontexten ausführt.</span><span class="sxs-lookup"><span data-stu-id="5dcae-121">In addition, there is no real performance gain if a COM object activated in the default context makes a number of calls to objects in other contexts.</span></span> <span data-ttu-id="5dcae-122">(Ausführlichere Informationen finden Sie unter [Kontexte](com--contexts.md).)</span><span class="sxs-lookup"><span data-stu-id="5dcae-122">(For more detail, see [Contexts](com--contexts.md).)</span></span>

<span data-ttu-id="5dcae-123">**So erzwingen Sie die Aktivierung im Standardkontext**</span><span class="sxs-lookup"><span data-stu-id="5dcae-123">**To enforce activation in the default context**</span></span>

1.  <span data-ttu-id="5dcae-124">Klicken Sie im Detailbereich des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die Komponente (befindet sich im Ordner **Komponenten** der ausgewählten COM+-Anwendung), die Sie im Standardkontext aktivieren möchten, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="5dcae-124">In the details pane of the Component Services administrative tool, right-click the component (located within the **Components** folder of any selected COM+ application) that you want to activate in the default context and then click **Properties**.</span></span>

2.  <span data-ttu-id="5dcae-125">Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Aktivierung** .</span><span class="sxs-lookup"><span data-stu-id="5dcae-125">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="5dcae-126">Aktivieren Sie das Kontrollkästchen **muss im Standardkontext aktiviert werden**.</span><span class="sxs-lookup"><span data-stu-id="5dcae-126">Select the **Must be activated in the default context** check box.</span></span>

4.  <span data-ttu-id="5dcae-127">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="5dcae-127">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="5dcae-128">Wenn Sie eine konfigurierte Komponente im Standardkontext ausführen, aktiviert com+ keinen der konfigurierten Dienste für diese Komponente.</span><span class="sxs-lookup"><span data-stu-id="5dcae-128">When you run a configured component in the default context, COM+ does not activate any of the configured services for that component.</span></span> <span data-ttu-id="5dcae-129">Diese Dienste sind erneut verfügbar, wenn Sie das Kontrollkästchen **muss im Standardkontext aktiviert werden aktiviert** deaktivieren und anschließend die konfigurierte Komponente in einem eigenen Kontext ausführen.</span><span class="sxs-lookup"><span data-stu-id="5dcae-129">These services are available again when you uncheck the **Must be activated in the default context** check box and subsequently run the configured component in its own context.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5dcae-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5dcae-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dcae-131">Konzepte für die Just-in-Time-Aktivierung in com+</span><span class="sxs-lookup"><span data-stu-id="5dcae-131">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="5dcae-132">Erzwingen der Aktivierung im Kontext des Aufrufers</span><span class="sxs-lookup"><span data-stu-id="5dcae-132">Enforcing Activation in the Caller's Context</span></span>](enforcing-activation-in-the-caller-s-context.md)
</dt> </dl>

 

 



