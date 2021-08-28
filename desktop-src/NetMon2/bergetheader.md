---
description: Die BERGetHeader-Funktion decodiert einen Auswahlheader.
ms.assetid: 2574a9b3-c28e-43d1-904f-d45888617584
title: BERGetHeader-Funktion (Netmon.h)
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
ms.openlocfilehash: d6dfd50856202e78177d2ad259b16638f466d9bca236a691c65802ce2758c948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012308"
---
# <a name="bergetheader-function"></a>BERGetHeader-Funktion

Die **BERGetHeader-Funktion** decodiert einen Auswahlheader.

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

*pCurrentPointer* 
</dt> <dd>

Zeiger auf den Auswahlheader.

</dd> <dt>

*pTag* 
</dt> <dd>

Zeiger auf das zurückgegebene Tag.

</dd> <dt>

*pHeaderLength* 
</dt> <dd>

Zeiger auf die zurückgegebene Headerlänge.

</dd> <dt>

*pDataLength* 
</dt> <dd>

Zeiger auf die zurückgegebene Datenlänge.

</dd> <dt>

*ppNext* 
</dt> <dd>

Zeiger auf den Headerinhalt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (d. h. ein gültiger BER-Auswahlheader gefunden wird), ist der Rückgabewert **TRUE.**

Wenn die Funktion nicht erfolgreich ist, lautet der Rückgabewert **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




