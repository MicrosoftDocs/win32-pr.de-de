---
description: Generiert eine Mipmapkette mit einem bestimmten Texturfilter.
ms.assetid: 19e651dd-dc34-405b-8769-00d91c097a1f
title: D3DX10FilterTexture-Funktion (D3DX10Tex.h)
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
ms.openlocfilehash: 225caf2c9b08a498e77723dbb7ab43c8fd4850262c1f58f5ae37a3157e953edd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497640"
---
# <a name="d3dx10filtertexture-function"></a>D3DX10FilterTexture-Funktion

Generiert eine Mipmapkette mit einem bestimmten Texturfilter.

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

*pTexture* 
</dt> <dd>

Typ: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Das zu filternde Texturobjekt. Siehe [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*SrcLevel* 
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Mipmapebene, deren Daten verwendet werden, um den Rest der Mipmapkette zu generieren.

</dd> <dt>

*MipFilter* 
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Flags, die steuern, wie die einzelnen miplevel gefiltert werden (oder D3DX10 \_ DEFAULT für D3DX10 \_ FILTER \_ BOX). Weitere Informationen finden Sie unter [**D3DX10 \_ FILTER \_ FLAG**](d3dx10-filter-flag.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texturfunktionen in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
