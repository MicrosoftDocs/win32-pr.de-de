---
description: Die Wait-Methode blockiert, bis das-Ereignis signalisiert wird, oder bis ein Timeout auftritt.
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: Camevent. Wait-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Wait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ab5bc2aabf77fb73739528e99cda7961ae87e9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365732"
---
# <a name="cameventwait-method"></a>Camevent. Wait-Methode

Die- `Wait` Methode wird blockiert, bis das-Ereignis signalisiert wird, oder bis ein Timeout auftritt.

## <a name="syntax"></a>Syntax


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwtimeout* 
</dt> <dd>

Optionaler Timeout Wert, dargestellt in Millisekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn das Ereignis signalisiert wird. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Bei automatischen Zurücksetzungs Ereignissen wird das Ereignis auf einen nicht signalisierten Zustand zurückgesetzt, wenn diese Methode zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camevent-Klasse**](camevent.md)
</dt> </dl>

 

 




