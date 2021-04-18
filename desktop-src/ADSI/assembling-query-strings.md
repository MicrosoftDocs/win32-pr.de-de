---
title: Assemblieren von Abfrage
description: In Active Directory kann die Suchleistung durch die Verwendung spezifischer Filterkriterien gesteigert werden. Der Grund hierfür ist, dass Active Directory alle Prädikate auswertet, die Indizes identifiziert und dann einen Index auswählt, der wahrscheinlich die kleinste Menge an zurückgegebenen Werten liefert.
ms.assetid: 4139eedb-1383-4654-9b40-5e294a71be24
ms.tgt_platform: multiple
keywords:
- Assemblierungszeichenfolgen ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e56dec34f63a4a3e12385a36ad5fe5339a0f3d9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340811"
---
# <a name="assembling-query-strings"></a>Assemblieren von Abfrage

In Active Directory kann die Suchleistung durch die Verwendung spezifischer Filterkriterien gesteigert werden. Der Grund hierfür ist, dass Active Directory alle Prädikate auswertet, die Indizes identifiziert und dann einen Index auswählt, der wahrscheinlich die kleinste Menge an zurückgegebenen Werten liefert.

Vermeiden Sie das Suchen nach Text in der Mitte oder am Ende einer Zeichenfolge, z. b. "CN = \* Hille \* " oder "CN = \* larouse".

Suchen Sie nach Möglichkeit nach indizierten Attributen. Indizierte Attribute werden auf allen Domänen Controllern gespeichert, sodass die Abfrage höchstwahrscheinlich schneller ist als bei der Suche nach einem nicht indizierten Attribut.

 

 




