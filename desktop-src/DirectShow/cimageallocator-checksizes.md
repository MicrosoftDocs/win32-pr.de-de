---
description: Die CheckSizes-Methode überprüft Zuweisungseigenschaften mit dem aktuellen Medientyp.
ms.assetid: 040b4ed0-c1cc-4995-a0f8-86efa493f84b
title: CImageAllocator.CheckSizes-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CheckSizes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 070c0cac981f73ea6fa7e3c0ecb620e262f744edd651571be9b592840ad23956
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076230"
---
# <a name="cimageallocatorchecksizes-method"></a>CImageAllocator.CheckSizes-Methode

Die `CheckSizes` -Methode überprüft Zuweisungseigenschaften mit dem aktuellen Medientyp.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckSizes(
   ALLOCATOR_PROPERTIES *pRequest
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pRequest* 
</dt> <dd>

Zeiger auf eine [**ALLOCATOR \_ PROPERTIES-Struktur,**](/windows/win32/api/strmif/ns-strmif-allocator_properties) die die angeforderten Zuweisungseigenschaften beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                           | Beschreibung                                                                 |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Die angeforderten Eigenschaften sind mit dem Medientyp kompatibel.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Die angeforderten Eigenschaften sind nicht mit dem Medientyp kompatibel.<br/> |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der besitzende Pin ist nicht verbunden.<br/>                                 |



 

## <a name="remarks"></a>Hinweise

Wenn die Methode zurückgegeben wird und der Rückgabewert S OK ist, enthält \_ das **cbBuffer-Element** von *pRequest* die tatsächliche Puffergröße. Dies ist möglicherweise größer als die angeforderte Größe, wird aber nie kleiner sein.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CImageAllocator-Klasse**](cimageallocator.md)
</dt> </dl>

 

 




