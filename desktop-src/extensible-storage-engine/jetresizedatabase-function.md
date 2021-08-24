---
description: Weitere Informationen finden Sie unter JetResizeDatabase-Funktion.
title: JetResizeDatabase-Funktion
TOCTitle: JetResizeDatabase Function
ms:assetid: b6420de7-acff-480e-838b-f0e5acc29c65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835047(v=EXCHG.10)
ms:contentKeyID: 49894669
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetResizeDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dd7faf1a28d6cafe7b33e4df49f32c631bb699e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477526"
---
# <a name="jetresizedatabase-function"></a>JetResizeDatabase-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetResizeDatabase-Funktion** erweitert oder verkleinert die Größe einer derzeit geöffneten Datenbank.

Die **JetResizeDatabase-Funktion** wurde im Windows 8 eingeführt.

``` c++
JET_ERR JET_API JetResizeDatabase(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          unsigned long cpg,
  __out         unsigned long* pcpgActual,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*Dbid*

Die Datenbank, die erweitert wird.

*Cpg*

Die angeforderte Größe der Datenbank in Seiten.

*pcpgActual*

Ein Zeiger auf eine Zahl, die die Größe der Datenbank in Seiten nach dem API-Aufruf empfängt. Wenn der API-Aufruf fehlschlägt, ist der Inhalt des *parameters pcpgActual* nicht definiert.

*grbit*

Eine Gruppe von Bits, die null oder mehr der in der folgenden Tabelle aufgeführten Werte angibt.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitResizeDatabaseOnlyGrow</p> | <p>Verwächst nur die Datenbank. Wenn der Aufruf zum Ändern der Größe die Datenbank verkleinert, unternehmen Sie nichts.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der in der folgenden Tabelle aufgeführten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errDiskFull</p> | <p>Es ist nicht genügend freier Speicherplatz auf dem Volume zum Ausführen des Verwächste-Vorgangs zur Verfügung.</p> | 
| <p>JET_errDiskIO</p> | <p>Von der <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize-Funktion</a> wurde ein dateibezogener Fehler zurückgegeben. Weitere Informationen zu anderen dateibezogenen Fehlern, die möglicherweise zurückgegeben werden, finden Sie unter <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</p> | 



#### <a name="remarks"></a>Hinweise

Wenn die **JetResizeDatabase-Funktion** vor dem Einfügen großer Datenmengen aufgerufen wird, wird die Datenbankdatei in einem Vorgang größer. Dies verringert die Wahrscheinlichkeit, dass die Datenbankdatei auf Dateisystemebene fragmentiert wird, und verringert auch die Anzahl, mit der die Datenbankdatei wachsen muss. Das once-Anwachsen der Datenbankdatei kann schneller sein, als sie mehrmals zu wachsen.

Informationen zum Festlegen der Größe einer nicht geöffneten Datenbank finden Sie unter [JetSetDatabaseSize](./jetsetdatabasesize-function.md).

Die Dateigröße passt möglicherweise nicht zur Anzahl der Seiten, die im *pcpgReal-Parameter zurückgegeben* werden. Zwei zusätzliche reservierte Seiten werden im parameter *pcpgReal möglicherweise nicht* gezählt.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows 8.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2012.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetSetDatabaseSize](./jetsetdatabasesize-function.md)
