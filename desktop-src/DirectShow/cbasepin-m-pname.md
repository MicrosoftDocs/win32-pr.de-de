---
description: Der Name der PIN.
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: 'Cbasepin:: m_pName Member (amfilter. h)'
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
ms.openlocfilehash: f2580b9aba379362c39e3d792504434fa18fe076
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362061"
---
# <a name="cbasepinm_pname-member"></a>Cbasepin:: m \_ PName-Member

Der Name der PIN.

## <a name="syntax"></a>Syntax


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a>Bemerkungen

Die [**cbasepin:: querypininfo**](cbasepin-querypininfo.md) -Methode gibt diese Zeichenfolge als Pin-Namen zurück, und die [**cbasepin:: QueryId**](cbasepin-queryid.md) -Methode gibt Sie als PIN-Bezeichner zurück. Im Allgemeinen ist es jedoch nicht erforderlich, dass der PIN-Name und der PIN-Bezeichner identisch sind. Der PIN-Bezeichner wird für die Diagramm Persistenz verwendet. Weitere Informationen finden Sie unter [**ibasefilter:: findpin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




