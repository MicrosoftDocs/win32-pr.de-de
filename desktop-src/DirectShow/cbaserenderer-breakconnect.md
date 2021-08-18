---
description: Die BreakConnect-Methode gibt den Eingabepin von einer Verbindung frei.
ms.assetid: e295cec1-8c8f-471c-8832-075ac7708cb1
title: CBaseRenderer.BreakConnect-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cefaa91578f397a5ce967dc9cb6200acbe45f016e81f4552b9d185ad9ffa2609
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044060"
---
# <a name="cbaserendererbreakconnect-method"></a>CBaseRenderer.BreakConnect-Methode

Die `BreakConnect` -Methode gibt den Eingabepin von einer Verbindung frei.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                         | Beschreibung                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>             | Die Stecknadel war nicht verbunden.<br/>  |
| <dl> <dt>**S \_ OK**</dt> </dl>                | Erfolg.<br/>                    |
| <dl> <dt>**VFW \_ E \_ NICHT \_ BEENDET**</dt> </dl> | Der Filter ist weiterhin aktiv.<br/> |



 

## <a name="remarks"></a>Hinweise

Der Eingabepin des Filters ruft diese Methode aus der eigenen Methode heraus `BreakConnect` auf. (Weitere Informationen finden Sie unter [**CBasePin::BreakConnect**](cbasepin-breakconnect.md).) Der Filter führt eine interne Buchführung durch, z. B. das Zurücksetzen des Flags für das Ende des Streams.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




