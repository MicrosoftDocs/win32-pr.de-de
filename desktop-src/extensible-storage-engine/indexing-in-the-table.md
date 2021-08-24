---
description: Weitere Informationen finden Sie unter Indizierung in der Tabelle.
title: Indizierung in der Tabelle
TOCTitle: Indexing in the Table
ms:assetid: d86c2c6b-d001-468d-ab74-937911b0036d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294106(v=EXCHG.10)
ms:contentKeyID: 32765721
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 8bfc5054e5fd2b2f13747b0b5729987b9f81d5c21aa2faf38385b11e757f6763
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721450"
---
# <a name="indexing-in-the-table"></a>Indizierung in der Tabelle


_**Gilt für:** Windows | Windows Server_

## <a name="indexing-in-the-table"></a>Indizierung in der Tabelle

Ein Index ist ein Satz von Schlüsselspalten, die eine persistente Reihenfolge von Datensätzen in einer Tabelle definieren. Datensätze sind Indexeinträge im primären Index. Ein primärer Index und mehrere sekundäre Indizes können definiert werden, um unterschiedliche Daten in der Tabelle zu erstellen.

Obwohl mehrere Indizes definiert werden können, werden die Datensätze physisch in B+-Strukturen in der vom primären Index angegebenen Reihenfolge gespeichert. Der primäre Index ist immer ein gruppierter Index und muss ebenfalls eindeutig sein. Der primäre Index muss vor dem ersten Tabellenupdate deklariert werden, um die Index reihenfolge bei erhalten. Wenn von der Anwendung kein primärer Index definiert wird, werden die Daten in der Reihenfolge gespeichert, in der der Tabelle Datensätze hinzugefügt werden. Dieser spezielle Index wird als sequenzieller Index bezeichnet.

Separate B+-Strukturen werden verwendet, um Datensätze nach dem sekundären Index zu bestellen. Indexeinträge im sekundären Index enthalten Zeiger auf die Daten, die gemäß dem primären Index gespeichert sind. Die Indexeinträge für Datensätze im primären Index müssen eindeutig sein, da der sekundäre Index mithilfe des Primärschlüssels des Datensatzes auf den Datensatz zeigt. Sekundäre Indizes verfügen möglicherweise über eine Eindeutigkeitseinschränkung. Weitere Informationen finden Sie im Thema [Datenbankübersicht.](./database-overview.md)
