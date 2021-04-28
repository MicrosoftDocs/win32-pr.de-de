---
description: 'CTransformFilter.Pause-Methode: Die Pause-Methode hält den Filter an. Diese Methode implementiert die IMediaFilter::P ause-Methode.'
ms.assetid: 3e3afd14-1c92-4f2b-a367-e10caaeb3b63
title: CTransformFilter.Pause-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 903522b63754ff7972e4cdcf5221946442497896
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095098"
---
# <a name="ctransformfilterpause-method"></a>CTransformFilter.Pause-Methode

Die `Pause` -Methode hält den Filter an. Diese Methode implementiert die [**IMediaFilter::P ause-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause)

## <a name="syntax"></a>Syntax


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**StartStreaming-Methode**](ctransformfilter-startstreaming.md) auf. Die **StartStreaming-Methode** führt in der Basisklasse nichts aus, aber die abgeleitete Klasse kann sie überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




