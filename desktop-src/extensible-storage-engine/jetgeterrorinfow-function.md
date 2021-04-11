---
description: 'Weitere Informationen zu: jetgeterrorinfow-Funktion'
title: Jetgeterrorinfow-Funktion
TOCTitle: JetGetErrorInfoW Function
ms:assetid: 7a84f937-7a16-434e-896d-789f316ee833
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475859(v=EXCHG.10)
ms:contentKeyID: 37033565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetErrorInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bf4db5d8d34a741e57f72e8f237f1497de0bacf
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104132436"
---
# <a name="jetgeterrorinfow-function"></a>Jetgeterrorinfow-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgeterrorinfow-function"></a>Jetgeterrorinfow-Funktion

Die **jetgeterrorinfow** -Funktion BAS_ der Datenbank-Engine.

Hinweis: Diese Dokumentation basiert auf einer vorläufigen Version der Extensible Storage-Engine. Diese Informationen können geändert werden.

```cpp
JET_ERR JET_API JetGetErrorInfoW( 
    _In_opt_ void *                      pvContext, 
    _Out_writes_bytes_( cbMax ) void *   pvResult, 
    _In_ unsigned long                   cbMax, 
    _In_ unsigned long                   InfoLevel, 
    _In_ JET_GRBIT                       grbit );
```

### <a name="parameters"></a>Parameter

*pvcontext*

Der Kontext-oder Fehlerwert, für den die erweiterten Fehlerinformationen benötigt werden. Der übergebene Wert hängt vom *infolevel* -Parameterwert ab.

*pvresult*

Ein Zeiger auf einen Puffer, der die Informationen empfängt. Der Typ des Puffers hängt vom Wert des *infolevel* -Parameters ab. Der Aufrufer muss so konfiguriert werden, dass der Puffer entsprechend ausgerichtet wird.

*cbmax*

Die maximale Größe der *pvresult* -Struktur, die übergeben wird.

*Infolevel*

Der Typ der Informationen, die für die Fehler Info/den Kontext abgerufen werden, wird durch den *pvcontext* -Parameter angegeben. Das Format der Daten, die in *pvresult* gespeichert sind, ist von *infolevel* abhängig.

In der folgenden Tabelle sind die möglichen Werte für diesen Parameter aufgeführt.

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
<td><p>JET_ErrorInfoSpecificErr</p></td>
<td><p><em>pvcontext</em> wird als <a href="gg269297(v=exchg.10).md">JET_ERR</a>/Error-Code interpretiert, <em>pvresult</em> wird als <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>interpretiert, und die Felder der <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> Struktur werden entsprechend ausgefüllt.</p></td>
</tr>
</tbody>
</table>


*grbit*

Reserviert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./extensible-storage-engine-error-codes.md) -Datentyp mit einem der in der folgenden Tabelle aufgelisteten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthält einen unerwarteten Wert oder enthält einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll ist. Dies kann bei <strong>jetgeterrorinfo</strong> vorkommen, wenn Folgendes zutrifft:</p>
<ul>
<li><p>Der angegebene <em>infolevel</em> -Parameterwert ist ungültig.</p></li>
<li><p>Der angegebene <em>grbit</em> -Wert ist ungültig.</p></li>
<li><p>Der <em>cbmax</em> -Wert des angegebenen <em>pvresult</em> -Parameter Puffers ist kleiner als die erforderliche Größe für die Ausgabe dieses <em>infolevel</em> -Parameters.</p></li>
<li><p>Bei <em>infolevel</em> = JET_ErrorInfoSpecificErr ist der <a href="gg294092(v=exchg.10).md">JET_ERR</a> Wert, der in der-Engine nicht angezeigt wird, unbekannt.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errDisabledFunctionality</p></td>
<td><p>Wenn diese Funktion von dieser SKU von Windows nicht unterstützt wird, wird dieser Fehler zurückgegeben.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird der Ausgabepuffer, der für den angeforderten Fehler Kontext/-Wert geeignet ist, auf die angeforderten erweiterten Fehlerinformationen festgelegt.

Bei einem Fehler wird der Status der Ausgabepuffer nicht definiert.

### <a name="remarks"></a>Bemerkungen

Die [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) -Funktion und [JET_ERRCAT](./jet-errcat.md) Gruppe von Konstanten enthalten Dokumentation zu den erweiterten Fehlerinformationen, die für *infolevel* = JET_ErrorInfoSpecificErr zurückgegeben werden.

### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows 8-Server.</p></td>
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
<td><p>Hinweis: nur <strong>jetgeterrorinfow</strong> (Unicode) ist implementiert. Diese API weist keine (ANSI)-Version auf.</p></td>
</tr>
</tbody>
</table>
