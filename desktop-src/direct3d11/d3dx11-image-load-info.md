---
title: D3DX11_IMAGE_LOAD_INFO-Struktur (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Stellen Sie optional Informationen für Textur Lade-APIs bereit, um zu steuern, wie Texturen geladen werden. | D3DX11_IMAGE_LOAD_INFO-Struktur (D3DX11tex. h)
ms.assetid: 6cd2f590-4e15-41e6-9f04-cd91eeb082db
keywords:
- D3DX11_IMAGE_LOAD_INFO Struktur Direct3D 11
- LPD3DX11_IMAGE_LOAD_INFO Struktur Zeiger Direct3D 11
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
ms.openlocfilehash: 2905d135a515f4ef90557ac74c35665623462439
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982556"
---
# <a name="d3dx11_image_load_info-structure"></a>Bibliothek d3dx11 \_ Image \_ Load \_ Info-Struktur

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Stellen Sie optional Informationen für Textur Lade-APIs bereit, um zu steuern, wie Texturen geladen werden. Der Wert Bibliothek d3dx11 \_ Default für einen dieser Parameter bewirkt, dass D3DX automatisch den Wert aus der Quelldatei verwendet.

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

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Ziel Breite der Textur. Wenn die tatsächliche Breite der Textur größer oder kleiner als dieser Wert ist, wird die Textur zentral hoch-oder herunterskaliert, um dieser Ziel Breite gerecht zu werden.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Zielhöhe der Textur. Wenn die tatsächliche Höhe der Textur größer oder kleiner als dieser Wert ist, wird die Textur zentral hoch-oder herunterskaliert, um an diese Zielhöhe angepasst zu werden.

</dd> <dt>

**Tiefe**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Tiefe der Textur. Dies gilt nur für Volumentexturen.

</dd> <dt>

**Firstmiplevel**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die höchste Auflösung der MipMap-Ebene der Textur. Wenn dieser Wert größer als 0 ist, wird firstmiplevel nach dem Laden der Textur der MipMap-Ebene 0 zugeordnet.

</dd> <dt>

**MipLevels**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die maximale Anzahl von MipMap-Ebenen in der Textur. Weitere Informationen finden Sie in den Hinweisen unter [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). Die Verwendung von 0 oder Bibliothek d3dx11 \_ default bewirkt, dass eine vollständige MipMap-Kette erstellt wird.

</dd> <dt>

**Verwendung**
</dt> <dd>

Type: **[ **D3D11 \_ Usage**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**

</dd> <dd>

Die Art und Weise, in der die Textur Ressource verwendet werden soll. Siehe [**D3D11 \_ Usage**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).

</dd> <dt>

**BindFlags**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Pipeline Stufen, an die die Textur gebunden werden darf. Siehe [**D3D11 \_ Bind- \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).

</dd> <dt>

**CpuAccessFlags**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Zugriffsberechtigungen der CPU für die Textur Ressource. Siehe [**D3D11 \_ CPU \_ - \_ Zugriffsflag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).

</dd> <dt>

**Fehlflags**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Verschiedene Ressourcen Eigenschaften (siehe [**D3D11 \_ Resource \_ misc- \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).

</dd> <dt>

**Format**
</dt> <dd>

Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Eine [**DXGI- \_ formatenumeration**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , die das Format angibt, in dem sich die Textur befindet, nachdem Sie geladen wurde.

</dd> <dt>

**Filter**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filtert die Textur mithilfe des angegebenen Filters (nur beim erneuten Sampling). Siehe [**Bibliothek d3dx11 \_ Filter- \_ Flag**](d3dx11-filter-flag.md).

</dd> <dt>

**MipFilter**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filtert die Textur-MIP-Ebenen mithilfe des angegebenen Filters (nur beim Erzeugen von Mipmaps). Gültige Werte sind Bibliothek d3dx11 \_ Filter \_ None, Bibliothek d3dx11 \_ Filter \_ Point, Bibliothek d3dx11 \_ Filter \_ linear oder Bibliothek d3dx11 \_ Filter \_ Dreieck. Siehe [**Bibliothek d3dx11 \_ Filter- \_ Flag**](d3dx11-filter-flag.md).

</dd> <dt>

**psrcinfo**
</dt> <dd>

Type: **[ **Bibliothek d3dx11 \_ Image \_ Info**](d3dx11-image-info.md)\***

</dd> <dd>

Informationen zum ursprünglichen Image. Siehe [**Bibliothek d3dx11 \_ Image \_ Info**](d3dx11-image-info.md). Kann mit [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)oder [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md)abgerufen werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie die Struktur initialisieren, können Sie ein beliebiges Element auf Bibliothek d3dx11 default festlegen, \_ und D3DX initialisiert es mit einem Standardwert aus der Quell Textur, wenn die Textur geladen wird.

Diese Struktur kann von APIs verwendet werden, die folgende Aktionen ausführen:

-   Erstellen Sie Ressourcen, z. b. [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) und [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).
-   Erstellen Sie Datenprozessoren, z. b. [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) oder [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).

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



Im folgenden finden Sie ein kurzes Beispiel, in dem diese Struktur verwendet wird, um beim Laden einer Textur das Pixel Format bereitzustellen. Den gesamten Code finden Sie unter HDRFormats10. cpp in [HDRToneMappingCS11 Sample](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).


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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

