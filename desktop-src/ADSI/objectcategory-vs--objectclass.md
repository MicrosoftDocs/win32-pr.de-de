---
title: objectCategory im Vergleich zu objectClass
description: Das objectCategory-Attribut und das objectClass-Attribut können auf eine bestimmte Schema Klasse eines Verzeichnis Objekts verweisen.
ms.assetid: 66dadedb-61e4-4184-9b87-0fff036a94d9
ms.tgt_platform: multiple
keywords:
- objectCategory im Vergleich zu objectClass ADSI
- Attribute ASI, suchen nach objectCategory-und objectClass-Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbbb8c5fe737b7c81193a75cdae6b772db64e69c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036309"
---
# <a name="objectcategory-vs-objectclass"></a>objectCategory im Vergleich zu objectClass

Das **objectCategory** -Attribut und das **objectClass** -Attribut können auf eine bestimmte Schema Klasse eines Verzeichnis Objekts verweisen. Es gibt jedoch einen wichtigen Unterschied in der Semantik zwischen den beiden. "objectClass = Joy" bezieht sich auf solche Verzeichnisobjekte, bei denen "Joy" eine beliebige Klasse in der Objektklassen Hierarchie darstellt. "objectCategory = Joy" bezieht sich hingegen auf die Verzeichnisobjekte, in denen "Joy" eine bestimmte Klasse in der Objektklassen Hierarchie identifiziert.

**objectClass** kann mehrere Werte annehmen, während **objectCategory** einen einzelnen Wert annimmt. Aus diesem Grund eignet sich **objectCategory** besser für die Typübereinstimmung von Objekten in einer Verzeichnis Suche. ADSI verwendet dies als Standard Übereinstimmungs Kriterium. Suchvorgänge mit einer **objectClass** können nicht in großen Datenbanken skaliert werden. ADSI unterstützt die Syntaxen "(objectCategory = somedn)" und "(objectCategory = LDAP \_ Display \_ Name \_ of \_ Class)".

Eine Ausnahme besteht darin, dass der LDAP-Suchfilter "(objectClass = \* )" keine Suche in der Objektklasse angibt, sondern lediglich prüft, ob die Objekte vorhanden sind.

 

 




