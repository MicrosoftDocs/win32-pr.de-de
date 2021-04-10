---
description: Die AddHead-Methode fügt ein Element am Anfang der Liste hinzu.
ms.assetid: 8f0012b7-bbc2-407c-ae5a-9843c2f692dc
title: Cgenericlist. AddHead-Methode (wxlist. h)-pobj-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62a32eb177c80d10a876a4b163c8a1609104fbea
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104050954"
---
# <a name="cgenericlistaddhead-method-wxlisth---pobj-parameter"></a>Cgenericlist. AddHead-Methode (wxlist. h)-pobj-Parameter

Mit der- `AddHead` Methode wird ein Element am Anfang der Liste hinzugefügt.

## <a name="syntax"></a>Syntax


```C++
POSITION AddHead(
   OBJECT *pObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pobj* 
</dt> <dd>

Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Positionswert zurück, der die neue Head-Position angibt. Wenn die Methode fehlschlägt, ist der Rückgabewert **null**.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Wxlist. h (Include Streams. h) |
| Bibliothek| "Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cgenericlist-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




