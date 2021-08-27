---
description: Pinname.
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: CBasePin::m_pName-Member (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pName
api_type:
- HeaderDef
api_location:
- Amfilter.h
ms.openlocfilehash: d118ed76650b9ea580c0143ff4334a480d110c4a9d9531a23dda60c05c614630
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052680"
---
# <a name="cbasepinm_pname-member"></a>CBasePin::m \_ pName-Member

Pinname.

## <a name="syntax"></a>Syntax


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a>Hinweise

Die [**CBasePin::QueryPinInfo-Methode**](cbasepin-querypininfo.md) gibt diese Zeichenfolge als Pinnamen zurück, und die [**CBasePin::QueryId-Methode**](cbasepin-queryid.md) gibt sie als Pinbezeichner zurück. Im Allgemeinen müssen der Pinname und der Pinbezeichner jedoch nicht identisch sein. Der Pinbezeichner wird für die Graphpersistenz verwendet. Weitere Informationen finden Sie unter [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




