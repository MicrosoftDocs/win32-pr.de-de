---
description: Die compareframedebug-Funktion vergleicht eine Adresse mit der Zieladresse eines Frames.
ms.assetid: 739b3b9f-f989-459d-ac3e-6be7769adc06
title: Compareframedebug-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: a9ce0ff776588c06b8fddc34240e9c2170ceca69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864796"
---
# <a name="compareframedestaddress-function"></a>Compareframedebug-Funktion

Die **compareframedebug** -Funktion vergleicht eine Adresse mit der Zieladresse eines Frames.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CompareFrameDestAddress(
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

Damit die **compareframedestaddress** -Funktion erfolgreich zurückgegeben wird, muss der Ziel Adresstyp mit dem im *lpAddress* -Parameter angegebenen Adresstyp identisch sein.

Netzwerkmonitor bietet zwei weitere Funktionen, [compareframesourceaddress](compareframesourceaddress.md) und [compareaddress](compareaddresses.md), die Sie zum Vergleichen von Adressen verwenden können. Die **compareframesourceaddress** -Funktion vergleicht eine angegebene Adresse mit der Quelladresse des Frames, und die **compareaddress** -Funktion vergleicht zwei angegebene Adressen.

[*Experten*](e.md) und [*Parser*](p.md) können die **compareframedebug** -Funktion aufzurufen.

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

[Compareframesourceaddress](compareframesourceaddress.md)
</dt> </dl>

 

 




