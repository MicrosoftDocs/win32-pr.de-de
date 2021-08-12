---
description: Die GetSourcePosition-Methode ruft die Position und dimensionen des Quellrechtecks in einem atomaren Vorgang ab.
ms.assetid: 44356f62-8b14-4b0e-a587-f832adff3bba
title: CBaseControlVideo.GetSourcePosition-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ed52109284d9c9f8aa7884f4a0e361ec1a8f5564d0a22ae7fbf528d35a5e6ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661074"
---
# <a name="cbasecontrolvideogetsourceposition-method"></a>CBaseControlVideo.GetSourcePosition-Methode

Die `GetSourcePosition` -Methode ruft die Position und die Abmessungen des Quellrechtecks in einem atomaren Vorgang ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSourcePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pLeft* 
</dt> <dd>

Zeiger auf die linke Koordinate des Quellrechtecks.

</dd> <dt>

*pTop* 
</dt> <dd>

Zeiger auf die obere Koordinate des Quellrechtecks.

</dd> <dt>

*pWidth* 
</dt> <dd>

Zeiger auf die Breite des Quellrechtecks.

</dd> <dt>

*pHeight* 
</dt> <dd>

Zeiger auf die Höhe des Quellrechtecks.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück, der von der Implementierung abhängt. kann einer der folgenden Werte sein, oder andere Werte, die nicht aufgeführt sind.



| Rückgabecode                                                                                           | Beschreibung                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Fehler.<br/>                                                              |
| <dl> <dt>**E \_ POINTER**</dt> </dl>             | **NULL-Zeigerargument.**<br/>                                            |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der Vorgang kann nicht ausgeführt werden, da die Pins nicht verbunden sind.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Erfolg.<br/>                                                              |



 

## <a name="remarks"></a>Hinweise

Eine Anwendung kann die Quell- und Zielrechtecke für das Video über die [**IBasicVideo-Schnittstelle**](/windows/desktop/api/Control/nn-control-ibasicvideo) ändern. Das Quellrechteck wirkt sich darauf aus, welcher Abschnitt der nativen Videoquelle auf der Anzeige angezeigt wird. das Zielrechteck wirkt sich darauf aus, wo das Video angezeigt wird, wenn es wiedergegeben wird. Das Zielrechteck ist relativ zum Clientbereich des Fensters, in dem es wiedergegeben wird. Die obere linke Ecke des Fensters ist die Koordinate (0,0).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




