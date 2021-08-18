---
description: 'Weitere Informationen finden Sie unter: Markierte, feste und variable Spalten'
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

Markierte Spalten, feste Spalten und Spalten variabler Länge sind die primären Spaltentypen, die von ESE unterstützt werden. Markierte Spalten sind in einem Datensatz nur vorhanden, wenn Daten in der Spalte gespeichert werden und eine feste oder variable Länge haben können. Markierte Spalten können auch mehr als einen Wert in einem einzelnen Datensatz enthalten. Feste Spalten nehmen dieselbe Menge an Speicherplatz in jeder Zeile an und erfordern 1 Bit, um den NULL-Wert darstellen zu können. Spalten variabler Länge erfordern 2 Bytes, um die Größe und den NULL-Wert darstellen zu können, und belegen eine variable Menge an Speicherplatz in jedem Datensatz. Weitere Informationen zu den markierten und festen Spalten finden Sie unter der Option Jet_bitColumnTagged und Jet_bitColumnFixed im **grbit-Member** der [JET_COLUMNDEF-Struktur,](./jet-columndef-structure.md) der im Aufruf von [JetAddColumn verwendet wird.](./jetaddcolumn-function.md)

Spalten variabler Länge werden durch den Spaltentyp bestimmt, der im *Coltyp-Parameter* im Aufruf von [JetAddColumn festgelegt wird.](./jetaddcolumn-function.md) Die folgenden Spaltentypen können eine feste oder variable Länge haben, je nachdem, ob die Jet_bitColumnFixed festgelegt ist:

  - JET_coltypBinary

  - JET_coltypText

  - JET_coltypLongBinary

  - JET_coltypLongText

Im Allgemeinen werden die Daten im Datensatz zuerst mit dem festen Bereich, dem variablen Bereich next und dem zuletzt gespeicherten markierten Bereich gespeichert. Das folgende Diagramm zeigt, wie die Datensätze in der Tabelle gespeichert werden. Wie im Diagramm dargestellt, kann der markierte Bereich Spalten mit mehreren Werten enthalten.

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")
