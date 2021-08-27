---
description: Die SetDefaultSourcePosition-Methode legt den Renderer wieder auf fest, indem die Standardquellenposition (in der Regel das gesamte native Video) verwendet wird.
ms.assetid: 1ac03298-4c25-45f7-9719-ea03fe4699b2
title: CBaseControlVideo.SetDefaultSourcePosition-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab067e9041a937c37e0df2bf9998dd1ecb7a6d1d434a4f10e1b2e1e1b50e6f75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087490"
---
# <a name="cbasecontrolvideosetdefaultsourceposition-method"></a>CBaseControlVideo.SetDefaultSourcePosition-Methode

Die `SetDefaultSourcePosition` -Methode legt den Renderer wieder auf fest, indem die Standardquellenposition (in der Regel das systemeigene Video) verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDefaultSourcePosition();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück, der von der Implementierung abhängt. kann einer der folgenden Werte oder ein anderer nicht aufgeführter Wert sein.



| Rückgabecode                                                                                           | Beschreibung                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Fehler.<br/>                                                              |
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

 

 




