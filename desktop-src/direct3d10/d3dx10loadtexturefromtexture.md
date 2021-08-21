---
description: Laden sie eine Textur aus einer Textur.
ms.assetid: 126e71e1-a3b2-418b-be35-434a2e9472ca
title: D3DX10LoadTextureFromTexture-Funktion (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10LoadTextureFromTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: bfc36423154bfd56f0695a3a8178b89aefce6e4dfc5a67f3866fa13a99c5e6d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990500"
---
# <a name="d3dx10loadtexturefromtexture-function"></a>D3DX10LoadTextureFromTexture-Funktion

Laden sie eine Textur aus einer Textur.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10LoadTextureFromTexture(
   ID3D10Resource           *pSrcTexture,
   D3DX10_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D10Resource           *pDstTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrcTexture* 
</dt> <dd>

Typ: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Zeiger auf die Quelltextur. Weitere Informationen [**finden Sie unter ID3D10Resource.**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)

</dd> <dt>

*pLoadInfo* 
</dt> <dd>

Typ: **[ **D3DX10 \_ \_ \_ TEXTURLADEINFORMATIONEN**](d3dx10-texture-load-info.md)\***

Zeiger auf Texturladeparameter. Weitere Informationen [**finden Sie unter D3DX10 \_ TEXTURE LOAD INFO (TEXTURLADEINFORMATIONEN \_ FÜR D3DX10). \_**](d3dx10-texture-load-info.md)

</dd> <dt>

*pDstTexture* 
</dt> <dd>

Typ: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Zeiger auf die Zieltextur. Siehe [**ID3D10Resource-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texturfunktionen in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




