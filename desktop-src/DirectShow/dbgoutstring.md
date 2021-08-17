---
description: Die DbgOutString-Funktion sendet eine Zeichenfolge an den Debugausgabespeicherort. Wird in Einzelhandelsbuilds ignoriert.
ms.assetid: 644bf4f7-ec2d-466e-85c6-690dd44da702
title: DbgOutString-Funktion (Wxdebug.h)
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
ms.openlocfilehash: b6d8b74b5f0643f619a58beeea2dcd5526889d1a65de4815b06d2d6047777d90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821558"
---
# <a name="dbgoutstring-function"></a>DbgOutString-Funktion

Die **DbgOutString-Funktion** sendet eine Zeichenfolge an den Debugausgabespeicherort. Wird in Einzelhandelsbuilds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void DbgOutString(
   LPCTSTR psz
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Psz* 
</dt> <dd>

Die auszugebende Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

In Debugbuilds gibt diese Funktion immer die Zeichenfolge aus, unabhängig von den aktuellen Debugausgabeebenen. Verwenden Sie das [**DbgLog-Makro,**](dbglog.md) um eine feineren Kontrolle über die Ausgabe zu haben.

## <a name="examples"></a>Beispiele


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Debuggen von Ausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




