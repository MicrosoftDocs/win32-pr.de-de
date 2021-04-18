---
description: Identifiziert nachfolgende Transformations Matrizen, die verwendet werden können, um Vertices mit der entsprechenden Matrix und einem im Vertex-Format angegebenen Mischungs Gewichtungswert (Beta) zu kombinieren.
ms.assetid: cab444c2-b245-4d1a-a90c-745c92a2ea89
title: D3DTS_WORLDn (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDn
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 004435d278538c788e21ed7dc3482fd5e248895b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351936"
---
# <a name="d3dts_worldn"></a>D3DTS \_ worldn

Identifiziert nachfolgende Transformations Matrizen, die verwendet werden können, um Vertices mit der entsprechenden Matrix und einem im Vertex-Format angegebenen Mischungs Gewichtungswert (Beta) zu kombinieren.

``` syntax
#define D3DTS_WORLDn 
#define D3DTS_WORLD1 D3DTS_WORLDMATRIX(1)
#define D3DTS_WORLD2 D3DTS_WORLDMATRIX(2)
#define D3DTS_WORLD3 D3DTS_WORLDMATRIX(3)
```

## <a name="remarks"></a>Bemerkungen

Diese Makros werden bereitgestellt, um das Portieren vorhandener Anwendungen auf Direct3D 9 zu vereinfachen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
