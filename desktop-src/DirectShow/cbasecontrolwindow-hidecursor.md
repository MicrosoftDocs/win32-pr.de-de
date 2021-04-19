---
description: Die hidecursor-Methode blendet den Cursor aus oder zeigt ihn an.
ms.assetid: 80175d1b-9874-4295-9ebc-b0d78961a263
title: Cbasecontrolwindow. hidecursor-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.HideCursor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0f379c719052de77b54dba47f83b34ae235415f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367082"
---
# <a name="cbasecontrolwindowhidecursor-method"></a>Cbasecontrolwindow. hidecursor-Methode

Mit der- `HideCursor` Methode wird der Cursor ausgeblendet oder angezeigt.

## <a name="syntax"></a>Syntax


```C++
HRESULT HideCursor(
   long HideCursor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hidecursor* 
</dt> <dd>

Wert, der angibt, ob der Cursor angezeigt werden soll. Legen Sie fest, um den Cursor auszublenden, oder oafalse, um den Cursor anzuzeigen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




