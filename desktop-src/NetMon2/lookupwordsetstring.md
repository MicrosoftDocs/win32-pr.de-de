---
description: Die LookupWordSetString-Funktion gibt die Zeichenfolge zurück, die dem angeforderten Wert aus einem bezeichneten Satz entspricht.
ms.assetid: e8d158a1-8544-4c10-b8e8-46888c1097e4
title: LookupWordSetString-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupWordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 15b529076660eec093df370df47823fb21aa13e53cce61565fe82de7fbb7e017
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364718"
---
# <a name="lookupwordsetstring-function"></a>LookupWordSetString-Funktion

Die **LookupWordSetString-Funktion** gibt die Zeichenfolge zurück, die dem angeforderten Wert aus einem bezeichneten Satz entspricht.

## <a name="syntax"></a>Syntax


```C++
LPBYTE WINAPI LookupWordSetString(
   LPSET lpSet,
   WORD  Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpSet* 
</dt> <dd>

Bezeichneter Satz, aus dem Sie die Bezeichnung des Werts extrahieren.

</dd> <dt>

*Wert* 
</dt> <dd>

Wert eines beschrifteten Satzes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert eine Zeichenfolge, die dem angeforderten Wert entspricht.

Wenn die Funktion nicht erfolgreich ist, der angegebene Wert nicht im Satz enthalten ist, ist der Rückgabewert **NULL.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




