---
description: 'Weitere Informationen zu: jetgetdatabaseingefo-Funktion'
title: JetGetDatabaseInfo-Funktion
TOCTitle: JetGetDatabaseInfo Function
ms:assetid: bd3f92d0-7e98-4aa6-87c5-1c2760cbd1b5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294076(v=EXCHG.10)
ms:contentKeyID: 32765691
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81c414a1dd38f621ba86bf7b1c9ce87710801446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216296"
---
# <a name="jetgetdatabaseinfo-function"></a>JetGetDatabaseInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetdatabaseinfo-function"></a>JetGetDatabaseInfo-Funktion

Die **jetgetdatabaseinfo** -Funktion Ruft verschiedene Arten von Informationen über die Datenbank ab. Diese API kann aufgerufen werden, während eine Datenbank angefügt oder Online ist (mit **jetgetdatabaseinfo**) oder wenn die Datenbank oder Datenbank-Engine offline ist (mit [jetgetdatabasefileinfo](./jetgetdatabasefileinfo-function.md)).

```cpp
    JET_ERR JET_API JetGetDatabaseInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*DBID*

Die [JET_DBID](./jet-dbid.md) für die Datenbank, aus der die Informationen abgerufen werden sollen.

*pvresult*

Zeiger auf einen Puffer, der die angegebenen Informationen empfängt. Die Größe des Puffers in Bytes wird in *cbmax* übermittelt.

Bei einem Fehler ist der Inhalt von *pvresult* nicht definiert.

Die in *pvresult* gespeicherten Informationen hängen von *infolevel* ab.

*cbmax*

Die Größe (in Bytes) des Puffers, der in *pvresult* übergeben wurde.

*Infolevel*

*Infolevel* gibt an, welche Art von Informationen über die angegebene Datenbank abgerufen werden sollen. Dies wirkt sich darauf aus, wie *pvresult* interpretiert wird. Einige *infolevel* sind nur in der Offline Version ([jetgetdatabasefileinfo](./jetgetdatabasefileinfo-function.md)) oder Online (**jetgetdatabaseinfo**) der API verfügbar.

Wenn der bereitgestellte *pvresult* -Puffer zu klein ist, wird entweder JET_errInvalidBufferSize oder JET_errBufferTooSmall abhängig von *infolevel* zurückgegeben.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_DbInfoCollate</p></td>
<td><p>Wird noch nicht unterstützt und gibt Standardwerte zurück. Darf nicht verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoConnect</p></td>
<td><p>Diese <em>infolevels</em> sind veraltet und werden zurzeit nicht unterstützt. Darf nicht verwendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoCountry</p></td>
<td><p>Wird noch nicht unterstützt und gibt Standardwerte zurück. Darf nicht verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCp</p></td>
<td><p>Wird noch nicht unterstützt und gibt Standardwerte zurück. Darf nicht verwendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoFilename</p></td>
<td><p><em>pvresult</em> wird als Zeichen folgen Puffer (Char *) interpretiert. Es wird ein MAX_PATH Puffer vorgeschlagen, jedoch nicht erforderlich. Wenn der Puffer nicht lang genug ist, werden JET_errBufferTooSmall zurückgegeben. Die Zeichenfolge wird mit dem Pfad der Datenbank für diese DBID aufgefüllt.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoFilesize</p></td>
<td><p><em>pvresult</em> wird als DWORD (4 Bytes) interpretiert. Gibt die Größe der Datenbank auf Seiten zurück.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoIsam</p></td>
<td><p>Diese <em>infolevels</em> sind veraltet und werden zurzeit nicht unterstützt. Darf nicht verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoLCID</p></td>
<td><p>(Windows XP und höher) Diese <em>infolevel</em> wurde ursprünglich wie folgt angegeben: JET_DbInfoLangid (Windows 2000)</p>
<p><em>pvresult</em> wird als Long interpretiert. Dadurch wird der mit dieser Datenbank verknüpfte Gebiets Schema Bezeichner (LCID) zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoMisc</p></td>
<td><p><em>pvresult</em> wird als <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>interpretiert. Die <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> Struktur wird mit Informationen zu der angegebenen Datenbank aufgefüllt.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoOptions</p></td>
<td><p><em>pvresult</em> wird als <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD) interpretiert. Hiermit wird zurückgegeben, ob die Datenbank im exklusiven Modus geöffnet wird. Wenn sich die Datenbank im exklusiven Modus befindet JET_bitDbExclusive in der bereitgestellten <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> festgelegt werden, andernfalls wird 0 (null) festgelegt. Beachten Sie, dass keine anderen Datenbank- <em>grbit</em> -Optionen für <a href="gg294074(v=exchg.10).md">jetattachdatabase</a> und <a href="gg269299(v=exchg.10).md">jetopendatabase</a> zurückgegeben werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoPageSize</p></td>
<td><p>Nur unter Windows XP und höher verfügbar. <em>pvresult</em> wird als Ganzzahl ohne Vorzeichen long interpretiert. Dadurch wird die Seitengröße der Datenbank in Bytes zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoSpaceAvailable</p></td>
<td><p><em>pvresult</em> wird als DWORD interpretiert. Dadurch wird der verfügbare Speicherplatz für die Datenbank auf Seiten zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoSpaceOwned</p></td>
<td><p><em>pvresult</em> wird als DWORD interpretiert. Dadurch wird der im Besitz befindliche Speicherplatz für die Datenbank auf Seiten zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoTransactions</p></td>
<td><p><em>pvresult</em> wird als Long interpretiert. Dadurch wird ein Wert zurückgegeben, der größer ist als die maximale Ebene, auf die Transaktionen eingefügt werden können. Wenn <a href="gg294083(v=exchg.10).md">jetbegintransaction</a> (Schachtelungs Weise, d. h. in derselben Sitzung, ohne Commit oder Rollback) so oft wie dieser Wert aufgerufen wird, wird beim letzten Aufruf JET_errTransTooDeep von <a href="gg294083(v=exchg.10).md">jetbegintransaction</a>zurückgegeben. Beachten Sie, dass der Wert in Windows 2000, Windows XP und Windows Server 2003 7 ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoVersion</p></td>
<td><p><em>pvresult</em> wird als Long interpretiert. Dadurch wird die native Hauptversion der Datenbank-Engine zurückgegeben. Dieser Wert ist 0x620 für Windows 2000, Windows XP und Windows Server 2003.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Die Größe des in <em>cbmax</em> angegebenen Puffers war zu klein (oder nicht korrekt), um die gewünschten Informationen zu speichern.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Die angeforderte <em>infolevel</em> wurde JET_DbInfoIsam. Dieser Vorgang wird nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Die Größe des in <em>cbmax</em> angegebenen Puffers war zu klein (oder nicht korrekt), um die gewünschten Informationen zu speichern.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde. Dieser Fehler wird von <strong>jetgetdatabaseingefo</strong> zurückgegeben, wenn der bereitgestellte <a href="gg269248(v=exchg.10).md">JET_DBID</a> keine gültige (angefügte) Datenbank ist. Dieser Fehler wird von <a href="gg269239(v=exchg.10).md">jetgetdatabasefileinfo</a> und <strong>jetgetdatabaseinfo</strong> zurückgegeben, wenn ein angefordertes <em>infolevel</em> von dieser Version der Funktion nicht unterstützt wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg werden die angeforderten Daten im Ausgabepuffer zurückgegeben.

Bei einem Fehler befindet sich der Ausgabepuffer in einem nicht definierten Zustand.

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
<td><p>Implementiert als <strong>jetgetdatabasanfow</strong> (Unicode) und <strong>jetgetdatabaseingefoa</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[Jetgetdatabasefileingefo](./jetgetdatabasefileinfo-function.md)
