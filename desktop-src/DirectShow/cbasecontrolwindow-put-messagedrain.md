---
description: Die \_ put MessageDrain-Methode legt das Fenster fest, um Fenstermeldungen zu empfangen, die an den Videorenderer gesendet werden.
ms.assetid: b2d2d489-a66f-474a-b8bf-b019179f6f69
title: CBaseControlWindow.put_MessageDrain-Methode (Ctlutil.h)
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
ms.openlocfilehash: b58ac59d83023530ca6da51efc2f84ba42c4bef9ac0d3f25ad9a234a320291f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017258"
---
# <a name="cbasecontrolwindowput_messagedrain-method"></a>CBaseControlWindow.put \_ MessageDrain-Methode

Die `put_MessageDrain` -Methode legt das Fenster fest, um Fenstermeldungen zu empfangen, die an den Videorenderer gesendet werden.

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

Fenster zum Posten von Nachrichten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Nachrichten, die an den Filter des Videorenderers gesendet werden, können an ein anderes Fenster gesendet werden. Diese Memberfunktion registriert das Fenster, um diese Nachrichten zu empfangen. Im Gegensatz zur [**Memberfunktion CBaseControlWindow::p ut \_ Owner**](cbasecontrolwindow-put-owner.md) macht diese Memberfunktion das Videofenster nicht zu einem untergeordneten Element eines anderen Fensters. Dies ist besonders nützlich für Vollbildvideorenderer, bei denen es sich nicht um untergeordnete Fenster handelt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




