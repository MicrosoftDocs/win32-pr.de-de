---
title: D3DX11CreateShaderResourceViewFromResource-Funktion (D3DX11tex.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Hinweis Anstelle dieser Funktion wird empfohlen, Ressourcenfunktionen zu verwenden, dann diese DirectXTK-Bibliothek (Runtime), CreateXXXTextureFromMemory (wobei XXX DDS oder WIC ist)DirectXTex-Bibliothek (Tools), LoadFromXXXMemory (wobei XXX für WIC, DDS oder TGA steht; WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Art-Source-Format für Spiele) und anschließend CreateShaderResourceView Erstellen einer Shader-Ressourcenansicht aus einer Ressource.
ms.assetid: 64620e6d-fc0d-4411-8744-d9d8ffe6ccb8
keywords:
- D3DX11CreateShaderResourceViewFromResource-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60eb6cf54dc32b3bb860b9ef963101428cc0cc2a7e4dacd1a24781c604b2ea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124725"
---
# <a name="d3dx11createshaderresourceviewfromresource-function"></a>D3DX11CreateShaderResourceViewFromResource-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, empfiehlt es sich, [Ressourcenfunktionen und](/windows/desktop/menurc/resources-functions)dann die folgenden zu verwenden:
>
> -   [DirectXTK-Bibliothek](https://github.com/Microsoft/DirectXTK) (Runtime), **CreateXXXTextureFromMemory** (wobei XXX DDS oder WIC ist)
> -   [DirectXTex-Bibliothek](https://github.com/Microsoft/DirectXTex) (Tools), **LoadFromXXXMemory** (wobei XXX WIC, DDS oder TGA ist; WIC unterstützt DDS und TGA nicht. Von D3DX 9 unterstützte TGA als gängiges Art Source-Format für Spiele) und **anschließend CreateShaderResourceView**

 

Erstellen Sie eine Shader-Ressourcenansicht aus einer Ressource.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11CreateShaderResourceViewFromResource(
  _In_  ID3D11Device             *pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Ein Zeiger auf das Gerät (siehe [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)), das die Ressource verwendet.

</dd> <dt>

*hSrcModule* \[ In\]
</dt> <dd>

Typ: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**

Handle für das Ressourcenmodul, das die Shader-Ressourcenansicht enthält. HMODULE kann mit der [GetModuleHandle-Funktion erhalten werden.](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)

</dd> <dt>

*pSrcResource* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Name der Shaderressourcenansicht in hSrcModule. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Datentyp in LPCSTR auflösen.

</dd> <dt>

*pLoadInfo* \[ In\]
</dt> <dd>

Typ: **[ **D3DX11 \_ \_ \_ BILDLADEINFORMATIONEN**](d3dx11-image-load-info.md)\***

Optional. Identifiziert die Merkmale einer Textur (siehe [**D3DX11 \_ IMAGE \_ LOAD \_ INFO),**](d3dx11-image-load-info.md)wenn der Datenprozessor erstellt wird. Legen Sie diese auf **NULL** fest, um die Merkmale einer Textur zu lesen, wenn die Textur geladen wird.

</dd> <dt>

*pPump* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Ein Zeiger auf eine Threadpumpschnittstelle (siehe [**ID3DX11ThreadPump-Schnittstelle**](id3dx11threadpump.md)). Wenn **NULL** angegeben wird, verhält sich diese Funktion synchron und gibt erst dann zurück, wenn sie abgeschlossen ist.

</dd> <dt>

*ppShaderResourceView* \[ out\]
</dt> <dd>

Typ: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***

Adresse eines Zeigers auf die Shaderressourcenansicht (siehe [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann NULL **sein.** Wenn *pPump* nicht **NULL ist,** muss *pHResult* ein gültiger Speicherort sein, bis die asynchrone Ausführung abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die unter [Direct3D 11-Rückgabecodes aufgeführt sind.](d3d11-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

