---
description: Die lookupbytesetstring-Funktion gibt die Zeichenfolge zurück, die dem angegebenen Wert einer gekennzeichneten Menge entspricht.
ms.assetid: 295891f9-dc8d-4dbe-aac9-7d0a96993cfa
title: Lookupbytesetstring-Funktion (Netmon. h)
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
ms.openlocfilehash: 7a2b5bffbfcb30ed8ec00da42fbc9ad6008fd5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372854"
---
# <a name="lookupbytesetstring-function"></a>Lookupbytesetstring-Funktion

Die **lookupbytesetstring** -Funktion gibt die Zeichenfolge zurück, die dem angegebenen Wert einer gekennzeichneten Menge entspricht.

## <a name="syntax"></a>Syntax


```C++
LPBYTE WINAPI LookupByteSetString(
   LPSET lpSet,
   BYTE  Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpset* 
</dt> <dd>

Ein Zeiger auf eine bezeichnete Menge, aus der die Bezeichnung des Werts extrahiert werden kann.

</dd> <dt>

*Wert* 
</dt> <dd>

Der Wert einer gekennzeichneten Menge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert eine Zeichenfolge, die dem bereitgestellten Wert entspricht.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




