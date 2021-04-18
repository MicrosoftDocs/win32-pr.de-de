---
description: Die Put \_ messagedrain-Methode legt das Fenster fest, um Fenster Meldungen zu empfangen, die an den Videorenderer gesendet werden.
ms.assetid: b2d2d489-a66f-474a-b8bf-b019179f6f69
title: CBaseControlWindow.put_MessageDrain-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f03f944a6af6ac99de6000a2507178eea510c06a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354751"
---
# <a name="cbasecontrolwindowput_messagedrain-method"></a>Cbasecontrolwindow. Put \_ messagedrain-Methode

Die- `put_MessageDrain` Methode legt das Fenster fest, um Fenster Meldungen zu empfangen, die an den Videorenderer gesendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_MessageDrain(
   OAHWND Drain
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Entladen* 
</dt> <dd>

Fenster, an das Nachrichten gesendet werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Nachrichten, die an den Videorenderer-Filter gesendet werden, können in einem anderen Fenster gepostet werden. Diese Member-Funktion registriert das Fenster, um diese Nachrichten zu empfangen. Anders als bei der [**cbasecontrolwindow::p UT- \_ Besitzer**](cbasecontrolwindow-put-owner.md) Element Funktion macht diese Member-Funktion das Videofenster nicht als untergeordnetes Element eines anderen Fensters. Er ist besonders nützlich für Vollbild-Videorenderer, die keine untergeordneten Fenster sein können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




