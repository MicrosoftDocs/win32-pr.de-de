---
title: D3DX11CreateTextureFromResource-Funktion (D3DX11.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Hinweis Anstelle dieser Funktion wird empfohlen, Ressourcenfunktionen zu verwenden, dann diese DirectXTK-Bibliothek (Runtime), CreateXXXTextureFromMemory (wobei XXX DDS oder WIC ist)DirectXTex-Bibliothek (Tools), LoadFromXXXMemory (wobei XXX für WIC, DDS oder TGA steht; WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützt TGA als gängiges Art Source-Format für Spiele) und anschließend CreateTexture Create a texture from another resource (Erstellen einer Textur aus einer anderen Ressource).
ms.assetid: 2b62239a-c19b-4d4f-9fd2-afcd87ba0fac
keywords:
- D3DX11CreateTextureFromResource-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 886e289905ba10be088cc1fdc21802a07051ae8f9ea65f6e8781644db2c42183
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124675"
---
# <a name="d3dx11createtexturefromresource-function"></a>D3DX11CreateTextureFromResource-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, empfiehlt es sich, [Ressourcenfunktionen und](/windows/desktop/menurc/resources-functions)dann die folgenden zu verwenden:
>
> -   [DirectXTK-Bibliothek](https://github.com/Microsoft/DirectXTK) (Runtime), **CreateXXXTextureFromMemory** (wobei XXX DDS oder WIC ist)
> -   [DirectXTex-Bibliothek](https://github.com/Microsoft/DirectXTex) (Tools), **LoadFromXXXMemory** (wobei XXX WIC, DDS oder TGA ist; WIC unterstützt DDS und TGA nicht. Von D3DX 9 unterstützte TGA als gängiges Art Source-Format für Spiele) und **anschließend CreateTexture**

 

Erstellen Sie eine Textur aus einer anderen Ressource.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11CreateTextureFromResource(
  _In_  ID3D11Device           *pDevice,
  _In_  HMODULE                hSrcModule,
  _In_  LPCTSTR                pSrcResource,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
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

Ein Handle für die Quellressource. HMODULE kann mit der [GetModuleHandle-Funktion erhalten werden.](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)

</dd> <dt>

*pSrcResource* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Eine Zeichenfolge, die den Namen der Quellressource enthält. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Datentyp in LPCSTR auflösen.

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

*ppTexture* \[ out\]
</dt> <dd>

Typ: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***

Die Adresse eines Zeigers auf die Texturressource (siehe [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)).

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
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

