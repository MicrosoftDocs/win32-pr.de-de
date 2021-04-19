---
description: Die productlanguage-Eigenschaft muss auf den numerischen sprach Bezeichner (langid) für die neue Sprache aktualisiert werden.
ms.assetid: e00ef69b-c54b-41de-9230-a7582b260891
title: Aktualisieren von productlanguage-und ProductCode-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a7537cdb0295075fbfd1b8b58e45a051610cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360835"
---
# <a name="updating-productlanguage-and-productcode-properties"></a>Aktualisieren von productlanguage-und ProductCode-Eigenschaften

Die [**productlanguage**](productlanguage.md) -Eigenschaft muss auf den numerischen sprach Bezeichner (langid) für die neue Sprache aktualisiert werden. Im Beispiel für die Lokalisierung muss der Wert der **productlanguage** -Eigenschaft von der langid für Englisch (1033) in die langid für Französisch (1036) in der [Eigenschaften Tabelle](property-table.md)geändert werden.

Der Wert der [**ProductCode**](productcode.md) -Eigenschaft in der [Eigenschaften Tabelle](property-table.md) muss beim Lokalisieren einer Datenbank in einen neuen, eindeutigen Wert geändert werden, da ein lokalisiertes Produkt als anderes Produkt angesehen wird. Beispielsweise werden die deutsche und die englische Version einer Anwendung als zwei verschiedene Produkte betrachtet und müssen über unterschiedliche Produktcodes verfügen. Siehe [Produkt Codes](product-codes.md).

Verwenden Sie den Datenbanktabellen-Editor, um die Werte der ProductCode-Eigenschaft und der productlanguage-Eigenschaft in der Eigenschaften Tabelle zu aktualisieren. Verwenden Sie nicht die GUID, die angezeigt wird, wenn Sie dieses Beispiel kopieren.

[Eigenschaften Tabelle](property-table.md)



| Eigenschaft                                   | Wert                                  |
|--------------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md)         | {EE389960-E426-4EEA-B669-AD8129249881} |
| [**Productlanguage**](productlanguage.md) | 1036                                   |



 

[Fortsetzen](updating-a-summary-information-stream.md)

 

 



