---
description: Definiert die Position, an der für Beleuchtungsberechnungen auf eine Farbkomponente zugegriffen werden muss.
ms.assetid: 76061d47-a31c-4008-aa8d-a0464dd3423f
title: D3DMATERIALCOLORSOURCE-Enumeration (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIALCOLORSOURCE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3c8069fdde062fdc6dea311b40b8614d2165356ff397f0d056c43569f391e02a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988890"
---
# <a name="d3dmaterialcolorsource-enumeration"></a>D3DMATERIALCOLORSOURCE-Enumeration

Definiert die Position, an der für Beleuchtungsberechnungen auf eine Farbkomponente zugegriffen werden muss.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DMATERIALCOLORSOURCE { 
  D3DMCS_MATERIAL     = 0,
  D3DMCS_COLOR1       = 1,
  D3DMCS_COLOR2       = 2,
  D3DMCS_FORCE_DWORD  = 0x7fffffff
} D3DMATERIALCOLORSOURCE, *LPD3DMATERIALCOLORSOURCE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**D3DMCS \_ MATERIAL**
</dt> <dd>

Verwenden Sie die Farbe aus dem aktuellen Material.

</dd> <dt>

<span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS \_ COLOR1**
</dt> <dd>

Verwenden Sie die diffuse Scheitelpunktfarbe.

</dd> <dt>

<span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS \_ COLOR2**
</dt> <dd>

Verwenden Sie die Specular Vertex-Farbe.

</dd> <dt>

<span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration in eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Flags werden verwendet, um den Wert der folgenden Renderzustände im [**Enumerationstyp D3DRENDERSTATETYPE**](./d3drenderstatetype.md) festzulegen.

-   D3DRS \_ AMBIENTMATERIALSOURCE
-   D3DRS \_ DIFFUSEMATERIALSOURCE
-   D3DRS \_ EMISSIVEMATERIALSOURCE
-   D3DRS \_ SPECULARMATERIALSOURCE

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
