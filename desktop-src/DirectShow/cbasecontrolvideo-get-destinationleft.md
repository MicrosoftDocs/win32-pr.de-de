---
description: Die get \_ DestinationLeft-Methode ruft die linke Koordinate des aktuellen Zielrechtecks ab.
ms.assetid: f1c6d784-7ec3-4d44-a3fb-c1e3b988e392
title: CBaseControlVideo.get_DestinationLeft -Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6ec35cc3fa831218fb7c5c4810643d58b9c9d303a9501d10969d847649c2efb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661516"
---
# <a name="cbasecontrolvideoget_destinationleft-method"></a>CBaseControlVideo.get \_ DestinationLeft-Methode

Die `get_DestinationLeft` -Methode ruft die linke Koordinate des aktuellen Zielrechtecks ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DestinationLeft(
   long *pDestinationLeft
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDestinationLeft* 
</dt> <dd>

Zeiger auf die linke Koordinate des Zielrechtecks.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück, der von der Implementierung abhängt. kann einer der folgenden Werte oder ein anderer nicht aufgeführter Wert sein.



| Rückgabecode                                                                                           | Beschreibung                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Fehler.<br/>                                                              |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>             |  NULL-Zeigerargument.<br/>                                            |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der Vorgang kann nicht ausgeführt werden, da die Stecknadeln nicht verbunden sind.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Erfolg.<br/>                                                              |



 

## <a name="remarks"></a>Hinweise

Diese Memberfunktion implementiert die [**IBasicVideo::get \_ DestinationLeft-Methode.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationleft)

Eine Anwendung kann die Quell- und Zielrechtecke für das Video über die [**IBasicVideo-Schnittstelle**](/windows/desktop/api/Control/nn-control-ibasicvideo) ändern. Das Quellrechteck wirkt sich darauf aus, welcher Abschnitt der nativen Videoquelle auf der Anzeige angezeigt wird. Das Zielrechteck wirkt sich darauf aus, wo das Video angezeigt wird, wenn es abgespielt wird. Das Zielrechteck ist relativ zum Clientbereich des Fensters, in dem es abspielt. Die obere linke Ecke des Fensters ist koordinate (0,0).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




