---
description: Die get \_ SourceLeft-Methode ruft die linke Koordinate des aktuellen Quellrechtecks ab.
ms.assetid: dbfb1850-6e49-481c-b26a-22ccb9e4455a
title: CBaseControlVideo.get_SourceLeft -Methode (Ctlutil.h)
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
ms.openlocfilehash: 195c968b93f57bed0a8bb611b642ab19e7024cb4d67e49bf84c643dc8e340432
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057100"
---
# <a name="cbasecontrolvideoget_sourceleft-method"></a>CBaseControlVideo.get \_ SourceLeft-Methode

Die `get_SourceLeft` -Methode ruft die linke Koordinate des aktuellen Quellrechtecks ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SourceLeft(
   long *pSourceLeft
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSourceLeft* 
</dt> <dd>

Zeiger auf die linke Koordinate des aktuellen Quellrechtecks.

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

 

 




