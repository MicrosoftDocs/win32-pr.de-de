---
description: Die lookupwordsetstring-Funktion gibt die Zeichenfolge zurück, die dem angeforderten Wert aus einer gekennzeichneten Menge entspricht.
ms.assetid: e8d158a1-8544-4c10-b8e8-46888c1097e4
title: Lookupwordsetstring-Funktion (Netmon. h)
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
ms.openlocfilehash: 7487becb195571e1eb88044195293b2c0b226e8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526762"
---
# <a name="lookupwordsetstring-function"></a>Lookupwordsetstring-Funktion

Die **lookupwordsetstring** -Funktion gibt die Zeichenfolge zurück, die dem angeforderten Wert aus einer gekennzeichneten Menge entspricht.

## <a name="syntax"></a>Syntax


```C++
LPBYTE WINAPI LookupWordSetString(
   LPSET lpSet,
   WORD  Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpset* 
</dt> <dd>

Der Satz, aus dem Sie die Bezeichnung des Werts extrahieren.

</dd> <dt>

*Wert* 
</dt> <dd>

Der Wert einer gekennzeichneten Menge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert eine Zeichenfolge, die dem angeforderten Wert entspricht.

Wenn die Funktion nicht erfolgreich ist, ist der angegebene Wert nicht im Satz, der Rückgabewert ist **null**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




