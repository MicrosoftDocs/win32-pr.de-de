---
description: Ruft die in einen Shader eingebettete Shader-Konstante Tabelle ab.
ms.assetid: eb965074-819f-44d2-889b-6c6eada4f062
title: D3DXGetShaderConstantTable-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTable
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 876802023601c14b4cceed0ef0e2db431d7339e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353723"
---
# <a name="d3dxgetshaderconstanttable-function"></a>D3DXGetShaderConstantTable-Funktion

Ruft die in einen Shader eingebettete Shader-Konstante Tabelle ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXGetShaderConstantTable(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXCONSTANTTABLE * ppConstantTable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfunction* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Ein Zeiger auf die Funktion DWORD-Stream.

</dd> <dt>

 *ppconstanbar* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Gibt die Konstante Tabellen Schnittstelle (siehe [**ID3DXConstantTable**](id3dxconstanttable.md)) zurück, die die Konstante Tabelle verwaltet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Eine Konstante Tabelle wird von [**D3DXCompileShader**](d3dxcompileshader.md) generiert und in den Shader-Text eingebettet. Wenn Sie zusätzlichen virtuellen Adressraum benötigen, finden Sie weitere Informationen unter [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
