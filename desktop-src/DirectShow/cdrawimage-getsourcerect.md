---
description: Die GetSourceRect-Methode ruft das aktuelle Quellrechteck ab.
ms.assetid: e9ca091f-3fd7-4e42-90e9-b7831dd488a9
title: CDrawImage.GetSourceRect-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81d7de629ec89fe31296a9efd10df3d4895f53a7dc67db58bfde77be8a75a82f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697886"
---
# <a name="cdrawimagegetsourcerect-method"></a>CDrawImage.GetSourceRect-Methode

Die `GetSourceRect` -Methode ruft das aktuelle Quellrechteck ab.

## <a name="syntax"></a>Syntax


```C++
void GetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Zeiger auf eine **RECT-Struktur,** die das Quellrechteck empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDrawImage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




