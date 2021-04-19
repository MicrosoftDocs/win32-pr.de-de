---
description: Textur Wrapping Optionen für IMT-Berechnungs-APIs.
ms.assetid: ec364418-67c6-42c7-9c5d-b97aa7e17c24
title: D3DXIMT Flags-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 97731d4720e67fce899bf96f457e55f6adbc05a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366640"
---
# <a name="d3dximt-flags-enumeration"></a>D3DXIMT Flags-Enumeration

Textur Wrapping Optionen für IMT-Berechnungs-APIs.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXIMT_FLAGS { 
  D3DXIMT_WRAP_U   = 1,
  D3DXIMT_WRAP_V   = 2,
  D3DXIMT_WRAP_UV  = 3
} D3DXIMT FLAGS, *LPD3DXIMT FLAGS;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXIMT_WRAP_U"></span><span id="d3dximt_wrap_u"></span>**D3DXIMT \_ Wrap \_ U**
</dt> <dd>

Die Textur wird in die U-Richtung umschlossen.

</dd> <dt>

<span id="D3DXIMT_WRAP_V"></span><span id="d3dximt_wrap_v"></span>**D3DXIMT \_ Wrap \_ V**
</dt> <dd>

Die Textur wird in die Richtung V umschlossen.

</dd> <dt>

<span id="D3DXIMT_WRAP_UV"></span><span id="d3dximt_wrap_uv"></span>**D3DXIMT \_ Wrap \_ -UV**
</dt> <dd>

Die Textur umschließt sowohl die Richtung "Sie" als auch "V".

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md)
</dt> <dt>

[**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md)
</dt> <dt>

[**D3DXComputeIMTFromPerTexelSignal**](d3dxcomputeimtfrompertexelsignal.md)
</dt> <dt>

[**D3DXComputeIMTFromPerVertexSignal**](d3dxcomputeimtfrompervertexsignal.md)
</dt> </dl>

 

 




