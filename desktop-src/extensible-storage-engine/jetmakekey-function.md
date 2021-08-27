---
description: 'Weitere Informationen zu: JetMakeKey-Funktion'
title: JetMakeKey-Funktion
TOCTitle: JetMakeKey Function
ms:assetid: 8c1cff2f-2f24-4990-a9d8-fb4f822e50b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269329(v=EXCHG.10)
ms:contentKeyID: 32765619
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMakeKey
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a642a103d67b023fdf42aa532cc328964c7734a4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482846"
---
# <a name="jetmakekey-function"></a>JetMakeKey-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetmakekey-function"></a>JetMakeKey-Funktion

Die **JetMakeKey-Funktion** erstellt Suchschlüssel, die dann verwendet werden können, um einen Satz von Einträgen in einem Index anhand einiger einfacher Suchkriterien für ihre Schlüsselspaltenwerte zu finden. Ein Suchschlüssel ist auch eine der systeminternen Eigenschaften eines Cursors und wird von den [Vorgängen JetSeek](./jetseek-function.md) und [JetSetIndexRange](./jetsetindexrange-function.md) verwendet, um Indexeinträge zu suchen, die diesen Suchkriterien für den aktuellen Index dieses Cursors entsprechen. Ein vollständiger Suchschlüssel wird in einer Reihe von **JetMakeKey-Aufrufen** erstellt, wobei jeder Aufruf verwendet wird, um den Spaltenwert für die nächste Schlüsselspalte des aktuellen Indexes eines Cursors zu laden. Es ist auch möglich, einen zuvor erstellten Suchschlüssel zu laden, der mithilfe von [JetRetrieveKey](./jetretrievekey-function.md)aus dem Cursor abgerufen wurde.

```cpp
    JET_ERR JET_API JetMakeKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*pvData*

Der Eingabepuffer, der die Spaltendaten für die aktuelle Schlüsselspalte des aktuellen Indexes des Cursors enthält, für den der Suchschlüssel erstellt wird.

Der Datentyp der Spaltendaten im Eingabepuffer muss genau mit dem Datentyp und anderen Eigenschaften der Spaltendefinition der aktuellen Schlüsselspalte übereinstimmen. Es wird keine Typkoersion für die Spaltendaten ausgeführt.

Wenn JET_bitNormalizedKey im *grbit-Parameter* angegeben ist, muss der Eingabepuffer einen zuvor erstellten Suchschlüssel enthalten. Solche Schlüssel werden mithilfe eines Aufrufs von [JetRetrieveKey](./jetretrievekey-function.md)abgerufen.

*cbData*

Die Größe der im Eingabepuffer bereitgestellten Spaltendaten in Bytes.

Wenn JET_bitNormalizedKey im *grbit-Parameter* angegeben ist, entspricht dies der Größe des im Eingabepuffer bereitgestellten Suchschlüssels.

Wenn die Größe der Spaltendaten 0 (null) ist, wird der Inhalt des Eingabepuffers ignoriert. Wenn JET_bitKeyDataZeroLength im *grbit-Parameter* angegeben ist und die aktuelle Schlüsselspalte des aktuellen Index des Cursors eine Spalte variabler Länge ist, wird davon ausgegangen, dass es sich bei den Eingabespaltendaten um einen Wert der Länge 0 (null) handelt. Andernfalls wird davon ausgegangen, dass die Eingabespaltendaten ein NULL-Wert sind.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angibt.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitFullColumnEndLimit</p> | <p>Der Suchschlüssel sollte so erstellt werden, dass alle Schlüsselspalten, die nach der aktuellen Schlüsselspalte stammen, als Platzhalter betrachtet werden. Dies bedeutet, dass der konstruierte Suchschlüssel verwendet werden kann, um Indexeinträge abzugleichen, die Folgendes aufweisen:</p><ul><li><p>Die genauen Spaltenwerte, die für diese Schlüsselspalte und alle vorherigen Schlüsselspalten bereitgestellt werden.</p></li><li><p>Alle Spaltenwerte, die für nachfolgende Schlüsselspalten benötigt werden.</p></li></ul><p>Diese Option sollte beim Erstellen von Platzhaltersuchschlüsseln verwendet werden, die zum Suchen von Indexeinträgen verwendet werden sollen, die am nächsten am Ende eines Indexes liegen. Das Ende des Indexes ist der Indexeintrag, der beim Verschieben zum letzten Datensatz in diesem Index gefunden wird. Das Ende des Indexes ist nicht dasselbe wie das obere Ende des Indexes, das sich je nach Sortierreihenfolge der Schlüsselspalten im Index ändern kann.</p><p>Diese Option ist nur für Windows XP und höhere Versionen verfügbar.</p> | 
| <p>JETbitFullColumnStartLimit</p> | <p>Der Suchschlüssel sollte so konstruiert werden, dass alle Schlüsselspalten, die nach der aktuellen Schlüsselspalte stammen, als Platzhalter betrachtet werden sollten. Dies bedeutet, dass der konstruierte Suchschlüssel verwendet werden kann, um Indexeinträge abzugleichen, die Folgendes aufweisen:</p><ul><li><p>Die genauen Spaltenwerte, die für diese Schlüsselspalte und alle vorherigen Schlüsselspalten bereitgestellt werden.</p></li><li><p>Alle Spaltenwerte, die für nachfolgende Schlüsselspalten benötigt werden.</p></li></ul><p>Diese Option sollte beim Erstellen von Platzhaltersuchschlüsseln verwendet werden, die zum Suchen von Indexeinträgen verwendet werden sollen, die am nächsten am Anfang eines Indexes liegen. Der Anfang des Indexes ist der Indexeintrag, der beim Verschieben zum ersten Datensatz in diesem Index gefunden wird. Der Anfang des Indexes entspricht nicht dem unteren Indexende, das sich je nach Sortierreihenfolge der Schlüsselspalten im Index ändern kann.</p><p>Diese Option ist nur für Windows XP und höhere Versionen verfügbar.</p> | 
| <p>JET_bitKeyDataZeroLength</p> | <p>Wenn die Größe des Eingabepuffers 0 (null) und die aktuelle Schlüsselspalte eine Spalte variabler Länge ist, gibt diese Option an, dass der Eingabepuffer einen Längenwert von 0 (null) enthält. Andernfalls würde eine Eingabepuffergröße von 0 (null) einen NULL-Wert angeben.</p> | 
| <p>JET_bitNewKey</p> | <p>Ein neuer Suchschlüssel sollte erstellt werden. Alle zuvor vorhandenen Suchschlüssel werden verworfen.</p> | 
| <p>JET_bitNormalizedKey</p> | <p>Wenn diese Option angegeben wird, werden alle anderen Optionen ignoriert, alle zuvor vorhandenen Suchschlüssel verworfen, und der Inhalt des Eingabepuffers wird als neuer Suchschlüssel geladen.</p> | 
| <p>JET_bitPartialColumnEndLimit</p> | <p>Der Suchschlüssel sollte so konstruiert werden, dass die aktuelle Schlüsselspalte als Präfix-Platzhalter betrachtet wird und dass alle Schlüsselspalten, die nach der aktuellen Schlüsselspalte stehen, als Platzhalter betrachtet werden sollten. Dies bedeutet, dass der konstruierte Suchschlüssel verwendet werden kann, um Indexeinträge abzugleichen, die Folgendes aufweisen:</p><ul><li><p>Die genauen Spaltenwerte, die für diese Schlüsselspalte und alle vorherigen Schlüsselspalten bereitgestellt werden.</p></li><li><p>Alle Spaltenwerte, die für nachfolgende Schlüsselspalten benötigt werden.</p></li></ul><p>Diese Option sollte beim Erstellen von Platzhaltersuchschlüsseln verwendet werden, die zum Suchen von Indexeinträgen verwendet werden sollen, die am nächsten am Ende eines Indexes liegen. Das Ende des Indexes ist der Indexeintrag, der beim Verschieben zum letzten Datensatz in diesem Index gefunden wird. Das Ende des Indexes ist nicht dasselbe wie das obere Ende des Indexes, das sich je nach Sortierreihenfolge der Schlüsselspalten im Index ändern kann.</p><p>Diese Option kann nicht verwendet werden, wenn die aktuelle Schlüsselspalte keine Textspalte oder variable binäre Spalte ist. Der Vorgang schlägt mit JET_errInvalidgrbit fehl, wenn dies versucht wird.</p><p>Diese Option ist nur für Windows XP und höhere Versionen verfügbar.</p> | 
| <p>JET_bitPartialColumnStartLimit</p> | <p>Diese Option gibt an, dass der Suchschlüssel so konstruiert werden soll, dass die aktuelle Schlüsselspalte als Präfix-Platzhalter betrachtet wird und dass alle Schlüsselspalten, die nach der aktuellen Schlüsselspalte stehen, als Platzhalter betrachtet werden sollten. Dies bedeutet, dass der konstruierte Suchschlüssel verwendet werden kann, um Indexeinträge abzugleichen, die Folgendes aufweisen:</p><ul><li><p>Die genauen Spaltenwerte, die für diese Schlüsselspalte und alle vorherigen Schlüsselspalten bereitgestellt werden.</p></li><li><p>Alle Spaltenwerte, die für nachfolgende Schlüsselspalten benötigt werden.</p></li></ul><p>Diese Option sollte beim Erstellen von Platzhaltersuchschlüsseln verwendet werden, die zum Suchen von Indexeinträgen verwendet werden sollen, die am nächsten am Anfang eines Indexes liegen. Der Anfang des Indexes ist der Indexeintrag, der beim Verschieben zum ersten Datensatz in diesem Index gefunden wird. Der Anfang des Indexes entspricht nicht dem unteren Indexende, das sich je nach Sortierreihenfolge der Schlüsselspalten im Index ändern kann.</p><p>Diese Option kann nicht verwendet werden, wenn die aktuelle Schlüsselspalte keine Textspalte oder variable binäre Spalte ist. Der Vorgang schlägt mit JET_errInvalidgrbit fehl, wenn dies versucht wird.</p><p>Diese Option ist nur für Windows XP und höhere Versionen verfügbar.</p> | 
| <p>JET_bitStrLimit</p> | <p>Diese Option gibt an, dass der Suchschlüssel so konstruiert werden soll, dass alle Schlüsselspalten, die hinter der aktuellen Schlüsselspalte stehen, als Platzhalter betrachtet werden sollen. Dies bedeutet, dass der konstruierte Suchschlüssel verwendet werden kann, um Indexeinträge abzugleichen, die Folgendes aufweisen:</p><ul><li><p>Die genauen Spaltenwerte, die für diese Schlüsselspalte und alle vorherigen Schlüsselspalten bereitgestellt werden.</p></li><li><p>Alle Spaltenwerte, die für nachfolgende Schlüsselspalten benötigt werden.</p></li></ul><p>Diese Option sollte beim Erstellen von Platzhaltersuchschlüsseln verwendet werden, die zum Suchen von Indexeinträgen verwendet werden sollen, die am nächsten am Ende eines Indexes liegen. Das Ende des Indexes ist der Indexeintrag, der beim Verschieben zum letzten Datensatz in diesem Index gefunden wird. Das Ende des Indexes ist nicht dasselbe wie das obere Ende des Indexes, das sich je nach Sortierreihenfolge der Schlüsselspalten im Index ändern kann.</p><p>Wenn diese Option in Kombination mit JET_bitSubStrLimit angegeben wird und die aktuelle Schlüsselspalte eine Textspalte ist, wird diese Option ignoriert. Dieses Verhalten soll es ermöglichen, dass der Typ der aktuellen Schlüsselspalte beim Erstellen des Suchschlüssels abgeleitet wird.</p><p>Wenn Sie einen ähnlichen Suchschlüssel für den Anfang eines Indexes erstellen möchten, sollte ein ähnlicher Aufruf von <strong>JetMakeKey</strong> für die letzte Schlüsselspalte erfolgen, bei der es sich nicht um einen Platzhalter handelt, aber keine Platzhalteroptionen angegeben sind. Der Suchschlüssel befindet sich dann in einem geeigneten Zustand, der für eine solche Suche verwendet werden soll. Dies entspricht der Verwendung von JET_bitFullColumnStartLimit, mit dem Unterschied, dass der Suchschlüssel nicht wie nach der Verwendung einer Platzhalteroption sauber abgeschlossen ist.</p><p>Diese Option ist für Windows XP und höhere Versionen veraltet, um diese umständliche Semantik zu beheben. stattdessen sollten nach Möglichkeit JET_bitFullColumnStartLimit und JET_bitFullColumnEndLimit verwendet werden.</p> | 
| <p>JET_bitSubStrLimit</p> | <p>Diese Option gibt an, dass der Suchschlüssel so konstruiert werden soll, dass die aktuelle Schlüsselspalte als Präfix-Platzhalter betrachtet wird und dass alle Schlüsselspalten, die nach der aktuellen Schlüsselspalte stehen, als Platzhalter betrachtet werden sollten. Dies bedeutet, dass der konstruierte Suchschlüssel verwendet werden kann, um Indexeinträge abzugleichen, die Folgendes aufweisen:</p><ul><li><p>Die genauen Spaltenwerte, die für alle vorherigen Schlüsselspalten bereitgestellt werden.</p></li><li><p>Die angegebenen Spaltendaten als Präfix ihres Spaltenwerts für die aktuelle Schlüsselspalte.</p></li><li><p>Alle Spaltenwerte für nachfolgende Schlüsselspalten.</p></li></ul><p>Diese Option sollte beim Erstellen von Platzhaltersuchschlüsseln verwendet werden, die zum Suchen von Indexeinträgen verwendet werden sollen, die am nächsten am Ende eines Indexes liegen. Das Ende des Indexes ist der Indexeintrag, der beim Verschieben zum letzten Datensatz in diesem Index gefunden wird. Das Ende des Indexes ist nicht dasselbe wie das obere Ende des Indexes, das sich je nach Sortierreihenfolge der Schlüsselspalten im Index ändern kann.</p><p>Wenn diese Option in Kombination mit JET_bitStrLimit angegeben wird und die aktuelle Schlüsselspalte eine Textspalte ist, hat diese Option Vorrang. Diese Option wird ignoriert, wenn die aktuelle Schlüsselspalte keine Textspalte ist. Dieses Verhalten soll es ermöglichen, dass der Typ der aktuellen Schlüsselspalte beim Erstellen des Suchschlüssels abgeleitet wird.</p><p>Wenn Sie einen ähnlichen Suchschlüssel für den Anfang eines Indexes erstellen möchten, sollte ein ähnlicher Aufruf von <strong>JetMakeKey</strong> für die Schlüsselspalte erfolgen, die als Präfix-Platzhalter verwendet werden soll, wobei jedoch keine Platzhalteroptionen angegeben sind. Der Suchschlüssel befindet sich dann in einem geeigneten Zustand, der für eine solche Suche verwendet werden soll. Dies entspricht der Verwendung von JET_bitPartialColumnStartLimit, mit dem Unterschied, dass der Suchschlüssel nicht wie nach der Verwendung einer Platzhalteroption sauber abgeschlossen ist.</p><p>Diese Option ist für Windows XP und höhere Versionen veraltet, um diese umständliche Semantik zu beheben. stattdessen sollten nach Möglichkeit JET_bitPartialColumnStartLimit und JET_bitPartialColumnEndLimit verwendet werden.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errIndexTuplesKeyTooSmall</p> | <p>Die bereitgestellten Spaltendaten waren zu klein, um einen gültigen Schlüssel für den aktuellen Index zu erstellen, da dieser Index ein Tupelindex ist und die minimale Tupelgröße größer als die bereitgestellten Spaltendaten war. Weitere Informationen zu Tupelindizes finden Sie unter <a href="gg294099(v=exchg.10).md">JetCreateIndex.</a> Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Die bereitgestellten Spaltendaten stimmten nicht mit der größe überein, die für die Spaltendefinition erforderlich ist. Dies kann passieren, wenn der Datentyp der Spalte intrinsisch eine bestimmte Größe hat. Dies kann auch der Fall sein, wenn der Datentyp der Spalte nicht intrinsisch eine bestimmte Größe hat, die Definition der Spalte sie jedoch als feste Länge deklariert. Eine Ausnahme besteht darin, dass dieser Fehler nicht auftritt, wenn für eine Textspalte mit fester Länge zu wenig Daten bereitgestellt werden, da fehlende Daten automatisch mit Leerzeichen aufgefüllt werden. Eine zweite Ausnahme besteht darin, dass dieser Fehler nicht auftritt, wenn für eine binäre Spalte mit fester Länge zu wenig Daten bereitgestellt werden, da fehlende Daten automatisch mit Nullen aufgefüllt werden.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Eine der angeforderten Optionen war ungültig, wurde auf unzulässige Weise verwendet oder nicht implementiert. Dies kann für <strong>JetMakeKey</strong> passieren, wenn:</p><ul><li><p>JET_bitPartialColumnStartLimit oder JET_bitPartialColumnEndLimit angegeben werden, und die entsprechende Schlüsselspalte ist keine Textspalte und keine binäre Spalte variabler Länge. Dieser Fall tritt nur bei Windows XP und späteren Versionen auf.</p></li><li><p>Es wird versucht, mehrere der folgenden Optionen zusammen zu verwenden: JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit und JET_bitFullColumnEndLimit. Dieser Fall tritt nur bei Windows XP und späteren Versionen auf.</p></li><li><p>Es wird versucht, JET_bitStrLimit oder JET_bitSubStrLimit zu verwenden, wenn eine der folgenden Optionen verwendet wird: JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit und JET_bitFullColumnEndLimit. Dieser Fall tritt nur bei Windows XP und späteren Versionen auf.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war.</p><p>Dies kann für <strong>JetMakeKey</strong> passieren, wenn JET_bitNormalizedKey angegeben wurde und der im Eingabepuffer angegebene Wert zu groß war, um ein gültiger Suchschlüssel zu sein.</p> | 
| <p>JET_errKeyIsMade</p> | <p>Die für <strong>JetMakeKey</strong> bereitgestellten Spaltendaten wurden abgelehnt, da die Spaltendaten bereits für alle Schlüsselspalten im aktuellen Index bereitgestellt wurden. Dies kann auf drei Arten geschehen. Die erste Möglichkeit ist, wenn Spaltendaten für jede Schlüsselspalte im aktuellen Index bereitgestellt werden. Die zweite Möglichkeit ist, wenn Spaltendaten für mindestens eine Schlüsselspalte bereitgestellt wurden und eine Platzhalteroption für den letzten Aufruf ausgewählt wurde. Die dritte Möglichkeit besteht darin, dass ein zuvor erstellter Suchschlüssel mit JET_bitNormalizedKey bereitgestellt wurde, der alle Schlüsselspalten abdeckt.</p> | 
| <p>JET_errKeyNotMade</p> | <p>Es gibt keinen aktuellen Suchschlüssel für den Cursor. Dies geschieht für <strong>JetMakeKey,</strong> wenn JET_bitNewKey nicht angegeben ist und kein Suchschlüssel für diesen Cursor mit einem vorherigen Aufruf von <strong>JetMakeKey</strong>erstellt wurde. Der Suchschlüssel wird durch einen vorherigen Aufruf einer beliebigen Navigations-API auf dem Cursor außer <a href="gg294117(v=exchg.10).md">JetMove</a>gelöscht.</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>Es gibt keinen aktuellen Index für den Cursor. Dies geschieht für <strong>JetMakeKey,</strong> wenn sich der Cursor im gruppierten Index einer Tabelle befindet, kein primärer Index definiert wurde und JET_bitNormalizedKey nicht angegeben wurde. Es ist nicht möglich, einen Suchschlüssel zu erstellen, wenn sich der Cursor in einem Index befindet, der keine Schlüsselspalten aufweist, es sei denn, es wird ein zuvor konstruierter Suchschlüssel bereitgestellt.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Wenn bei Erfolg JET_bitNormalizedKey und JET_bitNewKey nicht angegeben wurden, wurde der Suchschlüssel durch die Suchkriterien für eine weitere Schlüsselspalte im aktuellen Index erstellt. Wenn JET_bitNormalizedKey nicht angegeben wurde und JET_bitNewKey angegeben wurde, wurde jeder zuvor vorhandene Suchschlüssel verworfen, und ein neuer Suchschlüssel wurde anhand der Suchkriterien für die erste Schlüsselspalte im aktuellen Index erstellt. Wenn JET_bitNormalizedKey angegeben wurde, wurde jeder zuvor vorhandene Suchschlüssel verworfen und ein neuer aus dem Eingabepuffer geladen. In jedem Fall erfolgt keine Änderung des Datenbankzustands.

Wenn bei einem Fehler JET_bitNormalizedKey oder JET_bitNewKey angegeben wurde, ist der Status des Suchschlüssels nicht definiert. Wenn weder JET_bitNormalizedKey noch JET_bitNewKey angegeben wurden, erfolgt keine Änderung des Status des Suchschlüssels. In jedem Fall erfolgt keine Änderung des Datenbankzustands.

#### <a name="remarks"></a>Hinweise

Schlüssel sollten als nicht transparente Datenblöcke behandelt werden. Es sollte nicht versucht werden, die interne Struktur dieser Daten auszunutzen. Folgendes ist jedoch über alle ESENT-Schlüssel bekannt:

  - Schlüssel können miteinander verglichen werden, indem [sie memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) verwenden, um ihre relative Reihenfolge im ursprünglichen Index über der Tabelle der Quellindexeinträge herzustellen.

  - Es ist bedeutungslos, Schlüssel von Indexeinträgen aus verschiedenen Indizes miteinander zu vergleichen.

  - Ein Schlüssel ist immer kleiner oder gleich JET_cbKeyMost (255) Bytes vor Windows Vista. Bei Windows Vista und höheren Versionen können die Schlüssel größer sein. Die maximale Größe eines Schlüssels entspricht dem aktuellen Wert von JET_paramKeyMost.

Suchschlüssel können ein Byte länger sein, wenn eine Platzhalteroption verwendet wurde. In diesem Fall beträgt der Suchschlüssel bis zu JET_cbLimitKeyMost (256) Bytes für Releases vor Windows Vista und JET_paramKeyMost + 1 Bytes für Windows Vista und höhere Versionen.

Diese maximale Schlüsselgröße hat eine sehr wichtige Bedeutung. Wenn ein Indexeintrag mit Spaltenwerten vorhanden ist, die groß genug sind, um die Generierung eines Schlüssels für diesen Index zu bewirken, der andernfalls größer als diese maximale Größe wäre, wird dieser Schlüssel automatisch bei dieser maximalen Größe abgeschnitten. Dies hat zwei Auswirkungen:

  - Bei Einträgen in einem eindeutigen Index werden Einträge, die andernfalls eindeutig sind, als Duplikate deklariert.

  - Bei Einträgen in allen Indizes führt das Abschneiden von Schlüsseln dazu, dass Indexeinträge, die andernfalls nicht den Suchkriterien eines bestimmten Suchschlüssels entsprechen, als Übereinstimmungen deklariert werden.

Anwendungen müssen diese Kürzung antizipieren und sie entweder vermeiden oder ihre Auswirkungen kompensieren. In Windows Vista wurde ein neues Indexflag JET_bitIndexDisallowTruncation hinzugefügt, um Anwendungen das Verhindern von Schlüsselkürzungen zu erleichtern. Weitere [](./jet-indexcreate-structure.md) Informationen zu dieser Indizierungsoption finden Sie in der JET_INDEXCREATE-Struktur.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetRetrikey](./jetretrievekey-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
