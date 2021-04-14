---
description: Registrieren und Aktivieren von Komponenten in Partitionen
ms.assetid: 2cca71da-c7f7-4997-b63a-74ba266e9e95
title: Registrieren und Aktivieren von Komponenten in Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31790bc9a3df12d961a4b16271937ae22f963c38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523531"
---
# <a name="registering-and-activating-components-in-partitions"></a><span data-ttu-id="2ab1f-103">Registrieren und Aktivieren von Komponenten in Partitionen</span><span class="sxs-lookup"><span data-stu-id="2ab1f-103">Registering and Activating Components in Partitions</span></span>

<span data-ttu-id="2ab1f-104">Nachdem eine Partition erstellt wurde, ist der nächste Schritt das Registrieren der COM+-Komponenten innerhalb dieser Partition.</span><span class="sxs-lookup"><span data-stu-id="2ab1f-104">After a partition has been created, the next step is register your COM+ components within that partition.</span></span> <span data-ttu-id="2ab1f-105">Eine Komponente wird in einer Partition registriert, wenn eine neue COM+-Anwendung erstellt wird oder wenn eine vorhandene COM+-Anwendung in der Partition installiert wird.</span><span class="sxs-lookup"><span data-stu-id="2ab1f-105">A component is registered within a partition when a new COM+ application is created or when an existing COM+ application is installed into the partition.</span></span> <span data-ttu-id="2ab1f-106">Um die Verwaltung der Registrierung zu vereinfachen, wenn mehrere Partitionen die gleichen com+-Komponenten enthalten, ermöglicht der Partitions Dienst einem Administrator, Anwendungen oder Komponenten aus einer Partition in eine andere zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="2ab1f-106">To ease the administration of registration when multiple partitions contain the same COM+ components, the partitions service allows an administrator to copy applications or components from one partition into another.</span></span> <span data-ttu-id="2ab1f-107">Wenn eine COM+-Anwendung oder eine Komponente kopiert wird, werden alle zugeordneten Partitions Eigenschaften mit dem Element kopiert, mit Ausnahme der Identität der Anwendung oder der Mitglieder einer Rolle.</span><span class="sxs-lookup"><span data-stu-id="2ab1f-107">When a COM+ application or a component is copied, all associated partition properties are copied with it, except the application's identity or any of the members of a role.</span></span>

<span data-ttu-id="2ab1f-108">Wenn das Client Programm die Funktion [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) oder [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) aufruft, um ein Objekt zu instanziieren, führt com+ wie folgt zwei unterschiedliche Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="2ab1f-108">When the client program calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) function to instantiate an object, COM+ performs two distinct steps, as follows:</span></span>

1.  <span data-ttu-id="2ab1f-109">Lokalisiert die Partition, in der sich die Komponente befindet.</span><span class="sxs-lookup"><span data-stu-id="2ab1f-109">Locates the partition in which the component resides</span></span>
2.  <span data-ttu-id="2ab1f-110">Gibt die richtige Komponente innerhalb dieser Partition an.</span><span class="sxs-lookup"><span data-stu-id="2ab1f-110">Locates the correct component within that partition</span></span>

<span data-ttu-id="2ab1f-111">In den folgenden Themen dieses Abschnitts werden diese Schritte ausführlich beschrieben:</span><span class="sxs-lookup"><span data-stu-id="2ab1f-111">The following topics in this section describe these steps in detail:</span></span>

-   [<span data-ttu-id="2ab1f-112">Suchen von Partitionen während der Aktivierung</span><span class="sxs-lookup"><span data-stu-id="2ab1f-112">Locating Partitions During Activation</span></span>](locating-partitions-during-activation.md)
-   [<span data-ttu-id="2ab1f-113">Suchen einer Komponente zur Aktivierung</span><span class="sxs-lookup"><span data-stu-id="2ab1f-113">Locating a Component for Activation</span></span>](locating-a-component-for-activation.md)

## <a name="related-topics"></a><span data-ttu-id="2ab1f-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2ab1f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ab1f-115">Einschränkungen beim Anwendungs Entwurf</span><span class="sxs-lookup"><span data-stu-id="2ab1f-115">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="2ab1f-116">Komponenten und Partitionen in der com+-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="2ab1f-116">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="2ab1f-117">Partitions Implementierung</span><span class="sxs-lookup"><span data-stu-id="2ab1f-117">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="2ab1f-118">Was sind COM+-Partitionen?</span><span class="sxs-lookup"><span data-stu-id="2ab1f-118">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 
