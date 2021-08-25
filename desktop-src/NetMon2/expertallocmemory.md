---
description: Die ExpertAllocMemory-Funktion weist dem Experten Arbeitsspeicher zu.
ms.assetid: 9ada5d3f-5f1d-4d3a-b79a-d51e021240f6
title: ExpertAllocMemory-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertAllocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: fd932a5330baf687d5578bac4e4bfac77ad4f5bad0560263ab7f1e8832e61fe6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890850"
---
# <a name="expertallocmemory-function"></a>ExpertAllocMemory-Funktion

Die **ExpertAllocMemory-Funktion** weist dem Experten Arbeitsspeicher zu.

## <a name="syntax"></a>Syntax


```C++
LPVOID WINAPI ExpertAllocMemory(
        HEXPERTKEY hExpertKey,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hExpertKey* 
</dt> <dd>

Eindeutiger Expertenbezeichner. Netzwerkmonitor übergibt *hExpertKey* an den Experten, wenn er die [Run-Funktion](run.md) aufruft.

</dd> <dt>

*nBytes* \[ In\]
</dt> <dd>

Zugeordneter Arbeitsspeicher, gemessen in Bytes.

</dd> <dt>

*pError* \[ out\]
</dt> <dd>

Fehlerindikator. Wenn die Funktion fehlschlägt, enthält der *nBytes-Parameter* den Fehlercode. Wenn der Fehlercode NMERR \_ EXPERT \_ TERMINATE lautet, muss der Experte bereinigen und sofort zurückkehren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den zugeordneten Arbeitsspeicher.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **NULL,** und *pError* stellt einen Fehlercode bereit, der den Grund für den Fehler angibt.

## <a name="remarks"></a>Hinweise

Es ist wichtig zu beachten, dass ein Experte die Netzwerkmonitor Speicherbelegungsfunktionen (einschließlich [ExpertReallocMemory)](expertreallocmemory.md)für die Speicherverwaltung verwenden sollte. Wenn Ihr Experte während der Laufzeit ausfällt, können Netzwerkmonitor mithilfe dieser Funktionen den zugewiesenen Arbeitsspeicher freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




