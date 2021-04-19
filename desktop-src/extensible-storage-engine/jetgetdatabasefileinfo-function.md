---
description: 'Weitere Informationen zu: jetgetdatabasefileingefo-Funktion'
title: Jetgetdatabasefilinput Info-Funktion
TOCTitle: JetGetDatabaseFileInfo Function
ms:assetid: 457079d9-46c9-4da0-a35b-0c11fca7ed5b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269239(v=EXCHG.10)
ms:contentKeyID: 32765541
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetDatabaseFileInfo
- JetGetDatabaseFileInfoW
- JetGetDatabaseFileInfoA
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2ac94dd6f088a82c932aaca5b60ec16f49644f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362778"
---
# <a name="jetgetdatabasefileinfo-function"></a>Jetgetdatabasefilinput Info-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetdatabasefileinfo-function"></a>Jetgetdatabasefilinput Info-Funktion

Die **jetgetdatabasefileinfo** -Funktion Ruft verschiedene Arten von Informationen über die Datenbank ab. Diese API kann aufgerufen werden, während eine Datenbank angefügt oder Online ist (mit [jetgetdatabaseinfo](./jetgetdatabaseinfo-function.md)) oder wenn die Datenbank oder Datenbank-Engine offline ist (mit **jetgetdatabasefileinfo**).

```cpp
    JET_ERR JET_API JetGetDatabaseFileInfo(
      __in          const tchar* szDatabaseName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parameter

*szdatabasename*

Der Pfad der Datenbank, aus der die Informationen abgerufen werden sollen.

*pvresult*

Zeiger auf einen Puffer, der die angegebenen Informationen empfängt. Die Größe des Puffers in Bytes wird in *cbmax* übermittelt.

Wenn diese Funktion fehlschlägt, ist der Inhalt von *pvresult* nicht definiert.

Die in *pvresult* gespeicherten Informationen hängen von *infolevel* ab.

*cbmax*

Die Größe (in Bytes) des Puffers, der in *pvresult* übergeben wird.

*Infolevel*

*Infolevel* gibt an, welche Art von Informationen über die angegebene Datenbank abgerufen werden sollen. Dies wirkt sich darauf aus, wie *pvresult* interpretiert wird. Einige *infolevel* -Objekte sind nur in der Offline Version (**jetgetdatabasefileinfo**) oder Online ([jetgetdatabaseinfo](./jetgetdatabaseinfo-function.md)) der API verfügbar.

Wenn der bereitgestellte *pvresult* -Puffer zu klein ist, werden je nach *infolevel* entweder JET_errInvalidBufferSize oder JET_errBufferTooSmall zurückgegeben.

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
<td><p>JET_DbInfoFilesize</p></td>
<td><p><em>pvresult</em> wird als QWORD (8 Bytes) interpretiert. Gibt die Größe der Datenbank in Bytes zurück.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoUpgrade</p></td>
<td><p><em>pvresult</em> wird als <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>interpretiert. Die <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> Struktur wird mit Informationen aufgefüllt, die sich auf die angegebene Datenbank beziehen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoMisc</p></td>
<td><p><em>pvresult</em> wird als <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>interpretiert. Die <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> Struktur wird mit Informationen aufgefüllt, die sich auf die angegebene Datenbank beziehen.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoDBInUse</p></td>
<td><p><em>pvresult</em> wird als bool (4 Bytes) interpretiert. Dadurch wird zurückgegeben, ob die Datenbank-Engine zurzeit über geöffnete oder angefügte Datenbanken verfügt.</p>
<p><strong>Windows XP:  </strong> Dieser Wert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoPageSize</p></td>
<td><p><em>pvresult</em> wird als Ganzzahl ohne Vorzeichen long interpretiert. Dadurch wird die Seitengröße der Datenbank in Bytes zurückgegeben.</p>
<p><strong>Windows XP:  </strong> Dieser Wert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCp</p></td>
<td><p>Diese <em>infolevels</em> werden noch nicht unterstützt, und es werden Standardwerte zurückgegeben. Verwenden Sie diese <em>infolevels</em>nicht.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoCountry</p></td>
<td><p>Diese <em>infolevels</em> werden noch nicht unterstützt, und es werden Standardwerte zurückgegeben. Verwenden Sie diese <em>infolevels</em>nicht.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCollate</p></td>
<td><p>Identisch mit JET_DbInfoCp.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoIsam</p></td>
<td><p>Diese <em>infolevels</em> sind veraltet und werden zurzeit nicht unterstützt. Verwenden Sie diese <em>infolevels</em>nicht.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoConnect</p></td>
<td><p>Identisch mit JET_DbInfoIsam.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoFileType</p></td>
<td><p><strong>Windows Vista:  </strong> Dieser <em>infolevel</em> -Wert wird in Windows Vista eingeführt.</p>
<p><em>pvresult</em> wird als Zeiger auf ein DWORD behandelt. Gibt einen Enumerationswert zurück, der angibt, welche Art von Datei das Modul als ist. Dateitypen sind in der folgenden Tabelle aufgeführt. Weitere Informationen zu diesen Dateitypen und deren Verwendung für die-Engine finden Sie unter <a href="gg294069(v=exchg.10).md">Extensible Storage Engine Files</a>.</p>
<div class="tableSection">
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
<td><p>JET_filetypeUnknown</p></td>
<td><p>Der Dateityp ist unbekannt, oder es handelt sich nicht um einen ESE-Dateityp.</p></td>
</tr>
<tr class="even">
<td><p>JET_filetypeDatabase</p></td>
<td><p>Bei der Datei handelt es sich um eine Datenbankdatei.</p></td>
</tr>
<tr class="odd">
<td><p>JET_filetypeLog</p></td>
<td><p>Bei der Datei handelt es sich um eine Transaktionsprotokoll Datei.</p></td>
</tr>
<tr class="even">
<td><p>JET_filetypeCheckpoint</p></td>
<td><p>Die Datei ist eine Prüf Punkt Datei.</p></td>
</tr>
<tr class="odd">
<td><p>JET_filetypeTempDatabase</p></td>
<td><p>Die Datei ist eine temporäre Datenbankdatei.</p></td>
</tr>
</tbody>
</table>

</div></td>
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
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Die angeforderte <em>infolevel</em> wurde JET_DbInfoIsam. Dieser Vorgang wird nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Der in <em>cbmax</em> angegebene Puffer ist zu klein für die gewünschten Informationen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Der in <em>cbmax</em> angegebene Puffer weist nicht die richtige Größe für die gewünschten Informationen auf.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der Parameter, die bereitgestellt wurden, enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte hat ein unerwartetes Ergebnis zurückgegeben. Dieser Fehler wird von <a href="gg294076(v=exchg.10).md">jetgetdatabaseinfo</a> zurückgegeben, wenn es sich bei der bereitgestellten DBID nicht um eine gültige (angefügte) Datenbank handelt. Dieser Fehler wird von <strong>jetgetdatabasefileinfo</strong> und <a href="gg294076(v=exchg.10).md">jetgetdatabaseinfo</a> zurückgegeben, wenn ein angefordertes <em>infolevel</em> von dieser Version der Funktion nicht unterstützt wird.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, werden die angeforderten Daten im Ausgabepuffer zurückgegeben.

Wenn diese Funktion fehlschlägt, befindet sich der Ausgabepuffer in einem nicht definierten Zustand.

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
<td><p>Implementiert als <strong>jetgetdatabasefileingefow</strong> (Unicode) und <strong>jetgetdatabasefileingefoa</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[Jetgetdatabaseingefo](./jetgetdatabaseinfo-function.md)
