---
description: Die AddressToString-Funktion konvertiert eine Adresse in eine Zeichenfolge.
ms.assetid: 999a6142-1423-4006-a489-63895dd19ce3
title: AddressToString-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddressToString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 58c105fb8fa646fbffcc7d7d4a3f1dad3a9cd86e7bb6ef8cc426dc982873f720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796370"
---
# <a name="addresstostring-function"></a>AddressToString-Funktion

Die **AddressToString-Funktion** konvertiert eine Adresse in eine Zeichenfolge.

## <a name="syntax"></a>Syntax


```C++
LPSTR WINAPI AddressToString(
  _Out_ LPSTR string,
  _In_  BYTE  *lpAddress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*string* \[ out\]
</dt> <dd>

Zeichenfolge, in die die Adresse konvertiert wird.

</dd> <dt>

*lpAddress* \[ In\]
</dt> <dd>

Die Adresse, die gedruckt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein Zeiger auf die konvertierte Zeichenfolge.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




