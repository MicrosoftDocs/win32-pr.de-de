---
description: 'D3DXGetShaderConstantTable-Funktion: Ruft die shaderkonstante Tabelle ab, die in einen Shader eingebettet ist.'
ms.assetid: eb965074-819f-44d2-889b-6c6eada4f062
title: D3DXGetShaderConstantTable-Funktion (D3DX9Shader.h)
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
ms.openlocfilehash: b397901578a1e6ce6fecc01ed25c99d4681d1c40
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114418"
---
# <a name="d3dxgetshaderconstanttable-function"></a>D3DXGetShaderConstantTable-Funktion

Ruft die shaderkonstante Tabelle ab, die in einen Shader eingebettet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXGetShaderConstantTable(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXCONSTANTTABLE * ppConstantTable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFunction* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf den DWORD-Funktionsstream.

</dd> <dt>

 *ppConstantTable* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Gibt die Konstante-Tabellenschnittstelle (siehe [**ID3DXConstantTable)**](id3dxconstanttable.md)zurück, die die konstante Tabelle verwaltet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Bemerkungen

Eine konstante Tabelle wird von [**D3DXCompileShader**](d3dxcompileshader.md) generiert und in den Shadertext eingebettet. Wenn Sie zusätzlichen virtuellen Adressraum benötigen, finden Sie weitere Informationen unter [**D3DXGetShaderConstantTableEx.**](d3dxgetshaderconstanttableex.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
