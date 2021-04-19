---
description: Gibt an, dass die Transformationsmatrix als World Transformation Matrix festgelegt wird.
ms.assetid: 2bf7ac8a-43d8-460e-a400-3b33e96441db
title: D3DTS_WORLD-Makro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLD
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3c8f0ac30230a747fba34d9962791b4b331d647
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363126"
---
# <a name="d3dts_world-macro"></a>D3DTS \_ World-Makro

Gibt an, dass die Transformationsmatrix als World Transformation Matrix festgelegt wird.

## <a name="syntax"></a>Syntax


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLD(void);
```



## <a name="parameters"></a>Parameter

Dieses Makro weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Ein [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) Äquivalent zu [**D3DTS \_ worldmatrix (0)**](./d3dts-worldmatrix.md).

## <a name="remarks"></a>Bemerkungen

Dieses Makro wird bereitgestellt, um das Portieren vorhandener Anwendungen auf Direct3D 9 zu vereinfachen.

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

 

 
