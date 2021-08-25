---
description: Die ExpertFreeMemory-Funktion gibt Arbeitsspeicher frei, der durch Aufrufe der Funktionen ExpertAllocMemory und ExpertReallocMemory erworben wurde.
ms.assetid: 0e7cc791-98dd-4522-afab-76ac9e74c715
title: ExpertFreeMemory-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertFreeMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: edc4d1a9e33139372d0f397053d233a28c9e2445ba270a47e7dbfe97090eb6a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890829"
---
# <a name="expertfreememory-function"></a>ExpertFreeMemory-Funktion

Die **ExpertFreeMemory-Funktion** gibt Arbeitsspeicher frei, der durch Aufrufe der [**Funktionen ExpertAllocMemory**](expertallocmemory.md) und [**ExpertReallocMemory erworben wurde.**](expertreallocmemory.md)

## <a name="syntax"></a>Syntax


```C++
SIZE_T WINAPI ExpertFreeMemory(
       HEXPERTKEY hExpertKey,
  _In_ LPVOID     pMemory
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hExpertKey* 
</dt> <dd>

Eindeutiger Expertenbezeichner. Netzwerkmonitor *hExpertKey* an den Experten übergeben, wenn er die [Run-Funktion](run.md) aufruft.

</dd> <dt>

*pMemory* \[ In\]
</dt> <dd>

Zeiger auf den Arbeitsspeicher, der von Netzwerkmonitor wird. Der *pMemory-Zeiger* kann durch einen vorherigen Aufruf von [**ExpertAllocMemory**](expertallocmemory.md) oder [**ExpertReallocMemory zurückgegeben werden.**](expertreallocmemory.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist. Der Rückgabewert ist NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, gibt der Rückgabewert den Grund für den Fehler an. Wenn der Rückgabewert NMERR EXPERT TERMINATE ist, bereinigt der Experte \_ \_ sofort und gibt zurück.

## <a name="remarks"></a>Hinweise

Es ist wichtig zu beachten, dass ein Experte die Netzwerkmonitor für die Speicherverwaltung verwenden sollte. Wenn Ihr Experte während der Laufzeit ausfällt, ermöglicht die Verwendung dieser Funktionen Netzwerkmonitor, den zugewiesenen Arbeitsspeicher frei zu geben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




