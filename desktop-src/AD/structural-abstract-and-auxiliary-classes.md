---
title: Struktur-, abstrakte und Hilfsklassen
description: Das objectClassCategory-Attribut eines classSchema-Objekts kann über einen Wert verfügen, der in der folgenden Tabelle aufgeführt ist und angibt, ob die Klasse strukturell, abstrakt oder hilfsweise ist.
ms.assetid: 5af740cb-b292-4d80-abe5-3e3d194758f3
ms.tgt_platform: multiple
keywords:
- Struktur-, abstrakte und Hilfsklassen AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561bc836794b45b6c028fe8da772b0b38d0936a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036338"
---
# <a name="structural-abstract-and-auxiliary-classes"></a><span data-ttu-id="cc12d-104">Struktur-, abstrakte und Hilfsklassen</span><span class="sxs-lookup"><span data-stu-id="cc12d-104">Structural, Abstract, and Auxiliary Classes</span></span>

<span data-ttu-id="cc12d-105">Das **objectClassCategory** -Attribut eines **classSchema** -Objekts kann über einen Wert verfügen, der in der folgenden Tabelle aufgeführt ist und angibt, ob die Klasse strukturell, abstrakt oder hilfsweise ist.</span><span class="sxs-lookup"><span data-stu-id="cc12d-105">The **objectClassCategory** attribute of a **classSchema** object can have a value, as listed in the following table, that indicates whether the class is structural, abstract, or auxiliary.</span></span>



| <span data-ttu-id="cc12d-106">Wert</span><span class="sxs-lookup"><span data-stu-id="cc12d-106">Value</span></span> | <span data-ttu-id="cc12d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc12d-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc12d-108">1</span><span class="sxs-lookup"><span data-stu-id="cc12d-108">1</span></span>     | <span data-ttu-id="cc12d-109">Eine strukturelle Klasse, bei der es sich um den einzigen Typ der Klasse handelt, die über Instanzen in Active Directory Domain Services verfügen kann.</span><span class="sxs-lookup"><span data-stu-id="cc12d-109">A structural class, which is the only type of class that can have instances in Active Directory Domain Services.</span></span> <span data-ttu-id="cc12d-110">Eine strukturelle Klasse kann eine Unterklasse einer abstrakten oder strukturellen Klasse sein.</span><span class="sxs-lookup"><span data-stu-id="cc12d-110">A structural class can be a subclass of an abstract or structural class.</span></span> <span data-ttu-id="cc12d-111">Eine strukturelle Klasse kann eine beliebige Anzahl von Hilfsklassen in ihrer Definition enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc12d-111">A structural class can include any number of auxiliary classes in its definition.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="cc12d-112">2</span><span class="sxs-lookup"><span data-stu-id="cc12d-112">2</span></span>     | <span data-ttu-id="cc12d-113">Eine abstrakte Klasse, bei der es sich um eine Vorlage handelt, mit der neue abstrakte, zusätzliche und strukturelle Klassen abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="cc12d-113">An abstract class, which is a template used to derive new abstract, auxiliary, and structural classes.</span></span> <span data-ttu-id="cc12d-114">Eine abstrakte Klasse kann nur eine Unterklasse einer abstrakten Klasse sein.</span><span class="sxs-lookup"><span data-stu-id="cc12d-114">An abstract class can only be a subclass of an abstract class.</span></span> <span data-ttu-id="cc12d-115">Abstrakte Klassen können nicht in Active Directory Domain Services instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="cc12d-115">Abstract classes cannot be instantiated in Active Directory Domain Services.</span></span> <span data-ttu-id="cc12d-116">Eine abstrakte Klasse kann eine beliebige Anzahl von Hilfsklassen in ihrer Definition enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc12d-116">An abstract class can include any number of auxiliary classes in its definition.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="cc12d-117">3</span><span class="sxs-lookup"><span data-stu-id="cc12d-117">3</span></span>     | <span data-ttu-id="cc12d-118">Eine Hilfsklasse, die in die Definition einer Struktur-, abstrakten oder Erweiterungs Klasse eingeschlossen werden kann. in diesem Fall werden die Werte **mustare**, **systemmustare**, **mayare** und **systemmayare** der Erweiterungs Klasse den Werten der Klasse hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cc12d-118">An auxiliary class, which can be included in the definition of a structural, abstract, or auxiliary class, in which case, the **mustContain**, **systemMustContain**, **mayContain**, and **systemMayContain** values of the auxiliary class are added to those of the class.</span></span> <span data-ttu-id="cc12d-119">Eine Hilfsklasse kann eine Unterklasse einer abstrakten oder einer Hilfsklasse sein.</span><span class="sxs-lookup"><span data-stu-id="cc12d-119">An auxiliary class can be a subclass of an abstract or auxiliary class.</span></span> <span data-ttu-id="cc12d-120">Erweiterungs Klassen können nicht in Active Directory Domain Services instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="cc12d-120">Auxiliary classes cannot be instantiated in Active Directory Domain Services.</span></span> <span data-ttu-id="cc12d-121">Eine Hilfsklasse kann eine beliebige Anzahl von Hilfsklassen in ihrer Definition enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc12d-121">An auxiliary class can include any number of auxiliary classes in its definition.</span></span> |



 

<span data-ttu-id="cc12d-122">Verwechseln Sie **objectClassCategory** nicht mit einer [Objekt Kategorie](object-class-and-object-category.md).</span><span class="sxs-lookup"><span data-stu-id="cc12d-122">Do not confuse the **objectClassCategory** with an [object category](object-class-and-object-category.md).</span></span>

 

 




