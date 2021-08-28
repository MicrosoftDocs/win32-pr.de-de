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
ms.openlocfilehash: 52ff674cdd256c8a9a983a5ba3a49d6abeb8cc6b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987413"
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



#### <a name="remarks"></a>Bemerkungen

Es ist nicht definiert, Arbeitsspeicher zu übergeben, der nicht von der Datenbank-Engine an *pbBuf* zugeordnet wurde.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)
