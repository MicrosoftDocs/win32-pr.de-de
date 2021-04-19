---
description: Qualifizierervarianten bieten weitere Informationen zu einem Qualifizierer, z. b. ob eine abgeleitete Klasse oder eine Instanz den ursprünglichen Wert des Qualifizierers über
ms.assetid: 6a0769ac-e16c-45e1-92b6-26e4969bf23d
ms.tgt_platform: multiple
title: Qualifizierervarianten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8ddf6c2daea59931e533174c532e3d07b147a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352338"
---
# <a name="qualifier-flavors"></a>Qualifizierervarianten

Qualifizierervarianten bieten weitere Informationen zu einem Qualifizierer, z. b. ob eine abgeleitete Klasse oder Instanz den ursprünglichen Wert des Qualifizierers überschreiben kann

Qualifizierervarianten können am Anfang der MOF-Datei mithilfe der folgenden Syntax hinzugefügt werden, wodurch Sie in der gesamten Definition angewendet werden. Beispiel:

``` syntax
Qualifier Description : ToSubClass Amended;
```

Die unter **Klasse** und die **geänderten** Varianten gelten für alle **Beschreibungs** Qualifizierer in der MOF-Datei.

In der folgenden Tabelle sind die qualifizierervarianten aufgeführt.



| Qualifiziererkonfiguration    | Bedeutung                                                                                                                                                                                                                                         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Abge**         | Der Qualifizierer ist in der Basisklassendefinition nicht erforderlich und kann zur Lokalisierung in die Ergänzung verschoben werden.                                                                                                                                  |
| **DisableOverride** | Der Qualifizierer kann in einer abgeleiteten Klasse oder Instanz nicht überschrieben werden. Beachten Sie, dass das Überschreiben eines weitergegebenen Qualifizierers die Standardeinstellung ist.                                                                                                      |
| **EnableOverride**  | Bei der Weitergabe an eine abgeleitete Klasse oder eine abgeleitete Instanz kann der Wert des Qualifizierers überschrieben werden. Das Festlegen von **EnableOverride** ist optional, da der qualifiziererwert überschrieben werden kann. |
| **Notat instance**   | Der Qualifizierer wird nicht an Klassen Instanzen weitergegeben.                                                                                                                                                                                             |
| **NotTo subclass**   | Der Q wird nicht an abgeleitete Klassen weitergegeben.                                                                                                                                                                                             |
| **Eingeschränkt**      | Der Qualifizierer wird nicht an-Instanzen oder abgeleitete Klassen weitergegeben.                                                                                                                                                                                |
| **Instanz von**      | Der Qualifizierer wird an Instanzen weitergegeben.                                                                                                                                                                                                       |
| **ToSubClass**      | Der Qualifizierer wird an abgeleitete Klassen weitergegeben. Diese Konfiguration eignet sich nur für Qualifizierer, die für eine Klasse definiert sind, und kann nicht an einen Qualifizierer angehängt werden, der eine Klasseninstanz                                                           |



 

 

 



