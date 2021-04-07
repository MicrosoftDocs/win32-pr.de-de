---
title: Überlegungen zu Eigenschaften Gruppen
description: Es wird dringend empfohlen, dass Eigenschaften Sätze klein gehalten werden, da der Eigenschaften Satz-Stream in den Arbeitsspeicher gelesen wird, bevor eine einzelne Eigenschaft gelesen oder geschrieben werden kann.
ms.assetid: 520db05e-81cd-40ef-af89-471d7194c634
keywords:
- Überlegungen zu Eigenschaften Gruppen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfd89140092b13d113122ffe1c1a2b576e654c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714561"
---
# <a name="property-set-considerations"></a>Überlegungen zu Eigenschaften Gruppen

Es wird dringend empfohlen, dass Eigenschaften Sätze klein gehalten werden, da der Eigenschaften Satz-Stream in den Arbeitsspeicher gelesen wird, bevor eine einzelne Eigenschaft gelesen oder geschrieben werden kann. "Small" bedeutet weniger als 32 Kilobyte an Daten. Dies stellt selten ein Problem dar, da in der Regel "Inline" Eigenschaften kleine Elemente wie beschreibende Zeichen folgen, Schlüsselwörter, Zeitstempel, Zahlen, Autorennamen, global eindeutige Bezeichner (GUIDs), Klassen Bezeichner (CLSIDs) usw. sein werden.

Zum Speichern größerer Datenblöcke oder in Fällen, in denen die Gesamtgröße eines Satzes verwandter Eigenschaften den empfohlenen Betrag überschreitet, wird dringend empfohlen, nicht einfache Typen wie z. b. **VT \_ Stream** und **VT- \_ Speicher** zu verwenden. Diese werden nicht im Eigenschaften Satz-Stream gespeichert, sodass Sie nicht maßgeblich den anfänglichen mehr Aufwand des ersten Zugriffs und Schreibens einer Eigenschaft beeinflussen. Da der Eigenschafts Satz-Stream den Namen des gleich geordneten Streams oder der Speicher Wert Eigenschaft enthält, ist ein minimaler mehr Aufwand erforderlich, da der Wert für die Verarbeitung etwas geringer ist.

Weitere Informationen finden Sie unter

-   [Überlegungen zur IPropertySetStorage-Implementierung](ipropertysetstorage-implementation-considerations.md)
-   [Speichern von Eigenschafts Sätzen](storing-property-sets.md)
-   [Leistungsmerkmale](performance-characteristics.md)
-   [Implementieren des Eigenschaften Satzes für Zusammenfassungs Informationen](implementing-the-summary-information-property-set.md)

 

 




