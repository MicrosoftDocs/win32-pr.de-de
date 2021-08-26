---
description: Die \_ Put Caption-Methode legt den Fenstertitel oder die Beschriftung fest.
ms.assetid: 6671805a-e1ef-40f1-bc3f-bf7954ff9851
title: CBaseControlWindow.put_Caption-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c7f0c9da5ad2c3ae409e14a1ca9918a0c1aa7ef04615ab4d647ce1a3467c7311
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983700"
---
# <a name="cbasecontrolwindowput_caption-method"></a>CBaseControlWindow.put \_ Caption-Methode

Die `put_Caption` -Methode legt den Fenstertitel oder die Beschriftung fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Caption(
   BSTR strCaption
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strCaption* 
</dt> <dd>

Neue Fensterbeschriftung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Den meisten Fenstern der obersten Ebene auf einem Windows-basierten Desktop ist ein Titel (Beschriftung) zugeordnet. Diese Eigenschaft kann über die [**IVideoWindow-Schnittstelle**](/windows/desktop/api/Control/nn-control-ivideowindow) abgefragt und festgelegt werden. Beschriftungssätze sind nur sichtbar, wenn auf das Fenster das WS \_ CAPTION-Format angewendet wurde. Andernfalls kann die Beschriftung weiterhin festgelegt (und abgerufen) werden, obwohl sie für den Benutzer nicht sichtbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




