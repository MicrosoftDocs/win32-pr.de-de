---
description: Die put \_ SourceHeight-Methode legt die Höhe des Quellrechtecks fest.
ms.assetid: 45e7d73b-d141-4dc1-8b06-38e9d6ad9851
title: CBaseControlVideo.put_SourceHeight -Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_SourceHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3511cfd5d12b782fb12765ff76b3013abd402c90488fa904577bf0d51e92ebc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056770"
---
# <a name="cbasecontrolvideoput_sourceheight-method"></a>CBaseControlVideo.put \_ SourceHeight-Methode

Die `put_SourceHeight` -Methode legt die Höhe des Quellrechtecks fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SourceHeight(
   long SourceHeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SourceHeight* 
</dt> <dd>

Quellhöhe.

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

 

 




