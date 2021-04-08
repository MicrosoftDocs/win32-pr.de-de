---
title: Klassifizierender Komponenten
description: Klassifizierender Komponenten
ms.assetid: 4d805532-96c9-400d-b78a-f8d0d9bdbf83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ea1547c219a44262fdeaf7edb02f65c7a3aac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856616"
---
# <a name="classifying-components"></a><span data-ttu-id="ccc05-103">Klassifizierender Komponenten</span><span class="sxs-lookup"><span data-stu-id="ccc05-103">Classifying Components</span></span>

<span data-ttu-id="ccc05-104">Während ein Client die Liste der CLSIDs in der Registrierung durchsuchen und eine zu verwendende Komponente auswählen kann, ist das Laden der einzelnen Komponenten in der Registrierung und das Abfragen für die unterstützten Schnittstellen sehr zeitaufwändig.</span><span class="sxs-lookup"><span data-stu-id="ccc05-104">While a client is able to browse through the list of CLSIDs in the registry and select a component to use, loading each component in the registry and querying it for its supported interfaces is very time-consuming.</span></span> <span data-ttu-id="ccc05-105">Um zu bestimmen, ob eine Komponente die erforderlichen Schnittstellen vor dem Erstellen einer Instanz der Komponente unterstützt, wurde eine Methode zum Klassifizieren von Komponenten in Kategorien entwickelt.</span><span class="sxs-lookup"><span data-stu-id="ccc05-105">To determine whether a component supports the interfaces required before creating an instance of the component, a method to classify components into categories was developed.</span></span>

<span data-ttu-id="ccc05-106">Eine Komponenten Kategorie ist ein Satz von Schnittstellen, denen eine Guid namens CATID zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="ccc05-106">A component category is a set of interfaces that have been assigned a GUID named CATID.</span></span> <span data-ttu-id="ccc05-107">Komponenten, die alle Schnittstellen in einer Komponenten Kategorie implementieren, registrieren sich selbst als Mitglieder dieser Komponenten Kategorie.</span><span class="sxs-lookup"><span data-stu-id="ccc05-107">Components that implement all of the interfaces in a component category register themselves as members of that component category.</span></span> <span data-ttu-id="ccc05-108">Komponenten, die zu einer bestimmten Komponenten Kategorie gehören, können dann aus der Registrierung ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="ccc05-108">Components that belong to a certain component category can then be selected from the registry.</span></span> <span data-ttu-id="ccc05-109">Wenn Sie sich selbst als Mitglied einer Komponenten Kategorie registrieren, gewährleistet die Komponente, dass Sie alle Member-Schnittstellen in der Komponenten Kategorie unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ccc05-109">By registering itself as a member of a component category, the component is guaranteeing that it supports all of the member interfaces in the component category.</span></span>

<span data-ttu-id="ccc05-110">Eine Komponente kann Mitglied vieler Kategorien sein.</span><span class="sxs-lookup"><span data-stu-id="ccc05-110">A component can be a member of many categories.</span></span> <span data-ttu-id="ccc05-111">Es ist nicht auf die Unterstützung von Schnittstellen in einer Komponenten Kategorie beschränkt.</span><span class="sxs-lookup"><span data-stu-id="ccc05-111">It is not limited to supporting interfaces in a component category.</span></span> <span data-ttu-id="ccc05-112">Zusätzlich zu den Komponenten in einer Komponenten Kategorie kann Sie beliebige Schnittstellen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ccc05-112">It can support any interface, in addition to those in a component category.</span></span>

<span data-ttu-id="ccc05-113">Im Gegensatz zur Standard Registrierung von-Komponenten, bei denen Entwickler Code schreiben müssen, mit dem-Objekte manuell registriert werden, werden in Komponenten Kategorien viele dieser Aufgaben automatisiert.</span><span class="sxs-lookup"><span data-stu-id="ccc05-113">In contrast to the standard registration of components, in which developers must write code that manually registers objects, component categories automates much of this work.</span></span> <span data-ttu-id="ccc05-114">Die sechs Methoden der [**itorregister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) -Schnittstelle definieren Komponenten Kategorien und registrieren Objekte, die Sie implementieren oder erfordern.</span><span class="sxs-lookup"><span data-stu-id="ccc05-114">The six methods of the [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) interface define component categories and register objects that implement or require them.</span></span> <span data-ttu-id="ccc05-115">Das [Komponenten Kategorien-Manager](the-component-categories-manager.md) -Objekt implementiert diese Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ccc05-115">The [Component Categories Manager](the-component-categories-manager.md) object implements this interface.</span></span> <span data-ttu-id="ccc05-116">Weitere Informationen zur Verwendung von Komponenten Kategorien finden Sie unter **i-Register** und [**ikatinformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) .</span><span class="sxs-lookup"><span data-stu-id="ccc05-116">See **ICatRegister** and [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) for additional information on using component categories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccc05-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ccc05-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccc05-118">Registrieren von com-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ccc05-118">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 




