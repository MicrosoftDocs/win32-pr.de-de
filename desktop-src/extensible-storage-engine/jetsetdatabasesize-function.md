---
description: 'Weitere Informationen zu: JetSetDatabaseSize-Funktion'
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
ms.openlocfilehash: 6759508e42b380f0c1987c2f69b422baf4025d58b0de3c503fdae6d55c15df09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118071955"
---
# <a name="jetsetdatabasesize-function"></a>JetSetDatabaseSize-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetdatabasesize-function"></a>JetSetDatabaseSize-Funktion

Die **JetSetDatabaseSize-Funktion** legt die Größe einer ungeöffneten Datenbankdatei fest.

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

Gibt den Namen der Datenbankdatei an, deren Größe geändert werden soll.

*Cpg*

Gibt die gewünschte Größe der Datenbank in Seiten an.

*pcpgReal*

Zeiger auf eine Zahl, die die Größe der Datenbank in Seiten nach dem API-Aufruf empfängt. Wenn der API-Aufruf nicht erfolgreich war, ist der Inhalt von *pcpgReal* nicht definiert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>JET_errDatabaseInconsistent und JET_errDatabaseDirtyShutdown sind derselbe numerische Wert. Die Datenbank, deren Größe angepasst werden soll, muss sich in einem sauberen Herunterfahren befinden, das als konsistenter Zustand bezeichnet wird. Eine inkonsistente Datenbank ist nicht beschädigt, erfordert jedoch, dass Protokolldateien wiedergegeben werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p><em>szDatabaseName</em> darf keine leere Zeichenfolge ungleich NULL sein.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDiskFull</p></td>
<td><p>Es ist nicht genügend freier Speicherplatz auf dem Volume vorhanden, um den Zuwachsvorgang auszuführen. <strong>JetSetDatabaseSize</strong> kann auch viele dateibezogene Fehler zurückgeben, einschließlich, aber nicht beschränkt auf:</p>
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
<td><p>Einer der Gründe, warum dieser Fehler zurückgegeben werden kann, ist, wenn <em>cpg</em> die minimale Datenbankgröße erfüllt. Die aktuelle Minimale Datenbankgröße beträgt 256 Seiten.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Die Arbeitsspeicherressourcen des Systems sind gering.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Hinweise

Wenn **JetSetDatabaseSize** vor dem Einfügen großer Datenmengen aufgerufen wird, wird die Datenbankdatei in einem Vorgang vergrößert. Dies verringert die Wahrscheinlichkeit, dass die Datenbankdatei auf Dateisystemebene fragmentiert wird, und die Anzahl der Erweiterungen der Datenbankdatei. Das einmalige Anwachsen der Datenbankdatei kann schneller sein, als sie mehrmals zu erhöhen.

Derzeit wird nur das Anwachsen der Datei unterstützt. Um eine Datei zu verkleinern, verwenden Sie das Defragmentierungsfeature des Hilfsprogramms esentutl.exe.

Wenn *cpg* kleiner als die aktuelle Größe der Datenbank ist, wird der Vorgang ignoriert. Wenn *cpg* kleiner als die minimale Datenbankgröße (derzeit 256 Seiten) ist, wird JET_errInvalidParameter zurückgegeben.

Informationen zum Festlegen der Größe einer geöffneten Datenbank finden Sie unter [JetGrowDatabase.](./jetgrowdatabase-function.md)

Die Dateigröße stimmt möglicherweise nicht mit der Anzahl der seiten überein, die in *pcpgReal* zurückgegeben werden. Es gibt zwei zusätzliche reservierte Seiten, die in *pcpgReal* möglicherweise nicht gezählt werden.

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
<td><p>Deklariert in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Wird als <strong>JetSetDatabaseSizeW</strong> (Unicode) und <strong>JetSetDatabaseSizeA</strong> (ANSI) implementiert.</p></td>
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
[JetGrowDatabase](./jetgrowdatabase-function.md)
