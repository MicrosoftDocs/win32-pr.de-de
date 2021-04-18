---
description: Mit der GetState-Methode wird der Zustand des Filters abgerufen (wird ausgeführt, beendet oder angehalten).
ms.assetid: 5d35824c-2509-499a-bbb1-1fb916b51808
title: Cbaserderderer. GetState-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 451078a6167ff7ca89ad4153c416826af8ac6d05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371013"
---
# <a name="cbaserenderergetstate-method"></a>Cbaserderderer. GetState-Methode

Mit der `GetState` -Methode wird der Zustand des Filters abgerufen (wird ausgeführt, beendet oder angehalten).

## <a name="syntax"></a>Syntax


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwmillisecstimeout* 
</dt> <dd>

Timeout Intervall in Millisekunden.

</dd> <dt>

*State* 
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Member des Enumerationstyps des [**Filter \_ Zustands**](/windows/win32/api/strmif/ne-strmif-filter_state) empfängt, der den Zustand des Filters angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                                | Beschreibung                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                                            |
| <dl> <dt>**VFW \_ S \_ State \_ Intermediate**</dt> </dl> | Der Filter wechselt in den Status "angegeben".<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>                  | **Null** -Zeigerargument.<br/>                          |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbasefilter:: GetState**](cbasefilter-getstate.md) -Methode. Wenn der Renderer angehalten wird, schließt er den Zustandsübergang erst ab, wenn er ein zum renderingmuster empfängt. Wenn das Timeout abläuft, bevor der Zustandsübergang beendet ist, gibt die Methode VFW \_ S \_ State Intermediate zurück \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




