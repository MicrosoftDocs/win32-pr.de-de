---
description: Disassemblieren sie einen Shader.
ms.assetid: 30159223-8f88-4929-8ef1-7a6acc13f485
title: D3DXDisassembleShader-Funktion (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b185945098d4439753b5582a81d4d112c7984f53155e2901af8560afb404bf62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857070"
---
# <a name="d3dxdisassembleshader-function"></a>D3DXDisassembleShader-Funktion

Disassemblieren sie einen Shader.

> [!Note]  
> Anstatt diese Legacyfunktion zu verwenden, wird empfohlen, die [**D3DDisassemble-API zu**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) verwenden.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXDisassembleShader(
  _In_  const DWORD        *pShader,
  _In_        BOOL         EnableColorCode,
  _In_        LPCSTR       pComments,
  _Out_       LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pShader* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf einen Speicherpuffer, der die Shaderdaten enthält.

</dd> <dt>

*EnableColorCode* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Aktivieren Sie Farbcode, um das Lesen der Disassemblierung zu vereinfachen.

</dd> <dt>

*pComments* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine optionale auf NULL beendete Kommentarzeichenfolge. Dieser Wert kann NULL **sein.**

</dd> <dt>

*ppDisassembly* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Gibt einen Puffer zurück, der den disassemblierten Shader enthält. Siehe [**ID3DXBuffer**](id3dxbuffer.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
