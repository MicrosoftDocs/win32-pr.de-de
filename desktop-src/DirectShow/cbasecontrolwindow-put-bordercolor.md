---
description: Die Put \_ BorderColor-Methode ändert die Rahmenfarbe.
ms.assetid: bb19d338-7fd1-448c-be94-1c71d4a9a330
title: CBaseControlWindow.put_BorderColor-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54db6de704f2ee0fde1a5087e83df4b362a57959
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353004"
---
# <a name="cbasecontrolwindowput_bordercolor-method"></a>Cbasecontrolwindow. Put \_ BorderColor-Methode

Die- `put_BorderColor` Methode ändert die Rahmenfarbe.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BorderColor(
   long Color
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Farbe* 
</dt> <dd>

Neue Rahmenfarbe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung kann ein Ziel Rechteck einrichten, in dem das Video angezeigt werden soll. Dieses Rechteck ist relativ zum Client Bereich des Fensters. Wenn dies geschieht (Standardmäßig wird das gesamte Fenster gezeichnet), gibt es einen Rahmen, der das Video umgibt. Diese Eigenschaft wirkt sich auf die vom Rahmen verwendete Farbe aus. Obwohl der-Parameter als **Long** -Typ angegeben ist, handelt es sich tatsächlich um einen **COLORREF** -Wert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




