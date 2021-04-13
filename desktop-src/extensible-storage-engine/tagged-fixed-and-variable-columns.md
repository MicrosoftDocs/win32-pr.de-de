---
description: 'Weitere Informationen finden Sie unter: markierte, fixierte und Variablen Spalten.'
title: Markierte, fixierte und Variablen Spalten
TOCTitle: Tagged, Fixed and Variable Columns
ms:assetid: 78a905b8-71a9-4b2e-b9f2-c81bfe3aef8e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269304(v=EXCHG.10)
ms:contentKeyID: 32765595
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 3f27237c5f75874f7320f675affe20f3833084b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484870"
---
# <a name="tagged-fixed-and-variable-columns"></a>Markierte, fixierte und Variablen Spalten


_**Gilt für:** Windows | Windows Server_

## <a name="tagged-fixed-and-variable-columns"></a>Markierte, fixierte und Variablen Spalten

Die Spalten "markiert", "Fixed" und "Variable Länge" sind die von ESE unterstützten primären Spaltentypen. Markierte Spalten sind nicht in einem Datensatz vorhanden, es sei denn, die Daten werden in der Spalte gespeichert und können eine fest oder eine Variable Länge aufweisen. Markierte Spalten können auch mehrere Werte in einem einzelnen Datensatz enthalten. Bei Fixed-Spalten wird die gleiche Menge an Speicherplatz in jeder Zeile benötigt, und es ist ein Bit erforderlich, um den NULL-Wert darzustellen. Spalten variabler Länge erfordern 2 Bytes, um die Größe und den NULL-Wert darzustellen, und belegen in jedem Datensatz eine Variable Menge an Speicherplatz. Weitere Informationen zu den markierten und fixierten Spalten finden Sie in der Jet_bitColumnTagged-und Jet_bitColumnFixed-Option im **grbit** -Member [JET_COLUMNDEF](./jet-columndef-structure.md) Struktur, die im Befehl [jetaddcolumn](./jetaddcolumn-function.md)verwendet wird.

Spalten variabler Länge werden durch den Spaltentyp bestimmt, der im *coltionparameter* im Befehl [jetaddcolumn](./jetaddcolumn-function.md)festgelegt wird. Abhängig davon, ob die Jet_bitColumnFixed-Option festgelegt ist, können die folgenden Spaltentypen fest oder eine Variable Länge aufweisen:

  - JET_coltypBinary

  - JET_coltypText

  - JET_coltypLongBinary

  - JET_coltypLongText

Im Allgemeinen werden die Daten im Datensatz zunächst mit dem festgelegten Bereich, dem Variablen Bereich Next und dem zuletzt gespeicherten markierten Bereich gespeichert. Das folgende Diagramm zeigt, wie die Datensätze in der-Tabelle gespeichert werden. Wie im Diagramm gezeigt, kann der markierte Bereich Spalten mit mehreren Werten enthalten.

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")
