---
description: Dieses Makro erstellt einen Wert, der von Issue verwendet wird, um ein Abfrage Ende auszugeben.
ms.assetid: 9ced932a-5d98-4bf8-aa11-06560f53546d
title: D3DISSUE_END (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DISSUE_END
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 7a448346bdc5dcfbbca4cf0d55273bdadc2fdcbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355086"
---
# <a name="d3dissue_end"></a>D3DISSUE \_ Ende

Dieses Makro erstellt einen Wert, der von [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) verwendet wird, um ein Abfrage Ende auszugeben.

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a>Parameter





 

## <a name="remarks"></a>Bemerkungen

Dieses Makro ändert den Abfrage Status in "nicht signalisiert".

D3DISSUE \_ End ist für die folgenden Abfrage Typen gültig.

-   D3DQUERYTYPE \_ VCACHE
-   D3DQUERYTYPE \_ ResourceManager
-   D3DQUERYTYPE \_ vertexstats
-   D3DQUERYTYPE- \_ Ereignis
-   D3DQUERYTYPE- \_ oksion

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DISSUE \_ Begin**](d3dissue-begin.md)
</dt> <dt>

[**D3DQUERYTYPE**](./d3dquerytype.md)
</dt> </dl>

 

 
