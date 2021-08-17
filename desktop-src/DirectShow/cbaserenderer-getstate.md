---
description: Die GetState-Methode ruft den Zustand der Filter ab (wird ausgeführt, angehalten oder angehalten).
ms.assetid: 5d35824c-2509-499a-bbb1-1fb916b51808
title: CBaseRenderer.GetState-Methode (Renbase.h)
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
ms.openlocfilehash: 532a41bb9e39f844b3a485fc236ae8d03450d45cdcb45d92c8cfa94d9af4a4bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403409"
---
# <a name="cbaserenderergetstate-method"></a>CBaseRenderer.GetState-Methode

Die `GetState` -Methode ruft den Zustand der Filter ab (wird ausgeführt, angehalten oder angehalten).

## <a name="syntax"></a>Syntax


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwMsecsTimeout* 
</dt> <dd>

Time out-Intervall in Millisekunden.

</dd> <dt>

*State* 
</dt> <dd>

Zeiger auf eine Variable, die einen Member des Enumerationstyps [**FILTER \_ STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) empfängt, der den Zustand des Filters angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                                | Beschreibung                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                                            |
| <dl> <dt>**VFW \_ S \_ STATE \_ INTERMEDIATE**</dt> </dl> | Der Filter wechselt in den angegebenen Zustand.<br/> |
| <dl> <dt>**E \_ POINTER**</dt> </dl>                  | **NULL-Zeigerargument.**<br/>                          |



 

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBaseFilter::GetState-Methode.**](cbasefilter-getstate.md) Wenn der Renderer angehalten wird, wird der Zustandsübergang erst abgeschlossen, wenn er ein Beispiel zum Rendern empfängt. Wenn das Time out abläuft, bevor der Zustandsübergang abgeschlossen ist, gibt die Methode VFW \_ S \_ STATE INTERMEDIATE \_ zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




