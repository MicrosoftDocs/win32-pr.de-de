---
description: Nachdem die konzeptionellen und logischen Modelle fertiggestellt wurden, können Sie Entscheidungen über die physische Implementierung der Anwendung treffen.
ms.assetid: 18c440f0-88c8-4738-9f29-c82772439b51
title: 'Das physische Modell: Anwendungsarchitektur'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0fab87d76e445a365958ab330f572f657d1505
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127541"
---
# <a name="the-physical-model-application-architecture"></a><span data-ttu-id="556a1-103">Das physische Modell: Anwendungsarchitektur</span><span class="sxs-lookup"><span data-stu-id="556a1-103">The Physical Model: Application Architecture</span></span>

<span data-ttu-id="556a1-104">Nachdem die konzeptionellen und logischen Modelle fertiggestellt wurden, können Sie Entscheidungen über die physische Implementierung der Anwendung treffen.</span><span class="sxs-lookup"><span data-stu-id="556a1-104">After the conceptual and logical models are complete, you can make decisions on the physical implementation of the application.</span></span> <span data-ttu-id="556a1-105">Um das physische Modell zu erstellen, müssen Sie wissen, wo sich die verschiedenen Dienste der Anwendung befinden sollten und wie Sie implementiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="556a1-105">To create the physical model, you must understand where the various services of the application should be located and how they should be implemented.</span></span> <span data-ttu-id="556a1-106">Zu bestimmen, wo sich verschiedene Dienste befinden, sollte vor der Implementierung der Dienste stehen.</span><span class="sxs-lookup"><span data-stu-id="556a1-106">Determining where various services reside should come before how the services will be implemented.</span></span>

<span data-ttu-id="556a1-107">Eine grundlegende Regel, die festlegt, wo sich verschiedene Dienste befinden, ist Folgendes: Platzieren Sie die Komponente, in der Sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="556a1-107">One basic rule for determining where various services reside is this: Put the component where it is being used.</span></span> <span data-ttu-id="556a1-108">Wenn z. b. eine Komponente Informationen für den Basis Client anzeigt, muss Sie auf dem Computer des Benutzers angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="556a1-108">If, for example, a component displays information for the base client, it should go on the user's computer.</span></span> <span data-ttu-id="556a1-109">Wenn eine Komponente Informationen vom Basis Client überprüft, sollte Sie sich auch auf dem Computer des Basis Clients befinden.</span><span class="sxs-lookup"><span data-stu-id="556a1-109">If a component validates information from the base client, it should also reside on the base client's computer.</span></span> <span data-ttu-id="556a1-110">Wenn eine Komponente Informationen in einer-Datenbank aktualisiert, sollte Sie sich auf dem Datenbankserver befinden.</span><span class="sxs-lookup"><span data-stu-id="556a1-110">If a component updates information in a database, it should reside on the database server.</span></span>

<span data-ttu-id="556a1-111">Es gibt natürlich weitere Überlegungen, die Ausnahmen zu dieser Regel machen.</span><span class="sxs-lookup"><span data-stu-id="556a1-111">There are, of course, additional considerations that make exceptions to this rule.</span></span> <span data-ttu-id="556a1-112">Leistungs-und Sicherheitsprobleme können auch vorschreiben, wo sich eine Komponente befindet.</span><span class="sxs-lookup"><span data-stu-id="556a1-112">Performance and security issues can also dictate where a component is located.</span></span> <span data-ttu-id="556a1-113">Beachten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="556a1-113">Consider the following:</span></span>

-   <span data-ttu-id="556a1-114">Wird eine Komponente häufig geändert, sodass die Verteilung von Updates erschwert wird?</span><span class="sxs-lookup"><span data-stu-id="556a1-114">Is a component going to change frequently, making distributing updates difficult?</span></span>
-   <span data-ttu-id="556a1-115">Wird die Komponente von anderen Anwendungen, z. b. einer allgemeinen Sicherheits Überprüfungs Komponente, verwendet?</span><span class="sxs-lookup"><span data-stu-id="556a1-115">Will the component be used by other applications, such as a common security verification component?</span></span>
-   <span data-ttu-id="556a1-116">Nimmt die Komponente lange Berechnungen vor oder führt Funktionen wie z. b. Drucken aus, die auf einen Server ausgelagert werden können?</span><span class="sxs-lookup"><span data-stu-id="556a1-116">Does the component make lengthy calculations or performs functions, such as printing, that can be offloaded to a server?</span></span>
-   <span data-ttu-id="556a1-117">Kann die Sicherheit einer Komponente durch die Platzierung auf einem Server verbessert werden?</span><span class="sxs-lookup"><span data-stu-id="556a1-117">Can the security of a component be enhanced by placing it on a server?</span></span>

<span data-ttu-id="556a1-118">Wenn Sie die Komponenten einer Anwendung ordnungsgemäß suchen, können Sie das Entwicklungsteam auch vor kostspieligen neuzustellungen isolieren, wenn sich das System oder der Speicherort der Daten ändert.</span><span class="sxs-lookup"><span data-stu-id="556a1-118">Properly locating components of an application can also insulate the development team from costly recoding if the system or the location of the data changes.</span></span> <span data-ttu-id="556a1-119">Wenn Sie z. b. die Datenzugriffs Regeln in einer Datenschicht anstatt in gespeicherten Prozeduren platzieren, kann die Anwendung leichter von der Abhängigkeit von einem bestimmten DBMS isoliert werden.</span><span class="sxs-lookup"><span data-stu-id="556a1-119">For example, by putting the data access rules in a data layer rather than in stored procedures, the application is more easily insulated from dependence on a specific DBMS.</span></span> <span data-ttu-id="556a1-120">Nicht nur die Änderungen sind eingeschränkt, und die Tests werden getrennt, aber Datenquellen können geändert werden, und Daten können verteilt werden, ohne dass die Anwendung grundsätzlich geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="556a1-120">Not only are changes confined and testing compartmentalized, but data sources can be changed and data can be distributed without fundamentally changing the application.</span></span>

<span data-ttu-id="556a1-121">Zum Schluss sollte das Auffinden von Komponenten die Effizienz des Systems ausnutzen.</span><span class="sxs-lookup"><span data-stu-id="556a1-121">Finally, locating components should take advantage of system efficiencies.</span></span> <span data-ttu-id="556a1-122">Es ist Zeit und kostengünstig, Geschäftsobjekte an zentralen Orten im Netzwerk zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="556a1-122">It is time and cost-effective to place business objects in centralized locations on the network.</span></span> <span data-ttu-id="556a1-123">-Objekte können von-Anwendungen gemeinsam genutzt werden. Komponententests können vor der Bereitstellung von Komponenten ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="556a1-123">Objects can be shared among applications, and unit testing can be done before any components are deployed.</span></span> <span data-ttu-id="556a1-124">Wartungskosten können auch verringert werden, da Regeländerungen nur an einem einzigen Punkt erfolgen.</span><span class="sxs-lookup"><span data-stu-id="556a1-124">Maintenance costs can also be decreased because rule changes occur only at a single point.</span></span>

## <a name="related-topics"></a><span data-ttu-id="556a1-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="556a1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="556a1-126">Das konzeptionelle Modell: Anwendungsanforderungen</span><span class="sxs-lookup"><span data-stu-id="556a1-126">The Conceptual Model: Application Requirements</span></span>](the-conceptual-model--application-requirements.md)
</dt> <dt>

[<span data-ttu-id="556a1-127">Das logische Modell: Anwendungs Definition und-Planung</span><span class="sxs-lookup"><span data-stu-id="556a1-127">The Logical Model: Application Definition and Planning</span></span>](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



