---
description: Die Wait-Methode wird blockiert, bis das Ereignis signalisiert wird oder bis ein Time out auftritt.
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: WEBCAMEvent.Wait-Methode (Wxutil.h)
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
ms.openlocfilehash: 3875647cb93619e8326066bc9af7a6f99f79a0b0a2df58f668b1e365fd39102b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662511"
---
# <a name="cameventwait-method"></a>CAMEvent.Wait-Methode

Die `Wait` -Methode wird blockiert, bis das Ereignis signalisiert wird oder bis ein Time out auftritt.

## <a name="syntax"></a>Syntax


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwTimeout* 
</dt> <dd>

Optionaler Time out-Wert, dargestellt in Millisekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn das Ereignis signalisiert wird. Andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

Bei Automatisch zurücksetzungsereignissen wird das Ereignis in einen nicht signalisierte Zustand zurückgesetzt, wenn diese Methode zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CAMEvent-Klasse**](camevent.md)
</dt> </dl>

 

 




