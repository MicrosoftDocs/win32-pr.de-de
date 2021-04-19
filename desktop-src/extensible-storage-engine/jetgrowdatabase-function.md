---
description: 'Weitere Informationen zu: jetgrowdatabase-Funktion'
title: Jetgrowdatabase-Funktion
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
ms.openlocfilehash: 9ed8ee9888a2e4ab7908b72cc071f7b8143ca6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348657"
---
# <a name="jetgrowdatabase-function"></a>Jetgrowdatabase-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgrowdatabase-function"></a>Jetgrowdatabase-Funktion

Die **jetgrowdatabase** -Funktion erweitert die Größe einer Datenbank, die derzeit geöffnet ist.

```cpp
    JET_ERR JET_API JetGrowDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          unsigned long cpg,
      __in          unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*DBID*

Die Datenbank, die erweitert wird.

*Verbrauchsgüter*

Die gewünschte Größe der Datenbank in Seiten.

*pcpgreal*

Zeiger auf eine Zahl, die die Größe der Datenbank in Seiten nach dem API-Befehl empfängt. Wenn der API-Rückruf fehlschlägt, ist der Inhalt von *pcpgreal* nicht definiert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDiskFull</p></td>
<td><p>Auf dem Volume ist nicht genügend freier Speicherplatz vorhanden, um die Vergrößerung auszuführen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskIO</p></td>
<td><p>Von <a href="gg269242(v=exchg.10).md">jetsetdatabasesize</a>wurde ein Datei bezogener Fehler zurückgegeben. Weitere Informationen zu anderen Datei bezogenen Fehlern, die zurückgegeben werden können, finden Sie unter <a href="gg269242(v=exchg.10).md">jetsetdatabasesize</a>.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Wenn **jetgrowdatabase** vor dem Einfügen großer Datenmengen aufgerufen wird, wird die Datenbankdatei in einem Vorgang vergrößert. Dadurch wird die Wahrscheinlichkeit verringert, dass die Datenbankdatei auf Dateisystem Ebene fragmentiert wird. Außerdem wird die Häufigkeit reduziert, mit der die Datenbankdatei vergrößert werden muss. Wenn Sie die Datenbankdatei einmal vergrößern, kann Sie schneller sein, als Sie mehrmals anwachsen.

Derzeit wird nur die Vergrößerung der Datei unterstützt. Um eine Datei zu verkleinern, verwenden Sie die Defragmentierungs Funktion des Programms **esentutl.exe** Hilfsprogramms.

Informationen zum Festlegen der Größe einer Datenbank, die nicht geöffnet wird, finden Sie unter [jetsetdatabasesize](./jetsetdatabasesize-function.md).

Die Dateigröße stimmt möglicherweise nicht mit der Anzahl der Seiten, die in *pcpgreal* zurückgegeben werden, ab. Es gibt zwei weitere reservierte Seiten, die möglicherweise nicht in *pcpgreal* gezählt werden.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[Jetsetdatabasesize](./jetsetdatabasesize-function.md)
