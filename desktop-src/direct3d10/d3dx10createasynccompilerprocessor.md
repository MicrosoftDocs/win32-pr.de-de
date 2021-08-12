---
description: Erstellen Sie einen asynchronen Datenprozessor für einen Shader.
ms.assetid: e23290fa-ccd7-4703-ae6b-4fffe352875e
title: D3DX10CreateAsyncCompilerProcessor-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: f5e7011d868b46196293f441d76d182156fb0ba1431227d6bf01212f8c809249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303465"
---
# <a name="d3dx10createasynccompilerprocessor-function"></a>D3DX10CreateAsyncCompilerProcessor-Funktion

Erstellen Sie einen asynchronen Datenprozessor für einen Shader.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D10_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge, die den Shaderdateinamen enthält.

</dd> <dt>

*pDefdefdefine* \[ In\]
</dt> <dd>

Typ: **const [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Ein auf NULL terminiertes Array von Shadermakros (siehe [**D3D-SHADER-MAKRO). \_ \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)Legen Sie dies auf **NULL** fest, um keine Makros anzugeben.

</dd> <dt>

*pInclude* \[ In\]
</dt> <dd>

Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Ein Zeiger auf eine Includeschnittstelle (siehe [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))). Dieser Parameter kann **NULL** sein.

</dd> <dt>

*pFunctionName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Name der Shader-Einstiegspunktfunktion, an der die Shaderausführung beginnt. Wenn Sie einen Effekt kompilieren, ignoriert **D3DX10CreateAsyncCompilerProcessor** *pFunctionName*; Es wird empfohlen, *pFunctionName* auf **NULL** zu setzen, da es sich empfiehlt, einen Zeigerparameter auf **NULL** zu setzen, wenn die aufgerufene Funktion ihn nicht verwendet.

</dd> <dt>

*pProfile* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge, die das [Shaderprofil oder](../direct3dhlsl/dx-graphics-hlsl-models.md) Shadermodell angibt.

</dd> <dt>

*Flags1* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

[Shader-Kompilierungsflags.](d3d10-shader.md)

</dd> <dt>

*Flags2* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

[Effect-Kompilierungsflags](d3d10-graphics-reference-effect-constants.md). Wenn Sie einen Shader und keine Effektdatei kompilieren, ignoriert **D3DX10CreateAsyncCompilerProcessor** *Flags2*; Es wird empfohlen, *Flags2* auf 0 (null) zu setzen, da es sich empfiehlt, einen Zeigerparameter auf **NULL** zu setzen, wenn die aufgerufene Funktion ihn nicht verwendet.

</dd> <dt>

*ppCompiledShader* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Adresse eines Zeigers auf den kompilierten Effekt (siehe [**ID3D10Blob-Schnittstelle**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).

</dd> <dt>

*ppErrorBuffer* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Adresse eines Zeigers zum Kompilieren von Fehlern (siehe [**ID3D10Blob-Schnittstelle**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).

</dd> <dt>

*ppDataProcessor* \[ out\]
</dt> <dd>

Typ: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***

Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX10DataProcessor-Schnittstelle**](id3dx10dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
