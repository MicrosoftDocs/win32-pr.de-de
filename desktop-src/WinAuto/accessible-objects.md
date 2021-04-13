---
title: Barrierefreie Objekte
description: Mit Microsoft Active Accessibility werden Benutzeroberflächen Elemente für Clients als Component Object Model (com)-Objekte verfügbar gemacht.
ms.assetid: ab5669c3-33ce-4d56-a028-e36db25c0b28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba496e011d42fac9a3c4b047a7d8c3b9e0ecf84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388725"
---
# <a name="accessible-objects"></a><span data-ttu-id="8fb8c-103">Barrierefreie Objekte</span><span class="sxs-lookup"><span data-stu-id="8fb8c-103">Accessible Objects</span></span>

<span data-ttu-id="8fb8c-104">Mit Microsoft Active Accessibility werden Benutzeroberflächen Elemente für Clients als Component Object Model (com)-Objekte verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="8fb8c-104">With Microsoft Active Accessibility, UI elements are exposed to clients as Component Object Model (COM) objects.</span></span> <span data-ttu-id="8fb8c-105">Diese *barrierefreien Objekte* behalten Informationen, die als *Eigenschaften* bezeichnet werden, die den Namen des Objekts, den Bildschirm Speicherort und andere von hilfshilfen benötigte Informationen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="8fb8c-105">These *accessible objects* maintain pieces of information, called *properties*, which describe the object's name, screen location, and other information needed by accessibility aids.</span></span> <span data-ttu-id="8fb8c-106">Barrierefreie Objekte stellen auch *Methoden* bereit, die von Clients aufgerufen werden, damit das Objekt Aktionen ausführt.</span><span class="sxs-lookup"><span data-stu-id="8fb8c-106">Accessible objects also provide *methods* that clients call to cause the object to perform some action.</span></span> <span data-ttu-id="8fb8c-107">Barrierefreie Objekte, denen einfache Elemente zugeordnet sind, werden *auch als über* geordnete Elemente oder *Container* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8fb8c-107">Accessible objects that have simple elements associated with them are also called *parents*, or *containers*.</span></span>

<span data-ttu-id="8fb8c-108">Barrierefreie Objekte werden mithilfe der com-basierten [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle von Microsoft Active Accessibility implementiert.</span><span class="sxs-lookup"><span data-stu-id="8fb8c-108">Accessible objects are implemented using Microsoft Active Accessibility's COM-based [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="8fb8c-109">Die **IAccessible** -Methoden und-Eigenschaften ermöglichen es Client Anwendungen, Informationen zu Benutzeroberflächen Elementen zu erhalten, die von Benutzern benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="8fb8c-109">The **IAccessible** methods and properties enable client applications to get information about UI elements needed by users.</span></span> <span data-ttu-id="8fb8c-110">[**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) gibt z. b. einen Schnittstellen Zeiger auf das übergeordnete Element eines barrierefreien Objekts zurück, und [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) bietet Clients die Möglichkeit, Informationen zu anderen Objekten in einem Container zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8fb8c-110">For example, [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) returns an interface pointer to an accessible object's parent, and [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) provides a means for clients to get information about other objects within a container.</span></span>

<span data-ttu-id="8fb8c-111">Weitere Informationen dazu, wie barrierefreie Objekte und einfache Elemente verknüpft sind, finden Sie unter [einfache Elemente](simple-elements.md).</span><span class="sxs-lookup"><span data-stu-id="8fb8c-111">For more information about how accessible objects and simple elements are related, see [Simple Elements](simple-elements.md).</span></span>

 

 




