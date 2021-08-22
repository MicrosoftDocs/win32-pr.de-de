---
description: Die Get \_ Caption-Methode ruft die aktuelle Fensterbeschriftung ab.
ms.assetid: 51ce9cf8-0b2a-4459-b005-02dc45444fd8
title: CBaseControlWindow.get_Caption -Methode (Ctlutil.h)
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
ms.openlocfilehash: 0f05501adbd486eaa60e939aacfdd5896c0fbcae059673029f04fcca8aeb742a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640889"
---
# <a name="cbasecontrolwindowget_caption-method"></a>CBaseControlWindow.get \_ Caption-Methode

Die `get_Caption` -Methode ruft die aktuelle Fensterbeschriftung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Caption(
   BSTR *pstrCaption
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstrCaption* 
</dt> <dd>

Zeiger auf die aktuelle Fensterbeschriftung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Den meisten Fenstern der obersten Ebene auf einem Windows desktopbasierten Desktop ist ein Titel (Beschriftung) zugeordnet. Diese Eigenschaft kann über die [**IVideoWindow-Schnittstelle abgefragt und festgelegt**](/windows/desktop/api/Control/nn-control-ivideowindow) werden. Beschriftungssatz sind nur sichtbar, wenn auf das Fenster der WS \_ CAPTION-Stil angewendet wurde. Wenn nicht, kann die Beschriftung weiterhin festgelegt (und abgerufen) werden, obwohl sie für den Benutzer nicht sichtbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




