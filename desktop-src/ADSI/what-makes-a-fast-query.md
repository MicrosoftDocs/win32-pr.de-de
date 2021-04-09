---
title: Was macht eine schnelle Abfrage?
description: In diesem Thema werden bevorzugte Programmiermethoden aufgelistet, die beim Abfragen eines Verzeichnisses verwendet werden.
ms.assetid: d96f330f-3c57-4edc-9fd2-970f908b54c2
ms.tgt_platform: multiple
keywords:
- Was macht eine schnelle Abfrage von ADSI?
- Abfragen von ADSI, was eine schnelle Abfrage macht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883db1e9de7b7b7a1179c814d6f66f774685083e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858473"
---
# <a name="what-makes-a-fast-query"></a>Was macht eine schnelle Abfrage?

Beachten Sie beim Ausführen einer Abfrage die folgenden Konzepte zur Leistungsverbesserung:

-   Filtern Sie nach Möglichkeit nur indizierte Attribute. Verwenden Sie die von Ihnen erwarteten Index Attribute, um die geringste Anzahl von Treffern zu generieren. Weitere Informationen und eine umfassende Liste der indizierten Attribute für Windows finden Sie unter [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema).
-   Suchen Sie nach **objectCategory** anstelle von **objectClass** , weil **objectClass** keine indizierte Eigenschaft ist.
-   Beachten Sie die Verweise. Sie sollten den globalen Katalog durchsuchen, wenn ihre Attribute als GC repliziert aufgeführt sind.
-   Vermeiden Sie das Suchen von Text in der Mitte und am Ende einer Zeichenfolge. Beispiel: "CN = \* Hille \* " oder "CN = \* larouse".
-   Angenommen, eine Unterstruktur Suche gibt ein großes Resultset zurück. Paging beim Durchführen von untergeordneten Such Vorgängen verwenden. Der Server kann dann ein großes Resultset in Blöcken streamen, wodurch die serverseitigen Speicherressourcen verringert werden. Dies vereinfacht die Netzwerk Auslastung und verringert die Notwendigkeit, extrem große Datenblöcke über das Netzwerk zu senden.
-   Sie können Ihre Suchvorgänge ordnungsgemäß festlegen, sodass nicht mehr benötigt wird, als erforderlich ist.
-   Führen Sie eine komplexe Suche nach mehreren Attributen durch, da diese weniger Leistungs intensiv ist als bei der Durchführung mehrerer Suchvorgänge. Eine Suche nach einem Objekt, das zwei Attribute liest, ist effizienter als zwei Suchvorgänge für dasselbe Objekt, von denen jedes ein Attribut zurückgibt.
-   Verwenden Sie zum Lesen des Attributs mit einer großen Anzahl von Werten Bereichs Limits, um die Suchgröße zu minimieren, sodass Sie einige tausend Elemente gleichzeitig lesen können. Weitere Informationen zum Angeben von Attribut Bereichs Limits finden Sie unter [Attribut Bereichs Abruf](attribute-range-retrieval.md).
-   Binden an ein Objekt halten das Bindungs Handle für den Rest der Sitzung. Binden und Aufheben der Bindung für jeden-Befehl. Wenn Sie ADO oder OLE DB verwenden, erstellen Sie keine zahlreichen Verbindungs Objekte.
-   Lesen Sie den RootDSE einmal, und merken Sie sich den Inhalt für den Rest der Sitzung.

 

 