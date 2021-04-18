---
description: Die get \_ Fullscreenmode-Methode ruft den aktuellen Vollbildmodus ab.
ms.assetid: 351af361-5cfd-4e82-bd8a-92f629bd270d
title: CBaseControlWindow.get_FullScreenMode-Methode (ctlutil. h)
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
ms.openlocfilehash: fc77b43db2bb420e6cfe2eace44e96e1ab43b0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354666"
---
# <a name="cbasecontrolwindowget_fullscreenmode-method"></a>Cbasecontrolwindow. get \_ Fullscreenmode-Methode

Die- `get_FullScreenMode` Methode ruft den aktuellen Vollbildmodus ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_FullScreenMode(
   long *FullScreenMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fullscreenmode* 
</dt> <dd>

Zeiger auf den aktuellen Vollbildmodus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion gibt \_ standardmäßig E notimpl zurück. Dadurch wird dem [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Plug-in-Verteiler mitgeteilt, dass dieser Renderer keinen Vollbild-Renderer implementiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




