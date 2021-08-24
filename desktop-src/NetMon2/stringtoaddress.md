---
description: Die StringToAddress-Funktion konvertiert eine Zeichenfolge in eine Adresse.
ms.assetid: b1ada88d-04bb-4869-87c6-99f5046356c5
title: StringToAddress-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringToAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 9dbac01f5df9d32a65fe5afb1c1437064f6dd0d4480c95dacd0fe8f7d58e2fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676690"
---
# <a name="stringtoaddress-function"></a>StringToAddress-Funktion

Die **StringToAddress-Funktion** konvertiert eine Zeichenfolge in eine Adresse.

## <a name="syntax"></a>Syntax


```C++
LPBYTE WINAPI StringToAddress(
  _Out_ BYTE  *lpAddress,
  _In_  LPSTR string
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpAddress* \[ out\]
</dt> <dd>

Zeiger auf die Adresse, in die die Zeichenfolge konvertiert wird.

</dd> <dt>

*string* \[ In\]
</dt> <dd>

Zeichenfolge, die in eine Adresse konvertiert wird.

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



 

 




