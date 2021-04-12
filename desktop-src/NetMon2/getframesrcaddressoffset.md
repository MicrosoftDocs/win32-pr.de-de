---
description: Die getframesrcaddressoffset-Funktion gibt den Offset der Quelladresse der Frames zurück.
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: Getframesrcaddressoffset-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSrcAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f7310c0ac2c6f402c37537100cc8060fef9eedd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217173"
---
# <a name="getframesrcaddressoffset-function"></a>Getframesrcaddressoffset-Funktion

Die **getframesrcaddressoffset** -Funktion gibt den Offset der Quelladresse des Frames zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI GetFrameSrcAddressOffset(
   HFRAME  hFrame,
   DWORD   AddressType,
   LPDWORD AddressLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hframe* 
</dt> <dd>

Handle für den Frame.

</dd> <dt>

*Adresstyp* 
</dt> <dd>

Der Quell Adressentyp. Der Parameterwert kann eines der folgenden sein:

-   \_Adresstyp \_ Ethernet
-   Address \_ Type \_ IP
-   \_Adresstyp \_ IPX
-   \_Adresstyp \_ TokenRing
-   Adresstyp " \_ \_ f"
-   Address \_ Type \_ XNS
-   Address \_ Type \_ Vines \_ IP
-   \_Adresstyp \_ ATM

</dd> <dt>

*Addresslength* 
</dt> <dd>

Ein Zeiger auf ein **DWORD**, das bei der Rückgabe die Länge der Adresse in Bytes enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert der Offset zur Quelladresse.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert minus eins (-1).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




