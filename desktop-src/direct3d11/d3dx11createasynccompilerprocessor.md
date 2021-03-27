---
title: D3DX11CreateAsyncCompilerProcessor-Funktion (D3DX11async. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Siehe Hinweise. Erstellen eines asynchronen Daten Prozessors für einen Shader.
ms.assetid: 90756ac3-946d-49fa-9f97-70dc5da812c6
keywords:
- D3DX11CreateAsyncCompilerProcessor-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncCompilerProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533e487e65640b8c17a0ff8d061388e8b5a6c0f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996051"
---
# <a name="d3dx11createasynccompilerprocessor-function"></a>D3DX11CreateAsyncCompilerProcessor-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise.

 

Erstellen eines asynchronen Daten Prozessors für einen Shader.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfilename* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Eine Zeichenfolge, die den Shader-Dateinamen enthält.

</dd> <dt>

*pdefinitionen* \[ in\]
</dt> <dd>

Type: **Konstanten D3D11 \_ Shader- \_ Makro \***

Ein mit Null endendes Array von Shader-Makros. Legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.

</dd> <dt>

*pinclude* \[ in\]
</dt> <dd>

Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Ein Zeiger auf eine include-Schnittstelle. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*pfunctionname* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Der Name der Shader-Einstiegspunkt Funktion, bei der die Shader-Ausführung beginnt. Wenn Sie einen Effekt kompilieren,  ignoriert D3DX11CreateAsyncCompilerProcessor *pfunctionname*;. Es wird empfohlen, *pfunctionname* auf **null** festzulegen, da es eine gute Programmierpraxis ist, einen Zeiger Parameter auf **null** festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.

</dd> <dt>

*pprofile* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Eine Zeichenfolge, die das Shader-Profil oder Shader-Modell angibt. kann ein beliebiges Profil in Shader Model 2, Shader Model 3, Shader Model 4 oder Shader Model 5 sein. Das Profil kann auch für den Typ "Effect" (z \_ . b. FX 4 \_ 1) sein.

</dd> <dt>

*Flags1* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Shader-Kompilierungs Flags.

</dd> <dt>

*Flags2* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Effekt Kompilierungs Flags. Wenn Sie einen Shader und keine Effekt Datei kompilieren, ignoriert **D3DX11CreateAsyncCompilerProcessor** *Flags2*; Es wird empfohlen, *Flags2* auf NULL festzulegen, da es eine gute Programmierpraxis ist, einen Typ-Parameter auf 0 (null) festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.

</dd> <dt>

*ppcompiledshader* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Adresse eines Zeigers auf den kompilierten Effekt.

</dd> <dt>

*pperrorbuffer* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Adresse eines Zeigers auf Kompilierungsfehler.

</dd> <dt>

*ppdataprocessor* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX11DataProcessor-Schnittstelle**](id3dx11dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen

Es gibt keine Implementierung des Async-Lade Moduls außerhalb von D3DX 10 und D3DX 11.

Für Windows Store-Apps enthalten die DirectX-Beispiele (z. b. das [Direct3D-tutorialbeispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) das **basicloader** -Modul, das das asynchrone Programmiermodell ([**asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) Windows-Runtime verwendet.

Für Win32-Desktop-Apps können Sie den [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) verwenden, um etwas ähnliches wie das Windows-Runtime asynchrone Programmiermodell zu implementieren.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11async. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Bibliothek d3dx11. lib</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

