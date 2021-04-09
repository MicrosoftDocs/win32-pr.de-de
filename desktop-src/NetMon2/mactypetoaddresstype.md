---
description: Die Funktion "mactypedeadresssstype" konvertiert einen angegebenen Mac-Typ in einen Adresstyp.
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: Mactypedeadresssstype-Funktion (Netmon. h)
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
ms.openlocfilehash: b0a0eb7a18126062c201fb7f0b122bca3ea8b631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862859"
---
# <a name="mactypetoaddresstype-function"></a>Mactypedeadresssstype-Funktion

Die Funktion " **mactypedeadresssstype** " konvertiert einen angegebenen Mac-Typ in einen Adresstyp.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MacType* \[ in\]
</dt> <dd>

Der Mac-Typ, der konvertiert werden soll. Geben Sie einen der folgenden Werte an.

Mac \_ Type \_ Ethernet Mac \_ Type \_ TokenRing Mac \_ Type \_ f

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert einer der folgenden Adresstypen.

Address \_ Type \_ Ethernet Address \_ Type \_ TokenRing Address \_ Type \_ f

Wenn die Funktion nicht erfolgreich ist, ist der Mac-Typ unbekannt. der Rückgabewert ist-1.

## <a name="remarks"></a>Bemerkungen

[*Experten*](e.md) und [*Parser*](p.md) können die Funktion " **mactypedeadresssstype** " aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




