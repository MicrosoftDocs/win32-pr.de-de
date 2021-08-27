---
description: Qualifizierer-Varianten bieten weitere Informationen zu einem Qualifizierer, z. B. ob eine abgeleitete Klasse oder Instanz den ursprünglichen Wert der Qualifizierer überschreiben kann.
ms.assetid: 6a0769ac-e16c-45e1-92b6-26e4969bf23d
ms.tgt_platform: multiple
title: Qualifizierer-Varianten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a48c5ed3c7b695b19c182bcf05a9ce55b31b0bb94081570c58c8d55f7e48994c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050478"
---
# <a name="qualifier-flavors"></a>Qualifizierer-Varianten

Qualifizierer-Varianten bieten weitere Informationen zu einem Qualifizierer, z. B. ob eine abgeleitete Klasse oder Instanz den ursprünglichen Wert des Qualifizierers überschreiben kann.

Qualifizierer-Varianten können am Anfang der MOF-Datei mithilfe der folgenden Syntax hinzugefügt werden, sodass sie in der gesamten Definition angewendet werden. Beispiel:

``` syntax
Qualifier Description : ToSubClass Amended;
```

Die **Varianten ToSubClass** und **Flavor gelten** für alle **Beschreibungsqualifizierer** in der MOF.

In der folgenden Tabelle sind die Qualifizierer-Varianten aufgeführt.



| Qualifier Flavor    | Bedeutung                                                                                                                                                                                                                                         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Geändert**         | Der Qualifizierer ist in der Basisklassendefinition nicht erforderlich und kann zur Lokalisierung in die Ergänzung verschoben werden.                                                                                                                                  |
| **DisableOverride** | Der Qualifizierer kann in einer abgeleiteten Klasse oder Instanz nicht überschrieben werden. Beachten Sie, dass das Überschreiben eines weitergegebenen Qualifizierers die Standardeinstellung ist.                                                                                                      |
| **EnableOverride**  | Bei der Propagieren an eine abgeleitete Klasse oder Instanz kann der Wert des Qualifizierers überschrieben werden. Das **Festlegen von EnableOverride** ist optional, da die Möglichkeit, den Qualifiziererwert zu überschreiben, die Standardfunktionalität für propagierte Qualifizierer ist. |
| **NotToInstance**   | Der Qualifizierer wird nicht an Klasseninstanzen propagiert.                                                                                                                                                                                             |
| **NotToSubClass**   | Der Q wird nicht an abgeleitete Klassen weitergegeben.                                                                                                                                                                                             |
| **Eingeschränkt**      | Der Qualifizierer wird nicht an Instanzen oder abgeleitete Klassen propagiert.                                                                                                                                                                                |
| **ToInstance**      | Der Qualifizierer wird an Instanzen weitergegeben.                                                                                                                                                                                                       |
| **ToSubClass**      | Der Qualifizierer wird an abgeleitete Klassen propagiert. Diese Variante eignet sich nur für Qualifizierer, die für eine Klasse definiert sind, und kann nicht an einen Qualifizierer angefügt werden, der eine Klasseninstanz beschreibt.                                                           |



 

 

 



