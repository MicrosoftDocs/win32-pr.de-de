---
description: Erstellt ein Textur-Shader-Objekt aus dem kompilierten Shader.
ms.assetid: 3e8017f7-fe6b-4f4e-a80e-b16b16c0b348
title: D3DXCreateTextureShader-Funktion (D3DX9Shader. h)
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
ms.openlocfilehash: c32715f1b939d30acb53b1cbe07e081d43d21823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354906"
---
# <a name="d3dxcreatetextureshader-function"></a>D3DXCreateTextureShader-Funktion

Erstellt ein Textur-Shader-Objekt aus dem kompilierten Shader.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateTextureShader(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXTEXTURESHADER *ppTextureShader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfunction* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Ein Zeiger auf die Funktion DWORD-Stream.

</dd> <dt>

*pptextureshader* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***

Gibt ein [**ID3DXTextureShader**](id3dxtextureshader.md) -Objekt zurück, das verwendet werden kann, um den Inhalt einer Textur mithilfe der [**D3DXFillTextureTX**](d3dxfilltexturetx.md) -Funktionen zu verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
