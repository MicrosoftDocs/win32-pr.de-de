---
description: Die SetProperties-Methode gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an. Diese Methode implementiert die IMemAllocator::SetProperties-Methode.
ms.assetid: f53c22a4-c01d-4d2f-81f0-bedf8f2ae5f0
title: CBaseAllocator.SetProperties-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d81ee1c29f1c9e2cc9927f926144a7427b5e94f72406f94ce65f7d4a20e2ab32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057480"
---
# <a name="cbaseallocatorsetproperties-method"></a>CBaseAllocator.SetProperties-Methode

Die `SetProperties` -Methode gibt die Anzahl der zuzuordnenden Puffer und die Größe jedes Puffers an. Diese Methode implementiert die [**IMemAllocator::SetProperties-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties)

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

Gibt einen der folgenden **HRESULT-Werte** zurück.



| Rückgabecode                                                                                                 | Beschreibung                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                        | Erfolg.<br/>                                                   |
| <dl> <dt>**E \_ POINTER**</dt> </dl>                   | **NULL-Zeigerargument.**<br/>                                 |
| <dl> <dt>**VFW \_ E \_ ALREADY \_ COMMITTED**</dt> </dl>   | Der zugeordnete Arbeitsspeicher kann nicht geändert werden, während der Filter aktiv ist.<br/> |
| <dl> <dt>**VFW \_ E \_ BADALIGN**</dt> </dl>             | Es wurde eine ungültige Ausrichtung angegeben.<br/>                        |
| <dl> <dt>**VFW \_ E \_ BUFFERS \_ OUTSTANDING**</dt> </dl> | Mindestens ein Puffer ist noch aktiv.<br/>                      |



 

## <a name="remarks"></a>Hinweise

Diese Methode gibt die Pufferanforderungen an, ordnet jedoch keine Puffer zu. Rufen Sie die [**CBaseAllocator::Commit-Methode**](cbaseallocator-commit.md) auf, um Puffer zuzuordnen.

Der Aufrufer ordnet zwei ALLOCATOR \_ PROPERTIES-Strukturen zu. Der *pRequest-Parameter* enthält die Pufferanforderungen des Aufrufers, einschließlich der Anzahl der Puffer und der Größe jedes Puffers. Wenn die Methode zurückgegeben wird, enthält der *pActual-Parameter* die tatsächlichen Puffereigenschaften, die von der Zuweisung festgelegt werden. In der Basisklasse stimmen die tatsächlichen Eigenschaften immer mit den angeforderten Eigenschaften überein, sofern die Methode erfolgreich ist. Abgeleitete Klassen können dieses Verhalten überschreiben.

Für die Zuweisung darf kein Commit ausgeführt werden, und es dürfen keine ausstehenden Puffer vorhanden sein. In der Basisklasse muss die Ausrichtung gleich 1 sein. Die [**CMemAllocator-Klasse**](cmemallocator.md) überschreibt diese Anforderung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




