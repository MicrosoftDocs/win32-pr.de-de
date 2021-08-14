---
description: 'Weitere Informationen zu: Markierte, feste und variable Spalten'
title: Markierte, feste und variable Spalten
TOCTitle: Tagged, Fixed and Variable Columns
ms:assetid: 78a905b8-71a9-4b2e-b9f2-c81bfe3aef8e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269304(v=EXCHG.10)
ms:contentKeyID: 32765595
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: af2ab8ece57342f211b0dd4488b6feb25b191c1977ae39038fb61ea56f20d543
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118484741"
---
# <a name="tagged-fixed-and-variable-columns"></a>Markierte, feste und variable Spalten


_**Gilt für:** Windows | Windows Server_

## <a name="tagged-fixed-and-variable-columns"></a>Markierte, feste und variable Spalten

Markierte Spalten, Spalten variabler Länge und fester Länge sind die primären Spaltentypen, die von ESE unterstützt werden. Markierte Spalten sind nicht in einem Datensatz vorhanden, es sei denn, daten werden in der Spalte gespeichert und können eine feste oder variable Länge aufweisen. Markierte Spalten können auch mehr als einen Wert in einem einzelnen Datensatz enthalten. Feste Spalten benötigen in jeder Zeile die gleiche Menge an Speicherplatz und benötigen 1 Bit, um den NULL-Wert darzustellen. Spalten variabler Länge erfordern 2 Bytes, um die Größe und den NULL-Wert darzustellen, und belegen eine variable Menge an Speicherplatz in jedem Datensatz. Weitere Informationen zu den markierten und festen Spalten finden Sie unter der option Jet_bitColumnTagged und Jet_bitColumnFixed im **grbit-Member** der [JET_COLUMNDEF](./jet-columndef-structure.md) Struktur, die im Aufruf von [JetAddColumn](./jetaddcolumn-function.md)verwendet wird.

Spalten variabler Länge werden durch den Spaltentyp bestimmt, der im *coltyp-Parameter* beim Aufruf von [JetAddColumn](./jetaddcolumn-function.md)festgelegt wird. Die folgenden Spaltentypen können eine feste oder variable Länge aufweisen, je nachdem, ob die option Jet_bitColumnFixed festgelegt ist:

  - JET_coltypBinary

  - JET_coltypText

  - JET_coltypLongBinary

  - JET_coltypLongText

Im Allgemeinen werden Daten im Datensatz mit dem festen Bereich zuerst, dem Variablenbereich als nächstem und dem zuletzt gespeicherten markierten Bereich gespeichert. Das folgende Diagramm zeigt, wie die Datensätze in der Tabelle gespeichert werden. Wie im Diagramm dargestellt, kann der markierte Bereich Spalten mit mehreren Werten enthalten.

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")
