---
title: D3DX11CreateShaderResourceViewFromMemory-Funktion (D3DX11tex.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Hinweis Anstelle dieser Funktion wird empfohlen, diese DirectXTK-Bibliothek (Runtime), CreateXXXTextureFromMemory (wobei XXX DDS oder WIC ist)DirectXTex-Bibliothek (Tools), LoadFromXXXMemory (wobei XXX für WIC, DDS oder TGA steht) zu verwenden. WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützt TGA als gängiges Art Source-Format für Spiele) und anschließend CreateShaderResourceView Erstellen sie eine Shader-Ressourcenansicht aus einer Datei im Arbeitsspeicher.
ms.assetid: fd75b187-2c9c-403c-8327-c312c4cda238
keywords:
- D3DX11CreateShaderResourceViewFromMemory-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a8d242885fc09ee513f5107298f1bac98b5cb9cb684de0f6e85e960fb9c7078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124735"
---
# <a name="d3dx11createshaderresourceviewfrommemory-function"></a>D3DX11CreateShaderResourceViewFromMemory-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, empfiehlt es sich, diese zu verwenden:
>
> -   [DirectXTK-Bibliothek](https://github.com/Microsoft/DirectXTK) (Runtime), **CreateXXXTextureFromMemory** (wobei XXX DDS oder WIC ist)
> -   [DirectXTex-Bibliothek](https://github.com/Microsoft/DirectXTex) (Tools), **LoadFromXXXMemory** (wobei XXX WIC, DDS oder TGA ist; WIC unterstützt DDS und TGA nicht. Von D3DX 9 unterstützte TGA als gängiges Art Source-Format für Spiele) und **anschließend CreateShaderResourceView**

 

Erstellen Sie eine Shaderressourcenansicht aus einer Datei im Arbeitsspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11CreateShaderResourceViewFromMemory(
  _In_  ID3D11Device             *pDevice,
  _In_  LPCVOID                  pSrcData,
  _In_  SIZE_T                   SrcDataSize,
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

*pSrcData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

Zeiger auf die Datei im Arbeitsspeicher, die die Shaderressourcenansicht enthält.

</dd> <dt>

*SrcDataSize* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Größe der Datei im Arbeitsspeicher.

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

Adresse eines Zeigers auf die neu erstellte Shaderressourcenansicht. Siehe [**ID3D11ShaderResourceView.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)

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

 

