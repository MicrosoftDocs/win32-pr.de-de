---
description: Die stringto Address-Funktion konvertiert eine Zeichenfolge in eine Adresse.
ms.assetid: b1ada88d-04bb-4869-87c6-99f5046356c5
title: Stringtaddress-Funktion (Netmon. h)
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
ms.openlocfilehash: 70a9e6b42359a2f73fba55194c9b6e6e21ffa9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347920"
---
# <a name="stringtoaddress-function"></a>Stringto Address-Funktion

Die **stringto Address** -Funktion konvertiert eine Zeichenfolge in eine Adresse.

## <a name="syntax"></a>Syntax


```C++
LPBYTE WINAPI StringToAddress(
  _Out_ BYTE  *lpAddress,
  _In_  LPSTR string
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpAddress* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Adresse, in die die Zeichenfolge konvertiert wird.

</dd> <dt>

*Zeichenfolge* \[ in\]
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
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




