---
description: Die GetCurrentPosition-Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab. Nicht implementiert.
ms.assetid: 386f41e4-a673-4c67-a28f-e155810fbb5a
title: Csourceseeking. GetCurrentPosition-Methode (ctlutil. h)
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
ms.openlocfilehash: 52f99323e5ce3a62f1964cad2586a18ad473cdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361316"
---
# <a name="csourceseekinggetcurrentposition-method"></a>Csourceseeking. GetCurrentPosition-Methode

Die- `GetCurrentPosition` Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab. Nicht implementiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcurrent* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die aktuelle Position in Einheiten des aktuellen Zeit Formats empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "E \_ notimpl" zurück.

## <a name="remarks"></a>Bemerkungen

Quell Filter unterstützen diese Methode in der Regel nicht. Stattdessen melden rendererfilter die aktuelle Position über die [**crendererpospassthru**](crendererpospassthru.md) -Klasse.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




