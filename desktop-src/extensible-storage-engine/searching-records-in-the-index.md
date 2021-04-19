---
description: 'Weitere Informationen finden Sie unter: Durchsuchen von Datensätzen im Index'
title: Durchsuchen von Datensätzen im Index
TOCTitle: Searching Records in the Index
ms:assetid: 9141b1d6-81b6-49ad-a5d4-2409fe0d511a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269342(v=EXCHG.10)
ms:contentKeyID: 32765631
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 89a4ffe1f1c13280f236442ae218580fa5699741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349269"
---
# <a name="searching-records-in-the-index"></a>Durchsuchen von Datensätzen im Index


_**Gilt für:** Windows | Windows Server_

## <a name="searching-records-in-the-index"></a>Durchsuchen von Datensätzen im Index

Suchschlüssel werden erstellt, um nach einem einzelnen Eintrag oder einer Gruppe von Einträgen in einem Index zu suchen. Suchschlüssel können nur für die Schlüssel Spalten im Index erstellt werden und enthalten möglicherweise einen oder mehrere Spaltenwerte. Der Suchschlüssel wird mit einem einzigen Aufruf oder einer Reihe von Aufrufen von [jetmakekey](./jetmakekey-function.md)erstellt und kann mit [jetretrievekey](./jetretrievekey-function.md) mithilfe von JET_bitRetrieveCopy abgerufen werden. Nachdem der Suchschlüssel erstellt wurde, kann er verwendet werden, um den Cursor in den Datensatz im Index zu verschieben.

Es gibt drei Methoden zum Suchen von Datensätzen in einer Tabelle:

1.  Suchen Sie nach einem einzelnen Index Eintrag. Erstellen Sie hierzu den Suchschlüssel mit [jetmakekey](./jetmakekey-function.md), und fahren Sie dann mit [JetSeek](./jetseek-function.md)mit diesem Datensatz fort.

2.  Durchsuchen Sie den Index Datensatz-für-Datensatz. Datensätze können jeweils durch einen Aufruf von [jetmove](./jetmove-function.md)durchsucht werden. Der Cursor kann in den ersten Datensatz im Index verschoben werden, indem JET_MoveFirst im " *cRow* "-Parameter von [jetmove](./jetmove-function.md)angegeben wird. Auf dieselbe Weise kann der Cursor vorwärts, rückwärts oder zum letzten Eintrag im Index verschoben werden.

3.  Durchsuchen Sie eine Reihe von Datensätzen. Legen Sie zu diesem Zweck einen Bereich von Indexeinträgen für die Suche fest, und verschieben Sie die Datensätze nacheinander. Weitere Informationen finden Sie im Abschnitt [Durchsuchen eines Satzes von Datensätzen]() in diesem Thema.

### <a name="searching-through-a-set-of-records"></a>Durchsuchen eines Satzes von Datensätzen

Das Diagramm zeigt den Cursor, der durch einen Bereich von Indexeinträgen bewegt wird, die durch Aufrufe von [JetSeek](./jetseek-function.md) und [jetsetindexrange](./jetsetindexrange-function.md)definiert werden.

Verwenden Sie das folgende Verfahren, um einen Satz von Datensätzen in einem Index zu durchsuchen.

### <a name="to-search-a-set-of-records-in-an-index"></a>So durchsuchen Sie eine Gruppe von Datensätzen in einem Index

1.  Erstellen Sie den Suchschlüssel für den ersten Datensatz in der Gruppe von Datensätzen, die mit [jetmakekey](./jetmakekey-function.md)gesucht werden sollen.

2.  Bewegen Sie den Cursor in den Datensatz, der im Suchschlüssel mit [JetSeek](./jetseek-function.md)angegeben ist.

3.  Erstellen Sie einen weiteren Suchschlüssel für den letzten Index Eintrag im Bereich mit [jetmakekey](./jetmakekey-function.md).

4.  Legen Sie den Index Bereich mit [jetsetindexrange](./jetsetindexrange-function.md) fest, indem Sie den in Schritt 3 erstellten Schlüssel verwenden.

5.  Nennen Sie [jetmove](./jetmove-function.md) , um sequenziell durch jeden Datensatz im Index Bereich zu wechseln, wie im folgenden Diagramm dargestellt.

![ESE_Documentation_IndexRange](images/Gg269342.ESE_Documentation_IndexRange(EXCHG.10).gif "ESE_Documentation_IndexRange")

Der Cursor im Diagramm kann sich nur durch den Index Bereich bewegen, der im Aufrufen von [jetsetindexrange](./jetsetindexrange-function.md)festgelegt ist. Wenn die Anwendung versucht, den Cursor über den Index Bereich hinaus zu bewegen, gibt ESE einen Jet_errNoCurrentRecord Fehler vom [jetmove](./jetmove-function.md)-Befehl zurück. Beachten Sie, dass jeder Typ der Navigation mit diesem Cursor, der nicht zum nächsten oder vorherigen Datensatz wechselt, den Index Bereich abbricht. Weitere Informationen finden Sie unter [jetsetindexrange](./jetsetindexrange-function.md) .

Der Typ der Daten, die im *pvData* -Parameter für [jetmakekey](./jetmakekey-function.md) eingegeben werden, muss mit dem Typ der Daten und Eigenschaften, die für die Spalte angegeben werden, identisch sein. Beispielsweise ist der Aufruf von [jetmakekey](./jetmakekey-function.md) mit "Ben Miller" im *pvData* -Parameter für einen Spaltentyp JET_coltypText eine gültige Datentyp Übereinstimmung. Wenn Sie einen Suchschlüssel erstellen möchten, um zwischen den Namen "Ben Miller" und "Max Stevens" in einem Index zu suchen, verschieben Sie den Cursor durch Aufrufen von [JetSeek](./jetseek-function.md)in den Datensatz mit dem Namen "Ben Miller". Nennen Sie [jetmakekey](./jetmakekey-function.md) ein zweites Mal, und geben Sie einen Zeiger auf eine Zeichenfolge mit dem Namen "Max Stevens" an. Der Index Bereich wird so festgelegt, dass der Cursor auf den Wechsel zwischen den Namen "Ben Miller" und "Max Stevens" im " [jetsetindexrange](./jetsetindexrange-function.md)"-Befehl beschränkt wird.
