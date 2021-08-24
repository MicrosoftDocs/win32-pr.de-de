---
description: Die CompleteConnect-Methode benachrichtigt das Fenster, dass der Eingabepin des Renderers verbunden wurde.
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: CBaseWindow.CompleteConnect-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e04e0adf1d11a4878d860dd5c8a1eea9395095c71d8b5c86d6023a24ccdb28c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016708"
---
# <a name="cbasewindowcompleteconnect-method"></a>CBaseWindow.CompleteConnect-Methode

Die `CompleteConnect` -Methode benachrichtigt das Fenster, dass der Eingabepin des Renderers verbunden wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode setzt das Fensteraktivierungsflag ([**CBaseWindow::m \_ bActivated**](cbasewindow-m-bactivated.md)) auf **FALSE** zurück. Wenn ein Videorenderer eine Pinverbindung abschließt, kann er die [**CBaseWindow::ActivateWindow-Methode**](cbasewindow-activatewindow.md) aufrufen, um die Größe und Position des Fensters festzulegen. Um zu erzwingen, dass **ActivateWindow** diese Attribute neu berechnet, rufen Sie zuerst die `CompleteConnect` -Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




