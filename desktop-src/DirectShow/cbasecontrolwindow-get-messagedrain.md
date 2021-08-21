---
description: Die get \_ MessageDrain-Methode ruft den aktuellen Nachrichtenabfluss ab.
ms.assetid: d679e7f7-4628-479b-b722-843cdd91ffe6
title: CBaseControlWindow.get_MessageDrain -Methode (Ctlutil.h)
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
ms.openlocfilehash: 9a1e63e96950093bb7cc5760032d0b1f622c5df93a6f31673c595f54e5ea8e70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017398"
---
# <a name="cbasecontrolwindowget_messagedrain-method"></a>CBaseControlWindow.get \_ MessageDrain-Methode

Die `get_MessageDrain` -Methode ruft den aktuellen Nachrichtenabfluss ab.

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

Zeiger auf das aktuelle Fenster, das Fenstermeldungen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Nachrichten, die an den Videorendererfilter gesendet werden, können in einem anderen Fenster veröffentlicht werden. Das fenster, das für den Empfang dieser Nachrichten registriert ist (mithilfe der **CBaseControlWindow::get \_ MessageDrain-Memberfunktion),** ist der aktuelle Nachrichtenabfluss.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




