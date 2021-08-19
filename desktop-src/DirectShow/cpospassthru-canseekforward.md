---
description: Die CanSeekForward-Methode bestimmt, ob der Stream vorwärts durchsuchen werden kann. Diese Methode implementiert die IMediaPosition::CanSeekForward-Methode.
ms.assetid: ccb2db8d-b52e-4e3d-b49b-9689197a974a
title: CPosPassThru.CanSeekForward-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekForward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f07491a94522280357c85d773d28ea4732f2f85879b55cf5d1b5a99ec72d23f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073564"
---
# <a name="cpospassthrucanseekforward-method"></a>CPosPassThru.CanSeekForward-Methode

Die `CanSeekForward` -Methode bestimmt, ob der Stream vorwärts durchsuchen werden kann. Diese Methode implementiert die [**IMediaPosition::CanSeekForward-Methode.**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward)

## <a name="syntax"></a>Syntax


```C++
HRESULT CanSeekForward(
   LONG *pCanSeekForward
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCanSeekForward* 
</dt> <dd>

Zeiger auf eine Variable, die den Wert OATRUE empfängt, wenn der Filter vorwärts suchen kann, andernfalls OAFALSE.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** vom verbundenen Pin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




