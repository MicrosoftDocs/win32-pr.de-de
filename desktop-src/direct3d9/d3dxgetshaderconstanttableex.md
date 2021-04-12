---
description: Ruft die in einen Shader eingebettete Shader-Konstante Tabelle ab.
ms.assetid: f7e846e4-9cb4-4634-95e3-4b2a752978a8
title: D3DXGetShaderConstantTableEx-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTableEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2107e7f30733c8f8a19e39e220c4c1d6cb174424
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219511"
---
# <a name="d3dxgetshaderconstanttableex-function"></a>D3DXGetShaderConstantTableEx-Funktion

Ruft die in einen Shader eingebettete Shader-Konstante Tabelle ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXGetShaderConstantTableEx(
  _In_  const DWORD               *pFunction,
  _In_        DWORD               Flags,
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

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Verwenden Sie das D3DXCONSTTABLE \_ LARGEADDRESSAWARE-Flag, um auf bis zu 4 GB virtuellen Adressraum zuzugreifen (anstelle der Standardeinstellung von 2 GB). Wenn Sie den zusätzlichen virtuellen Adressraum nicht benötigen, verwenden Sie [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md).

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

Eine Konstante Tabelle wird von [**D3DXCompileShader**](d3dxcompileshader.md) generiert und in den Shader-Text eingebettet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
