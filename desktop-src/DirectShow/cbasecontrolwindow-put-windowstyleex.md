---
description: Die put \_ WindowStyleEx-Methode legt die erweiterten Fensterstile fest.
ms.assetid: 3c5928fe-7cd3-4e1c-9a3f-fa6d7a73dbc3
title: CBaseControlWindow.put_WindowStyleEx -Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48bdfba6b388d4595af3ba886ed97567c12f080953e238c03d8a5fb36f7a6ce4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635540"
---
# <a name="cbasecontrolwindowput_windowstyleex-method"></a>CBaseControlWindow.put \_ WindowStyleEx-Methode

Die `put_WindowStyleEx` -Methode legt die erweiterten Fensterstile fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_WindowStyleEx(
  [in] long WindowStyleEx
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*WindowStyleEx* \[ In\]
</dt> <dd>

Ein Wert, der den Stil des Steuerelementfensters angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NOERROR zurück.

## <a name="remarks"></a>Hinweise

Diese Methode verwendet erweiterte Fensterstile. Eine vollständige Liste der erweiterten Fensterstile finden Sie in der Microsoft Win32 **CreateWindowEx-Funktion.** Rufen Sie zum Ändern des Fensterstils den aktuellen Fensterstil ab, und fügen Sie dann die erforderlichen Bitfelder hinzu, oder entfernen Sie sie.

Verwenden Sie nicht die folgenden Fensterstile, da sie nicht überprüft werden.

-   WS \_ DISABLED
-   WS \_ HSCROLL
-   \_WS-SYMBOL
-   \_WS-MAXIMIERUNG
-   \_WS-MINIMIERUNG
-   WS \_ VSCROLL

Mit einigen Ausnahmen (wie hier erwähnt) sind die zulässigen Flags die gleichen, die von der Win32 **CreateWindow-Funktion zugelassen** werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




