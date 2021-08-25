---
description: Dieses Makro erstellt einen Wert, der von Issue verwendet wird, um ein Abfrageende auszugeben.
ms.assetid: 9ced932a-5d98-4bf8-aa11-06560f53546d
title: D3DISSUE_END (D3d9types.h)
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
ms.openlocfilehash: 0c2e7a197612b56eb5ae966da3cd4cc224edd2bd07e3fded3d0b72907f717d5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987250"
---
# <a name="d3dissue_end"></a>D3DISSUE \_ END

Dieses Makro erstellt einen Wert, der von [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) verwendet wird, um ein Abfrageende auszugeben.

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a>Parameter





 

## <a name="remarks"></a>Hinweise

Dieses Makro ändert den Abfragezustand in nicht signalisiert.

D3DISSUE \_ END ist für die folgenden Abfragetypen gültig.

-   D3DQUERYTYPE \_ VCACHE
-   D3DQUERYTYPE \_ ResourceManager
-   D3DQUERYTYPE \_ VERTEXSTATS
-   D3DQUERYTYPE-EREIGNIS \_
-   D3DQUERYTYPE \_ OCCLUSION

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DISSUE \_ BEGIN**](d3dissue-begin.md)
</dt> <dt>

[**D3DQUERYTYPE**](./d3dquerytype.md)
</dt> </dl>

 

 
