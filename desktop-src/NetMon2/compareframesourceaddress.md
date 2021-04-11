---
description: Die compareframesourceaddress-Funktion vergleicht eine Adresse mit der Quelladresse eines Frames.
ms.assetid: 7221c0cc-d6c1-4ec9-bf11-3ba1fefb35da
title: Compareframesourceaddress-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a100273c37e25a7b1deba86ed2704886dbfccc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217339"
---
# <a name="compareframesourceaddress-function"></a>Compareframesourceaddress-Funktion

Die **compareframesourceaddress** -Funktion vergleicht eine Adresse mit der Quelladresse eines Frames.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CompareFrameSourceAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hframe* \[ in\]
</dt> <dd>

Handle für einen Frame.

</dd> <dt>

*lpAddress* \[ in\]
</dt> <dd>

Zeiger auf eine Adresse.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Adressen identisch sind, ist der Rückgabewert " **true**".

Wenn die Adressen nicht identisch sind, ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

Damit die **compareframesourceaddress** -Funktion erfolgreich ausgeführt werden kann, muss der Quell Adresstyp mit dem Adresstyp übereinstimmen, der im *lpAddress* -Parameter angegeben ist.

Netzwerkmonitor bietet zwei weitere Funktionen zum Vergleichen von Adressen: [compareframedestaddress](compareframedestaddress.md) und [compareadressen](compareaddresses.md). Die **compareframerestaddress** -Funktion vergleicht eine angegebene Adresse mit der Zieladresse des Frames, und die **compareaddress** -Funktion vergleicht zwei angegebene Adressen.

[*Experten*](e.md) und [*Parser*](p.md) können die **compareframesourceaddress** -Funktion abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Compareadressen](compareaddresses.md)
</dt> <dt>

[Compareframedebug](compareframedestaddress.md)
</dt> </dl>

 

 




