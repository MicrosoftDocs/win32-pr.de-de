---
description: Die SetProperties-Methode gibt die Anzahl der zu reservierenden Puffer und die Größe der einzelnen Puffer an.
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: CMemAllocator.SetProperties-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5c5a145e630101bda4d060058cde7bfd91796386f0915e9e5329f63ced43ef19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821965"
---
# <a name="cmemallocatorsetproperties-method"></a>CMemAllocator.SetProperties-Methode

Die `SetProperties` -Methode gibt die Anzahl der zu reservierenden Puffer und die Größe der einzelnen Puffer an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pRequest* 
</dt> <dd>

Zeiger auf eine [**ALLOCATOR \_ PROPERTIES-Struktur,**](/windows/win32/api/strmif/ns-strmif-allocator_properties) die die Pufferanforderungen enthält.

</dd> <dt>

*pActual* 
</dt> <dd>

Zeiger auf eine **ALLOCATOR \_ PROPERTIES-Struktur,** die die tatsächlichen Puffereigenschaften empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                                 | Beschreibung                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                        | Erfolg.<br/>                                                   |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>                   |  NULL-Zeigerargument.<br/>                                 |
| <dl> <dt>**VFW \_ E \_ ALREADY \_ COMMITTED**</dt> </dl>   | Der zugeordnete Arbeitsspeicher kann nicht geändert werden, während der Filter aktiv ist.<br/> |
| <dl> <dt>**VFW \_ E \_ BADALIGN**</dt> </dl>             | Es wurde eine ungültige Ausrichtung angegeben.<br/>                        |
| <dl> <dt>**AUSSTEHENDE VFW \_ \_ \_ E-PUFFER**</dt> </dl> | Mindestens ein Puffer ist noch aktiv.<br/>                      |



 

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBaseAllocator::SetProperties-Methode.**](cbaseallocator-setproperties.md)

Die Pufferausrichtung, die vom **cbAlign-Member** der **ALLOCATOR \_ PROPERTIES-Struktur** angegeben wird, muss eine gleichmäßige Leistung von zwei aufweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMemAllocator-Klasse**](cmemallocator.md)
</dt> </dl>

 

 




