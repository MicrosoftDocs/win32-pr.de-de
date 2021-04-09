---
description: Die bergetinteger-Funktion decodiert eine BER-codierte Ganzzahl.
ms.assetid: 1ab0dcec-05cf-4322-a44e-28aa9131495a
title: Bergetinteger-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetInteger
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: c89cd5e3f4e4eb35157936f990939154f23966d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867027"
---
# <a name="bergetinteger-function"></a>Bergetinteger-Funktion

Die **bergetinteger** -Funktion decodiert eine BER-codierte Ganzzahl.

## <a name="syntax"></a>Syntax


```C++
BOOL BERGetInteger(
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

Ein Zeiger auf die Ganzzahl, die decodiert wird.

</dd> <dt>

*ppvaluepointer* 
</dt> <dd>

Zeiger auf den Zeiger auf den zurückgegebenen Wert.

</dd> <dt>

*pheaderlength* 
</dt> <dd>

Zeiger auf die zurückgegebene Header Länge.

</dd> <dt>

*pdatalength* 
</dt> <dd>

Zeiger auf die Daten Länge.

</dd> <dt>

*ppnext* 
</dt> <dd>

Zeiger auf den Zeiger auf den nächsten ber-Eintrag.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (d. h., wenn eine gültige ber-codierte Ganzzahl gefunden und konvertiert wird), ist der Rückgabewert " **true**".

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




