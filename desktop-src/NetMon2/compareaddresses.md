---
description: Die CompareAddresses-Funktion vergleicht zwei Adressen und gibt an, dass eine der Adressen größer als, kleiner oder gleich der anderen Adresse ist.
ms.assetid: 76ff37d2-714f-4bac-adcc-eab78c8f25d3
title: CompareAddresses-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 323afb66d251d58bf13670fd335da2bd26ad2193ce03d5aa799ddb0f28e875fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744720"
---
# <a name="compareaddresses-function"></a>CompareAddresses-Funktion

Die **CompareAddresses-Funktion** vergleicht zwei Adressen und gibt an, dass eine der Adressen größer als, kleiner oder gleich der anderen Adresse ist.

## <a name="syntax"></a>Syntax


```C++
int WINAPI CompareAddresses(
  _In_ LPADDRESS lpAddress1,
  _In_ LPADDRESS lpAddress2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpAddress1* \[ In\]
</dt> <dd>

Zeiger auf die erste Adresse.

</dd> <dt>

*lpAddress2* \[ In\]
</dt> <dd>

Zeiger auf die zweite Adresse.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Adressen identisch sind, gibt die Funktion 0 (null) zurück.

Wenn der *lpAddress1-Parameter* eine Adresse angibt, die kleiner als die Adresse ist, die der *lpAddress2-Parameter* angibt, ist der Rückgabewert eine negative Zahl.

Wenn der *lpAddress1-Parameter* eine Adresse angibt, die größer ist als die Adresse, die der *lpAddress2-Parameter* angibt, ist der Rückgabewert eine positive Zahl.

## <a name="remarks"></a>Hinweise

Eine Adresse, die kleiner als eine andere Adresse ist, gibt einen vorherigen Frame an. Eine Adresse, die größer als eine andere Adresse ist, gibt einen späteren Frame an.

Netzwerkmonitor stellt zwei weitere Funktionen bereit: [CompareFrameDestAddress](compareframedestaddress.md) und [CompareFrameSourceAddress,](compareframesourceaddress.md)die Sie zum Vergleichen von Adressen verwenden können. Die **CompareFrameDestAddress-Funktion** vergleicht eine angegebene Adresse mit der Zieladresse des Frames, und die **CompareFrameSourceAddress-Funktion** vergleicht eine angegebene Adresse mit der Quelladresse des Frames.

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

[CompareFrameDestAddress](compareframedestaddress.md)
</dt> <dt>

[CompareFrameSourceAddress](compareframesourceaddress.md)
</dt> </dl>

 

 




