---
description: Weitere Informationen finden Sie unter Indizieren von mehrwertigen Spalten
title: Indizierung über mehrwertige Spalten
TOCTitle: Indexing over Multi-Valued Columns
ms:assetid: 90e31df2-2f5b-47a8-84c1-ece6bcc40858
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269341(v=EXCHG.10)
ms:contentKeyID: 32765630
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: aea24e8423b704b7e0345898bcb6ae4b6d7c057b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343746"
---
# <a name="indexing-over-multi-valued-columns"></a>Indizierung über mehrwertige Spalten


_**Gilt für:** Windows | Windows Server_

## <a name="indexing-over-multi-valued-columns"></a>Indizierung über mehrwertige Spalten

Die Indizierung über mehrwertige Spalten erfolgt nur über die erste mehrwertige Spalte im Index. Die erste mehrwertige Spalte wird erweitert, sodass jeder Wert in der Spalte indiziert wird. Alle anderen mehrwertigen Spalten werden nur über den ersten Wert in der Spalte indiziert. Beispielsweise wird ein Index für Spalte a und Spalte B definiert, wobei beide Spalten mehr wertig sind. In einem Datensatz weist Spalte a die Werte rot, blau und Spalte B die Werte 1, 2 und 3 auf. Der resultierende Index würde Einträge für "Red-1" und "Blue-1" ergeben. Die Werte in der zweiten Spalte, Spalte B, werden nicht erweitert. Beachten Sie, dass auch bei jeder markierten Spalte mit mehreren Werten markierte Spalten, die explizit als mehr wertig gekennzeichnet sind, über JET_bitColumnMultiValued auf diese Weise erweitert werden. Aufgrund der Tatsache, dass primäre Indexeinträge Datensätze enthalten, ist es außerdem nicht zulässig, einen primären Index für eine mehrwertige Spalte zu haben, da dies zu mehreren Positionen im Index führen würde, in denen sich der Datensatz befinden müsste. Weitere Informationen finden Sie im Thema [markierte Spalten mit fester Größe und Variablen Spalten](./tagged-fixed-and-variable-columns.md) .

Ab Windows Vista haben Benutzer die Möglichkeit, die JET_bitIndexCrossProduct-Option festzulegen, wenn der Index mit [jetkreateindex](./jetcreateindex-function.md) oder [JetCreateIndex2](./jetcreateindex2-function.md) mithilfe der [JET_INDEXCREATE](./jet-indexcreate-structure.md) Struktur erstellt wird. Wenn diese Option für einen Index festgelegt wird, werden alle mehrwertigen Schlüssel Spalten im Index erweitert, und für jeden Wert in diesen Spalten wird ein Kreuz Produkt im Index erstellt. Im obigen Beispiel werden nun Einträge für Red-1, Red-2, Red-3, Blue-1, Blue-2, Blue-3, Auch hier muss jede Schlüssel Spalte explizit als mehr wertig deklariert werden, indem JET_bitColumnMultiValued im Index erweitert wird.
