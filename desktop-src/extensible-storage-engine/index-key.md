---
description: 'Weitere Informationen finden Sie unter: Index Schlüssel'
title: Index Schlüssel
TOCTitle: Index Key
ms:assetid: 104bdb1c-71ac-44f4-bbda-c553131aaad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269188(v=EXCHG.10)
ms:contentKeyID: 32765491
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: eff0812f363fa83d133ab087140d415d8e2dbad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553283"
---
# <a name="index-key"></a>Index Schlüssel


_**Gilt für:** Windows | Windows Server_

## <a name="index-key"></a>Index Schlüssel

Ein Index wird für Daten in der Tabelle mit [jetkreateindex](./jetcreateindex-function.md) erstellt, oder es können mehrere Indizes gleichzeitig mit [JetCreateIndex2](./jetcreateindex2-function.md) erstellt werden, wobei die [JET_INDEXCREATE](./jet-indexcreate-structure.md) Struktur verwendet wird. Der Index wird in Form eines Spalten Arrays in der Rangfolge definiert. Dieses Spalten Array wird auch als Index Schlüssel bezeichnet. Der Index Schlüssel kann als primärer Index definiert werden, wenn die JET_bitIndexPrimary-Option im *grbit* -Parameter von [jetkreateindex](./jetcreateindex-function.md) oder [JET_INDEXCREATE](./jet-indexcreate-structure.md)festgelegt wird. Der Index Schlüssel ist eine NULL-terminierte Zeichenfolge von mit NULL endenden Token, wie im folgenden Beispiel gezeigt:

\+Col1 \\ 0-Col2 \\ 0 + Col3 \\ 0 \\ 0

Der Schlüssel im Beispiel kann verwendet werden, um einen Index über drei Spalten in der Tabelle zu erstellen. Jede im Index angegebene Spalte wird als "Index Segment" oder "Schlüssel Spalte" bezeichnet. Das Index Segment kann in Bezug auf den Bestell Beitrag entweder aufsteigend oder absteigend sein. Im obigen Beispiel ist der Name der ersten Spalte im Index col1. + Gibt an, dass col1 in aufsteigender Reihenfolge indiziert wird. – Before Col2 gibt an, dass die Indizierung in absteigender Reihenfolge erfolgt.

Wenn im Index bedingte Spalten vorhanden sind, wird die [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) Struktur verwendet, um anzugeben, wie Sie indiziert werden. Eine bedingte Spalte kann verwendet werden, um das vorhanden sein oder Fehlen eines Index Eintrags in einem Index auf der Grundlage des Werts in der entsprechenden Bedingungs Spalte zu steuern, ohne dass sich dies auf die Sortierreihenfolge des Indexes auswirkt. Eine bedingte Spalte kann einen Index Eintrag aus dem Index einschließen oder ausschließen, wenn der Wert dieser Bedingungs Spalte für den entsprechenden Datensatz NULL ist.

Standardmäßig wird die maximale Größe des Index Schlüssels durch die JET_cbKeyMost Konstante angegeben, bei der es sich immer um 255 Bytes normalisierter Daten (Bytes der Daten einschließlich des Indizierungs Aufwands) handelt. Ab Windows Vista kann die maximale Größe des Index Schlüssels mit der [JET_INDEXCREATE](./jet-indexcreate-structure.md) Struktur festgelegt werden. Die maximale Größe des Index Schlüssels entspricht der Größe der Datenbankseite. Um eine benutzerdefinierte maximale Schlüsselgröße zu aktivieren, geben Sie die Jet_bitIndexKeyMost-Option im grbits-Member von [JET_INDEXCREATE](./jet-indexcreate-structure.md)an, und legen Sie den **cbkeymost** -Member auf einen der folgenden Werte fest:

  - JET_cbKeyMost2KBytePage: Wenn die Größe der Datenbankseite 2048 Bytes beträgt, kann die maximale Index Schlüsselgröße zwischen mindestens 255 Bytes und maximal 500 Byte betragen.

  - JET_cbKeyMost4KBytePage: Wenn die Größe der Datenbankseite 4096 Bytes beträgt, kann die maximale Index Schlüsselgröße zwischen mindestens 255 Bytes und maximal 1000 Byte betragen.

  - JET_cbKeyMost8KBytePage: Wenn die Größe der Datenbankseite 8196 Bytes beträgt, kann die maximale Index Schlüsselgröße zwischen mindestens 255 Bytes und maximal 2000 Byte betragen.

Das Beispiel in der Abbildung unten zeigt eine Tabelle mit Mitarbeiter Informationen. Die Tabelle enthält 6 Spalten, von denen jedes ein bestimmtes Employee-Attribut definiert. Ein Datensatz in der Tabelle enthält Werte für einen Mitarbeiter, z. b. den Mitarbeiter Namen in Spalte 1 und die Mitarbeiter-ID in Spalte 2. Ein primärer Index, der für diese Tabelle erstellt wird, ordnet die Daten zuerst nach dem Mitarbeiter Namen und der Mitarbeiter-ID an. Sowohl Name als auch ID werden in aufsteigender Reihenfolge indiziert. Beispielsweise wird ein Datensatz mit dem Namen Johnson und Employee ID 12345 vor einem Datensatz mit dem Mitarbeiter Namen Jones und der ID 10000 aufgeführt. Alle Datensätze für Jones werden in der Tabelle mit ihren Mitarbeiter-IDs in aufsteigender Reihenfolge gespeichert, wie in der Tabelle dargestellt.

![ESE_Documentation_IndexTable](images/Gg269188.ESE_Documentation_IndexTable(EXCHG.10).gif "ESE_Documentation_IndexTable")

Der Schlüssel im primären Index muss eindeutig sein, aber die Schlüssel im sekundären Index können Duplikate sein. Wenn ein Index z. b. mit dem Nachnamen erstellt wird und in der Datenbank zwei Personen mit Stevens vorhanden sind, gibt ESE einen Jet_errKeyDuplicate Fehler von [jetupdate](./jetupdate-function.md) oder [JetUpdate2](./jetupdate2-function.md)zurück, wenn die Anwendung versucht, den zweiten "Stevens" einzufügen. Wenn der tatsächliche Schlüssel größer als die maximale Schlüsselgröße ist, wird der Schlüssel abgeschnitten. Das Durchsuchen und Eindeutigkeit der Schlüssel abkürzen wirkt sich auf die Verwendung durch die Anwendung aus. Wenn z. b. "Stevens" und "Stevenson" in einem Index über den Nachnamen gespeichert wurden und die maximale Schlüsselgröße zu klein ist, um den "on"-Teil von "Stevenson" zu speichern, würde die Schlüssel abkürzen dazu führen, dass "Stevens" und "Stevenson" dupliziert werden, auch wenn dies nicht der Fall ist. Die Anwendung muss so vorbereitet sein, dass Sie Fälle wie diese während der Suche und Aktualisierung verarbeitet, wenn die Index Definition und die von ihr indizierenden Spaltenwerte so lauten, dass die Schlüssel Abschneiden eine Möglichkeit ist. Ab Windows Vista können Anwendungen die Jet_bitIndexDisallowTruncation Option in [JET_INDEXCREATE](./jet-indexcreate-structure.md) oder [jetmakekey](./jetmakekey-function.md)angeben. Die Angabe dieses Flags führt dazu, dass ein Update des Indexes, das zu einem abgeschnittene Schlüssel führt, mit JET_errKeyTruncated fehlschlägt. Andernfalls werden Schlüssel automatisch abgeschnitten. Dadurch kann die Anwendung ohne Bedenken für die Artefakte funktionieren, die durch zuvor beschriebene Schlüssel abkürzen verursacht wurden.
