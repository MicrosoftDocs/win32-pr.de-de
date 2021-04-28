---
description: 'CBaseRenderer.GetPin-Methode: Die GetPin-Methode ruft einen Pin ab.'
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: CBaseRenderer.GetPin-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b7c30767b7cba68931bc1ddde4905c9b7bc2bc29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119888"
---
# <a name="cbaserenderergetpin-method"></a>CBaseRenderer.GetPin-Methode

Die `GetPin` -Methode ruft einen Pin ab.

## <a name="syntax"></a>Syntax


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*n* 
</dt> <dd>

Die Nummer des angegebenen Pins. Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den [**\_ PInputPin-Zeiger CBaseRenderer::m**](cbaserenderer-m-pinputpin.md) zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode implementiert die [**CBaseFilter::GetPin-Methode,**](cbasefilter-getpin.md) die in der **CBaseFilter-Klasse** rein virtuell ist. Der Filter unterstützt genau einen Pin (den Eingabepin). Beim ersten Aufrufen dieser Methode wird der Pin als neues [**CRendererInputPin-Objekt**](crendererinputpin.md) erstellt.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




