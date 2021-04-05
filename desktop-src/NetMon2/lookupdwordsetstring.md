---
description: Die lookupdwordsetstring-Funktion gibt die Zeichenfolge zurück, die dem angegebenen Wert einer gekennzeichneten Menge entspricht.
ms.assetid: ee2b1b7a-6b64-4c8c-a71d-de970b66d46e
title: Lookupdwordsetstring-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupDwordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57688edab7421f939e03322b8b244219b00d31fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752185"
---
# <a name="lookupdwordsetstring-function"></a>Lookupdwordsetstring-Funktion

Die **lookupdwordsetstring** -Funktion gibt die Zeichenfolge zurück, die dem angegebenen Wert einer gekennzeichneten Menge entspricht.

## <a name="syntax"></a>Syntax


```C++
LPBYTE WINAPI LookupDwordSetString(
   LPSET lpSet,
   DWORD Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpset* 
</dt> <dd>

Bezeichnete Menge, aus der Sie die Bezeichnung des Werts extrahieren können.

</dd> <dt>

*Wert* 
</dt> <dd>

Der Wert einer gekennzeichneten Menge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Zeichenfolge, die dem angegebenen Wert entspricht.

Wenn die Funktion nicht erfolgreich ist, ist der angegebene Wert nicht im Satz, der Rückgabewert ist **null**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




