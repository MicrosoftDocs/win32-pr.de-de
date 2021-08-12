---
description: Bilddateiformate, die von den Funktionen D3DXCreatexxx und D3DX10Savexxx unterstützt werden.
ms.assetid: 39602f3c-5c91-4667-96d0-c3bdba712d88
title: D3DX10_IMAGE_FILE_FORMAT-Enumeration (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_FILE_FORMAT
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 597f929a2a5f2800b1761fdba377f2ed022460e7585e1a9d0131d3e6e21127e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303495"
---
# <a name="d3dx10_image_file_format-enumeration"></a>D3DX10 \_ IMAGE \_ FILE \_ FORMAT-Enumeration

Bilddateiformate, die von den Funktionen D3DXCreatexxx und D3DX10Savexxx unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_IMAGE_FILE_FORMAT { 
  D3DX10_IFF_BMP          = 0,
  D3DX10_IFF_JPG          = 1,
  D3DX10_IFF_PNG          = 3,
  D3DX10_IFF_DDS          = 4,
  D3DX10_IFF_TIFF         = 10,
  D3DX10_IFF_GIF          = 11,
  D3DX10_IFF_WMP          = 12,
  D3DX10_IFF_FORCE_DWORD  = 0x7fffffff
} D3DX10_IMAGE_FILE_FORMAT, *LPD3DX10_IMAGE_FILE_FORMAT;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10 \_ IFF \_ BMP**
</dt> <dd>

Windows Bitmapdateiformat (BMP). Enthält einen Header, der die Auflösung des Geräts beschreibt, auf dem das Pixelrechteck erstellt wurde, die Abmessungen des Rechtecks, die Größe des Arrays von Bits, eine logische Palette und ein Array von Bits, das die Beziehung zwischen Pixeln im Bitmapbild und Einträgen in der logischen Palette definiert. Die Dateierweiterung für dieses Format ist .bmp.

</dd> <dt>

<span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10 \_ IFF \_ JPG**
</dt> <dd>

Joint Photographic Experts Group (JPEG) komprimiertes Dateiformat. Gibt die variable Komprimierung von 24-Bit-RGB-Farb- und 8-Bit-TIFF-Bilddokumentdateien (Gray Scale Tagged Image File Format) an. Die Dateierweiterung für dieses Format ist .jpg.

</dd> <dt>

<span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3DX10 \_ IFF \_ PNG**
</dt> <dd>

png-Dateiformat (Portable Network Graphics). Ein nicht proprietäres Bitmapformat mit verlustfreier Komprimierung. Die Dateierweiterung für dieses Format ist .png.

</dd> <dt>

<span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10 \_ IFF \_ DDS**
</dt> <dd>

DDS-Dateiformat (DirectDraw Surface). Speichert Texturen, Volumentexturen und kubische Umgebungskarten mit oder ohne Mipmapebenen und mit oder ohne Pixelkomprimierung. Die Dateierweiterung für dieses Format lautet .dds.

</dd> <dt>

<span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**D3DX10 \_ IFF \_ TIFF**
</dt> <dd>

Tagged Image File Format (TIFF). Die Dateierweiterungen für dieses Format sind .tif und .tiff.

</dd> <dt>

<span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**D3DX10 \_ IFF \_ GIF**
</dt> <dd>

Graphics Interchange Format (GIF). Die Dateierweiterung für dieses Format ist .gif.

</dd> <dt>

<span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10 \_ IFF \_ WMP**
</dt> <dd>

Windows Medienfotoformat (Media Photo Format, WMP). Dieses Format wird auch als HD Photo und JPEG XR bezeichnet. Die Dateierweiterungen für dieses Format sind .hdp, .jxr und .wdp.

Damit **D3DX10 \_ IFF \_ WMP** ordnungsgemäß funktioniert, müssen Sie COM initialisieren. Rufen Sie daher [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) oder [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in Ihrer Anwendung auf, bevor Sie D3DX aufrufen.

</dd> <dt>

<span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10 \_ IFF \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration in eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Weitere Informationen zu einigen dieser Formate finden Sie unter [Bitmaptypen (GDI+).](../gdiplus/-gdiplus-types-of-bitmaps-about.md)

D3DX10 verwendet die Windows Imaging Component, um den Großteil der unterstützten Bitmapdateitypen zu implementieren. Weitere Informationen finden [Sie unter Übersicht über Windows Imaging Component.](https://msdn.microsoft.com/library/ms737408.aspx)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 
