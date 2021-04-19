---
description: Die completeconnect-Methode benachrichtigt das Fenster, dass die Eingabe-PIN des Renderers verbunden wurde.
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: Cbasewindow. completeconnect-Methode (winutil. h)
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
ms.openlocfilehash: 15d5719ab78c3e95cd0128d4075797221af1f4c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356352"
---
# <a name="cbasewindowcompleteconnect-method"></a>Cbasewindow. completeconnect-Methode

Die `CompleteConnect` -Methode benachrichtigt das Fenster, dass die Eingabe-PIN des Renderers verbunden wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode setzt das Fenster Aktivierungs Flag ([**cbasewindow:: m \_ bactivated**](cbasewindow-m-bactivated.md)) auf **false** zurück. Wenn ein Videorenderer eine PIN-Verbindung abschließt, kann er die [**cbasewindow:: activatewindow**](cbasewindow-activatewindow.md) -Methode aufrufen, um die Größe und Position des Fensters festzulegen. Um die Neuberechnung dieser Attribute durch **activatewindow** zu erzwingen, müssen Sie zuerst die- `CompleteConnect` Methode aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




