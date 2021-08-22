---
description: Die \_ Methode "WindowState abrufen" ruft den aktuellen Fensterzustand ab.
ms.assetid: 118b6710-b041-4a7d-8cdb-b96ae3dcbb09
title: CBaseControlWindow.get_WindowState-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5603e846fcf3357f01f896e6a0d34e34da6c355e5d41ab5d8f7b0c344c1a16dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586421"
---
# <a name="cbasecontrolwindowget_windowstate-method"></a>CBaseControlWindow.get \_ WindowState-Methode

Die `get_WindowState` -Methode ruft den aktuellen Fensterzustand ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_WindowState(
   long *pWindowState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pWindowState* 
</dt> <dd>

Zeiger auf den Fensterzustand.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion gibt eine Teilmenge der Parameter der Microsoft Win32 **ShowWindow-Funktion** zurück. Insbesondere werden SW \_ SHOW und SW \_ HIDE zurückgegeben, abhängig von der aktuellen Sichtbarkeit des Fensters. Außerdem werden SW \_ MINIMIZE und SW MAXIMIZE \_ zurückgegeben, je nachdem, ob das Fenster ein Symbol ist oder erweitert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




