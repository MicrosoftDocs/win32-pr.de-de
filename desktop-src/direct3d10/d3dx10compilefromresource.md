---
description: Hinweis Anstatt diese Legacyfunktion zu verwenden, wird empfohlen, offline zu kompilieren, indem Sie Fxc.exe Befehlszeilencompiler oder die D3DCompile-API verwenden. Kompilieren Sie einen Shader oder einen Effekt aus einer Ressource.
ms.assetid: d291e47d-e04f-4e2d-9d05-9aef8e4fcf7e
title: D3DX10CompileFromResource-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 2c938ca302e21be16dfd1d2700a80e0ee350d7acb52ce7ab72fe2c52cbae4bf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634930"
---
# <a name="d3dx10compilefromresource-function"></a>D3DX10CompileFromResource-Funktion

> [!Note]  
> Anstatt diese Legacyfunktion zu verwenden, wird empfohlen, offline zu kompilieren, indem Fxc.exe Befehlszeilencompiler oder die [**D3DCompile-API**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) verwendet wird.

 

Kompilieren Sie einen Shader oder einen Effekt aus einer Ressource.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSrcModule* \[ In\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle für das Ressourcenmodul, das den Shader enthält. HMODULE kann mit der [GetModuleHandle-Funktion erhalten werden.](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)

</dd> <dt>

*pSrcResource* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Name der Ressource, die den Shader enthält. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Datentyp in LPCSTR auflösen.

</dd> <dt>

*pSrcFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Optional. Name der Effect-Datei, die nur für Fehlermeldungen verwendet wird. Kann NULL **sein.**

</dd> <dt>

*pDefdefine* \[ In\]
</dt> <dd>

Typ: **const [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Optional. Zeiger auf ein Array von Makrodefinitionen (siehe [**\_ D3D-SHADER-MAKRO \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). Die letzte Struktur im Array dient als Abschlusszeichen und muss alle Member auf 0 festlegen. Wenn sie nicht verwendet wird, legen *Sie pDefdefdefinitionen* auf **NULL fest.**

</dd> <dt>

*pInclude* \[ In\]
</dt> <dd>

Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Optional. Zeiger auf eine [**ID3D10Include-Schnittstelle**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) für die Verarbeitung von Includedateien. Das Festlegen auf **NULL** verursacht einen Kompilierungsfehler, wenn ein Shader ein Include \# enthält.

</dd> <dt>

*pFunctionName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Name der Shader-Einstiegspunktfunktion, an der die Shaderausführung beginnt. Wenn Sie einen Effekt kompilieren, ignoriert **D3DX10CompileFromResource** *pFunctionName*; Es wird empfohlen, *pFunctionName* auf **NULL** zu setzen, da es sich empfiehlt, einen Zeigerparameter auf **NULL** zu setzen, wenn die aufgerufene Funktion ihn nicht verwendet.

</dd> <dt>

*pProfile* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge, die das Shadermodell angibt. kann ein beliebiges Profil in [Shadermodell 2,](../direct3dhlsl/dx-graphics-hlsl-sm2.md) [Shadermodell 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)oder [Shadermodell 4 sein.](../direct3dhlsl/dx-graphics-hlsl-sm4.md)

</dd> <dt>

*Flags1* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

[Shader-Kompilierungsflags.](d3d10-shader.md)

</dd> <dt>

*Flags2* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

[Effect-Kompilierungsflags](d3d10-graphics-reference-effect-constants.md). Wenn Sie einen Shader und keine Effektdatei kompilieren, ignoriert **D3DX10CompileFromResource** *Flags2*; Es wird empfohlen, *Flags2* auf 0 (null) zu setzen, da es sich empfiehlt, einen Nichtpointerparameter auf 0 (null) zu setzen, wenn die aufgerufene Funktion ihn nicht verwendet.

</dd> <dt>

*pPump* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Ein Zeiger auf eine Threadpumpschnittstelle (siehe [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md)). Verwenden **Sie NULL,** um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn sie abgeschlossen ist.

</dd> <dt>

*ppShader* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Ein Zeiger auf eine [**ID3D10Blob-Schnittstelle,**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) die den kompilierten Shader sowie alle eingebetteten Debug- und Symboltabelleninformationen enthält.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Ein Zeiger auf eine [**ID3D10Blob-Schnittstelle,**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) die eine Liste von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind. Diese Fehler und Warnungen sind identisch mit der Debugausgabe eines Debuggers.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann NULL **sein.** Wenn *pPump* nicht **NULL ist,** muss *pHResult* ein gültiger Speicherort sein, bis die asynchrone Ausführung abgeschlossen ist.

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

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
