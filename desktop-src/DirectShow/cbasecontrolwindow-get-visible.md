---
description: Die get \_ Visible-Methode ruft die aktuelle Fenster Sichtbarkeit ab.
ms.assetid: 7e643569-1116-4562-be33-babd12a7e899
title: CBaseControlWindow.get_Visible-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bc38a0b35f46de223ed84174c3b10f5300cc94d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365775"
---
# <a name="cbasecontrolwindowget_visible-method"></a>Cbasecontrolwindow. get \_ Visible-Methode

Die- `get_Visible` Methode ruft die aktuelle Fenster Sichtbarkeit ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Visible(
   long *pVisible
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvisible* 
</dt> <dd>

Zeiger auf ein boolesches Automatisierungs Flag (0 ist off, 1 ist on).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion gibt 1 zurück, wenn das Fenster den \_ sichtbaren WS-Stil aufweist; andernfalls 0.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




