---
description: Weitere Informationen finden Sie unter JetGetErrorInfoW-Funktion.
title: JetGetErrorInfoW-Funktion
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
ms.openlocfilehash: f459d98ee2cc3c0bb1b57eb5cd4fb630d076836b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468977"
---
# <a name="jetgeterrorinfow-function"></a>JetGetErrorInfoW-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgeterrorinfow-function"></a>JetGetErrorInfoW-Funktion

Die **JetGetErrorInfoW-BAS_** der Datenbank-Engine.

Hinweis: Diese Dokumentation basiert auf einer vorläufigen Version der Extensible Storage Engine. Diese Informationen können geändert werden.

```cpp
JET_ERR JET_API JetGetErrorInfoW( 
    _In_opt_ void *                      pvContext, 
    _Out_writes_bytes_( cbMax ) void *   pvResult, 
    _In_ unsigned long                   cbMax, 
    _In_ unsigned long                   InfoLevel, 
    _In_ JET_GRBIT                       grbit );
```

### <a name="parameters"></a>Parameter

*pvContext*

Der Kontext- oder Fehlerwert, für den die erweiterten Fehlerinformationen benötigt werden. Der übergebene Wert hängt vom *InfoLevel-Parameterwert* ab.

*pvResult*

Ein Zeiger auf einen Puffer, der die Informationen erhält. Der Typ des Puffers hängt vom *InfoLevel-Parameterwert* ab. Der Aufrufer muss so konfiguriert werden, dass der Puffer entsprechend ausgerichtet wird.

*cbMax*

Die maximale Größe der *pvResult-Struktur,* die übergeben wird.

*InfoLevel*

Der Typ der Informationen, die für die Fehlerinformationen/den Kontext abgerufen werden, wird durch den *pvContext-Parameter* angegeben. Das Format der in *pvResult* gespeicherten Daten hängt von *InfoLevel ab.*

In der folgenden Tabelle sind die möglichen Werte für diesen Parameter aufgeführt.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_ErrorInfoSpecificErr</p> | <p><em>pvContext</em> wird als JET_ERR /error-Code interpretiert, <em>pvResult</em> wird als <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>interpretiert, und <a href="hh475861(v=exchg.10).md"></a> die Felder der JET_ERRINFOBASIC_W-Struktur werden entsprechend ausgefüllt. <a href="gg269297(v=exchg.10).md"></a></p> | 



*grbit*

Reserviert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./extensible-storage-engine-error-codes.md) datentyp mit einem der in der folgenden Tabelle aufgeführten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthält einen unerwarteten Wert oder einen Wert, der nicht sinnvoll ist, wenn er mit dem Wert eines anderen Parameters kombiniert wird. Dies kann für <strong>JetGetErrorInfo passieren,</strong> wenn Folgendes auftritt:</p><ul><li><p>Der angegebene <em>InfoLevel-Parameterwert</em> ist ungültig.</p></li><li><p>Der angegebene <em>Grbitwert</em> ist ungültig.</p></li><li><p>Der <em>cbMax-Wert</em> des angegebenen pvResult-Parameterpuffers ist kleiner als die erforderliche Größe für die Ausgabe dieses <em>InfoLevel-Parameters.</em> <em></em></p></li><li><p>Für <em>InfoLevel</em> = JET_ErrorInfoSpecificErr ist <a href="gg294092(v=exchg.10).md">der JET_ERR</a> übergebene Wert für die Engine unbekannt.</p></li></ul> | 
| <p>JET_errDisabledFunctionality</p> | <p>Wenn diese Funktion von dieser SKU von Windows nicht unterstützt wird, wird dieser Fehler zurückgegeben.</p> | 



Bei Erfolg wird der Ausgabepuffer, der für den angeforderten Fehlerkontext/-wert geeignet ist, auf die angeforderten erweiterten Fehlerinformationen festgelegt.

Bei einem Fehler ist der Status der Ausgabepuffer nicht definiert.

### <a name="remarks"></a>Hinweise

Die [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) und [JET_ERRCAT](./jet-errcat.md) Gruppe von Konstanten enthalten Dokumentation zu den erweiterten Fehlerinformationen, die für *InfoLevel* = JET_ErrorInfoSpecificErr.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows 8.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows 8 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Hinweis: Nur <strong>JetGetErrorInfoW</strong> (Unicode) wird implementiert. Diese API verfügt nicht über eine A-Version (ANSI).</p> | 

