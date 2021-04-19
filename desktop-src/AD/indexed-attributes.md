---
title: Indizierte Attribute (AD DS)
description: Attribute können indiziert werden. Das Indizieren eines Attributs kann die Leistung von Abfragen für dieses Attribut verbessern.
ms.assetid: 20e10fc9-d767-4d82-9ed6-b9f384e77b12
ms.tgt_platform: multiple
keywords:
- Indizierte Attribute ad
- Attribute ad, indiziert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c280d5390d666b6b0f95f49972e4c569f046865b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106341919"
---
# <a name="indexed-attributes-ad-ds"></a>Indizierte Attribute (AD DS)

Attribute können indiziert werden. Das Indizieren eines Attributs kann die Leistung von Abfragen für dieses Attribut verbessern.

Attribute werden indiziert, wenn für das [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) -Attribut in der Schema Definition des Attributs das am wenigsten bedeutende Bit auf 1 festgelegt ist. Wenn Sie das am wenigsten bedeutende Bit der **searchFlags** -Attribut Schema Definition auf 1 festlegen, wird dynamisch ein Index erstellt. Wenn Sie das am wenigsten bedeutende Bit der **searchFlags** -Attribut Schema Definition auf 0 festlegen, wird der Index für das Attribut entfernt. Der Index wird automatisch von einem Hintergrund Thread auf dem Domänen Controller erstellt.

Im Idealfall sollten indizierte Attribute einen Einzelwert mit stark eindeutigen Werten aufweisen, die gleichmäßig auf den Satz von Instanzen verteilt sind. Weniger eindeutig die Werte eines Attributs sind, desto weniger effektiv ist der Index.

Mehrwertige Attribute können ebenfalls indiziert werden, aber die Kosten für das Erstellen des Indexes für ein mehr wertiges Attribut sind im Hinblick auf Speicher, Update und Suchzeit größer. Die Eindeutigkeits Anforderung für eine mehrwertige Eigenschaft ist identisch mit der für eine einwertige Eigenschaft – je größer die Werte sind, desto effektiver ist der Index.

Die mehr indizierten Attribute, die eine Klasse besitzt, desto mehr Zeit ist erforderlich, um neue Instanzen der-Klasse zu erstellen.

Indizes gelten für Attribute, nicht für Klassen. Das heißt, wenn ein Attribut als indiziert gekennzeichnet ist, werden alle Instanzen des Attributs dem Index hinzugefügt, nicht nur die Instanzen, die Mitglieder einer bestimmten Klasse sind.

Legen Sie den folgenden Registrierungs Wert auf einem Domänen Controller auf 4 fest, um zu überprüfen, ob ein Server einen Index für die Verarbeitung einer Abfrage verwendet. Führen Sie dann eine Abfrage auf diesem Domänen Controller aus, und suchen Sie im Verzeichnis Ereignisprotokoll nach Daten zu den Indizes, die zum Verarbeiten der Abfrage verwendet werden.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      Current Control Set
         Services
            NTDS
               Diagnostics
                  9 Internal Processing
```

Weitere Informationen zu anderen Bits in der [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) -Eigenschaft finden Sie unter [Merkmale von Attributen](characteristics-of-attributes.md).

 

 