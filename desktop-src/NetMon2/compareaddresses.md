---
description: Die compareaddress-Funktion vergleicht zwei Adressen, die angeben, dass eine der Adressen größer als, kleiner oder gleich der anderen Adresse ist.
ms.assetid: 76ff37d2-714f-4bac-adcc-eab78c8f25d3
title: Compareadressen-Funktion (Netmon. h)
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
ms.openlocfilehash: fd72ef0281615c0b56176e86ee9bb3659b498a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348106"
---
# <a name="compareaddresses-function"></a>Compareadressen-Funktion

Die **compareaddress** -Funktion vergleicht zwei Adressen, die angeben, dass eine der Adressen größer als, kleiner oder gleich der anderen Adresse ist.

## <a name="syntax"></a>Syntax


```C++
int WINAPI CompareAddresses(
  _In_ LPADDRESS lpAddress1,
  _In_ LPADDRESS lpAddress2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpAddress1* \[ in\]
</dt> <dd>

Zeiger auf die erste Adresse.

</dd> <dt>

*lpAddress2* \[ in\]
</dt> <dd>

Zeiger auf die zweite Adresse.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Adressen identisch sind, gibt die Funktion 0 (null) zurück.

Wenn der *lpAddress1* -Parameter eine Adresse angibt, die kleiner als die Adresse ist, die der *lpAddress2* -Parameter angibt, ist der Rückgabewert eine negative Zahl.

Wenn der *lpAddress1* -Parameter eine Adresse angibt, die größer als die Adresse ist, die der *lpAddress2* -Parameter angibt, ist der Rückgabewert eine positive Zahl.

## <a name="remarks"></a>Bemerkungen

Eine Adresse, die kleiner als eine andere Adresse ist, weist auf einen vorherigen Frame hin. Eine Adresse, die größer als eine andere Adresse ist, weist auf einen späteren Frame hin.

Netzwerkmonitor bietet zwei weitere Funktionen, [compareframedestaddress](compareframedestaddress.md) und [compareframesourceaddress](compareframesourceaddress.md), die Sie zum Vergleichen von Adressen verwenden können. Die **compareframedebug** -Funktion vergleicht eine angegebene Adresse mit der Zieladresse des Frames, und die **compareframesourceaddress** -Funktion vergleicht eine angegebene Adresse mit der Quelladresse des Frames.

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

[Compareframedebug](compareframedestaddress.md)
</dt> <dt>

[Compareframesourceaddress](compareframesourceaddress.md)
</dt> </dl>

 

 




