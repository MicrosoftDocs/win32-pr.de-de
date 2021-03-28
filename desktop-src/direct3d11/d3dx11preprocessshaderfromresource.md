---
title: D3DX11PreprocessShaderFromResource-Funktion (D3DX11async. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie, dass Sie die D3DPreprocess-API verwenden, anstatt diese Funktion zu verwenden. Erstellen Sie einen Shader aus einer Ressource, ohne ihn zu kompilieren.
ms.assetid: 13362ad6-f02e-4899-8962-4f7d4750ff69
keywords:
- D3DX11PreprocessShaderFromResource-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645d872e983cabbcd81aab05a59ee8f1f83cc403
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995986"
---
# <a name="d3dx11preprocessshaderfromresource-function"></a>D3DX11PreprocessShaderFromResource-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, empfiehlt es sich, die [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) -API zu verwenden.

 

Erstellen Sie einen Shader aus einer Ressource, ohne ihn zu kompilieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HMODULE* \[ in\]
</dt> <dd>

Typ: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**

Handle für das Ressourcen Modul, das den Shader enthält. HMODULE kann mit der [GetModuleHandle-Funktion](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)abgerufen werden.

</dd> <dt>

*presourcename* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Der Name der Ressource in Side HMODULE, die den Shader enthält. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Datentyp in LPCSTR aufgelöst.

</dd> <dt>

*psrcfilename* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Optional. Der Effekt Dateiname, der nur für Fehlermeldungen verwendet wird. Kann **null** sein.

</dd> <dt>

*pdefinitionen* \[ in\]
</dt> <dd>

Type: **Konstanten D3D11 \_ Shader- \_ Makro \***

Ein mit Null endendes Array von Shader-Makros. Legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.

</dd> <dt>

*pinclude* \[ in\]
</dt> <dd>

Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Ein Zeiger auf eine include-Schnittstelle. Legen Sie dies auf **null** fest, um anzugeben, dass keine Includedatei vorhanden ist.

</dd> <dt>

*ppump* \[ in\]
</dt> <dd>

Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)). Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.

</dd> <dt>

*ppshadertext* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Ein Zeiger auf den Arbeitsspeicher, der den nicht kompilierten Shader enthält.

</dd> <dt>

*pperrormsgs* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Die Adresse eines Zeigers auf den Arbeitsspeicher, der Fehler bei der Fehler Erstellung enthält (sofern vorhanden).

</dd> <dt>

*phresult* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann **null** sein. Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11async. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Bibliothek d3dx11. lib</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

