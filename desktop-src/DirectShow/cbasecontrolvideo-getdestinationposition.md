---
description: Die getdestinationposition-Methode ruft das Ziel Rechteck in einem atomaren Vorgang ab.
ms.assetid: 780cbcb5-1db5-4087-8c51-350183cfca31
title: Cbasecontrolvideo. getdestinationposition-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86ed919af270df508eb8f76e32597b410dec56b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371570"
---
# <a name="cbasecontrolvideogetdestinationposition-method"></a>Cbasecontrolvideo. getdestinationposition-Methode

Die- `GetDestinationPosition` Methode ruft das Ziel Rechteck in einem atomaren Vorgang ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDestinationPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pleft* 
</dt> <dd>

Ein Zeiger auf die linke Koordinate des Ziel Rechtecks.

</dd> <dt>

*ptop* 
</dt> <dd>

Ein Zeiger auf die obere Koordinate des Ziel Rechtecks.

</dd> <dt>

*pWidth* 
</dt> <dd>

Ein Zeiger auf die Breite des Ziel Rechtecks.

</dd> <dt>

*pHeight* 
</dt> <dd>

Ein Zeiger auf die Höhe des Ziel Rechtecks.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.



| Rückgabecode                                                                                           | Beschreibung                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>                | Fehler.<br/>                                                              |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>             | **Null** -Zeigerargument.<br/>                                            |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Der Vorgang kann nicht ausgeführt werden, da die Pins nicht verbunden sind.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Erfolg.<br/>                                                              |



 

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion kann anstelle von separaten Aufrufen der [**cbasecontrolvideo:: get \_ destinationleft**](cbasecontrolvideo-get-destinationleft.md)-, [**cbasecontrolvideo:: get \_ destinationtop**](cbasecontrolvideo-get-destinationtop.md)-, [**cbasecontrolvideo:: get \_ destinationwidth**](cbasecontrolvideo-get-destinationwidth.md)-und [**cbasecontrolvideo:: get \_ destinationheight**](cbasecontrolvideo-get-destinationheight.md) -Member-Funktionen verwendet werden. Eine Anwendung kann die Quell-und Ziel Rechtecke für das Video über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle ändern. Das Quell Rechteck wirkt sich darauf aus, welcher Abschnitt der systemeigenen Videoquelle auf der Anzeige angezeigt wird. Das Ziel Rechteck wirkt sich darauf aus, wo das Video bei der Wiedergabe angezeigt wird. Das Ziel Rechteck ist relativ zum Client Bereich des Fensters, in dem es abgespielt wird. Die linke obere Ecke des Fensters ist Koordinaten (0,0).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




