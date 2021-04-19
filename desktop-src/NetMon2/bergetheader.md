---
description: Die "bergeteader"-Funktion decodiert einen Choice-Header.
ms.assetid: 2574a9b3-c28e-43d1-904f-d45888617584
title: Bergederader-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetHeader
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e2213b15b6b4d2cbaa15b3b9aa9de028e20a62d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363446"
---
# <a name="bergetheader-function"></a>Bergederader-Funktion

Die " **bergeteader** "-Funktion decodiert einen Choice-Header.

## <a name="syntax"></a>Syntax


```C++
BOOL BERGetHeader(
   LPBYTE  pCurrentPointer,
   LPBYTE  pTag,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcurrentpointer* 
</dt> <dd>

Zeiger auf den Choice-Header.

</dd> <dt>

*ptag* 
</dt> <dd>

Zeiger auf das zurückgegebene Tag.

</dd> <dt>

*pheaderlength* 
</dt> <dd>

Zeiger auf die zurückgegebene Header Länge.

</dd> <dt>

*pdatalength* 
</dt> <dd>

Zeiger auf die zurückgegebene Daten Länge.

</dd> <dt>

*ppnext* 
</dt> <dd>

Zeiger auf den Header Inhalt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (d. h., es wurde ein gültiger ber Choice-Header gefunden), ist der Rückgabewert " **true**".

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




