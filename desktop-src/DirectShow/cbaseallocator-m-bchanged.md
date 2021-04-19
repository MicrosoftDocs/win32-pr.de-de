---
description: Flag zum angeben, ob sich die Puffer Anforderungen geändert haben.
ms.assetid: 34d946f9-125c-40fb-b09e-82457add07d6
title: 'Cbasezucator:: m_bChanged Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86c700f3c0ee820206613bcf3147652b1826b57a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365595"
---
# <a name="cbaseallocatorm_bchanged-member"></a>Cbasezucator:: m- \_ bchanged-Member

Flag zum angeben, ob sich die Puffer Anforderungen geändert haben. Die [**cbasezucator:: SetProperties**](cbaseallocator-setproperties.md) -Methode legt den Wert auf **true** fest. In einer abgeleiteten Klasse sollte die rein virtuelle Methode [**cbasezucator:: zuordc**](cbaseallocator-alloc.md) den Wert auf **false** zurücksetzen. Nachdem Puffer zugeordnet wurden, müssen Sie Sie nicht erneut zuordnen, während *m \_ bchanged* den Wert **false** hat.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bChanged;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasezucator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




