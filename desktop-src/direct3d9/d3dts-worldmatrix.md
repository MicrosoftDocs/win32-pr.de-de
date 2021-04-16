---
description: Ordnet Indizes im Bereich von 0 bis 255 den entsprechenden Transformations Zuständen zu.
ms.assetid: b0a1548c-de5d-4eff-baf9-4aecb5e13443
title: D3DTS_WORLDMATRIX-Makro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDMATRIX
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f80996a37e2fb48bf8ca7ea73f714b04e711b263
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530875"
---
# <a name="d3dts_worldmatrix-macro"></a>D3DTS \_ worldmatrix-Makro

Ordnet Indizes im Bereich von 0 bis 255 den entsprechenden Transformations Zuständen zu.

## <a name="syntax"></a>Syntax


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLDMATRIX(
   int index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Ein Indexwert im Bereich von 0 bis 255.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) , der dem angegebenen *Index* zugeordnet ist.

## <a name="remarks"></a>Bemerkungen

Transformations Zustände im Bereich von 256 bis 511 sind zum Speichern von bis zu 256 Matrizen reserviert, die mithilfe von 8-Bit-Indizes indiziert werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 
