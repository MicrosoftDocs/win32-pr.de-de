---
description: Die SetSourcePosition-Methode legt eine neue Quellposition für das Video fest.
ms.assetid: e3c9ce31-9c24-4ef5-9526-ef6b890f5109
title: CBaseControlVideo.SetSourcePosition-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9f99ebab9551348dc2c1121b33d2f7e7dc04e7d3e8c014f8fc537f674914d20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017418"
---
# <a name="cbasecontrolvideosetsourceposition-method"></a>CBaseControlVideo.SetSourcePosition-Methode

Die `SetSourcePosition` -Methode legt eine neue Quellposition für das Video fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSourcePosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Left* 
</dt> <dd>

Neue linke Koordinate.

</dd> <dt>

*Top* 
</dt> <dd>

Neue obere Koordinate.

</dd> <dt>

*Width* 
</dt> <dd>

Neue Breite.

</dd> <dt>

*Height* 
</dt> <dd>

Neue Höhe.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




