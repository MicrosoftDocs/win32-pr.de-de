---
description: Weitere Informationen finden Sie unter JetGetDatabaseFileInfo-Funktion.
title: JetGetDatabaseFileInfo-Funktion
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
ms.openlocfilehash: b19d783480a8d82485bce32689b8d49e046b0285
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623506"
---
# <a name="jetgetdatabasefileinfo-function"></a>JetGetDatabaseFileInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetdatabasefileinfo-function"></a>JetGetDatabaseFileInfo-Funktion

Die **JetGetDatabaseFileInfo-Funktion** ruft verschiedene Arten von Informationen über die Datenbank ab. Diese API kann aufgerufen werden, während eine Datenbank angefügt oder online ist (mit [JetGetDatabaseInfo)](./jetgetdatabaseinfo-function.md)oder während die Datenbank oder Datenbank-Engine offline ist (mit **JetGetDatabaseFileInfo**).

```cpp
    JET_ERR JET_API JetGetDatabaseFileInfo(
      __in          const tchar* szDatabaseName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parameter

*szDatabaseName*

Der Pfad der Datenbank, aus der die Informationen abgerufen werden sollen.

*pvResult*

Zeiger auf einen Puffer, der die angegebenen Informationen empfängt. Die Größe des Puffers in Bytes wird in *cbMax* übergeben.

Wenn diese Funktion fehlschlägt, ist der Inhalt von *pvResult* nicht definiert.

Die in *pvResult* gespeicherten Informationen hängen von *InfoLevel ab.*

*cbMax*

Die Größe des in *pvResult* übergebenen Puffers in Bytes.

*InfoLevel*

*InfoLevel* gibt an, welcher Informationstyp über die angegebene Datenbank abgerufen werden soll. Dies wirkt sich darauf aus, wie *pvResult* interpretiert wird. Einige *InfoLevel-Objekte* sind nur in der Offlineversion **(JetGetDatabaseFileInfo)** oder online ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) der API verfügbar.

Wenn der *bereitgestellte pvResult-Puffer* zu klein ist, werden je nach *InfoLevel* entweder JET_errInvalidBufferSize oder JET_errBufferTooSmall zurückgegeben.

<table>
<colgroup>
<col  />
<col  />
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
<td><p><em>pvResult</em> wird als QWORD (8 Bytes) interpretiert. Gibt die Größe der Datenbank in Bytes zurück.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoUpgrade</p></td>
<td><p><em>pvResult</em> wird als <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>interpretiert. Die <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE-Struktur</a> wird mit Informationen zur angegebenen Datenbank aufgefüllt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoMisc</p></td>
<td><p><em>pvResult</em> wird als <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>interpretiert. Die <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC-Struktur</a> wird mit Informationen zur angegebenen Datenbank aufgefüllt.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoDBInUse</p></td>
<td><p><em>pvResult</em> wird als BOOL (4 Bytes) interpretiert. Dadurch wird zurückgegeben, ob die Datenbank-Engine derzeit über geöffnete oder angefügte Datenbanken verfügt.</p>
<p><strong>Windows XP:</strong> Dieser Wert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoPageSize</p></td>
<td><p><em>pvResult</em> wird als unsigned long interpretiert. Dadurch wird die Seitengröße der Datenbank in Bytes zurückgegeben.</p>
<p><strong>Windows XP:</strong> Dieser Wert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCp</p></td>
<td><p>Diese <em>InfoLevels</em> werden noch nicht unterstützt und geben Standardwerte zurück. Verwenden Sie diese <em>InfoLevels</em>nicht.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoCountry</p></td>
<td><p>Diese <em>InfoLevels</em> werden noch nicht unterstützt und geben Standardwerte zurück. Verwenden Sie diese <em>InfoLevels</em>nicht.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCollate</p></td>
<td><p>Entspricht JET_DbInfoCp.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoIsam</p></td>
<td><p>Diese <em>InfoLevels</em> sind veraltet und werden derzeit nicht unterstützt. Verwenden Sie diese <em>InfoLevels</em>nicht.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoConnect</p></td>
<td><p>Entspricht JET_DbInfoIsam.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoFileType</p></td>
<td><p><strong>Windows Vista:</strong> Dieser <em>InfoLevel-Wert</em> wird in Windows Vista eingeführt.</p>
<p><em>pvResult</em> wird als Zeiger auf ein DWORD behandelt. Gibt einen Enumerationswert zurück, der angibt, welche Art von Datei die Engine als solche ansieht. Dateitypen sind in der folgenden Tabelle aufgeführt. Weitere Informationen zu diesen Dateitypen und deren Verwendung für die Engine finden Sie unter <a href="gg294069(v=exchg.10).md">Extensible Storage Engine Files</a>.</p>
<div class="tableSection">
<table>
<colgroup>
<col  />
<col  />
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
<td><p>Der Dateityp ist unbekannt oder kein ESE-Dateityp.</p></td>
</tr>
<tr class="even">
<td><p>JET_filetypeDatabase</p></td>
<td><p>Die Datei ist eine Datenbankdatei.</p></td>
</tr>
<tr class="odd">
<td><p>JET_filetypeLog</p></td>
<td><p>Die Datei ist eine Transaktionsprotokolldatei.</p></td>
</tr>
<tr class="even">
<td><p>JET_filetypeCheckpoint</p></td>
<td><p>Die Datei ist eine Prüfpunktdatei.</p></td>
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

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col  />
<col  />
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
<td><p>Das angeforderte <em>InfoLevel</em> wurde JET_DbInfoIsam. Dieser Vorgang wird nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Der in <em>cbMax</em> angegebene Puffer ist für die gewünschten Informationen zu klein.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Der in <em>cbMax</em> angegebene Puffer ist nicht die richtige Größe für die gewünschten Informationen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte führte zu einem unerwarteten Ergebnis. Dieser Fehler wird von <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> zurückgegeben, wenn die bereitgestellte DBID-Datenbank keine gültige (angefügte) Datenbank ist. Dieser Fehler wird von <strong>JetGetDatabaseFileInfo</strong> und <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> zurückgegeben, wenn ein angefordertes <em>InfoLevel</em> von dieser Version der Funktion nicht unterstützt wird.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, werden die angeforderten Daten im Ausgabepuffer zurückgegeben.

Wenn diese Funktion fehlschlägt, befindet sich der Ausgabepuffer in einem nicht definierten Zustand.

#### <a name="requirements"></a>Requirements (Anforderungen)

<table>
<colgroup>
<col  />
<col  />
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
<td><p><strong>DLL</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Wird als <strong>JetGetDatabaseFileInfoW</strong> (Unicode) und <strong>JetGetDatabaseFileInfoA</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)
