---
description: 'Die GetProperties-Methode ruft die Anzahl der Puffer, die von der Zuweisung erstellt werden, und die Puffer Eigenschaften ab. Diese Methode implementiert die imemzuzucator:: GetProperties-Methode.'
ms.assetid: ccee4d69-52fc-4e3c-b6a4-787914708be4
title: Cbasezucator. GetProperties-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abf143b11b6dd67fca6c87f9a31ce69f18951311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359373"
---
# <a name="cbaseallocatorgetproperties-method"></a>Cbasezucator. GetProperties-Methode

Die `GetProperties` -Methode ruft die Anzahl der Puffer, die von der Zuweisung erstellt werden, und die Puffer Eigenschaften ab. Diese Methode implementiert die [**imemzuzucator:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProperties(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*p-Eigenschaften* 
</dt> <dd>

Zeiger auf eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die die zuordnereigenschaften empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasezucator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




