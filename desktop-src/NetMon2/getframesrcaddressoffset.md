---
description: Die GetFrameSrcAddressOffset-Funktion gibt den Offset der Quelladresse des Frames zurück.
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: GetFrameSrcAddressOffset-Funktion (Netmon.h)
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
ms.openlocfilehash: 5c8c2315b53d336a06a73e63019daee842439f65aa53e3fb7d34d4944dcab9cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366094"
---
# <a name="getframesrcaddressoffset-function"></a>GetFrameSrcAddressOffset-Funktion

Die **GetFrameSrcAddressOffset-Funktion** gibt den Offset der Quelladresse des Frames zurück.

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

*hFrame* 
</dt> <dd>

Handle für den Frame.

</dd> <dt>

*Adresstyp* 
</dt> <dd>

Quelladressentyp. Der Parameterwert kann einer der folgenden sein:

-   ADRESSTYP \_ \_ ETHERNET
-   \_ \_ IP-ADRESSTYP
-   ADRESSTYP \_ \_ IPX
-   ADDRESS \_ TYPE \_ TOKENRING
-   \_ \_ ADRESSTYP-FDDI
-   ADRESSTYP \_ \_ XNS
-   ADRESSE \_ TYP \_ VINES \_ IP
-   ADRESSTYP \_ \_ ATM

</dd> <dt>

*AddressLength* 
</dt> <dd>

Zeiger auf ein **DWORD,** das bei der Rückgabe die Länge der Adresse in Bytes enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert der Offset zur Quelladresse.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert minus eins (-1).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




