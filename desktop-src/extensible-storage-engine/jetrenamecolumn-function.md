---
description: Weitere Informationen finden Sie unter JetRenameColumn-Funktion.
title: JetRenameColumn-Funktion
TOCTitle: JetRenameColumn Function
ms:assetid: 30967765-355b-417c-b0d6-8b59e677cc98
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269218(v=EXCHG.10)
ms:contentKeyID: 32765521
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameColumn
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c60418a0723214b2d2312ebe67a4f47184814e0a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470237"
---
# <a name="jetrenamecolumn-function"></a>JetRenameColumn-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetrenamecolumn-function"></a>JetRenameColumn-Funktion

Die **JetRenameColumn-Funktion** kann verwendet werden, um den Namen einer vorhandenen Spalte in einer Tabelle zu ändern.

**Windows XP:****JetRenameColumn** wird in Windows XP eingeführt.  

```cpp
    JET_ERR JET_API JetRenameColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szName,
      __in          JET_PCSTR szNameNew,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*Szname*

Der aktuelle Name der Spalte, die umbenannt wird.

*szNameNew*

Der neue Name für die Spalte, die umbenannt wird.

*grbit*

Dieser Parameter muss 0 sein.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errColumnNotFound</p> | <p>Diese angegebene Spalte ist für diese Tabelle nicht vorhanden.</p> | 
| <p>JET_errInvalidName</p> | <p>Einer der angegebenen Objektnamen war ungültig. Alle Objektnamen müssen demselben Satz von Regeln entsprechen. Nachfolgend sind diese Regeln aufgeführt:</p><ul><li><p>Objektnamen müssen aus ASCII-Zeichen bestehen.</p></li><li><p>Objektnamen müssen mindestens ein Zeichen lang sein.</p></li><li><p>Objektnamen dürfen die Länge JET_cbNameMost (64) Zeichen nicht überschreiten.</p></li><li><p>Objektnamen dürfen nicht mit einem Leerzeichen beginnen. Objektnamen enthalten möglicherweise keine ASCII-Steuerzeichen (0x00 bis 0x1F).</p></li><li><p>Objektnamen dürfen kein Ausrufezeichen (!), Punkt (.), linke Klammer ([) oder rechte Klammer (]) enthalten.</p></li><li><p>Nach der Überprüfung wird nur der Teil der Zeichenfolge bis zum ersten Leerzeichen (falls möglich) für den Objektnamen verwendet. Dies bedeutet, dass Objektnamen möglicherweise auch kein Leerzeichen enthalten.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <strong>JetRenameColumn passieren, wenn:</strong></p><ul><li><p><em>szName</em> ist NULL.</p></li><li><p><em>szNameNew</em> ist NULL.</p></li></ul> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInTransaction</p> | <p>Dieser Vorgang kann nur ausgeführt werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Ein Update kann nicht innerhalb des Bereichs einer schreibgeschützten Transaktion ausgeführt werden. Eine schreibgeschützte Transaktion ist eine Transaktion, die mit einem Aufruf von <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> mit JET_bitTransactionReadOnly. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 



Bei Erfolg wird der Name der angegebenen Spalte in der Tabelle, die dem Cursor zugeordnet ist, dauerhaft in den neuen Namen geändert. Alle Indizes, die auf diese Spalte verweisen, werden ebenfalls aktualisiert.

Bei einem Fehler erfolgt keine Änderung des Datenbankstatus.

#### <a name="remarks"></a>Hinweise

Der Umbenennungsvorgang für Spalten ist ungewöhnlich, da er im Gegensatz zu anderen Schemavorgängen nicht als Transaktion ausgeführt wird. Wenn eine Spalte in einer bestimmten Tabelle in einer Sitzung umbenannt wird, wird jede andere Sitzung, die diese Tabelle verwendet, sofort die Änderung sehen, selbst wenn sie sich in einer Transaktion befinden, die verhindert, dass diese Sitzung andere Änderungen sieht, die von der Sitzung vorgenommen werden, die den Umbenennungsvorgang vor sich geht.

Die Spalten-ID einer Spalte ist vom Umbenennungsvorgang nicht betroffen.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetRenameColumnW</strong> (Unicode) und <strong>JetRenameColumnA</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)
