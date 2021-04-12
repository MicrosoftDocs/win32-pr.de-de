---
title: Dynamische Hilfsklassen
description: Ähnlich wie bei strukturellen und abstrakten Objektklassen werden zusätzliche Klassen durch ein classSchema-Objekt im Active Directory Schema definiert.
ms.assetid: bd5f6aed-c79a-4c03-ad03-a4ae00f0b888
ms.tgt_platform: multiple
keywords:
- Dynamische Hilfsklassen AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c13fc8231b5232b82a61b9409f1736e5bd9249
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472580"
---
# <a name="dynamic-auxiliary-classes"></a><span data-ttu-id="26e9f-104">Dynamische Hilfsklassen</span><span class="sxs-lookup"><span data-stu-id="26e9f-104">Dynamic Auxiliary Classes</span></span>

<span data-ttu-id="26e9f-105">Ähnlich wie bei strukturellen und abstrakten Objektklassen werden zusätzliche Klassen durch ein [**classSchema**](/windows/desktop/ADSchema/c-classschema) -Objekt im Active Directory Schema definiert.</span><span class="sxs-lookup"><span data-stu-id="26e9f-105">Similar to structural and abstract object classes, auxiliary classes are defined by a [**classSchema**](/windows/desktop/ADSchema/c-classschema) object in the Active Directory schema.</span></span> <span data-ttu-id="26e9f-106">Weitere Informationen finden Sie unter [Struktur-, abstrakte und Hilfsklassen](structural-abstract-and-auxiliary-classes.md).</span><span class="sxs-lookup"><span data-stu-id="26e9f-106">For more information, see [Structural, Abstract, and Auxiliary Classes](structural-abstract-and-auxiliary-classes.md).</span></span> <span data-ttu-id="26e9f-107">Diese Schema Definition gibt verschiedene Merkmale der-Klasse an, einschließlich der Attribute, die der-Klasse zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="26e9f-107">This schema definition specifies various characteristics of the class, including the attributes associated with the class.</span></span>

<span data-ttu-id="26e9f-108">Anders als bei Struktur Klassen können Sie eine Instanz einer Hilfsklasse nicht wie bei einer strukturellen Klasse erstellen.</span><span class="sxs-lookup"><span data-stu-id="26e9f-108">Unlike with structural classes, You cannot create an instance of an auxiliary class as you can with a structural class.</span></span> <span data-ttu-id="26e9f-109">Stattdessen verwenden Sie eine Hilfsklasse, um die Liste der Attribute zu erweitern, die einer anderen Struktur-, abstrakten oder zusätzlichen Objektklasse zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="26e9f-109">Instead, you use an auxiliary class to extend the list of attributes that is associated with another structural, abstract, or auxiliary object class.</span></span>

<span data-ttu-id="26e9f-110">In der ersten Version von Windows 2000 hat Active Directory Domain Services Unterstützung für das statische Verknüpfen von Erweiterungs Klassen mit der [**classSchema**](/windows/desktop/ADSchema/c-classschema) -Definition einer anderen Objektklasse bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="26e9f-110">In the initial release of Windows 2000, Active Directory Domain Services provided support for statically linking auxiliary classes to the [**classSchema**](/windows/desktop/ADSchema/c-classschema) definition of another object class.</span></span> <span data-ttu-id="26e9f-111">Wenn eine zusätzliche Klasse auf diese Weise verwendet wird, unterstützt jede Instanz der Objektklasse die Attribute der Erweiterungs Klasse.</span><span class="sxs-lookup"><span data-stu-id="26e9f-111">When an auxiliary class is used in this way, every instance of the object class supports the attributes of the auxiliary class.</span></span>

<span data-ttu-id="26e9f-112">**Windows 2000-Server und früher:** Active Directory Domain Services bietet keine Unterstützung für das dynamische Verknüpfen von Erweiterungs Klassen mit einzelnen Objekten, nicht nur für ganze Klassen von Objekten.</span><span class="sxs-lookup"><span data-stu-id="26e9f-112">**Windows 2000 Server and earlier:** Active Directory Domain Services does not provide support for dynamically linking auxiliary classes to individual objects, and not just to entire classes of objects.</span></span> <span data-ttu-id="26e9f-113">Außerdem können zusätzliche Klassen, die an eine Objektinstanz angefügt wurden, anschließend nicht aus der Instanz entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="26e9f-113">In addition, auxiliary classes that have been attached to an object instance cannot subsequently be removed from the instance.</span></span>

<span data-ttu-id="26e9f-114">**Windows Server 2003:** Dynamische Erweiterungs Klassen werden unterstützt, wenn auf allen Domänen Controllern in der Gesamtstruktur Windows Server 2003 und der Gesamtstruktur Funktionsmodus Windows Server 2003 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26e9f-114">**Windows Server 2003:** Dynamic Auxiliary Classes are supported when all domain controllers in the forest are running Windows Server 2003 and the forest functional mode is Windows Server 2003.</span></span>

<span data-ttu-id="26e9f-115">Weitere Informationen zu Erweiterungs Klassen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="26e9f-115">For more information about auxiliary classes, see:</span></span>

-   [<span data-ttu-id="26e9f-116">Dynamisch verknüpfte Hilfsklassen</span><span class="sxs-lookup"><span data-stu-id="26e9f-116">Dynamically Linked Auxiliary Classes</span></span>](dynamically-linked-auxiliary-classes.md)
-   [<span data-ttu-id="26e9f-117">Statisch verknüpfte Hilfsklassen</span><span class="sxs-lookup"><span data-stu-id="26e9f-117">Statically Linked Auxiliary Classes</span></span>](statically-linked-auxiliary-classes.md)
-   [<span data-ttu-id="26e9f-118">Bestimmen der Klassen, die einer Objektinstanz zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="26e9f-118">Determining the Classes Associated With an Object Instance</span></span>](determining-the-classes-associated-with-an-object-instance.md)
-   [<span data-ttu-id="26e9f-119">Hinzufügen einer Hilfsklasse zu einer Objektinstanz</span><span class="sxs-lookup"><span data-stu-id="26e9f-119">Adding an Auxiliary Class to an Object Instance</span></span>](adding-an-auxiliary-class-to-an-object-instance.md)

<span data-ttu-id="26e9f-120">Weitere Informationen zu Gesamtstruktur Funktionsebenen finden Sie unter "Vorgehensweise beim erhöhen Active Directory Domänen-und Gesamtstruktur Funktionsebenen" in der Hilfe-und Support Knowledge Base unter [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692) .</span><span class="sxs-lookup"><span data-stu-id="26e9f-120">For more information about forest functional levels, see "How to raise Active Directory domain and forest functional levels" in the Help and Support Knowledge Base at [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692).</span></span>

 

 