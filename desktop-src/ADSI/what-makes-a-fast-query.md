---
title: Was macht eine schnelle Abfrage?
description: In diesem Thema werden die bevorzugten Programmiermethoden aufgeführt, die beim Abfragen eines Verzeichnisses verwendet werden.
ms.assetid: d96f330f-3c57-4edc-9fd2-970f908b54c2
ms.tgt_platform: multiple
keywords:
- Was macht eine schnelle Abfrage ADSI aus?
- fragt ADSI ab, was eine schnelle Abfrage macht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134d391c728d543c407ee770081e2ced96afbba86d205462e814d89f74e82a57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589840"
---
# <a name="what-makes-a-fast-query"></a>Was macht eine schnelle Abfrage aus?

Berücksichtigen Sie beim Ausführen einer Abfrage die folgenden Leistungsverbesserungskonzepte:

-   Filtern Sie nach Möglichkeit nur nach indizierten Attributen. Verwenden Sie Indexattribute, von denen Sie erwarten, dass sie die geringste Anzahl von Treffern generieren. Weitere Informationen und eine umfassende Liste der indizierten Attribute für Windows finden Sie unter [Active Directory-Schema.](/windows/desktop/ADSchema/active-directory-schema)
-   Suchen Sie **nach objectCategory anstelle** von **objectClass,** **da objectClass** keine indizierte Eigenschaft ist.
-   Beachten Sie Empfehlungen. Erwägen Sie, den globalen Katalog zu durchsuchen, wenn Ihre Attribute als GC-repliziert aufgeführt sind.
-   Vermeiden Sie die Suche nach Text in der Mitte und am Ende einer Zeichenfolge. Beispiel: "cn= \* policiese \* " oder "cn=ouse". \*
-   Angenommen, eine Teilstruktursuche gibt ein großes Ergebnisset zurück. Verwenden Sie Paging, wenn Sie Teilstruktursuchen durchführen. Der Server kann dann ein großes Ergebnisset in Blocken streamen, um die serverseitigen Arbeitsspeicherressourcen zu reduzieren. Dies reduziert effektiv die Netzwerkauslastung und verringert den Bedarf für das Senden extrem großer Datenbrocken über das Netzwerk.
-   Geben Sie einen ordnungsgemäßen Bereich für Ihre Suchvorgänge ein, um nicht mehr als erforderlich abzurufen.
-   Führen Sie eine komplexe Suche nach mehreren Attributen durch, da sie weniger leistungsintensiv als das Ausführen mehrerer Suchvorgänge ist. Eine Suche nach einem Objekt, das zwei Attribute liest, ist effizienter als zwei Suchen nach demselben Objekt, die jeweils ein Attribut zurückgeben.
-   Verwenden Sie zum Lesen von Attributen mit einer großen Anzahl von Werten Bereichsgrenzwerte, um die Suchgröße zu minimieren, sodass Sie einige Tausend Elemente gleichzeitig lesen können. Weitere Informationen zum Angeben von Attributbereichsgrenzwerten finden Sie unter [Abrufen des Attributbereichs.](attribute-range-retrieval.md)
-   Binden an ein Objekt enthält das Bindungshand handle für den Rest der Sitzung. Binden und entbinden Sie die Bindung nicht für jeden Aufruf. Wenn Sie ADO oder ADO OLE DB, erstellen Sie nicht viele Verbindungsobjekte.
-   Lesen Sie rootDSE einmal, und merken Sie sich den Inhalt für den Rest der Sitzung.

 

 