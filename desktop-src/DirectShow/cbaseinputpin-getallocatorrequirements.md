---
description: Die GetAllocatorRequirements-Methode ruft die vom Eingabepin angeforderten Zuweisungseigenschaften ab.
ms.assetid: 81564924-6d5b-4b2a-b549-e3f358f18371
title: CBaseInputPin.GetAllocatorRequirements-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57b085cd82c45fd78ddaa4794084cba775e1c80cd8b9e3b8df4c9680379ba462
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586370"
---
# <a name="cbaseinputpingetallocatorrequirements-method"></a>CBaseInputPin.GetAllocatorRequirements-Methode

Die `GetAllocatorRequirements` -Methode ruft die vom Eingabepin angeforderten Zuweisungseigenschaften ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pProps* 
</dt> <dd>

Zeiger auf eine [**ALLOCATOR \_ PROPERTIES-Struktur,**](/windows/win32/api/strmif/ns-strmif-allocator_properties) die mit den Anforderungen gefüllt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ NOTIMPL zurück.

## <a name="remarks"></a>Hinweise

Wenn ein Ausgabepin eine Speicherzuweisung initialisiert, kann er diese Methode aufrufen, um zu bestimmen, ob der Eingabepin Pufferanforderungen hat. Weitere Informationen finden Sie unter [**CBaseOutputPin::D ecideAllocator**](cbaseoutputpin-decideallocator.md).

Die Implementierung dieser Methode ist optional. Wenn der Filter bestimmte Ausrichtungs- oder Präfixanforderungen hat, überschreiben Sie diese Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseInputPin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




