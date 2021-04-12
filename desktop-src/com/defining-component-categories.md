---
title: Definieren von Komponenten Kategorien
description: Definieren von Komponenten Kategorien
ms.assetid: 2d67a998-5200-4285-bd99-48cf59683569
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4609654827789949705a2f32803c154152d3f9c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207438"
---
# <a name="defining-component-categories"></a><span data-ttu-id="2bf3d-103">Definieren von Komponenten Kategorien</span><span class="sxs-lookup"><span data-stu-id="2bf3d-103">Defining Component Categories</span></span>

<span data-ttu-id="2bf3d-104">Der Autor einer Komponenten Kategoriedefinition erstellt eine eindeutige GUID (die CATID), die zusammen mit der Definition veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="2bf3d-104">The author of a component category definition creates a unique GUID (the CATID) that is published along with the definition.</span></span> <span data-ttu-id="2bf3d-105">Andere Parteien kennen die Definition dieses Typs und können die unterstützten Klassen entsprechend verwenden.</span><span class="sxs-lookup"><span data-stu-id="2bf3d-105">Other parties know the definition of this type and can make use of its supported classes accordingly.</span></span> <span data-ttu-id="2bf3d-106">Wie die Methoden Signatur einer Schnittstelle sollte die Semantik einer Kategorie nach der Installation nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2bf3d-106">Like the method signature of an interface, a category's semantics should not be modified after being installed.</span></span> <span data-ttu-id="2bf3d-107">Es ist besser, die Abwärtskompatibilität der Kategorie zu gewährleisten, indem Sie einen neuen Kategoriebezeichner mit überarbeiteten Semantik einführen.</span><span class="sxs-lookup"><span data-stu-id="2bf3d-107">It is better to maintain backward compatibility of the category by introducing a new category identifier with revised semantics.</span></span>

<span data-ttu-id="2bf3d-108">Da Schnittstellen Bezeichner (IID) und komponentenkategoriebezeichner (CATID) in unterschiedlichen Namespaces vorhanden sind, scheint es so, als ob es möglich wäre, dieselbe GUID für eine IID und eine CATID zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2bf3d-108">Because interface identifiers (IID) and component category identifiers (CATID) exist in different namespaces, it seems as if it would be possible to use the same GUID for both an IID and a CATID.</span></span> <span data-ttu-id="2bf3d-109">Da IIDs jedoch häufig für die CLSID des Proxy-/stubservers der Schnittstelle verwendet werden, besteht ein Konfliktpotenzial.</span><span class="sxs-lookup"><span data-stu-id="2bf3d-109">However, since IIDs are often used for the CLSID of the interface's proxy/stub server, there is the potential for conflict.</span></span> <span data-ttu-id="2bf3d-110">Verwenden Sie daher nicht dieselbe GUID für eine IID und eine CATID.</span><span class="sxs-lookup"><span data-stu-id="2bf3d-110">Therefore, do not use the same GUID for an IID and CATID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bf3d-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2bf3d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bf3d-112">Zuordnen von Symbolen zu einer Kategorie</span><span class="sxs-lookup"><span data-stu-id="2bf3d-112">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="2bf3d-113">Kategorisierung nach Komponenten Funktionen</span><span class="sxs-lookup"><span data-stu-id="2bf3d-113">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="2bf3d-114">Kategorisierung nach Container Funktionen</span><span class="sxs-lookup"><span data-stu-id="2bf3d-114">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="2bf3d-115">Standardklassen und-Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="2bf3d-115">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="2bf3d-116">Der Komponenten Kategorien-Manager</span><span class="sxs-lookup"><span data-stu-id="2bf3d-116">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




