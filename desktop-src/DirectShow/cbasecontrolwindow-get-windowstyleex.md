---
description: Die \_ Methode "WindowStyleEx abrufen" ruft die erweiterten Fensterstile ab.
ms.assetid: 72955958-bbda-4b8f-9c28-6d3f5eb56a82
title: CBaseControlWindow.get_WindowStyleEx-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 082b541c9f04122616f4f96548f1b1e58d940a6060fb4af1ac0fe51fa4887bb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331210"
---
# <a name="cbasecontrolwindowget_windowstyleex-method"></a>CBaseControlWindow.get \_ WindowStyleEx-Methode

Die `get_WindowStyleEx` -Methode ruft die erweiterten Fensterstile ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_WindowStyleEx(
   long *pWindowStyleEx
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pWindowStyleEx* 
</dt> <dd>

Zeiger auf erweiterte Fensterstile.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion ruft die erweiterten Fensterstile ab. Sie ruft die [**Memberfunktion CBaseControlWindow::D oGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




