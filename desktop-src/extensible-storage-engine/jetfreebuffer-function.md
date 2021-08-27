---
description: Weitere Informationen finden Sie unter JetFreeBuffer-Funktion.
title: JetFreeBuffer-Funktion
TOCTitle: JetFreeBuffer Function
ms:assetid: f37d35f6-4bea-46ba-a334-7b8ad7a1568c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294134(v=EXCHG.10)
ms:contentKeyID: 32765748
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetFreeBuffer
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7d7b56c38bde931cfe0c1a2e95579a515cf3538
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476436"
---
# <a name="jetfreebuffer-function"></a>JetFreeBuffer-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetfreebuffer-function"></a>JetFreeBuffer-Funktion

Die **JetFreeBuffer-Funktion** gibt Arbeitsspeicher frei, der durch einen Datenbank-Engine-Aufruf belegt wurde.

**Windows XP: JetFreeBuffer** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetFreeBuffer(
      __in          char* pbBuf
    );
```

### <a name="parameters"></a>Parameter

*pbBuf*

Zeiger auf einen Speicherbereich, der zuvor durch einen Aufruf der Datenbank-Engine zugeordnet wurde. **NULL** ist akzeptabel und wird ignoriert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 



#### <a name="remarks"></a>Hinweise

Es ist nicht definiert, Arbeitsspeicher zu übergeben, der nicht von der Datenbank-Engine an *pbBuf* zugeordnet wurde.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)
