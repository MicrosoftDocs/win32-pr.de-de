---
description: Die Semantik für alle Shader-Ausgabe Elemente erhalten.
ms.assetid: 1a3cdd5d-0ea7-48ae-a3f1-030e95b03a42
title: D3DXGetShaderOutputSemantics-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderOutputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 264db967d2959c2f6e5096e0362e9db576ba9f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530902"
---
# <a name="d3dxgetshaderoutputsemantics-function"></a>D3DXGetShaderOutputSemantics-Funktion

Die Semantik für alle Shader-Ausgabe Elemente erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXGetShaderOutputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfunction* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf den DWORD-Datenstrom der Shader-Funktion.

</dd> <dt>

*psemantik* \[ in\]
</dt> <dd>

Typ: **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***

Zeiger auf ein Array von [**D3DXSEMANTIC**](d3dxsemantic.md) -Strukturen. Die Funktion gibt dieses Array mit der Semantik für jedes Ausgabe Element aus, auf das vom Shader verwiesen wird. Es wird davon ausgegangen, dass in diesem Array mindestens MAXD3DDECLLENGTH Elemente enthalten sind. Wenn Sie **D3DXGetShaderOutputSemantics** mit psemantics = **null** aufrufen, wird jedoch die Anzahl der für pcount benötigten Elemente zurückgegeben.

</dd> <dt>

*pcount* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Gibt die Anzahl der Elemente in psemantik zurück.

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

 

 
