---
description: Weitere Informationen finden Sie unter JetSetDatabaseSize-Funktion.
title: JetSetDatabaseSize-Funktion
TOCTitle: JetSetDatabaseSize Function
ms:assetid: 4a87bf43-c8f7-4966-9f1f-68c16d1cb558
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269242(v=EXCHG.10)
ms:contentKeyID: 32765544
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetDatabaseSizeW
- JetSetDatabaseSize
- JetSetDatabaseSizeA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55a7625de4c8e1ef96740650313d3036cbb605f7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988863"
---
# <a name="jetsetdatabasesize-function"></a>JetSetDatabaseSize-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetdatabasesize-function"></a>JetSetDatabaseSize-Funktion

Die **JetSetDatabaseSize-Funktion** legt die Größe einer nicht öffnenden Datenbankdatei fest.

```cpp
    JET_ERR JET_API JetSetDatabaseSize(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseName,
      __in          unsigned long cpg,
      __out         unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Identifiziert den Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*szDatabaseName*

Identifiziert den Namen der Datenbankdatei, deren Größe geändert werden soll.

*Cpg*

Gibt die gewünschte Größe der Datenbank in Seiten an.

*pcpgReal*

Zeiger auf eine Zahl, die die Größe der Datenbank in Seiten nach dem API-Aufruf empfängt. Wenn der API-Aufruf nicht erfolgreich war, sind die Inhalte von *pcpgReal* nicht definiert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errDatabaseInconsistent<br />JET_errDatabaseDirtyShutdown</p> | <p>JET_errDatabaseInconsistent und JET_errDatabaseDirtyShutdown sind derselbe numerische Wert. Die Datenbank, deren Größe angepasst werden soll, muss sich in einem sauberen Herunterfahren (als konsistenter Zustand bezeichnet) befindet. Eine inkonsistente Datenbank ist nicht beschädigt, erfordert jedoch, dass Protokolldateien wiedergegeben werden.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p><em>szDatabaseName</em> darf keine leere Zeichenfolge sein, die nicht NULL ist.</p> | 
| <p>JET_errDiskFull</p> | <p>Es ist nicht genügend freier Speicherplatz auf dem Volume zum Ausführen des Verwächste-Vorgangs zur Verfügung. <strong>JetSetDatabaseSize gibt</strong> möglicherweise auch viele dateibezogene Fehler zurück, einschließlich, aber nicht beschränkt auf:</p><ul><li><p>JET_errDiskIO</p></li><li><p>JET_errFileNotFound</p></li><li><p>JET_errInvalidPath</p></li><li><p>JET_errFileAccessDenied</p></li><li><p>JET_errOutOfFileHandles</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Dieser Fehler kann unter anderem zurückgegeben werden, wenn <em>cpg</em> die Mindestgröße der Datenbank erfüllt. Die aktuelle minimale Datenbankgröße beträgt 256 Seiten.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Das System ist nicht genügend Arbeitsspeicherressourcen.</p> | 



#### <a name="remarks"></a>Bemerkungen

Wenn **JetSetDatabaseSize aufgerufen** wird, bevor große Datenmengen eingefügt werden, wird die Datenbankdatei in einem Vorgang größer. Dies verringert die Wahrscheinlichkeit, dass die Datenbankdatei auf Dateisystemebene fragmentiert wird, und verringert auch die Anzahl, mit der die Datenbankdatei wachsen muss. Das once-Anwachsen der Datenbankdatei kann schneller sein, als sie mehrmals zu wachsen.

Derzeit wird nur das Anwachsen der Datei unterstützt. Um eine Datei zu verkleinern, verwenden Sie die Defragmentierungsfunktion esentutl.exe Hilfsprogramm.

Wenn *cpg* kleiner als die aktuelle Größe der Datenbank ist, wird der Vorgang ignoriert. Wenn *cpg* kleiner als die minimale Datenbankgröße (derzeit 256 Seiten) ist, wird JET_errInvalidParameter.

Informationen zum Festlegen der Größe einer geöffneten Datenbank finden Sie unter [JetGrowDatabase](./jetgrowdatabase-function.md).

Die Dateigröße kann nicht mit der Anzahl der seiten übereinstimmen, die in *pcpgReal zurückgegeben werden.* Es gibt zwei zusätzliche reservierte Seiten, die möglicherweise nicht in *pcpgReal gezählt werden.*

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetSetDatabaseSizeW</strong> (Unicode) und <strong>JetSetDatabaseSizeA</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetGrowDatabase](./jetgrowdatabase-function.md)
