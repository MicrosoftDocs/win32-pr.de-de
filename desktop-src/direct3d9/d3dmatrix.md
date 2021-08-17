---
description: Beschreibt eine Matrix.
ms.assetid: d6b98a32-e745-4724-b8ce-a81a3f5416f3
title: D3DMATRIX (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATRIX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: ee4c67a4a743d3bff1cfc5ca88b6691e995f78a9fb01fe36aabc4ae6aca66e6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732365"
---
# <a name="d3dmatrix"></a>D3DMATRIX

Beschreibt eine Matrix.

``` syntax
typedef struct _D3DMATRIX {
    union {
        struct {
            float        _11, _12, _13, _14;
            float        _21, _22, _23, _24;
            float        _31, _32, _33, _34;
            float        _41, _42, _43, _44;

        };
        float m[4][4];
    };
} D3DMATRIX;
```

Abgeleitete Typen: \* LPD3DMATRIX

## <a name="members"></a>Member



| Element                                                        | Beschreibung                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_ij"></span><span id="_IJ"></span>\_Ij<br/> | Ein Array von Gleitkommazahlen, die eine 4x4-Matrix darstellen, wobei i die Zeilennummer und j die Spaltennummer ist. Beispielsweise \_ bedeutet 34 das gleiche wie \[ a₃₄ , die Komponente in der \] dritten Zeile und vierten Spalte.<br/> |



 

## <a name="remarks"></a>Hinweise

In Direct3D kann das \_ 34-Element einer Projektionsmatrix keine negative Zahl sein. Wenn Ihre Anwendung an dieser Position einen negativen Wert verwenden muss, sollte stattdessen die gesamte Projektionsmatrix um -1 skaliert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[**Graphics.multiplytransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

**SetTransform**
</dt> <dt>

[**D3DXMATRIX**](d3dxmatrix.md)
</dt> <dt>

[Transformationen (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
