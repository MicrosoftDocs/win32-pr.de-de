---
description: Erstellt ein Textur-Shaderobjekt aus dem kompilierten Shader.
ms.assetid: 3e8017f7-fe6b-4f4e-a80e-b16b16c0b348
title: D3DXCreateTextureShader-Funktion (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e989570c98b6b306782d8fb01e53b04d7157b1bb46db726a27fe2ade88a806c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298971"
---
# <a name="d3dxcreatetextureshader-function"></a>D3DXCreateTextureShader-Funktion

Erstellt ein Textur-Shaderobjekt aus dem kompilierten Shader.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateTextureShader(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXTEXTURESHADER *ppTextureShader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFunction* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf den DWORD-Datenstrom der Funktion.

</dd> <dt>

*ppTextureShader* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***

Gibt ein [**ID3DXTextureShader-Objekt**](id3dxtextureshader.md) zurück, mit dem der Inhalt einer Textur mithilfe der [**D3DXFillTextureTX-Funktionen**](d3dxfilltexturetx.md) prozedural aufgefüllt werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
