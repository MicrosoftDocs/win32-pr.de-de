---
title: Indizierte Attribute (AD DS)
description: Attribute können indiziert werden. Die Indizierung eines Attributs kann die Leistung von Abfragen für dieses Attribut verbessern.
ms.assetid: 20e10fc9-d767-4d82-9ed6-b9f384e77b12
ms.tgt_platform: multiple
keywords:
- Indizierte Attribute AD
- Attribute AD , indiziert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabd205fea66b198096a9a9427822eb4ba0ccb609fb3e6fef0854fa91848371c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187584"
---
# <a name="indexed-attributes-ad-ds"></a>Indizierte Attribute (AD DS)

Attribute können indiziert werden. Die Indizierung eines Attributs kann die Leistung von Abfragen für dieses Attribut verbessern.

Ein Attribut wird indiziert, wenn das [**attribut searchFlags**](/windows/desktop/ADSchema/a-searchflags) in der Schemadefinition des Attributs das am wenigsten signifikante Bit auf 1 festgelegt hat. Wenn Das am wenigsten signifikante Bit der Schemadefinition des **searchFlags-Attributs** auf 1 festgelegt wird, wird dynamisch ein Index erstellt. Das Festlegen des am wenigsten signifikanten Bits der Schemadefinition des **searchFlags-Attributs** auf 0 führt dazu, dass der Index für das Attribut entfernt wird. Der Index wird automatisch von einem Hintergrundthread auf dem Domänencontroller erstellt.

Im Idealfall sollten indizierte Attribute einwertig sein, wobei höchst eindeutige Werte gleichmäßig auf die Gruppe von Instanzen verteilt sind. Je weniger eindeutig die Werte eines Attributs sind, desto weniger effektiv ist der Index.

Mehrwertige Attribute können auch indiziert werden, aber die Kosten für die Indexerstellung für ein mehrwertiges Attribut sind hinsichtlich Speicher, Aktualisierung und Suchzeit höher. Die Eindeutigkeitsanforderung für eine mehrwertige Eigenschaft entspricht der Für eine einwertige Eigenschaft. Je eindeutiger die Werte sind, desto effektiver ist der Index.

Je mehr indizierte Attribute eine Klasse aufweist, desto mehr Zeit ist erforderlich, um neue Instanzen der -Klasse zu erstellen.

Indizes gelten für Attribute, nicht für Klassen. Das heißt, wenn ein Attribut als indiziert markiert ist, werden alle Instanzen des Attributs dem Index hinzugefügt, nicht nur die Instanzen, die Member einer bestimmten Klasse sind.

Um zu überprüfen, ob ein Server einen Index zum Verarbeiten einer Abfrage verwendet, legen Sie den folgenden Registrierungswert auf einem Domänencontroller auf 4 fest. Führen Sie dann eine Abfrage auf diesem Domänencontroller aus, und suchen Sie im Verzeichnisereignisprotokoll nach Daten zu den Indizes, die ggf. zum Verarbeiten der Abfrage verwendet werden.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      Current Control Set
         Services
            NTDS
               Diagnostics
                  9 Internal Processing
```

Weitere Informationen zu anderen Bits in der [**searchFlags-Eigenschaft**](/windows/desktop/ADSchema/a-searchflags) finden Sie unter [Merkmale von Attributen.](characteristics-of-attributes.md)

 

 