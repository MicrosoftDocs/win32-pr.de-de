---
description: Flag, das angibt, ob die PIN vor denen der empfangenden Pin ihre eigenen bevorzugten Medientypen ausprobiert.
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: 'Cbasepin:: m_bTryMyTypesFirst Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bTryMyTypesFirst
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f98021b6ba97d32974f26ac4e76ca31fa54e5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371275"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a>Cbasepin:: m \_ btrymytypesfirst-Member

Flag, das angibt, ob die PIN vor denen der empfangenden Pin ihre eigenen bevorzugten Medientypen ausprobiert.

## <a name="syntax"></a>Syntax


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a>Bemerkungen

Dieses Flag ist standardmäßig auf **false** eingestellt. Wenn das Flag " **true**" ist, kehrt die [**cbasepin:: agreemediatype**](cbasepin-agreemediatype.md) -Methode die Reihenfolge um, in der die Medientypen ausprobiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




