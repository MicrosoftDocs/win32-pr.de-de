---
title: D3DX11CreateAsyncCompilerProcessor-Funktion (D3DX11async.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise. Erstellen Sie einen asynchronen Datenprozessor für einen Shader.
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
ms.openlocfilehash: 0f5d3767bafda4f1914d37b7baacf599335877c30de216282f172ebe55739920
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124905"
---
# <a name="d3dx11createasynccompilerprocessor-function"></a>D3DX11CreateAsyncCompilerProcessor-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise.

 

Erstellen Sie einen asynchronen Datenprozessor für einen Shader.

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

*pFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Eine Zeichenfolge, die den Shaderdateinamen enthält.

</dd> <dt>

*pDefdefine* \[ In\]
</dt> <dd>

Typ: **const D3D11 \_ SHADER \_ MACRO \***

Ein NULL-terminiertes Array von Shadermakros; Legen Sie dies auf **NULL fest,** um keine Makros anzugeben.

</dd> <dt>

*pInclude* \[ In\]
</dt> <dd>

Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Ein Zeiger auf eine Includeschnittstelle. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*pFunctionName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Name der Shader-Einstiegspunktfunktion, an der die Shaderausführung beginnt. Wenn Sie einen Effekt kompilieren, ignoriert **D3DX11CreateAsyncCompilerProcessor** *pFunctionName*; Es wird empfohlen, *pFunctionName* auf **NULL** zu setzen, da es sich empfiehlt, einen Zeigerparameter auf **NULL** zu setzen, wenn die aufgerufene Funktion ihn nicht verwendet.

</dd> <dt>

*pProfile* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Eine Zeichenfolge, die das Shaderprofil oder Shadermodell angibt. kann ein beliebiges Profil in Shadermodell 2, Shadermodell 3, Shadermodell 4 oder Shadermodell 5 sein. Das Profil kann auch für den Effekttyp (z. B. fx \_ 4 \_ 1) verwendet werden.

</dd> <dt>

*Flags1* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Shader-Kompilierungsflags.

</dd> <dt>

*Flags2* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Effect-Kompilierungsflags. Wenn Sie einen Shader und keine Effektdatei kompilieren, ignoriert **D3DX11CreateAsyncCompilerProcessor** *Flags2*; Es wird empfohlen, *Flags2* auf 0 (null) zu setzen, da es sich empfiehlt, einen Nichtpointerparameter auf 0 (null) zu setzen, wenn die aufgerufene Funktion ihn nicht verwendet.

</dd> <dt>

*ppCompiledShader* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Adresse eines Zeigers auf den kompilierten Effekt.

</dd> <dt>

*ppErrorBuffer* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Adresse eines Zeigers zum Kompilieren von Fehlern.

</dd> <dt>

*ppDataProcessor* \[ out\]
</dt> <dd>

Typ: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX11DataProcessor-Schnittstelle**](id3dx11dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die unter [Direct3D 11-Rückgabecodes aufgeführt sind.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Es gibt keine Implementierung des asynchronen Ladeers außerhalb von D3DX 10 und D3DX 11.

Für Windows Store-Apps enthalten die DirectX-Beispiele (z. B. das [Direct3D-Tutorialbeispiel)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)das **BasicLoader-Modul,** das das asynchrone Programmiermodell Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) verwendet.

Für Win32-Desktop-Apps können [](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) Sie die Concurrency Runtime verwenden, um etwas zu implementieren, das dem asynchronen Windows-Runtime-Modell ähnelt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

