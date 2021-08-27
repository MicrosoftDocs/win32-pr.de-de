---
description: 'Weitere Informationen zu: JET_PFNREALLOC Rückruffunktion'
title: JET_PFNREALLOC Rückruffunktion
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f7427a28752384f6c30e050458e5844dcaedd1a7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989143"
---
# <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC Rückruffunktion


_**Gilt für:** Windows | Windows Server_

## <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC Rückruffunktion

Die JET_PFNREALLOC-Funktion ist ein [relokal](/cpp/c-runtime-library/reference/realloc?view=vs-2019) kompatibler Rückruf, der von [JetEnumerateColumns](./jetenumeratecolumns-function.md) verwendet wird, um Arbeitsspeicher für die Ausgabepuffer zuzuweisen.

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a>Parameter

*pvContext*

Der Kontextzeiger, der [jetEnumerateColumns](./jetenumeratecolumns-function.md)übergeben wird. Dieser Kontextzeiger kann verwendet werden, um den Zustand vom Aufrufer von [JetEnumerateColumns](./jetenumeratecolumns-function.md) an die Implementierung dieses Rückrufs zu übermitteln.

*Pv*

Wenn nicht NULL ist, gibt einen Zeiger auf einen Speicherblock an, der zuvor von diesem Rückruf zugeordnet wurde. Bei NULL wird ein neuer Speicherblock der angeforderten Größe zugeordnet.

*Cb*

Die neue Größe des Speicherblocks in Bytes. Wenn dieser Parameter 0 (null) ist und ein Speicherblock angegeben wird, wird dieser Speicherblock freigegeben.

### <a name="return-value"></a>Rückgabewert

Das System kann als Ergebnis eines Aufrufs dieser Funktion Erfolgs- oder Fehlercodes generieren. Informationen zum Zurückgeben dieser Codes als HRESULTs finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>Erfolg</p> | <p>Wenn ein zuvor zugeordneter Speicherblock angegeben und eine neue Größe von 0 angegeben wurde, wird dieser Block freigegeben, und NULL wird zurückgegeben. Wenn ein zuvor zugeordneter Speicherblock angegeben wurde und eine neue Größe ungleich 0 angegeben wurde, wird der neu zugeordnete Speicherblock zurückgegeben. Wenn kein Speicherblock angegeben wurde, wird ein neu zugeordneter Speicherblock der angegebenen Größe zurückgegeben.</p> | 
| <p>Fehler</p> | <p>NULL wird zurückgegeben. Wenn ein zuvor zugeordneter Speicherblock bereitgestellt wurde, bleibt dieser Block zugeordnet.</p> | 



### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetEnumerateColumns](./jetenumeratecolumns-function.md)
