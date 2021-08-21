---
title: Abfragen von Benutzern
description: Um einen Benutzer abzufragen, muss die Abfrage den Suchausdruck \ 0034;( (objectClass-Benutzer) (objectCategory person)) \ 0034;.
ms.assetid: a9f12de4-e1e2-41bb-b2cc-ff9c9fa1c39a
ms.tgt_platform: multiple
keywords:
- users AD , Abfragen von Benutzern
- Active Directory, using, users, querying for users
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae6939cef858c3dfc108611a1b0e7ab0367c302a091ca436c9c69b2fb5277b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025318"
---
# <a name="querying-for-users"></a>Abfragen von Benutzern

Um einen Benutzer abzufragen, muss die Abfrage den Suchausdruck "(&(objectClass=user)(objectCategory=person))" enthalten.

Da die Computerklasse eine Unterklasse des Benutzers ist, würde eine Abfrage, die nur (objectClass=user) enthält, Benutzerobjekte und Computerobjekte zurückgeben. Außerdem ist die Objektkategorie des Benutzerobjekts Person (nicht Benutzer); daher gibt der Ausdruck (objectCategory=user) keine Benutzer zurück. Wenn Sie den Ausdruck (objectCategory=person) verwenden, gibt die Abfrage Benutzerobjekte und Kontaktobjekte zurück.

Benutzer können in einem beliebigen Container oder einer Organisationseinheit in einer Domäne sowie im Stamm der Domäne platziert werden. Dies bedeutet, dass sich Benutzer an zahlreichen Speicherorten in der Verzeichnishierarchie befinden können. Sie können eine umfassende Suche nach "(objectCategory=user)" durchführen, um alle Benutzer in einem Container, einer Organisationseinheit, einer Domäne, einer Domänenstruktur oder einer Gesamtstruktur zu suchen– abhängig von dem Objekt, an das der von Ihnen [**verwendete IDirectorySearch-Zeiger**](/windows/desktop/api/iads/nn-iads-idirectorysearch) gebunden ist.

 

 