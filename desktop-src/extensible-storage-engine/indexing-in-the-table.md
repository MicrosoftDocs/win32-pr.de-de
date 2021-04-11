---
description: 'Weitere Informationen: Indizierung in der Tabelle'
title: Indizierung in der Tabelle
TOCTitle: Indexing in the Table
ms:assetid: d86c2c6b-d001-468d-ab74-937911b0036d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294106(v=EXCHG.10)
ms:contentKeyID: 32765721
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 5d09fde8c5fcdcf2411f6d40c5a3a70912bed27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041855"
---
# <a name="indexing-in-the-table"></a>Indizierung in der Tabelle


_**Gilt für:** Windows | Windows Server_

## <a name="indexing-in-the-table"></a>Indizierung in der Tabelle

Ein Index ist ein Satz von Schlüssel Spalten, die eine persistente Reihenfolge von Datensätzen in einer Tabelle definieren. Datensätze sind Indexeinträge im primären Index. Ein primärer Index und mehrere sekundäre Indizes können definiert werden, um unterschiedliche Datenreihen in der Tabelle zu erstellen.

Obwohl mehrere Indizes definiert werden können, werden die Datensätze physisch in B +-Bäumen in der vom primären Index angegebenen Reihenfolge gespeichert. Der primäre Index ist immer ein gruppierter Index und muss auch eindeutig sein. Der primäre Index muss vor der ersten Tabellen Aktualisierung deklariert werden, um die Index Reihenfolge beizubehalten. Wenn kein primärer Index von der Anwendung definiert wird, werden die Daten in der Reihenfolge gespeichert, in der die Datensätze der Tabelle hinzugefügt werden. Dieser spezielle Index wird als sequenzieller Index bezeichnet.

Separate B +-Strukturen werden verwendet, um Datensätze entsprechend dem sekundären Index zu sortieren. Index Einträge im sekundären Index enthalten Zeiger auf die Daten, die gemäß dem primären Index gespeichert werden. Die Indexeinträge für Datensätze im primären Index müssen eindeutig sein, da der sekundäre Index mit dem Primärschlüssel des Datensatzes auf den Datensatz verweist. Sekundäre Indizes verfügen möglicherweise über eine Eindeutigkeits Einschränkung. Weitere Informationen finden Sie im Thema [Übersicht über die Datenbank](./database-overview.md) .
