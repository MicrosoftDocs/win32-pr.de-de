---
description: Die "adresstostring"-Funktion konvertiert eine Adresse in eine Zeichenfolge.
ms.assetid: 999a6142-1423-4006-a489-63895dd19ce3
title: Adresssstostring-Funktion (Netmon. h)
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
ms.openlocfilehash: 0c7c659a05167055b18c36e5c6c36465538af483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131996"
---
# <a name="addresstostring-function"></a>Adresssstostring-Funktion

Die " **adresstostring** "-Funktion konvertiert eine Adresse in eine Zeichenfolge.

## <a name="syntax"></a>Syntax


```C++
LPSTR WINAPI AddressToString(
  _Out_ LPSTR string,
  _In_  BYTE  *lpAddress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zeichenfolge* \[ vorgenommen\]
</dt> <dd>

Zeichenfolge, in die die Adresse konvertiert wird.

</dd> <dt>

*lpAddress* \[ in\]
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
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




