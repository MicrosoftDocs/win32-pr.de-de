---
description: Die GetVideoSize-Methode ruft die Breite und Höhe des nativen Videos ab.
ms.assetid: b3461a56-705b-465a-9cfc-e86fd52a07c5
title: CBaseControlVideo.GetVideoSize-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b49f58901ac362b5a03d069485ec4dbf74e22d4549dc628f26baa5c2bfa85234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056940"
---
# <a name="cbasecontrolvideogetvideosize-method"></a>CBaseControlVideo.GetVideoSize-Methode

Die `GetVideoSize` -Methode ruft die Breite und Höhe des nativen Videos ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVideoSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pWidth* 
</dt> <dd>

Zeiger auf die Videobreite.

</dd> <dt>

*pHeight* 
</dt> <dd>

Zeiger auf die Videohöhe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




