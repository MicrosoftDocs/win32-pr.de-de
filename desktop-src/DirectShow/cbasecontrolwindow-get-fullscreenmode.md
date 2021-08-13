---
description: Die \_ Get FullScreenMode-Methode ruft den aktuellen Vollbildmodus ab.
ms.assetid: 351af361-5cfd-4e82-bd8a-92f629bd270d
title: CBaseControlWindow.get_FullScreenMode-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cebd74fd51551249c339100ac2dd3eda4a171cc316cca575f27f5194480978ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660533"
---
# <a name="cbasecontrolwindowget_fullscreenmode-method"></a>CBaseControlWindow.get \_ FullScreenMode-Methode

Die `get_FullScreenMode` -Methode ruft den aktuellen Vollbildmodus ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_FullScreenMode(
   long *FullScreenMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FullScreenMode* 
</dt> <dd>

Zeiger auf den aktuellen Vollbildmodus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion gibt standardmäßig E \_ NOTIMPL zurück. Dadurch wird der [**IVideoWindow-Plug-In-Verteiler**](/windows/desktop/api/Control/nn-control-ivideowindow) darüber informiert, dass dieser Renderer keinen Vollbildrenderer implementiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




