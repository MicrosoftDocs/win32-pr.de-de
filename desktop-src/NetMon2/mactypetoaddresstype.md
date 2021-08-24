---
description: Die MacTypeToAddressType-Funktion konvertiert einen angegebenen MAC-Typ in einen Adresstyp.
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: MacTypeToAddressType-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MacTypeToAddressType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: fe02cb6f0bec62a3bda35eabe288eafc2d5c3c15e422b7d68dc0b488546b83b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742320"
---
# <a name="mactypetoaddresstype-function"></a>MacTypeToAddressType-Funktion

Die **MacTypeToAddressType-Funktion** konvertiert einen angegebenen MAC-Typ in einen Adresstyp.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MacType* \[ In\]
</dt> <dd>

Der zu konvertierende MAC-Typ. Geben Sie einen der folgenden Werte an.

MAC \_ TYPE \_ ETHERNET MAC \_ TYPE \_ TOKENRING MAC \_ TYPE \_ FDDI

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert einer der folgenden Adresstypen.

ADRESSTYP \_ \_ ETHERNET-ADRESSTYP \_ \_ TOKENRING ADDRESS \_ TYPE \_ FDDI

Wenn die Funktion nicht erfolgreich ist, der MAC-Typ unbekannt ist, ist der Rückgabewert -1.

## <a name="remarks"></a>Hinweise

[*Experten*](e.md) und [*Parser*](p.md) können die **MacTypeToAddressType-Funktion** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




