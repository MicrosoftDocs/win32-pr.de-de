---
description: Ruft die Semantik für die shadereingaben ab. Verwenden Sie diese Methode, um das Format der Eingabe Vertex zu bestimmen.
ms.assetid: e94b2b14-3830-4a13-8c23-7841a56d6730
title: D3DXGetShaderInputSemantics-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderInputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2032f241d6ca5c22506c0875a21f9d5b431920df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355186"
---
# <a name="d3dxgetshaderinputsemantics-function"></a>D3DXGetShaderInputSemantics-Funktion

Ruft die Semantik für die shadereingaben ab. Verwenden Sie diese Methode, um das Format der Eingabe Vertex zu bestimmen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXGetShaderInputSemantics(
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

Zeiger auf ein Array von [**D3DXSEMANTIC**](d3dxsemantic.md) -Strukturen. Die Funktion gibt dieses Array mit der Semantik für jedes Eingabe Element aus, auf das vom Shader verwiesen wird. Es wird davon ausgegangen, dass in diesem Array mindestens MAXD3DDECLLENGTH Elemente enthalten sind. Wenn Sie **D3DXGetShaderInputSemantics** mit psemantics = **null** aufrufen, wird jedoch die Anzahl der für pcount benötigten Elemente zurückgegeben.

</dd> <dt>

*pcount* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Gibt die Anzahl der Elemente in psemantik zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie **D3DXGetShaderInputSemantics** , um eine Liste der vom Shader benötigten Eingabe Semantik zurückzugeben. Auf diese Weise können Sie herausfinden, was das Eingabe Vertex-Format für einen HLSL-Shader (High-Level Shader Language) ist. Wenn der Shader zusätzliche Eingaben hat, die ihre Scheitelpunkt Deklaration fehlt, können Sie einen zusätzlichen vertexstream mit einem Sprung von 0 erstellen, der die fehlenden Komponenten mit den Standardwerten aufweist. Diese Technik könnte beispielsweise verwendet werden, um Standard Scheitelpunkt Farben für Modelle bereitzustellen, die diese nicht angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
