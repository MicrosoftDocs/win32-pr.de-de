---
description: Die getframedstaddressoffset-Funktion gibt den Offset an die Zieladresse eines angegebenen Frames zurück.
ms.assetid: 8922d7d0-1a23-47ac-886b-fcc0bcaa6ba7
title: Getframedstaddressoffset-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDstAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8358afdbb303baf623cef6fc32e00d758570d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345660"
---
# <a name="getframedstaddressoffset-function"></a>Getframedstaddressoffset-Funktion

Die **getframedstaddressoffset** -Funktion gibt den Offset an die Zieladresse eines angegebenen Frames zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI GetFrameDstAddressOffset(
  _In_ HFRAME  hFrame,
  _In_ DWORD   AddressType,
  _In_ LPDWORD AddressLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hframe* \[ in\]
</dt> <dd>

Handle für den Frame.

</dd> <dt>

*Adresstype* \[ in\]
</dt> <dd>

Der Typ der Zieladresse. Geben Sie einen der folgenden Werte an.

Address \_ Type \_ Ethernet Address \_ Type \_ IP Address Type IP Address Type IP Address Type \_ \_ IPX Address \_ Type \_ TokenRing Address Type Typ des Typs " \_ \_ XNS Address Type" der \_ \_ \_ \_ \_ IP-Adresse \_ \_ des Typs "ATM".

</dd> <dt>

*Addresslength* \[ in\]
</dt> <dd>

Länge der Zieladresse in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert der Offset (in Bytes) bis zum angeforderten Adresstyp.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert minus eins (-1).

## <a name="remarks"></a>Bemerkungen

Wenn der *Adresstype* -Parameter auf Address Type Ethernet festgelegt ist \_ \_ , ist der Rückgabewert der **getframedstaddressoffset** -Funktion immer 0 (null). Der Offset einer Ethernet-Adresse ist immer 0 (null).

[*Experten*](e.md) und [*Parser*](p.md) können die **getframedstaddressoffset** -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




