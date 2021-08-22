---
description: Abrufen der Samplernamen, auf die in einem Shader verwiesen wird.
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: D3DXGetShaderSamplers-Funktion (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSamplers
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da4c7381b0fe058e18dd2edfd86ef49f434cd1b57bff18303fce0ba939c5d299
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044998"
---
# <a name="d3dxgetshadersamplers-function"></a>D3DXGetShaderSamplers-Funktion

Abrufen der Samplernamen, auf die in einem Shader verwiesen wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXGetShaderSamplers(
  _In_    const DWORD  *pFunction,
  _Inout_       LPCSTR *pSamplers,
  _Out_         UINT   *pCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFunction* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf den DWORD-Stream der Shaderfunktion.

</dd> <dt>

*pSamplers* \[ in, out\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von LPCSTRs. Die Funktion füllt dieses Array mit Zeigern auf die in *pFunction* enthaltenen Samplernamen. Die maximale Arraygröße ist die maximale Anzahl von Samplerregistern (16 für \_ vs. \_ 3 0 und ps \_ 3 \_ 0).

Um die Anzahl der verwendeten Sampler zu ermitteln, überprüfen Sie *pCount* nach dem Aufruf von **D3DXGetShaderSamplers** mit pSamplers = **NULL**.

</dd> <dt>

*pCount* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Gibt die Anzahl der Sampler zurück, auf die vom Shader verwiesen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
