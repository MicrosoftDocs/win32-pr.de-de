---
description: Holen Sie sich die in einem Shader referenzierten samplernamen.
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: D3DXGetShaderSamplers-Funktion (D3DX9Shader. h)
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
ms.openlocfilehash: 2135ba36f238188c6e7817001ba89bb47e3b9998
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365311"
---
# <a name="d3dxgetshadersamplers-function"></a>D3DXGetShaderSamplers-Funktion

Holen Sie sich die in einem Shader referenzierten samplernamen.

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

*pfunction* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf den DWORD-Datenstrom der Shader-Funktion.

</dd> <dt>

*psamplers* \[ in, out\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von lpcstrins. Die-Funktion wird dieses Array mit Zeigern auf die in *pfunction* enthaltenen samplnamen ausfüllen. Die maximale Array Größe ist die maximale Anzahl von samplerregistern (16 für vs \_ 3 \_ 0 und PS \_ 3 \_ 0).

Um die Anzahl der verwendeten Samplern zu ermitteln, überprüfen Sie *pcount* nach dem Aufruf von **D3DXGetShaderSamplers** mit psamplers = **null**.

</dd> <dt>

*pcount* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Gibt die Anzahl der Samplern zurück, auf die vom Shader verwiesen wird.

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

 

 
