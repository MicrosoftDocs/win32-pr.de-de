---
description: Die CompareFrameDestAddress-Funktion vergleicht eine Adresse mit der Zieladresse eines Frames.
ms.assetid: 739b3b9f-f989-459d-ac3e-6be7769adc06
title: CompareFrameDestAddress-Funktion (Netmon.h)
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
ms.openlocfilehash: 153d1a5768791a33fd4f7629e071a125a4ee2ee46feaae366e2c1a21d8118f01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367388"
---
# <a name="compareframedestaddress-function"></a>CompareFrameDestAddress-Funktion

Die **CompareFrameDestAddress-Funktion** vergleicht eine Adresse mit der Zieladresse eines Frames.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CompareFrameDestAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFrame* \[ In\]
</dt> <dd>

Handle für einen Frame.

</dd> <dt>

*lpAddress* \[ In\]
</dt> <dd>

Zeiger auf eine Adresse.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Adressen identisch sind, ist der Rückgabewert **TRUE.**

Wenn die Adressen nicht identisch sind, ist der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

Damit die **CompareFrameDestAddress-Funktion** erfolgreich zurückgibt, muss der Zieladressentyp mit dem Im *lpAddress-Parameter angegebenen Adresstyp* übereinstimmen.

Netzwerkmonitor bietet zwei weitere Funktionen, [CompareFrameSourceAddress und](compareframesourceaddress.md) [CompareAddresses,](compareaddresses.md)die Sie zum Vergleichen von Adressen verwenden können. Die **CompareFrameSourceAddress-Funktion** vergleicht eine angegebene Adresse mit der Quelladresse des Frames, und die **CompareAddress-Funktion** vergleicht zwei angegebene Adressen.

[*Experten*](e.md) und [*Parser*](p.md) können die **Funktion CompareFrameDestAddress** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[CompareAddresses](compareaddresses.md)
</dt> <dt>

[CompareFrameSourceAddress](compareframesourceaddress.md)
</dt> </dl>

 

 




