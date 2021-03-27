---
title: D3DX11SaveTextureToMemory-Funktion (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie anstelle dieser Funktion, dass Sie die directxtex-Bibliothek, capturetexture und savetoxxxmemory (xxx ist WIC, DDS oder TGA) verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele). Speichert eine Textur im Speicher.
ms.assetid: 3b54d8e1-6474-48fd-8348-a3baac406101
keywords:
- D3DX11SaveTextureToMemory-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4718f32f8d8288f83b30e3d742ebbe619421dc48
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219626"
---
# <a name="d3dx11savetexturetomemory-function"></a>D3DX11SaveTextureToMemory-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, empfiehlt es sich, dass Sie die [directxtex](https://github.com/Microsoft/DirectXTex) -Bibliothek **capturetexture** , dann **savetoxxxmemory** (xxx ist WIC, DDS oder TGA) verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele).

 

Speichert eine Textur im Speicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11SaveTextureToMemory(
        ID3D11DeviceContext      *pContext,
  _In_  ID3D11Resource           *pSrcTexture,
  _In_  D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContext* 
</dt> <dd>

Typ: **[ **Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Ein Zeiger auf ein [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Objekt.

</dd> <dt>

*psrctexture* \[ in\]
</dt> <dd>

Typ: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Zeiger auf die zu speichernde Textur. Siehe [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> <dt>

*Destformat* \[ in\]
</dt> <dd>

Type: **[ **Bibliothek d3dx11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md)**

Das Format, in dem die Textur gespeichert wird. Siehe [**Bibliothek d3dx11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md).

</dd> <dt>

*ppdestbuf* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***

Adresse eines Zeigers auf den Speicher, der die gespeicherte Textur enthält.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Optional.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Bibliothek d3dx11. lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

