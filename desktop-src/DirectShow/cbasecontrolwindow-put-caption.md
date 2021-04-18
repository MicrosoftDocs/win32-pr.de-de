---
description: Die Put \_ Caption-Methode legt den Titel oder die Beschriftung des Fensters fest.
ms.assetid: 6671805a-e1ef-40f1-bc3f-bf7954ff9851
title: CBaseControlWindow.put_Caption-Methode (ctlutil. h)
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
ms.openlocfilehash: aca8e5e7ad04acae9fab1cfe2d44f982266805e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368435"
---
# <a name="cbasecontrolwindowput_caption-method"></a>Cbasecontrolwindow. Put- \_ Beschriftungs Methode

Die- `put_Caption` Methode legt den Titel oder die Beschriftung des Fensters fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Caption(
   BSTR strCaption
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Überschrift* 
</dt> <dd>

Neue Fenster Beschriftung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Den meisten Fenstern der obersten Ebene auf einem Windows-basierten Desktop ist ein Titel (Beschriftung) zugeordnet. Diese Eigenschaft kann durch die [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle abgefragt und festgelegt werden. Jeder Beschriftungs Satz ist nur sichtbar, wenn für das Fenster der WS- \_ Beschriftungs Stil angewendet wurde. Wenn dies nicht der Fall ist, kann die Beschriftung weiterhin festgelegt (und abgerufen) werden, auch wenn Sie für den Benutzer nicht sichtbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




