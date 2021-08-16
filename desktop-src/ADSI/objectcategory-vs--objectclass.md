---
title: objectCategory im Vergleich zu objectClass
description: Sowohl das objectCategory-Attribut als auch das objectClass-Attribut können auf eine bestimmte Schemaklasse eines Verzeichnisobjekts verweisen.
ms.assetid: 66dadedb-61e4-4184-9b87-0fff036a94d9
ms.tgt_platform: multiple
keywords:
- objectCategory im Vergleich zu objectClass ADSI
- Attribute ASI , Suchen nach objectCategory- und objectClass-Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3833f8cf26cb2272fbe1e7c1063322f39a8c0147e4b22382d26067f90e72e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839220"
---
# <a name="objectcategory-vs-objectclass"></a>objectCategory im Vergleich zu objectClass

Sowohl das **objectCategory-Attribut als** **auch das objectClass-Attribut** können auf eine bestimmte Schemaklasse eines Verzeichnisobjekts verweisen. Es gibt jedoch einen wichtigen Unterschied in der Semantik zwischen den beiden. "objectClass=class" bezieht sich auf solche Verzeichnisobjekte, in denen "class" jede Klasse in der Objektklassenhierarchie darstellt. "objectCategory=class" bezieht sich hingegen auf die Verzeichnisobjekte, in denen "wild" eine bestimmte Klasse in der Objektklassenhierarchie identifiziert.

**objectClass** kann mehrere Werte verwenden, **während objectCategory** einen einzelnen Wert an sich nimmt. Daher eignet sich **objectCategory** besser für den Typabgleich von Objekten in einer Verzeichnissuche. ADSI verwendet dies als Standardabgleichskriterium. Suchvorgänge mit **einer objectClass** sind für große Datenbanken nicht skalierbar. ADSI unterstützt die Syntaxen "(objectCategory=SomeDN)" und "(objectCategory=Ldap \_ Display \_ Name of \_ \_ Class)".

Die Ausnahme ist, dass der LDAP-Suchfilter "(objectClass= )" keine Suche in der Objektklasse anknt, sondern lediglich testet, ob die \* Objekte vorhanden sind.

 

 




