---
title: Auflisten von Container Objekten
description: Gemäß der Konvention müssen alle Elemente in einer Enumeration in ADSI denselben Automatisierungs Datentyp aufweisen. Beispielsweise sollte eine Enumeration einige Elemente nicht als Variante vom Typ VT \_ I4 und andere als Variante des Typs VT BSTR zurückgeben \_ .
ms.assetid: 155caa67-05db-432b-b813-0d891a502301
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5514596b02521fa869ffd7c712dcac2cacb40192
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341215"
---
# <a name="enumerating-container-objects"></a><span data-ttu-id="ec5fc-104">Auflisten von Container Objekten</span><span class="sxs-lookup"><span data-stu-id="ec5fc-104">Enumerating Container Objects</span></span>

<span data-ttu-id="ec5fc-105">Gemäß der Konvention müssen alle Elemente in einer Enumeration in ADSI denselben Automatisierungs Datentyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ec5fc-105">By convention, all items in an enumeration in ADSI must be of the same Automation data type.</span></span> <span data-ttu-id="ec5fc-106">Beispielsweise sollte eine Enumeration einige Elemente nicht als **Variante** vom Typ **VT \_ I4** und andere als **Variante** des Typs **VT \_ BSTR** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ec5fc-106">For example, an enumeration should not return some items as a **VARIANT** of type **VT\_I4** and others as a **VARIANT** of type **VT\_BSTR**.</span></span>

<span data-ttu-id="ec5fc-107">Zum Auflisten einer Liste von Elementen, die von einem Objekt verwaltet werden, fordert ein Client die Erstellung eines Enumerationsobjekt für den bestimmten Typ der aufgelisteten Informationen an.</span><span class="sxs-lookup"><span data-stu-id="ec5fc-107">To enumerate a list of items that an object maintains, a client requests the creation of an enumeration object for the specific type of information being listed.</span></span> <span data-ttu-id="ec5fc-108">In ADSI kann der Client die Objekte in Namespace Objekten, generischen Container Objekten, Auflistungs Objekten, Element Objekten oder Schema Objekten auflisten.</span><span class="sxs-lookup"><span data-stu-id="ec5fc-108">In ADSI, the client may list the objects in namespace objects, generic container objects, collection objects, member objects, or schema objects.</span></span> <span data-ttu-id="ec5fc-109">ADSI stellt einen Filter bereit, der festgelegt und geändert werden kann, um die Übereinstimmungen in einer Enumeration mit der [**IADsContainer. Filter**](iadscontainer-property-methods.md) -Eigenschaft einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="ec5fc-109">ADSI provides a filter that can be set and modified to limit the matches in any enumeration though the [**IADsContainer.Filter**](iadscontainer-property-methods.md) property.</span></span> <span data-ttu-id="ec5fc-110">Beispiele für Implementierungen von enumeratorobjekten finden Sie im Beispiel Anbieter-Komponenten Code für die folgenden ADS-Containerobjekte.</span><span class="sxs-lookup"><span data-stu-id="ec5fc-110">Examples of implementations of enumerator objects can be found in the example provider component code for the following ADs container objects.</span></span>



| <span data-ttu-id="ec5fc-111">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="ec5fc-111">Object type</span></span>         | <span data-ttu-id="ec5fc-112">code</span><span class="sxs-lookup"><span data-stu-id="ec5fc-112">code</span></span>         |
|---------------------|--------------|
| <span data-ttu-id="ec5fc-113">Generischer Container</span><span class="sxs-lookup"><span data-stu-id="ec5fc-113">Generic Container</span></span>   | <span data-ttu-id="ec5fc-114">cenumubj. cpp</span><span class="sxs-lookup"><span data-stu-id="ec5fc-114">cenumobj.cpp</span></span> |
| <span data-ttu-id="ec5fc-115">Namespace Container</span><span class="sxs-lookup"><span data-stu-id="ec5fc-115">Namespace Container</span></span> | <span data-ttu-id="ec5fc-116">cenum NS. cpp</span><span class="sxs-lookup"><span data-stu-id="ec5fc-116">cenumns.cpp</span></span>  |
| <span data-ttu-id="ec5fc-117">Schema Container</span><span class="sxs-lookup"><span data-stu-id="ec5fc-117">Schema Container</span></span>    | <span data-ttu-id="ec5fc-118">cenum Sch. cpp</span><span class="sxs-lookup"><span data-stu-id="ec5fc-118">cenumsch.cpp</span></span> |



 

<span data-ttu-id="ec5fc-119">Informationen zu Client seitigen Informationen finden Sie unter [Sammlungen und Gruppen](collections-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="ec5fc-119">For client-side information, see [Collections and Groups](collections-and-groups.md).</span></span>

 

 




