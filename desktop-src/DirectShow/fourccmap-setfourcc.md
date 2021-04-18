---
description: Legt den FourCC-Teil des fourccmap-Objekts fest.
ms.assetid: cc821e39-e565-4255-a289-2c9507d43433
title: 'Fourccmap:: setfourcc-Methode (FourCC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.SetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 435eb209e39ffad29f041e2e117a45d735abffed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358634"
---
# <a name="fourccmapsetfourcc-method"></a>Fourccmap:: setfourcc-Methode

Legt den **FourCC** -Teil des [**fourccmap**](fourccmap.md) -Objekts fest.

## <a name="syntax"></a>Syntax


```C++
void SetFOURCC(
   const GUID *pguid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pguid* 
</dt> <dd>

Zeiger auf den zurückgegebenen Globally Unique Identifier (**GUID**)-Teil des **fourccmap** -Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>FourCC. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Fourccmap-Klasse**](fourccmap.md)
</dt> </dl>

 

 




