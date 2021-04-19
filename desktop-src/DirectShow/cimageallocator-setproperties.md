---
description: 'Die SetProperties-Methode gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an. Diese Methode überschreibt die cbasezucator:: SetProperties-Methode.'
ms.assetid: 8d419432-a9a7-44fb-b916-8dacd08eb6ec
title: Cimagezuzuordcator. SetProperties-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c04501fe3511d9cdd45f3513c68082d2ffece0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372225"
---
# <a name="cimageallocatorsetproperties-method"></a>Cimagezuzuordcator. SetProperties-Methode

Die `SetProperties` -Methode gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an. Diese Methode überschreibt die [**cbasezucator:: SetProperties**](cbaseallocator-setproperties.md) -Methode.

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

Zeiger auf eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die die Puffer Anforderungen enthält.

</dd> <dt>

*pactual* 
</dt> <dd>

Ein Zeiger auf eine **\_ zuordnereigenschafts** -Struktur, die die tatsächlichen Puffer Eigenschaften empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft [**cimagezuordcator:: checksizes**](cimageallocator-checksizes.md) auf, um die angeforderte Puffergröße zu überprüfen. Außerdem wird die Basisklassen Version von aufgerufen `SetProperties` .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagezuordcator-Klasse**](cimageallocator.md)
</dt> </dl>

 

 




