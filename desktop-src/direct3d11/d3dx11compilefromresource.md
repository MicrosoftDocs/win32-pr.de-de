---
title: D3DX11CompileFromResource-Funktion (D3DX11async.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Hinweis Anstelle dieser Funktion wird empfohlen, Ressourcenfunktionen zu verwenden und dann offline mit dem Fxc.exe-Befehlszeilencompiler zu kompilieren oder eine der HLSL-Kompilierungs-APIs wie die D3DCompile-API zu verwenden. Kompilieren Sie einen Shader oder einen Effekt aus einer Ressource.
ms.assetid: ececa469-f5e3-4cb3-befe-0ed1a5a57671
keywords:
- D3DX11CompileFromResource-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3aafa7d504bbbcd99591b45412d63cbf78270ef46ffa63bbf2d34497510802
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536764"
---
# <a name="d3dx11compilefromresource-function"></a>D3DX11CompileFromResource-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, [](/windows/desktop/menurc/resources-functions)sollten Sie Ressourcenfunktionen verwenden und dann offline kompilieren, indem Sie den Fxc.exe-Befehlszeilencompiler verwenden oder eine der HLSL-Kompilierungs-APIs wie die [**D3DCompile-API**](/windows/desktop/direct3dhlsl/d3dcompile) verwenden.

 

Kompilieren Sie einen Shader oder einen Effekt aus einer Ressource.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSrcModule* \[ In\]
</dt> <dd>

Typ: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**

Handle für das Ressourcenmodul, das den Shader enthält. HMODULE kann mit der [GetModuleHandle-Funktion erhalten werden.](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)

</dd> <dt>

*pSrcResource* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Name der Ressource, die den Shader enthält. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Datentyp in LPCSTR auflösen.

</dd> <dt>

*pSrcFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Optional. Name der Effect-Datei, die nur für Fehlermeldungen verwendet wird. Kann NULL **sein.**

</dd> <dt>

*pDefdefine* \[ In\]
</dt> <dd>

Typ: **const [**D3D10 \_ SHADER \_ MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Optional. Zeiger auf ein Array von Makrodefinitionen (siehe [**D3D10 \_ SHADER \_ MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). Die letzte Struktur im Array dient als Abschlusszeichen und muss alle Member auf 0 festlegen. Wenn sie nicht verwendet wird, legen *Sie pDefdefdefinitionen* auf **NULL fest.**

</dd> <dt>

*pInclude* \[ In\]
</dt> <dd>

Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Optional. Zeiger auf eine Schnittstelle zum Behandeln von Includedateien. Das Festlegen auf **NULL** verursacht einen Kompilierungsfehler, wenn ein Shader ein Include \# enthält.

</dd> <dt>

*pFunctionName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Name der Shader-Einstiegspunktfunktion, an der die Shaderausführung beginnt. Wenn Sie einen Effekt kompilieren, ignoriert **D3DX11CompileFromResource** *pFunctionName*; Es wird empfohlen, *pFunctionName* auf **NULL** zu setzen, da es sich empfiehlt, einen Zeigerparameter auf **NULL** zu setzen, wenn die aufgerufene Funktion ihn nicht verwendet.

</dd> <dt>

*pProfile* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Eine Zeichenfolge, die das Shadermodell angibt. kann ein beliebiges Profil in Shadermodell 2, Shadermodell 3, Shadermodell 4 oder Shadermodell 5 sein. Das Profil kann auch für den Effekttyp (z. B. fx \_ 4 \_ 1) verwendet werden.

</dd> <dt>

*Flags1* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

[**Shader-Kompilierungsflags.**](/windows/desktop/direct3dhlsl/d3dcompile-constants)

</dd> <dt>

*Flags2* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

[**Effect-Kompilierungsflags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants). Wenn Sie einen Shader und keine Effektdatei kompilieren, ignoriert **D3DX11CompileFromResource** *Flags2*; Es wird empfohlen, *Flags2* auf 0 (null) zu setzen, da es sich empfiehlt, einen Nichtpointerparameter auf 0 (null) zu setzen, wenn die aufgerufene Funktion ihn nicht verwendet.

</dd> <dt>

*pPump* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Ein Zeiger auf eine Threadpumpschnittstelle (siehe [**ID3DX11ThreadPump-Schnittstelle**](id3dx11threadpump.md)). Verwenden **Sie NULL,** um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn sie abgeschlossen ist.

</dd> <dt>

*ppShader* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Ein Zeiger auf den Arbeitsspeicher, der den kompilierten Shader sowie alle eingebetteten Debug- und Symboltabelleninformationen enthält.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Ein Zeiger auf den Arbeitsspeicher, der eine Liste von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind. Diese Fehler und Warnungen sind identisch mit der Debugausgabe eines Debuggers.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann NULL **sein.** Wenn *pPump* nicht **NULL ist,** muss *pHResult* ein gültiger Speicherort sein, bis die asynchrone Ausführung abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die unter [Direct3D 11-Rückgabecodes aufgeführt sind.](d3d11-graphics-reference-returnvalues.md)

**D3DX11CompileFromResource** gibt E INVALIDARG zurück, wenn Sie für den pHResult-Parameter nicht NULL angeben, wenn Sie NULL für den \_ *pPump-Parameter* angeben.   Weitere Informationen zu dieser Situation finden Sie unter Hinweise.

## <a name="remarks"></a>Hinweise

Weitere Informationen zu **D3DX11CompileFromResource finden** Sie unter [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).

Sie müssen NULL **für** den *pHResult-Parameter* angeben, wenn Sie auch **NULL** für den *pPump-Parameter* angeben. Andernfalls können Sie anschließend keinen Shader erstellen, indem Sie den kompilierten Shadercode verwenden, den **D3DX11CompileFromResource** im Arbeitsspeicher zurückgibt, auf den der *ppShader-Parameter* zeigt. Rufen Sie eine der folgenden [**ID3D11Device-Schnittstellenmethoden**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) auf, um einen Shader aus einem shader-Code zu erstellen:

-   [**CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**CreatePixelShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [**CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Wenn Sie bei der Bereitstellung von **NULL** für *pPump* einen **Nicht-NULL-Wert** für *pHResult* eingeben, gibt **D3DX11CompileFromResource** den Fehlercode E \_ INVALIDARG zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

