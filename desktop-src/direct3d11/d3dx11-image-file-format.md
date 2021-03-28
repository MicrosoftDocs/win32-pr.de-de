---
title: D3DX11_IMAGE_FILE_FORMAT-Enumeration (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Bild Dateiformate, die von den Funktionen D3DX11Createxxx und D3DX11Savexxx unterstützt werden.
ms.assetid: 89fa9ab8-3be0-4dc5-a533-94edb01df36a
keywords:
- D3DX11_IMAGE_FILE_FORMAT-Enumeration Direct3D 11
- LPD3DX11_IMAGE_FILE_FORMAT enumerationszeiger Direct3D 11
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
ms.openlocfilehash: 730ce59bb8a07f3fd8ef78bbeb27b4d01d198f7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982572"
---
# <a name="d3dx11_image_file_format-enumeration"></a>Bibliothek d3dx11 \_ Image \_ file \_ Format-Enumeration

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Bild Dateiformate, die von den Funktionen D3DX11Createxxx und D3DX11Savexxx unterstützt werden.

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

<span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**Bibliothek d3dx11 \_ IFF- \_ BMP**
</dt> <dd>

Windows-Bitmap-Dateiformat (BMP). Enthält einen Header, der die Auflösung des Geräts, auf dem das Rechteck von Pixeln erstellt wurde, die Abmessungen des Rechtecks, die Größe des Bits-Arrays, eine logische Palette und ein Array von Bits beschreibt, das die Beziehung zwischen Pixeln im bitzugeordneten Bild und Einträgen in der logischen Palette definiert. Die Dateierweiterung für dieses Format ist BMP.

</dd> <dt>

<span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**Bibliothek d3dx11 \_ IFF \_ JPG**
</dt> <dd>

Joint Photographic Experts Group (JPEG) komprimiertes Dateiformat. Gibt die Variablen Komprimierung von 24-Bit-RGB-Farb-und 8-Bit-Bilddokument Dateien mit Graustufen Tagged Image File Format (TIFF) an. Die Dateierweiterung für dieses Format ist. jpg.

</dd> <dt>

<span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**Bibliothek d3dx11 \_ IFF \_ PNG**
</dt> <dd>

Das Dateiformat Portable Network Graphics (PNG). Ein nicht proprietäres Bitmap-Format, das die Verlust lose Komprimierung verwendet. Die Dateierweiterung für dieses Format ist PNG.

</dd> <dt>

<span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**Bibliothek d3dx11 \_ IFF- \_ DDS**
</dt> <dd>

Das DDS-Dateiformat (DirectDraw Surface). Speichert Texturen, volumetexturen und kubische Umgebungs Zuordnungen mit oder ohne MipMap-Ebenen und mit oder ohne Pixel Komprimierung. Die Dateierweiterung für dieses Format lautet. DDS.

</dd> <dt>

<span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**Bibliothek d3dx11 \_ IFF \_ TIFF**
</dt> <dd>

Tagged Image File Format (TIFF). Die Dateierweiterungen für dieses Format sind. TIF und. TIFF.

</dd> <dt>

<span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**Bibliothek d3dx11 \_ IFF- \_ GIF**
</dt> <dd>

Graphics Interchange Format (GIF). Die Dateierweiterung für dieses Format ist GIF.

</dd> <dt>

<span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**Bibliothek d3dx11 \_ IFF- \_ WMP**
</dt> <dd>

Windows Media Photo Format (WMP). Dieses Format wird auch als HD-Foto und JPEG XR bezeichnet. Die Dateierweiterungen für dieses Format sind. HDP,. jxr und. WDP.

Um ordnungsgemäß zu funktionieren, erfordert **Bibliothek d3dx11 \_ IFF \_ WMP** , dass Sie com initialisieren. Daher müssen Sie [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) oder [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) in Ihrer Anwendung aufrufen, bevor Sie D3DX aufrufen.

</dd> <dt>

<span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**Bibliothek d3dx11 \_ IFF \_ \_ DWORD erzwingen**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu einigen dieser Formate finden Sie unter [Bitmaps-Typen (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

