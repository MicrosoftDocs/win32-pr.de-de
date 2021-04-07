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
# <a name="querying-for-users"></a>Abfragen von Benutzern

Um einen Benutzer abzufragen, muss die Abfrage den Such Ausdruck "(& (objectClass = User) (objectCategory = Person))" enthalten.

Da die Computerklasse eine Unterklasse von User ist, gibt eine Abfrage, die nur (objectClass = User) enthält, Benutzer Objekte und Computer Objekte zurück. Außerdem ist die Objekt Kategorie des Benutzer Objekts Person (Nichtbenutzer). Daher gibt der Ausdruck (objectCategory = user) keine Benutzer zurück. Wenn Sie den Ausdruck (objectCategory = Person) verwenden, gibt die Abfrage Benutzer Objekte und Kontakt Objekte zurück.

Benutzer können in einem beliebigen Container oder einer Organisationseinheit in einer Domäne und im Stammverzeichnis der Domäne abgelegt werden. Dies bedeutet, dass sich Benutzer an zahlreichen Orten in der Verzeichnishierarchie befinden können. Sie können eine Tiefe Suche nach "(objectCategory = user)" durchführen, um alle Benutzer in einem Container, einer Organisationseinheit, einer Domäne, einer Domänen Struktur oder einer Gesamtstruktur zu suchen – abhängig von dem Objekt, an das der [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) -Zeiger gebunden ist.

 

 