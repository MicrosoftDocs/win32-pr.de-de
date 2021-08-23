---
title: Zusammenbauen von Abfragezeichenfolgen
description: In Active Directory kann die Verwendung bestimmter Filterkriterien die Suchleistung steigern. Dies liegt daran, dass Active Directory alle Prädikate auswertet, die Indizes identifiziert und dann einen Index auswählt, der wahrscheinlich den kleinsten Satz zurückgegebener Werte ergibt.
ms.assetid: 4139eedb-1383-4654-9b40-5e294a71be24
ms.tgt_platform: multiple
keywords:
- Assembling Query Strings ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 610ba78d6536d9cfe12f296fcbfa46d04cd572ae05cdb7d3bb8b0e1e7b5d32a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962197"
---
# <a name="assembling-query-strings"></a>Zusammenbauen von Abfragezeichenfolgen

In Active Directory kann die Verwendung bestimmter Filterkriterien die Suchleistung steigern. Dies liegt daran, dass Active Directory alle Prädikate auswertet, die Indizes identifiziert und dann einen Index auswählt, der wahrscheinlich den kleinsten Satz zurückgegebener Werte ergibt.

Vermeiden Sie es, in der Mitte oder am Ende einer Zeichenfolge nach Text zu suchen, z. B. "cn= \* stringe" oder \* "cn= \* fadeouse".

Suchen Sie nach Möglichkeit nach indizierten Attributen. Indizierte Attribute werden auf allen Domänencontrollern gespeichert, sodass die Abfrage höchstwahrscheinlich schneller ist als die Suche nach einem nicht indizierten Attribut.

 

 




