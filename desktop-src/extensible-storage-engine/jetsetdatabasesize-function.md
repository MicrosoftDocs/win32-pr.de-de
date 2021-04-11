---
description: 'Weitere Informationen zu: jetsetdatabasesize-Funktion'
title: Jetsetdatabasesize-Funktion
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
ms.openlocfilehash: cd450a0afed0256b0b80d97a278dccf99418a900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128152"
---
# <a name="jetsetdatabasesize-function"></a>Jetsetdatabasesize-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetdatabasesize-function"></a>Jetsetdatabasesize-Funktion

Die **jetsetdatabasesize** -Funktion legt die Größe einer nicht geöffneten Datenbankdatei fest.

```cpp
    JET_ERR JET_API JetSetDatabaseSize(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseName,
      __in          unsigned long cpg,
      __out         unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Identifiziert den Daten Bank Sitzungs Kontext, der für den API-Befehl verwendet werden soll.

*szdatabasename*

Identifiziert den Namen der Datenbankdatei, deren Größe geändert werden soll.

*Verbrauchsgüter*

Gibt die gewünschte Größe der Datenbank in Seiten an.

*pcpgreal*

Zeiger auf eine Zahl, die die Größe der Datenbank in Seiten nach dem API-Befehl empfängt. Wenn der API-Befehl nicht erfolgreich war, ist der Inhalt von *pcpgreal* nicht definiert.

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
<td><p>JET_errDatabaseInconsistent<br />
JET_errDatabaseDirtyShutdown</p></td>
<td><p>JET_errDatabaseInconsistent und JET_errDatabaseDirtyShutdown haben denselben numerischen Wert. Die Datenbank, deren Größe angepasst werden soll, muss sich in einem sauberen Herunterfahren befinden, das als einheitlicher Zustand bezeichnet wird. Eine inkonsistente Datenbank ist nicht beschädigt, erfordert jedoch, dass Protokolldateien wiedergegeben werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p><em>szdatabasename</em> darf keine leere Zeichenfolge sein, die nicht NULL ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDiskFull</p></td>
<td><p>Auf dem Volume ist nicht genügend freier Speicherplatz vorhanden, um die Vergrößerung auszuführen. <strong>Jetsetdatabasesize</strong> kann auch eine Vielzahl von Datei bezogenen Fehlern zurückgeben, einschließlich, aber nicht beschränkt auf:</p>
<ul>
<li><p>JET_errDiskIO</p></li>
<li><p>JET_errFileNotFound</p></li>
<li><p>JET_errInvalidPath</p></li>
<li><p>JET_errFileAccessDenied</p></li>
<li><p>JET_errOutOfFileHandles</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Dieser Fehler kann zurückgegeben werden, wenn <em>Verbrauchsgüter</em> die minimale Datenbankgröße erreicht. Die aktuelle minimale Datenbankgröße beträgt 256 Seiten.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Das System verfügt nicht über genügend Arbeitsspeicher Ressourcen.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Wenn **jetsetdatabasesize** aufgerufen wird, bevor große Datenmengen eingefügt werden, wird die Datenbankdatei in einem Vorgang vergrößert. Dadurch wird die Wahrscheinlichkeit verringert, dass die Datenbankdatei auf Dateisystem Ebene fragmentiert wird. Außerdem wird die Häufigkeit reduziert, mit der die Datenbankdatei vergrößert werden muss. Wenn Sie die Datenbankdatei einmal vergrößern, kann Sie schneller sein, als Sie mehrmals anwachsen.

Derzeit wird nur die Vergrößerung der Datei unterstützt. Um eine Datei zu verkleinern, verwenden Sie die Defragmentierungs Funktion des Programms esentutl.exe Hilfsprogramms.

Wenn *Verbrauchsgüter* kleiner als die aktuelle Größe der Datenbank ist, wird der Vorgang ignoriert. Wenn *Verbrauchsgüter* kleiner ist als die minimale Datenbankgröße (derzeit 256 Seiten), wird JET_errInvalidParameter zurückgegeben.

Informationen zum Festlegen der Größe einer Datenbank, die geöffnet wird, finden Sie unter [jetgrowdatabase](./jetgrowdatabase-function.md).

Die Dateigröße entspricht möglicherweise nicht der Anzahl der Seiten, die in *pcpgreal* zurückgegeben werden. Es gibt zwei weitere reservierte Seiten, die möglicherweise nicht in *pcpgreal* gezählt werden.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>jetsetdatabasesizew</strong> (Unicode) und <strong>jetsetdatabasesizea</strong> (ANSI).</p></td>
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
[Jetgrowdatabase](./jetgrowdatabase-function.md)
