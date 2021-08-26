---
description: Die \_ put DestinationWidth-Methode legt die Breite des Zielrechtecks fest.
ms.assetid: 1e7a4d38-1453-4dfd-8a2f-0f76b352fc64
title: CBaseControlVideo.put_DestinationWidth-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_DestinationWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1762a7b86d38ffb4f8feeced3ce002f33fc434d07ed9716d3334aa25db69fe94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056820"
---
# <a name="cbasecontrolvideoput_destinationwidth-method"></a>CBaseControlVideo.put \_ DestinationWidth-Methode

Die `put_DestinationWidth` -Methode legt die Breite des Zielrechtecks fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_DestinationWidth(
   long DestinationWidth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DestinationWidth* 
</dt> <dd>

Neue Zielbreite.

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

 

 




