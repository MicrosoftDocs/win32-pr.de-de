---
description: Die GetCurrentPosition-Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab. Nicht implementiert.
ms.assetid: 386f41e4-a673-4c67-a28f-e155810fbb5a
title: CSourceSeeking.GetCurrentPosition-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff4069c8b1a83ade6897fedf87c16b89b1c63d3c1cef18d21a3bdbd594a3b2cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084057"
---
# <a name="csourceseekinggetcurrentposition-method"></a>CSourceSeeking.GetCurrentPosition-Methode

Die `GetCurrentPosition` -Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab. Nicht implementiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCurrent* 
</dt> <dd>

Zeiger auf eine Variable, die die aktuelle Position in Einheiten des aktuellen Zeitformats empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ NOTIMPL zurück.

## <a name="remarks"></a>Hinweise

Quellfilter unterstützen diese Methode in der Regel nicht. Rendererfilter melden stattdessen die aktuelle Position über die [**CRendererPosPassThru-Klasse.**](crendererpospassthru.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




