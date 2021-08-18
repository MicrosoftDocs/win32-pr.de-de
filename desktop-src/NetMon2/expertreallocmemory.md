---
description: Die ExpertReallocMemory-Funktion erhöht oder verringert die Menge an Arbeitsspeicher, die von der Netzwerkmonitor.
ms.assetid: 78b99a66-692a-4e83-8b0d-d68caf156bb6
title: ExpertReallocMemory-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertReallocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: be43fa99021ec5612a148ba42db1b11e1fd6d885fa64fa003c0dfa672688d555
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012258"
---
# <a name="expertreallocmemory-function"></a>ExpertReallocMemory-Funktion

Die **ExpertReallocMemory-Funktion** erhöht oder verringert die Menge an Arbeitsspeicher, die von der Netzwerkmonitor.

## <a name="syntax"></a>Syntax


```C++
LPVOID WINAPI ExpertReallocMemory(
  _In_  HEXPERTKEY hExpertKey,
  _In_  LPVOID     pOriginalMemory,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hExpertKey* \[ In\]
</dt> <dd>

Eindeutiger Bezeichner, der an den Experten unter [**Ausführen oder**](run.md) Konfigurieren von [**übergeben wird.**](configure.md)

</dd> <dt>

*pOriginalMemory* \[ In\]
</dt> <dd>

Zeiger auf den arbeitsspeicher, der von der Netzwerkmonitor. Der *pOriginalMemory-Zeiger* kann durch einen vorherigen Aufruf von [**ExpertAllocMemory**](expertallocmemory.md) oder **ExpertReallocMemory zurückgegeben werden.**

</dd> <dt>

*nBytes* \[ In\]
</dt> <dd>

Größe des neu zugewiesenen Arbeitsspeichers.

</dd> <dt>

*pError* \[ out\]
</dt> <dd>

Bei Rückgabe ein Fehlercode, wenn die Funktion fehlschlägt. Wenn der Fehlercode NMERR EXPERT TERMINATE ist, muss der Experte sofort bereinigt \_ \_ und zurückkehren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den zugeordneten Arbeitsspeicher.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **NULL,** und *pError* (wenn es sich um einen Nicht-NULL-Wert handelt) gibt den Grund für den Fehler an.

## <a name="remarks"></a>Hinweise

Es ist wichtig zu beachten, dass ein Experte die Netzwerkmonitor speicherzuteilungsfunktionen für die Speicherverwaltung verwenden sollte. Wenn Ihr Experte während der Laufzeit ausfällt, ermöglicht die Verwendung dieser Funktionen Netzwerkmonitor, den zugewiesenen Arbeitsspeicher frei zu geben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




