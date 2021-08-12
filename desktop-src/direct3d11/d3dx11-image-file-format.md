---
title: D3DX11_IMAGE_FILE_FORMAT -Enumeration (D3DX11tex.h)
description: 'Hinweis: Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Bilddateiformate, die von den Funktionen D3DX11Createxxx und D3DX11Savexxx unterstützt werden.'
ms.assetid: 89fa9ab8-3be0-4dc5-a533-94edb01df36a
keywords:
- D3DX11_IMAGE_FILE_FORMAT-Enumeration Direct3D 11
- LPD3DX11_IMAGE_FILE_FORMAT-Enumerationszeiger Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_FILE_FORMAT
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e34d3ab49987d499114c4b9eee695bfad02055fbbef785a955407e97843208f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536964"
---
# <a name="d3dx11_image_file_format-enumeration"></a>D3DX11 \_ IMAGE \_ FILE \_ FORMAT-Enumeration

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Bilddateiformate, die von den Funktionen D3DX11Createxxx und D3DX11Savexxx unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX11_IMAGE_FILE_FORMAT { 
  D3DX11_IFF_BMP          = 0,
  D3DX11_IFF_JPG          = 1,
  D3DX11_IFF_PNG          = 3,
  D3DX11_IFF_DDS          = 4,
  D3DX11_IFF_TIFF         = 10,
  D3DX11_IFF_GIF          = 11,
  D3DX11_IFF_WMP          = 12,
  D3DX11_IFF_FORCE_DWORD  = 0x7fffffff
} D3DX11_IMAGE_FILE_FORMAT, *LPD3DX11_IMAGE_FILE_FORMAT;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11 \_ IFF \_ BMP**
</dt> <dd>

Windows BMP-Dateiformat (Bitmap). Enthält einen Header, der die Auflösung des Geräts beschreibt, auf dem das Pixelrechteck erstellt wurde, die Abmessungen des Rechtecks, die Größe des Bitsarrays, eine logische Palette und ein Array von Bits, das die Beziehung zwischen Pixeln im Bitmapbild und Einträgen in der logischen Palette definiert. Die Dateierweiterung für dieses Format ist .bmp.

</dd> <dt>

<span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11 \_ IFF \_ JPG**
</dt> <dd>

Joint Photographic Experts Group komprimiertes Dateiformat (JPEG). Gibt die variable Komprimierung von 24-Bit-RGB-Farben und TIFF-Bilddokumentdateien (8-Bit Gray-Scale Tagged Image File Format) an. Die Dateierweiterung für dieses Format ist .jpg.

</dd> <dt>

<span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**D3DX11 \_ IFF \_ PNG**
</dt> <dd>

Portable Network Graphics -Dateiformat (PNG). Ein nicht proprietäres Bitmapformat mit verlustfreier Komprimierung. Die Dateierweiterung für dieses Format ist .png.

</dd> <dt>

<span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11 \_ IFF \_ DDS**
</dt> <dd>

DDS-Dateiformat (DirectDraw Surface). Speichert Texturen, Volumentexturen und kubische Umgebungszuordnungen mit oder ohne Mipmapebenen und mit oder ohne Pixelkomprimierung. Die Dateierweiterung für dieses Format ist .dds.

</dd> <dt>

<span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**D3DX11 \_ IFF \_ TIFF**
</dt> <dd>

Tagged Image File Format (TIFF). Die Dateierweiterungen für dieses Format sind TIF und TIFF.

</dd> <dt>

<span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**D3DX11 \_ IFF \_ GIF**
</dt> <dd>

Graphics Interchange Format (GIF). Die Dateierweiterung für dieses Format ist .gif.

</dd> <dt>

<span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11 \_ IFF \_ WMP**
</dt> <dd>

Windows Medienfotoformat (WMP). Dieses Format wird auch als HD-Foto und JPEG XR bezeichnet. Die Dateierweiterungen für dieses Format sind HDP, JXR und WDP.

Damit **D3DX11 \_ IFF \_ WMP** ordnungsgemäß funktioniert, müssen Sie COM initialisieren. Rufen Sie [**daher CoInitialize oder**](/windows/desktop/api/objbase/nf-objbase-coinitialize) [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) in Ihrer Anwendung auf, bevor Sie D3DX aufrufen.

</dd> <dt>

<span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11 \_ IFF \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration auf eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Unter [Bitmaptypen (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) finden Sie weitere Informationen zu einigen dieser Formate.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[D3DX-Enumerationen](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

