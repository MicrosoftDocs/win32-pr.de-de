---
description: Die dbgoutstring-Funktion sendet eine Zeichenfolge an den debugausgabespeicherort. Wird in Einzelhandels Builds ignoriert.
ms.assetid: 644bf4f7-ec2d-466e-85c6-690dd44da702
title: Dbgoutstring-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgOutString
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc12d4b73080f00a3d32c80074a801146ea4a74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354150"
---
# <a name="dbgoutstring-function"></a>Dbgoutstring-Funktion

Die **dbgoutstring** -Funktion sendet eine Zeichenfolge an den debugausgabespeicherort. Wird in Einzelhandels Builds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void DbgOutString(
   LPCTSTR psz
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PSZ* 
</dt> <dd>

Zu Ausgabe Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

In Debugbuilds gibt diese Funktion immer die Zeichenfolge aus, unabhängig von den aktuellen Debug-Ausgabe Ebenen. Verwenden Sie zum genaueren Steuern der Ausgabe das [**dbglog**](dbglog.md) -Makro.

## <a name="examples"></a>Beispiele


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Debug-Ausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




