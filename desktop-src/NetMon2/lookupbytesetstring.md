---
description: Die LookupByteSetString-Funktion gibt die Zeichenfolge zurück, die dem angegebenen Wert eines bezeichneten Satzes entspricht.
ms.assetid: 295891f9-dc8d-4dbe-aac9-7d0a96993cfa
title: LookupByteSetString-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupByteSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 208f7cef1a658ae321d7ce03aaee763e5387b5a45985d59134418a4d136e0b56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742500"
---
# <a name="lookupbytesetstring-function"></a>LookupByteSetString-Funktion

Die **LookupByteSetString-Funktion** gibt die Zeichenfolge zurück, die dem angegebenen Wert eines bezeichneten Satzes entspricht.

## <a name="syntax"></a>Syntax


```C++
LPBYTE WINAPI LookupByteSetString(
   LPSET lpSet,
   BYTE  Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpSet* 
</dt> <dd>

Zeiger auf einen bezeichneten Satz, aus dem Sie die Bezeichnung des Werts extrahieren können.

</dd> <dt>

*Wert* 
</dt> <dd>

Wert eines beschrifteten Satzes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert eine Zeichenfolge, die dem angegebenen Wert entspricht.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **NULL.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




