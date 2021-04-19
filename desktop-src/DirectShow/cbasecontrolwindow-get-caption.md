---
description: Die \_ Methode Get Caption Ruft die aktuelle Fenster Beschriftung ab.
ms.assetid: 51ce9cf8-0b2a-4459-b005-02dc45444fd8
title: CBaseControlWindow.get_Caption-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8d743c746f833007d91afd4346f7f48c6218dde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359308"
---
# <a name="cbasecontrolwindowget_caption-method"></a>Cbasecontrolwindow. get \_ Caption-Methode

Die- `get_Caption` Methode ruft die aktuelle Fenster Beschriftung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Caption(
   BSTR *pstrCaption
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstrincaption* 
</dt> <dd>

Zeiger auf die aktuelle Fenster Beschriftung.

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

 

 




