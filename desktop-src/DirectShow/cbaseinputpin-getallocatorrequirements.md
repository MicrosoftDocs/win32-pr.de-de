---
description: Die getallocatorrequirements-Methode ruft die von der eingabepin angeforderten zuordnereigenschaften ab.
ms.assetid: 81564924-6d5b-4b2a-b549-e3f358f18371
title: Cbaseinputpin. getalloovorrequirements-Methode (amfilter. h)
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
ms.openlocfilehash: f0239d226ea57ed5953fa65b925eeffaa0b13df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352898"
---
# <a name="cbaseinputpingetallocatorrequirements-method"></a>Cbaseinputpin. getalloovorrequirements-Methode

Die- `GetAllocatorRequirements` Methode ruft die von der eingabepin angeforderten zuordnereigenschaften ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*p-Eigenschaften* 
</dt> <dd>

Zeiger auf eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die mit den Anforderungen ausgefüllt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "E \_ notimpl" zurück.

## <a name="remarks"></a>Bemerkungen

Wenn eine Ausgabe-PIN eine Speicherzuweisung initialisiert, kann diese Methode aufgerufen werden, um zu bestimmen, ob die Eingabe-PIN über Puffer Anforderungen verfügt. Weitere Informationen finden Sie unter [**cbaseoutputpin::D ecidezuordcator**](cbaseoutputpin-decideallocator.md).

Das Implementieren dieser Methode ist optional. Wenn der Filter bestimmte Ausrichtung oder Präfix Anforderungen aufweist, überschreiben Sie diese Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseingeputpin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




