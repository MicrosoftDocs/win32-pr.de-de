---
description: Die methode \_ put SourceWidth legt die Breite des Quellrechtecks fest.
ms.assetid: 0becea4f-e47e-4f64-ab95-0ee333ad48f3
title: CBaseControlVideo.put_SourceWidth -Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_SourceWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cbc984e0baad4b2a4a287c6265df35c8d4ddccdd903e0ff79b80cc95f6cf8453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158652"
---
# <a name="cbasecontrolvideoput_sourcewidth-method"></a>CBaseControlVideo.put \_ SourceWidth-Methode

Die `put_SourceWidth` -Methode legt die Breite des Quellrechtecks fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SourceWidth(
   long SourceWidth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SourceWidth* 
</dt> <dd>

Neue Breite des Quellrechtecks.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück, der von der Implementierung abhängt. kann einer der folgenden Werte oder ein anderer nicht aufgeführter Wert sein.



| Rückgabecode                                                                                           | Beschreibung                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Fehler.<br/>                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Ungültiges Argument.<br/>                                                     |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>             |  NULL-Zeigerargument.<br/>                                            |
| <dl> <dt>**NOERROR**</dt> </dl>                | Erfolg.<br/>                                                              |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der Vorgang kann nicht ausgeführt werden, da die Stecknadeln nicht verbunden sind.<br/> |



 

## <a name="remarks"></a>Hinweise

Eine Anwendung kann die Quell- und Zielrechtecke für das Video über die [**IBasicVideo-Schnittstelle**](/windows/desktop/api/Control/nn-control-ibasicvideo) ändern. Das Quellrechteck wirkt sich darauf aus, welcher Abschnitt der nativen Videoquelle auf der Anzeige angezeigt wird. Das Zielrechteck wirkt sich darauf aus, wo das Video angezeigt wird, wenn es abgespielt wird. Das Zielrechteck ist relativ zum Clientbereich des Fensters, in dem es abspielt. Die obere linke Ecke des Fensters ist koordinate (0,0).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




