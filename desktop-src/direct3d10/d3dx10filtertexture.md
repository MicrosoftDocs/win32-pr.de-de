---
description: Generiert eine MipMap-Kette mithilfe eines bestimmten Textur Filters.
ms.assetid: 19e651dd-dc34-405b-8769-00d91c097a1f
title: D3DX10FilterTexture-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10FilterTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e2f500bcd7f7465ca1c24f1adaab3a77dd5cb7b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365287"
---
# <a name="d3dx10filtertexture-function"></a>D3DX10FilterTexture-Funktion

Generiert eine MipMap-Kette mithilfe eines bestimmten Textur Filters.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10FilterTexture(
   ID3D10Resource *pTexture,
   UINT           SrcLevel,
   UINT           MipFilter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptexture* 
</dt> <dd>

Typ: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Das zu filternde Textur Objekt. Siehe [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*Srclevel* 
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die MipMap-Ebene, deren Daten verwendet werden, um den Rest der MipMap-Kette zu generieren.

</dd> <dt>

*MipFilter* 
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Flags, die Steuern, wie die einzelnen miplevel-Werte gefiltert werden (oder d3dx10 \_ default for d3dx10 \_ Filter \_ Box). Siehe [**d3dx10 \_ Filter- \_ Flag**](d3dx10-filter-flag.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
