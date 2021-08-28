---
description: 'Weitere Informationen finden Sie unter: JetGetInstanceMiscInfo-Funktion'
title: JetGetInstanceMiscInfo-Funktion
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 07167dc0f2cad5192dc30e9897541b6619086bfc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481346"
---
# <a name="jetgetinstancemiscinfo-function"></a>JetGetInstanceMiscInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetinstancemiscinfo-function"></a>JetGetInstanceMiscInfo-Funktion

Die **JetGetInstanceMiscInfo-Funktion** ruft Informationen über die Instanz ab, während die Instanz online ist.

**Windows Vista: JetGetInstanceMiscInfo** wird in Windows Vista eingeführt.

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Identifiziert die Datenbankinstanz, die für den API-Aufruf verwendet wird.

*pvResult*

Zeiger auf einen Puffer, der die Informationen erhält. Der Typ des Puffers ist von *InfoLevel abhängig.* Der Aufrufer ist dafür verantwortlich, den Puffer entsprechend auszurichten.

*cbMax*

Die Größe des in pvResult übergebenen Puffers in *Bytes.*

*InfoLevel*

Bestimmt, welche Art von Informationen für die instanz angegebene Instanz abgerufen *wird.* Das Format der in *pvResult* gespeicherten Daten hängt von *InfoLevel ab.*

Die folgenden Optionen stehen für die Verwendung mit diesem Parameter zur Verfügung.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_InstanceMiscInfoLogSignature</p> | <p><em>pvResult</em> wird als <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> Struktur der Transaktionsprotokollsequenz interpretiert, die dieser Instanz zugeordnet ist.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Der Puffer war zu klein.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Entweder wurde ein <a href="gg294048(v=exchg.10).md">ungültiges JET_INSTANCE</a> oder ein ungültiges <em>InfoLevel</em> angegeben.</p> | 



#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SIGNATURE](./jet-signature-structure.md)
