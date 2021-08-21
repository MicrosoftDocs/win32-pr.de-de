---
description: Die HideCursor-Methode blendet den Cursor aus oder zeigt den Cursor an.
ms.assetid: 80175d1b-9874-4295-9ebc-b0d78961a263
title: CBaseControlWindow.HideCursor-Methode (Ctlutil.h)
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
ms.openlocfilehash: 6421a650471d0954031433db3814e8453cbc82586c7f37608ae947e7301c6969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158381"
---
# <a name="cbasecontrolwindowhidecursor-method"></a>CBaseControlWindow.HideCursor-Methode

Die `HideCursor` -Methode blendet den Cursor aus oder zeigt den Cursor an.

## <a name="syntax"></a>Syntax


```C++
HRESULT HideCursor(
   long HideCursor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HideCursor* 
</dt> <dd>

Wert, der an gibt, ob der Cursor angezeigt werden soll. Legen Sie auf OATRUE fest, um den Cursor auszublenden, oder OAFALSE, um den Cursor anzuzeigen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




