---
description: Weitere Informationen finden Sie unter JetGrowDatabase-Funktion.
title: JetGrowDatabase-Funktion
TOCTitle: JetGrowDatabase Function
ms:assetid: d9719991-6c80-4dcb-a1d6-f0c7de61f459
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294109(v=EXCHG.10)
ms:contentKeyID: 32765724
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGrowDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 710e41b29c55ec435db6eb1b9e1536740819478e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479066"
---
# <a name="jetgrowdatabase-function"></a>JetGrowDatabase-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgrowdatabase-function"></a>JetGrowDatabase-Funktion

Die **JetGrowDatabase-Funktion** erweitert die Größe einer derzeit geöffneten Datenbank.

```cpp
    JET_ERR JET_API JetGrowDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          unsigned long cpg,
      __in          unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*Dbid*

Die Datenbank, die erweitert wird.

*Cpg*

Die gewünschte Größe der Datenbank in Seiten.

*pcpgReal*

Zeiger auf eine Zahl, die die Größe der Datenbank in Seiten nach dem API-Aufruf empfängt. Wenn der API-Aufruf fehlschlägt, sind die Inhalte von *pcpgReal* nicht definiert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errDiskFull</p> | <p>Es ist nicht genügend freier Speicherplatz auf dem Volume zum Ausführen des Verwächste-Vorgangs zur Verfügung.</p> | 
| <p>JET_errDiskIO</p> | <p>Von <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>wurde ein dateibezogener Fehler zurückgegeben. Weitere Informationen zu anderen dateibezogenen Fehlern, die möglicherweise zurückgegeben werden, finden Sie unter <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</p> | 



#### <a name="remarks"></a>Hinweise

Wenn **JetGrowDatabase** vor dem Einfügen großer Datenmengen aufgerufen wird, wird die Datenbankdatei in einem Vorgang größer. Dies verringert die Wahrscheinlichkeit, dass die Datenbankdatei auf Dateisystemebene fragmentiert wird, und verringert auch die Anzahl, mit der die Datenbankdatei wachsen muss. Das once-Anwachsen der Datenbankdatei kann schneller sein, als sie mehrmals zu wachsen.

Derzeit wird nur das Anwachsen der Datei unterstützt. Um eine Datei zu verkleinern, verwenden Sie das Defragmentierungsfeature des **esentutl.exe** Hilfsprogramms.

Informationen zum Festlegen der Größe einer nicht geöffneten Datenbank finden Sie unter [JetSetDatabaseSize](./jetsetdatabasesize-function.md).

Die Dateigröße passt möglicherweise nicht zur Anzahl der Seiten, die in *pcpgReal zurückgegeben werden.* Es gibt zwei zusätzliche reservierte Seiten, die möglicherweise nicht in *pcpgReal gezählt werden.*

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetSetDatabaseSize](./jetsetdatabasesize-function.md)
