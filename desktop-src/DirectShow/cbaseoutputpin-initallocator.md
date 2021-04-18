---
description: Die initbelegcator-Methode erstellt eine Speicherzuweisung.
ms.assetid: a1fa0ffb-ed43-446d-811e-6c3594743592
title: CBaseOutputPin.IniTAllocator-Methode (amfilter. h)
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
ms.openlocfilehash: 7e5385671ba4c7fdf1b719f83aafba7d84421bce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371294"
---
# <a name="cbaseoutputpininitallocator-method"></a>CBaseOutputPin.IniTAllocator-Methode

Die- `InitAllocator` Methode erstellt eine Speicherzuweisung.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT InitAllocator(
   IMemAllocator **ppAlloc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppzuweisung* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " \_ OK" zurück, wenn erfolgreich, oder einen Fehlercode aus der **cokreateinzustance** -Funktion.

## <a name="remarks"></a>Bemerkungen

Wenn die Eingabe-PIN keine Speicherzuweisung bereitstellt, ruft die [**cbaseoutputpin::D ecidezuordcator**](cbaseoutputpin-decideallocator.md) -Methode diese Methode auf, um eine Zuweisung zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseoutputpin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




