---
description: Die Put \_ Visible-Methode zeigt das Fenster an oder blendet es aus.
ms.assetid: 77e8d071-f876-4e35-945c-d1daf96ad02b
title: CBaseControlWindow.put_Visible -Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2c8565d14c58d520a91c682e55d3dbc2ba079cf956213bdc61d044834d690c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793290"
---
# <a name="cbasecontrolwindowput_visible-method"></a>CBaseControlWindow.put \_ Visible-Methode

Die `put_Visible` -Methode zeigt das Fenster an oder blendet es aus.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Visible(
   long Visible
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Visible* 
</dt> <dd>

Boolean-Flag für Automation (0 bedeutet, dass das Fenster ausgeblendet ist, 1 bedeutet, dass das Fenster angezeigt wird).

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

 

 




