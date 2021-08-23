---
description: Die \_ put SourceTop-Methode legt die oberste Koordinate des Quellrechtecks fest.
ms.assetid: 8891771d-5a0b-4dfa-b961-9f375f13b4f7
title: CBaseControlVideo.put_SourceTop-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_SourceTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de7c0da0d38da2563e0a34b5f7f894a23e7b55390fc9291321dbca46a7cb61fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793850"
---
# <a name="cbasecontrolvideoput_sourcetop-method"></a>CBaseControlVideo.put-Methode \_ "SourceTop"

Die `put_SourceTop` -Methode legt die oberste Koordinate des Quellrechtecks fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SourceTop(
   long SourceTop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SourceTop* 
</dt> <dd>

Neue obere Koordinate des Quellrechtecks.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück, der von der Implementierung abhängt. kann einer der folgenden Werte sein, oder andere Werte, die nicht aufgeführt sind.



| Rückgabecode                                                                                           | Beschreibung                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Fehler.<br/>                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Ungültiges Argument.<br/>                                                     |
| <dl> <dt>**E \_ POINTER**</dt> </dl>             | **NULL-Zeigerargument.**<br/>                                            |
| <dl> <dt>**NOERROR**</dt> </dl>                | Erfolg.<br/>                                                              |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der Vorgang kann nicht ausgeführt werden, da die Pins nicht verbunden sind.<br/> |



 

## <a name="remarks"></a>Hinweise

Eine Anwendung kann die Quell- und Zielrechtecke für das Video über die [**IBasicVideo-Schnittstelle**](/windows/desktop/api/Control/nn-control-ibasicvideo) ändern. Das Quellrechteck wirkt sich darauf aus, welcher Abschnitt der nativen Videoquelle auf der Anzeige angezeigt wird. das Zielrechteck wirkt sich darauf aus, wo das Video angezeigt wird, wenn es wiedergegeben wird. Das Zielrechteck ist relativ zum Clientbereich des Fensters, in dem es wiedergegeben wird. Die obere linke Ecke des Fensters ist die Koordinate (0,0).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




