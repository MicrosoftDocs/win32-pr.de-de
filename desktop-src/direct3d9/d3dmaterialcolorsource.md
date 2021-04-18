---
description: Definiert den Speicherort, an dem für Beleuchtungsberechnungen auf eine Farb-oder Farbkomponente zugegriffen werden muss.
ms.assetid: 76061d47-a31c-4008-aa8d-a0464dd3423f
title: D3DMATERIALCOLORSOURCE-Enumeration (D3D9Types. h)
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
ms.openlocfilehash: 8877eece8e33c6508768b22c989e992cf8178823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354379"
---
# <a name="d3dmaterialcolorsource-enumeration"></a>D3DMATERIALCOLORSOURCE-Enumeration

Definiert den Speicherort, an dem für Beleuchtungsberechnungen auf eine Farb-oder Farbkomponente zugegriffen werden muss.

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

<span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**D3DMCS \_ Material**
</dt> <dd>

Verwenden Sie die Farbe aus dem aktuellen Material.

</dd> <dt>

<span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS \_ COLOR1**
</dt> <dd>

Verwenden Sie die diffuse Scheitelpunkt Farbe.

</dd> <dt>

<span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS \_ COLOR2**
</dt> <dd>

Verwenden Sie die Glanz Farbe des Scheitel Punkts.

</dd> <dt>

<span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Flags werden verwendet, um den Wert der folgenden Rendering-Zustände im [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) -enumerierten Typ festzulegen.

-   D3DRS \_ AmbientMaterialSource
-   D3DRS \_ DiffuseMaterialSource
-   D3DRS \_ emissivematerialsource
-   D3DRS \_ SpecularMaterialSource

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
