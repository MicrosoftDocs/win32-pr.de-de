---
description: Die get \_ sourceLeft-Methode ruft die linke Koordinate des aktuellen Quell Rechtecks ab.
ms.assetid: dbfb1850-6e49-481c-b26a-22ccb9e4455a
title: CBaseControlVideo.get_SourceLeft-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2b7ff62617b9fa378511dba2838f0dcbdb25dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364937"
---
# <a name="cbasecontrolvideoget_sourceleft-method"></a>Cbasecontrolvideo. get \_ sourceLeft-Methode

Die- `get_SourceLeft` Methode ruft die linke Koordinate des aktuellen Quell Rechtecks ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SourceLeft(
   long *pSourceLeft
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psourceleft* 
</dt> <dd>

Ein Zeiger auf die linke Koordinate des aktuellen Quell Rechtecks.

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

Eine Anwendung kann die Quell-und Ziel Rechtecke für das Video über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle ändern. Das Quell Rechteck wirkt sich darauf aus, welcher Abschnitt der systemeigenen Videoquelle auf der Anzeige angezeigt wird. Das Ziel Rechteck wirkt sich darauf aus, wo das Video bei der Wiedergabe angezeigt wird. Das Ziel Rechteck ist relativ zum Client Bereich des Fensters, in dem es abgespielt wird. Die linke obere Ecke des Fensters ist Koordinaten (0,0).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




