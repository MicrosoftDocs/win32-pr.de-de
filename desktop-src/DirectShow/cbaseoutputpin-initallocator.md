---
description: Die InitAllocator-Methode erstellt eine Speicherzuweisung.
ms.assetid: a1fa0ffb-ed43-446d-811e-6c3594743592
title: CBaseOutputPin.InitAllocator-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.InitAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce1e8f8097ca88d0434f79c20e855d8b61798b5a1b0e32b6a38077e4c7aa1271
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652460"
---
# <a name="cbaseoutputpininitallocator-method"></a>CBaseOutputPin.InitAllocator-Methode

Die `InitAllocator` -Methode erstellt eine Speicherzuweisung.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT InitAllocator(
   IMemAllocator **ppAlloc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppAlloc* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) der Zuweisung empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich, oder einen Fehlercode von der **CoCreateInstance-Funktion.**

## <a name="remarks"></a>Hinweise

Wenn der Eingabepin keine Speicherzuweisung bietet, ruft die [**CBaseOutputPin::D ecideAllocator-Methode**](cbaseoutputpin-decideallocator.md) diese Methode auf, um eine Zuweisung zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




