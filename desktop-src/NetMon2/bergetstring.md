---
description: Die bergetstring-Funktion decodiert eine BER-codierte Zeichenfolge.
ms.assetid: 1f72f061-c0ed-4634-9709-e08c2b9468bb
title: Bergetstring-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6f8f864b8042ad49502ae53061e157575192e7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864804"
---
# <a name="bergetstring-function"></a>Bergetstring-Funktion

Die **bergetstring** -Funktion decodiert eine BER-codierte Zeichenfolge.

## <a name="syntax"></a>Syntax


```C++
BOOL BERGetString(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcurrentpointer* 
</dt> <dd>

Ein Zeiger auf die Zeichenfolge, die decodiert wird.

</dd> <dt>

*ppvaluepointer* 
</dt> <dd>

Zeiger auf den Zeiger der decodierten Zeichenfolge.

</dd> <dt>

*pheaderlength* 
</dt> <dd>

Zeiger auf die zurückgegebene Header Länge.

</dd> <dt>

*pdatalength* 
</dt> <dd>

Zeiger auf die Zeichen folgen Länge.

</dd> <dt>

*ppnext* 
</dt> <dd>

Zeiger auf den Zeiger des nächsten ber-Eintrags.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (d. h., wenn eine gültige ber-codierte Zeichenfolge decodiert wird), ist der Rückgabewert " **true**".

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




