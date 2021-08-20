---
description: Die GetTargetRect-Methode ruft das aktuelle Zielrechteck ab.
ms.assetid: b6542b06-af36-4666-b6fa-d9fa3c6c7044
title: CDrawImage.GetTargetRect-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ba520b0bb48ed60ba2a9c48165eb83959107ecd777bdecc8bce12e7672d221e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076410"
---
# <a name="cdrawimagegettargetrect-method"></a>CDrawImage.GetTargetRect-Methode

Die `GetTargetRect` -Methode ruft das aktuelle Zielrechteck ab.

## <a name="syntax"></a>Syntax


```C++
void GetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Zeiger auf eine **RECT-Struktur,** die das Zielrechteck empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDrawImage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




