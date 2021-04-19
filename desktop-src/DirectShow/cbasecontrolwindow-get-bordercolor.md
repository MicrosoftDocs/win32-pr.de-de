---
description: Die get \_ BorderColor-Methode ruft die aktuelle Rahmenfarbe ab.
ms.assetid: 4b4cae1d-bef7-4f8d-8011-c220fcfb73eb
title: CBaseControlWindow.get_BorderColor-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d889f211b204c2c0180ae757a0240c8588552e83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359254"
---
# <a name="cbasecontrolwindowget_bordercolor-method"></a>Cbasecontrolwindow. get \_ BorderColor-Methode

Die- `get_BorderColor` Methode ruft die aktuelle Rahmenfarbe ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_BorderColor(
   long *Color
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Farbe* 
</dt> <dd>

Zeiger auf die aktuelle Rahmenfarbe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung kann ein Ziel Rechteck festlegen, in dem das Video angezeigt werden soll. Dieses Rechteck ist relativ zum Client Bereich des Fensters. Wenn dies geschieht (Standardmäßig wird das gesamte Fenster gezeichnet), gibt es einen Rahmen, der das Video umgibt. Diese Eigenschaft wirkt sich auf die vom Rahmen verwendete Farbe aus. Obwohl der-Parameter als **Long** -Typ angegeben ist, handelt es sich tatsächlich um einen **COLORREF** -Wert.

Diese Member-Funktion soll von externen Objekten über die [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle aufgerufen werden und sperrt daher den kritischen Abschnitt, um mit dem zugeordneten Filter synchronisiert zu werden. Rufen Sie die Member-Funktion [**cbasecontrolwindow:: getBorderColor**](cbasecontrolwindow-getbordercolour.md) auf, um diese Eigenschaft abzurufen, wenn Sie nicht von einem externen Objekt aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




