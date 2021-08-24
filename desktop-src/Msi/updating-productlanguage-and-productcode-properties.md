---
description: Die ProductLanguage-Eigenschaft muss auf den numerischen Sprachbezeichner (LANGID) für die neue Sprache aktualisiert werden.
ms.assetid: e00ef69b-c54b-41de-9230-a7582b260891
title: Aktualisieren von ProductLanguage- und ProductCode-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9d6cbb47a16e0e0f2f9d696dc73d3f3fe0d1bc278c4631a99469168e2ca23d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809860"
---
# <a name="updating-productlanguage-and-productcode-properties"></a>Aktualisieren von ProductLanguage- und ProductCode-Eigenschaften

Die [**ProductLanguage-Eigenschaft**](productlanguage.md) muss auf den numerischen Sprachbezeichner (LANGID) für die neue Sprache aktualisiert werden. Im Fall des Lokalisierungsbeispiels muss der Wert der **ProductLanguage-Eigenschaft** in der Property-Tabelle von LANGID für Englisch (1033) in LANGID für Französisch (1036) geändert [werden.](property-table.md)

Der Wert der [**ProductCode-Eigenschaft**](productcode.md) in der [Property-Tabelle](property-table.md) muss beim Lokalisieren einer Datenbank in einen neuen eindeutigen Wert geändert werden, da ein lokalisiertes Produkt als anderes Produkt betrachtet wird. Beispielsweise werden die deutsche und die englische Version einer Anwendung als zwei verschiedene Produkte betrachtet und müssen unterschiedliche Produktcodes haben. Weitere Informationen [finden Sie unter Product Codes](product-codes.md).

Verwenden Sie den Datenbanktabellen-Editor, um die Werte der Eigenschaften ProductCode und ProductLanguage in der Tabelle Property zu aktualisieren. Verwenden Sie die gezeigte GUID nicht wieder, wenn Sie dieses Beispiel kopieren.

[Eigenschaftentabelle](property-table.md)



| Eigenschaft                                   | Wert                                  |
|--------------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md)         | {EE389960-E426-4EEA-B669-AD8129249881} |
| [**ProductLanguage**](productlanguage.md) | 1036                                   |



 

[Fortsetzen](updating-a-summary-information-stream.md)

 

 



