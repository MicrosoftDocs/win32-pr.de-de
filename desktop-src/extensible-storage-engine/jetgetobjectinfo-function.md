---
description: 'Weitere Informationen zu: jetgetobjectinfo-Funktion'
title: JetGetObjectInfo-Funktion
TOCTitle: JetGetObjectInfo Function
ms:assetid: 3e069c61-6dab-4b79-8bf2-7844d017598f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269232(v=EXCHG.10)
ms:contentKeyID: 32765534
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetObjectInfo
- JetGetObjectInfoA
- JetGetObjectInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf4c3c9806d4dcf898d6daeb903eb6fc4322fee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358945"
---
# <a name="jetgetobjectinfo-function"></a>JetGetObjectInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetobjectinfo-function"></a>JetGetObjectInfo-Funktion

Die **jetgetobjectinfo** -Funktion Ruft Informationen zu Datenbankobjekten ab. Derzeit werden nur Tabellen unterstützt. [Jetgettableinfo](./jetgettableinfo-function.md) kann zum Abrufen von mehr Informationen als **jetgetobjectinfo** verwendet werden.

```cpp
    JET_ERR JET_API JetGetObjectInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_OBJTYP objtyp,
      __in_opt      const tchar* szContainerName,
      __in_opt      const tchar* szObjectName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Der zu verwendende Daten Bank Sitzungs Kontext.

*DBID*

Die Datenbank, aus der die Informationen abgerufen werden.

*objyp*

Die-Objekte, die Informationen enthalten, die abgerufen werden sollen. Derzeit werden nur JET_objtypNil und JET_objtypTable unterstützt, die beide identisch sind. Es werden nur Tabellen abgerufen.

*szcontainername*

Dieser Parameter ist für die zukünftige Verwendung reserviert und übergibt **null**. Der Name der Objekttypen, für die Informationen abgerufen werden sollen.

*szobjectname*

Der Name des Objekts, das Informationen enthält, die abgerufen werden sollen. Wenn *infolevel* die Optionen JET_ObjInfoList oder JET_ObjInfoListNoStats verwendet, um eine Liste aller Objekte abzurufen, muss dieser Wert **null** oder eine leere Zeichenfolge sein.

Zurzeit werden nur Tabellennamen unterstützt.

*pvresult*

Zeiger auf einen Puffer, der die angegebenen Informationen empfängt.

Die Größe des Puffers in Bytes wird in *cbmax* übermittelt. Bei einem Fehler ist der Inhalt von *pvresult* nicht definiert.

Die in *pvresult* gespeicherten Informationen hängen von *infolevel* ab.

*cbmax*

Die Größe (in Bytes) des Puffers, der in *pvresult* übergeben wird.

*Infolevel*

Gibt an, welche Art von Informationen für das angegebene Objekt abgerufen werden sollen. Dies wirkt sich darauf aus, wie *pvresult* interpretiert wird.

Die folgenden Optionen können für diesen Parameter festgelegt werden.

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
<td><p>JET_ObjInfo</p></td>
<td><p><em>pvresult</em> wird als <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> Struktur interpretiert.</p>
<p>Die <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> -Struktur wird mit Informationen zu dem Objekt aufgefüllt, das in <em>szobjectname</em>benannt ist.</p>
<p>Wenn der Aufrufer nicht die Anzahl der Datensätze und Seiten für das Objekt kennen möchte, sollten Sie JET_ObjInfoNoStats Informationsebene verwenden, die möglicherweise schneller ist, da keine Statistik enthalten ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoList</p></td>
<td><p><em>pvresult</em> wird als <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> Struktur interpretiert. Informationen zu allen Objekten werden abgerufen. Es wird eine temporäre Tabelle erstellt, und die Informationen, die für die Durchführung der temporären Tabelle erforderlich sind, werden in der <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> Struktur beschrieben. Weitere Informationen finden Sie unter <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>. Wenn der Aufrufer nicht die Anzahl der Datensätze und Seiten für das Objekt kennen möchte, sollten Sie JET_ObjInfoListNoStats verwenden, die möglicherweise schneller ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoListACM</p></td>
<td><p>Veraltet und wird derzeit nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoListNoStats</p></td>
<td><p><em>pvresult</em> wird als <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> Struktur interpretiert. Informationen zu allen Objekten werden abgerufen. Es wird eine temporäre Tabelle erstellt, und die Informationen, die für die Durchführung der temporären Tabelle erforderlich sind, werden in der <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> Struktur beschrieben. Weitere Informationen finden Sie unter <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>. JET_ObjInfoListNoStats ist mit JET_ObjInfoList identisch, mit der Ausnahme, dass die Spalten, die die Anzahl von Datensätzen (<em>columnidcrecord</em>) und Pages (<em>columnidcpage</em>) melden, nicht aktualisiert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoMax</p></td>
<td><p><em>pvresult</em> wird als <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>interpretiert. Die maximale Größe des Objekts befindet sich auf Seiten. Zurzeit werden nur Tabellen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoNoStats</p></td>
<td><p><em>pvresult</em> wird als <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>interpretiert. Informationen zu nur dem in " <em>szobjectname</em> " angegebenen Objekt werden abgerufen.</p>
<p>Die <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> Struktur wird mit Informationen zu dem Objekt aufgefüllt, das in <em>szobjectname</em>benannt ist.</p>
<p>JET_ObjInfoNoStats ist mit JET_ObjInfo identisch, mit dem Unterschied, dass die Felder, die die Anzahl von Datensätzen und Seiten melden, auf NULL festgelegt sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoRulesLoaded</p></td>
<td><p>Veraltet und wird derzeit nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoSysTabCursor</p></td>
<td><p>Veraltet und wird derzeit nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoSysTabReadOnly</p></td>
<td><p>Veraltet und wird derzeit nicht unterstützt.</p></td>
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
<td><p>Die Größe des in <em>cbmax</em> angegebenen Puffers war zu klein, um die gewünschten Informationen zu speichern.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName</p></td>
<td><p>In " <em>szobjectname</em> " oder " <em>szcontainername</em>" wurde ein ungültiger Name angegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Ein ungültiger Parameter wurde angegeben. Es ist möglich, dass eine ungültige Ebene an <em>infolevel</em>übermittelt wurde.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Wenn **jetgetobjectinfo** erfolgreich eine temporäre Tabelle erstellt (z. b. JET_ObjInfoList oder JET_ObjInfoNoStats), ist der Aufrufer für das Schließen der temporären Tabelle mit [jetclosetable](./jetclosetable-function.md)verantwortlich.

**Jetgetobjectinfo** unterstützt derzeit nur das Abrufen von Informationen zu Tabellen.

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
<td><p>Implementiert als <strong>jetgetobjectinfow</strong> (Unicode) und <strong>jetgetobjectinfoa</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[Jetclosetable](./jetclosetable-function.md)  
[Jetgettableinfo](./jetgettableinfo-function.md)
