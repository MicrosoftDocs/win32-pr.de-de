---
description: Die get \_ messagedrain-Methode ruft die aktuelle Nachrichten Ableitung ab.
ms.assetid: d679e7f7-4628-479b-b722-843cdd91ffe6
title: CBaseControlWindow.get_MessageDrain-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aaf51c3f4297f238e51bbe8677303730c04b89d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369601"
---
# <a name="cbasecontrolwindowget_messagedrain-method"></a>Cbasecontrolwindow. get \_ messagedrain-Methode

Die- `get_MessageDrain` Methode ruft den aktuellen Nachrichten Ausgleich ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MessageDrain(
   OAHWND *Drain
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Entladen* 
</dt> <dd>

Zeiger auf das aktuelle Fenster, das Fenster Meldungen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Nachrichten, die an den Videorenderer-Filter gesendet werden, können in einem anderen Fenster gepostet werden. Das Fenster, das für den Empfang dieser Meldungen registriert ist (mithilfe der **cbasecontrolwindow:: get \_ messagedrain** -Member-Funktion), ist der aktuelle Nachrichten Ausgleich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




