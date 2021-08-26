---
description: Die CanSeekBackward-Methode bestimmt, ob der Stream rückwärts durchsuchen werden kann. Diese Methode implementiert die IMediaPosition::CanSeekBackward-Methode.
ms.assetid: 6443980f-6863-4941-b2dd-4a31257b5810
title: CPosPassThru.CanSeekBackward-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekBackward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1d989acf074eb20e6ea3387c37129700320ce782e3c5d7c8bd4320641839ca1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108430"
---
# <a name="cpospassthrucanseekbackward-method"></a>CPosPassThru.CanSeekBackward-Methode

Die `CanSeekBackward` -Methode bestimmt, ob der Stream rückwärts durchsuchen werden kann. Diese Methode implementiert die [**IMediaPosition::CanSeekBackward-Methode.**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward)

## <a name="syntax"></a>Syntax


```C++
HRESULT CanSeekBackward(
   LONG *pCanSeekBackward
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCanSeekBackward* 
</dt> <dd>

Zeiger auf eine Variable, die den Wert OATRUE empfängt, wenn der Filter rückwärts suchen kann, andernfalls OAFALSE.

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

 

 




