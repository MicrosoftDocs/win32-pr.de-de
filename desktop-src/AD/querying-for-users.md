---
title: Abfragen von Benutzern
description: Die Abfrage muss den Such Ausdruck \ 0034;enthalten, um einen Benutzer abzufragen. (objectClass-Benutzer) (objectCategory-Person)) \ 0034;.
ms.assetid: a9f12de4-e1e2-41bb-b2cc-ff9c9fa1c39a
ms.tgt_platform: multiple
keywords:
- Benutzer AD, Abfragen für Benutzer
- Active Directory, verwenden von Benutzern, Abfragen von Benutzern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39037ff805dab753aae066d1f6611432b28ea73c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724457"
---
# <a name="querying-for-users"></a><span data-ttu-id="e7b58-105">Abfragen von Benutzern</span><span class="sxs-lookup"><span data-stu-id="e7b58-105">Querying for Users</span></span>

<span data-ttu-id="e7b58-106">Um einen Benutzer abzufragen, muss die Abfrage den Such Ausdruck "(& (objectClass = User) (objectCategory = Person))" enthalten.</span><span class="sxs-lookup"><span data-stu-id="e7b58-106">To query for a user, the query must contain the search expression "(&(objectClass=user)(objectCategory=person))".</span></span>

<span data-ttu-id="e7b58-107">Da die Computerklasse eine Unterklasse von User ist, gibt eine Abfrage, die nur (objectClass = User) enthält, Benutzer Objekte und Computer Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="e7b58-107">Because the computer class is a subclass of user, a query containing only (objectClass=user) would return user objects and computer objects.</span></span> <span data-ttu-id="e7b58-108">Außerdem ist die Objekt Kategorie des Benutzer Objekts Person (Nichtbenutzer). Daher gibt der Ausdruck (objectCategory = user) keine Benutzer zurück.</span><span class="sxs-lookup"><span data-stu-id="e7b58-108">Also, the object category of the user object is person (not user); therefore, the expression (objectCategory=user) does not return any users.</span></span> <span data-ttu-id="e7b58-109">Wenn Sie den Ausdruck (objectCategory = Person) verwenden, gibt die Abfrage Benutzer Objekte und Kontakt Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="e7b58-109">If you use the expression (objectCategory=person), the query returns user objects and contact objects.</span></span>

<span data-ttu-id="e7b58-110">Benutzer können in einem beliebigen Container oder einer Organisationseinheit in einer Domäne und im Stammverzeichnis der Domäne abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e7b58-110">Users can be placed in any container or organizational unit in a domain as well as the root of the domain.</span></span> <span data-ttu-id="e7b58-111">Dies bedeutet, dass sich Benutzer an zahlreichen Orten in der Verzeichnishierarchie befinden können.</span><span class="sxs-lookup"><span data-stu-id="e7b58-111">This means that users can be in numerous locations in the directory hierarchy.</span></span> <span data-ttu-id="e7b58-112">Sie können eine Tiefe Suche nach "(objectCategory = user)" durchführen, um alle Benutzer in einem Container, einer Organisationseinheit, einer Domäne, einer Domänen Struktur oder einer Gesamtstruktur zu suchen – abhängig von dem Objekt, an das der [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) -Zeiger gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="e7b58-112">You can perform a deep search for "(objectCategory=user)" to find all users in a container, organizational unit, domain, domain tree, or forest—depending on the object that the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer you are using is bound to.</span></span>

 

 