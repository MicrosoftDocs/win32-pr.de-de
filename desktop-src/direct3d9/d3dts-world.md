---
description: Identifiziert die Transformationsmatrix, die als Welttransformationsmatrix festgelegt wird.
ms.assetid: 2bf7ac8a-43d8-460e-a400-3b33e96441db
title: D3DTS_WORLD -Makro (D3d9types.h)
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
ms.openlocfilehash: 68b0a3435df2ec36fca34fb8a8e4f2638ae9d432a009870ce85cbbdf2a42f1ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850080"
---
# <a name="d3dts_world-macro"></a>D3DTS \_ WORLD-Makro

Identifiziert die Transformationsmatrix, die als Welttransformationsmatrix festgelegt wird.

## <a name="syntax"></a>Syntax


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLD(void);
```



## <a name="parameters"></a>Parameter

Dieses Makro verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Ein [**D3DTRANSFORMSTATETYPE-Wert,**](./d3dtransformstatetype.md) der [**D3DTS \_ WORLDMATRIX(0) entspricht.**](./d3dts-worldmatrix.md)

## <a name="remarks"></a>Hinweise

Dieses Makro wird bereitgestellt, um das Portieren vorhandener Anwendungen auf Direct3D 9 zu vereinfachen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
