---
description: 'Weitere Informationen finden Sie unter: Suchen von Datensätzen im Index.'
title: Durchsuchen von Datensätzen im Index
TOCTitle: Searching Records in the Index
ms:assetid: 9141b1d6-81b6-49ad-a5d4-2409fe0d511a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269342(v=EXCHG.10)
ms:contentKeyID: 32765631
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 57b8229c7f243c4a20bc3cd22cf285d58993a6371efc14620fe98bb8bf4620af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117703109"
---
# <a name="searching-records-in-the-index"></a>Durchsuchen von Datensätzen im Index


_**Gilt für:** Windows | Windows Server_

## <a name="searching-records-in-the-index"></a>Durchsuchen von Datensätzen im Index

Suchschlüssel werden erstellt, um nach einem einzelnen Eintrag oder einer Reihe von Einträgen in einem Index zu suchen. Suchschlüssel können nur für die Schlüsselspalten im Index erstellt werden und einen oder mehrere Spaltenwerte enthalten. Der Suchschlüssel wird mit einem einzelnen Aufruf oder einer Reihe von Aufrufen von [JetMakeKey](./jetmakekey-function.md)erstellt und kann mit [JetRetrikey](./jetretrievekey-function.md) mithilfe von JET_bitRetrieveCopy. Nachdem der Suchschlüssel erstellt wurde, kann er verwendet werden, um den Cursor in den Datensatz im Index zu verschieben.

Es gibt drei Methoden zum Suchen von Datensätzen in einer Tabelle:

1.  Suchen Sie nach einem einzelnen Indexeintrag. Erstellen Sie hierzu den Suchschlüssel mit [JetMakeKey,](./jetmakekey-function.md)und wechseln Sie dann mit [JetSeek](./jetseek-function.md)zu diesem Datensatz.

2.  Durchsuchen Sie den Indexdatensatz nach Datensatz. Datensätze können durch den Aufruf von [JetMove](./jetmove-function.md)nach dem anderen durch einen Datensatz durchlaufen werden. Der Cursor kann zum ersten Datensatz im Index verschoben werden, indem JET_MoveFirst *im cRow-Parameter* von [JetMove angegeben wird.](./jetmove-function.md) Auf die gleiche Weise kann der Cursor vorwärts, rückwärts oder zum letzten Eintrag im Index verschoben werden.

3.  Durchsuchen sie eine Gruppe von Datensätzen. Legen Sie hierzu einen Bereich von Indexeinträgen für die Suche fest, und wechseln Sie dann sequenziell durch die Datensätze. Weitere Informationen finden Sie im Abschnitt Suchen durch einen Satz von [Datensätzen]() dieses Themas.

### <a name="searching-through-a-set-of-records"></a>Durchsuchen einer Gruppe von Datensätzen

Das Diagramm zeigt den Cursor, der sich durch einen Bereich von Indexeinträgen bewegt, der durch Aufrufe von [JetSeek](./jetseek-function.md) und [JetSetIndexRange definiert wird.](./jetsetindexrange-function.md)

Verwenden Sie das folgende Verfahren, um einen Satz von Datensätzen in einem Index zu durchsuchen.

### <a name="to-search-a-set-of-records-in-an-index"></a>So durchsuchen Sie einen Satz von Datensätzen in einem Index

1.  Erstellen Sie den Suchschlüssel für den ersten Datensatz im Satz von Datensätzen, die mit [JetMakeKey durchsucht werden sollen.](./jetmakekey-function.md)

2.  Bewegen Sie den Cursor in den Datensatz, der im Suchschlüssel mit [JetSeek angegeben ist.](./jetseek-function.md)

3.  Erstellen Sie mit [JetMakeKey](./jetmakekey-function.md)einen weiteren Suchschlüssel für den letzten Indexeintrag im Bereich.

4.  Legen Sie den Indexbereich mit [JetSetIndexRange mithilfe](./jetsetindexrange-function.md) des in Schritt 3 erstellten Schlüssels fest.

5.  Rufen [Sie JetMove](./jetmove-function.md) auf, um sich sequenziell durch jeden Datensatz im Indexbereich zu bewegen, wie im folgenden Diagramm dargestellt.

![ESE_Documentation_IndexRange](images/Gg269342.ESE_Documentation_IndexRange(EXCHG.10).gif "ESE_Documentation_IndexRange")

Der Cursor im Diagramm kann sich hier nur durch den Bereich der Indizes bewegen, der im Aufruf von [JetSetIndexRange festgelegt wurde.](./jetsetindexrange-function.md) Wenn die Anwendung versucht, den Cursor über den Indexbereich hinaus zu verschieben, gibt ESE einen Fehler Jet_errNoCurrentRecord [jetmove zurück.](./jetmove-function.md) Beachten Sie, dass alle Navigationstypen mit diesem Cursor, die nicht zum nächsten oder vorherigen Datensatz navigieren, den Indexbereich abbrechen. Weitere Informationen finden Sie unter [JetSetIndexRange.](./jetsetindexrange-function.md)

Der typ der im *pvData-Parameter* für [JetMakeKey](./jetmakekey-function.md) eingegebenen Daten muss mit dem für die Spalte angegebenen Datentyp und den angegebenen Eigenschaften übereinstimmen. Beispielsweise ist der Aufruf von [JetMakeKey](./jetmakekey-function.md) mit dem im *pvData-Parameter* angegebenen "Ben Flock" für einen Spaltentyp JET_coltypText eine gültige Datentypüber übereinstimmung. Wenn Sie einen Suchschlüssel erstellen möchten, um zwischen den Namen "Ben Miller" und "Max. Aller" in einem Index zu suchen, verschieben Sie den Cursor in den Datensatz mit dem Namen "Ben Miller", indem Sie [JetSeek aufrufen.](./jetseek-function.md) Rufen [Sie JetMakeKey](./jetmakekey-function.md) ein zweites Mal auf, und geben Sie einen Zeiger auf eine Zeichenfolge an, die den Namen "Max Biss" enthält. Der Indexbereich wird so festgelegt, dass der Cursor im Aufruf von [JetSetIndexRange](./jetsetindexrange-function.md)zwischen den Namen "BenWert" und "Max. Aller" bewegt wird.
