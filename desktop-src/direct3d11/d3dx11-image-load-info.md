---
title: D3DX11_IMAGE_LOAD_INFO -Struktur (D3DX11tex.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Stellen Sie optional Informationen für Texturlader-APIs zur Verfügung, um zu steuern, wie Texturen geladen werden. | D3DX11_IMAGE_LOAD_INFO -Struktur (D3DX11tex.h)
ms.assetid: 6cd2f590-4e15-41e6-9f04-cd91eeb082db
keywords:
- D3DX11_IMAGE_LOAD_INFO-Struktur Direct3D 11
- LPD3DX11_IMAGE_LOAD_INFO Strukturzeiger Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45bc3b9ec948c869b121190f52435a257141f1e5a6e9f36c347ab29bafb5522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536857"
---
# <a name="d3dx11_image_load_info-structure"></a>D3DX11 \_ IMAGE \_ LOAD \_ INFO-Struktur

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Stellen Sie optional Informationen für Texturlader-APIs zur Verfügung, um zu steuern, wie Texturen geladen werden. Der Wert D3DX11 DEFAULT für einen dieser Parameter führt dazu, dass D3DX automatisch den Wert \_ aus der Quelldatei verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DX11_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D11_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX11_IMAGE_INFO *pSrcInfo;
} D3DX11_IMAGE_LOAD_INFO, *LPD3DX11_IMAGE_LOAD_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Width**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Zielbreite der Textur. Wenn die tatsächliche Breite der Textur größer oder kleiner als dieser Wert ist, wird die Textur hoch- oder herunterskaliert, um diese Zielbreite zu erreichen.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Zielhöhe der Textur. Wenn die tatsächliche Höhe der Textur größer oder kleiner als dieser Wert ist, wird die Textur hoch- oder herunterskaliert, um diese Zielhöhe zu erreichen.

</dd> <dt>

**Tiefe**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Tiefe der Textur. Dies gilt nur für Volumetexturen.

</dd> <dt>

**FirstMipLevel**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die mipmap-Ebene mit der höchsten Auflösung der Textur. Wenn dieser Wert größer als 0 ist, wird FirstMipLevel nach dem Laden der Textur der Mipmap-Ebene 0 zugeordnet.

</dd> <dt>

**MipLevels**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die maximale Anzahl von Mipmapebenen in der Textur. Weitere Informationen finden Sie unter [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). Wenn Sie 0 oder D3DX11 DEFAULT verwenden, wird \_ eine vollständige Mipmapkette erstellt.

</dd> <dt>

**Verwendung**
</dt> <dd>

Typ: **[ **D3D11 \_ USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**

</dd> <dd>

Die Art und Weise, wie die Texturressource verwendet werden soll. Weitere Informationen [**finden Sie unter D3D11 \_ USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).

</dd> <dt>

**BindFlags**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Pipelinestufen, an die die Textur gebunden werden darf. Weitere Informationen [**finden Sie unter D3D11-BINDUNGSFLAG. \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)

</dd> <dt>

**CpuAccessFlags**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Zugriffsberechtigungen, über die die CPU für die Texturressource verfügt. Weitere Informationen [**finden Sie unter D3D11 \_ CPU ACCESS \_ \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).

</dd> <dt>

**MiscFlags**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Verschiedene Ressourceneigenschaften (siehe [**D3D11 \_ RESOURCE \_ MISC \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).

</dd> <dt>

**Format**
</dt> <dd>

Typ: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Eine [**DXGI \_ FORMAT-Enumeration,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) die das Format angibt, in dem sich die Textur befindet, nachdem sie geladen wurde.

</dd> <dt>

**Filter**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filtern Sie die Textur mithilfe des angegebenen Filters (nur beim Resampling). Weitere Informationen [**finden Sie unter D3DX11 \_ FILTER \_ FLAG**](d3dx11-filter-flag.md).

</dd> <dt>

**MipFilter**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filtern Sie die Textur-Mip-Ebenen mithilfe des angegebenen Filters (nur, wenn Mipmaps generiert werden). Gültige Werte sind D3DX11 \_ FILTER \_ NONE, D3DX11 \_ FILTER \_ POINT, D3DX11 \_ FILTER LINEAR oder \_ D3DX11 \_ FILTER \_ TRIANGLE. Weitere Informationen [**finden Sie unter D3DX11 \_ FILTER \_ FLAG**](d3dx11-filter-flag.md).

</dd> <dt>

**pSrcInfo**
</dt> <dd>

Typ: **[ **D3DX11 \_ IMAGE \_ INFO**](d3dx11-image-info.md)\***

</dd> <dd>

Informationen zum ursprünglichen Bild. Siehe [**D3DX11 \_ IMAGE \_ INFO**](d3dx11-image-info.md). Kann mit [**D3DX11GetImageInfoFromFile,**](d3dx11getimageinfofromfile.md) [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)oder [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md)ermittelt werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beim Initialisieren der Struktur können Sie jeden Member auf D3DX11 DEFAULT festlegen, und D3DX initialisiert ihn mit einem Standardwert aus der Quelltextur, wenn die Textur \_ geladen wird.

Diese Struktur kann von APIs verwendet werden, die:

-   Erstellen Sie Ressourcen wie [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) und [**D3DX11CreateShaderResourceViewFromFile.**](d3dx11createshaderresourceviewfromfile.md)
-   Erstellen Sie Datenprozessoren wie [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) oder [**D3DX11CreateAsyncShaderResourceViewProcessor.**](d3dx11createasyncshaderresourceviewprocessor.md)

Die Standardwerte lauten wie folgt:


```
    Width = D3DX11_DEFAULT;
    Height = D3DX11_DEFAULT;
    Depth = D3DX11_DEFAULT;
    FirstMipLevel = D3DX11_DEFAULT;
    MipLevels = D3DX11_DEFAULT;
    Usage = (D3D11_USAGE) D3DX11_DEFAULT;
    BindFlags = D3DX11_DEFAULT;
    CpuAccessFlags = D3DX11_DEFAULT;
    MiscFlags = D3DX11_DEFAULT;
    Format = DXGI_FORMAT_FROM_FILE;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
    pSrcInfo = NULL;
```



Hier ist ein kurzes Beispiel, in dem diese -Struktur verwendet wird, um das Pixelformat beim Laden einer Textur zu verwenden. Den vollständigen Code finden Sie unter HDRFormats10.cpp im [HDRToneMappingCS11-Beispiel.](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx)


```
ID3D11ShaderResourceView* pCubeRV = NULL;
WCHAR strPath[MAX_PATH];
D3DX11_IMAGE_LOAD_INFO LoadInfo;

    DXUTFindDXSDKMediaFileCch( strPath, MAX_PATH, 
        L"Light Probes\\uffizi_cross.dds" );

    LoadInfo.Format = DXGI_FORMAT_R16G16B16A16_FLOAT;

    hr = D3DX11CreateShaderResourceViewFromFile( pd3dDevice, strPath, 
        &LoadInfo, NULL, &pCubeRV, NULL );
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

