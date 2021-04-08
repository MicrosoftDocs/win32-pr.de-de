---
description: Bild Dateiformate, die von den Funktionen D3DXCreatexxx und D3DX10Savexxx unterstützt werden.
ms.assetid: 39602f3c-5c91-4667-96d0-c3bdba712d88
title: D3DX10_IMAGE_FILE_FORMAT-Enumeration (D3DX10Tex. h)
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
ms.openlocfilehash: fba878a40f510cc5e76256161255e01deaa7ee04
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762261"
---
# <a name="d3dx10_image_file_format-enumeration"></a>D3dx10 \_ Image \_ file \_ Format-Enumeration

Bild Dateiformate, die von den Funktionen D3DXCreatexxx und D3DX10Savexxx unterstützt werden.

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

<span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3dx10 \_ IFF- \_ BMP**
</dt> <dd>

Windows-Bitmap-Dateiformat (BMP). Enthält einen Header, der die Auflösung des Geräts, auf dem das Rechteck von Pixeln erstellt wurde, die Abmessungen des Rechtecks, die Größe des Bits-Arrays, eine logische Palette und ein Array von Bits beschreibt, das die Beziehung zwischen Pixeln im bitzugeordneten Bild und Einträgen in der logischen Palette definiert. Die Dateierweiterung für dieses Format ist BMP.

</dd> <dt>

<span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3dx10 \_ IFF \_ JPG**
</dt> <dd>

Joint Photographic Experts Group (JPEG) komprimiertes Dateiformat. Gibt die Variablen Komprimierung von 24-Bit-RGB-Farb-und 8-Bit-Bilddokument Dateien mit Graustufen Tagged Image File Format (TIFF) an. Die Dateierweiterung für dieses Format ist. jpg.

</dd> <dt>

<span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3dx10 \_ IFF \_ PNG**
</dt> <dd>

Das Dateiformat Portable Network Graphics (PNG). Ein nicht proprietäres Bitmap-Format, das die Verlust lose Komprimierung verwendet. Die Dateierweiterung für dieses Format ist PNG.

</dd> <dt>

<span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3dx10 \_ IFF- \_ DDS**
</dt> <dd>

Das DDS-Dateiformat (DirectDraw Surface). Speichert Texturen, volumetexturen und kubische Umgebungs Zuordnungen mit oder ohne MipMap-Ebenen und mit oder ohne Pixel Komprimierung. Die Dateierweiterung für dieses Format lautet. DDS.

</dd> <dt>

<span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**D3dx10 \_ IFF \_ TIFF**
</dt> <dd>

Tagged Image File Format (TIFF). Die Dateierweiterungen für dieses Format sind. TIF und. TIFF.

</dd> <dt>

<span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**D3dx10 \_ IFF- \_ GIF**
</dt> <dd>

Graphics Interchange Format (GIF). Die Dateierweiterung für dieses Format ist GIF.

</dd> <dt>

<span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3dx10 \_ IFF- \_ WMP**
</dt> <dd>

Windows Media Photo Format (WMP). Dieses Format wird auch als HD-Foto und JPEG XR bezeichnet. Die Dateierweiterungen für dieses Format sind. HDP,. jxr und. WDP.

Um ordnungsgemäß zu funktionieren, erfordert **d3dx10 \_ IFF \_ WMP** , dass Sie com initialisieren. Daher müssen Sie [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) oder [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in Ihrer Anwendung aufrufen, bevor Sie D3DX aufrufen.

</dd> <dt>

<span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3dx10 \_ IFF \_ \_ DWORD erzwingen**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu einigen dieser Formate finden Sie unter [Bitmaps-Typen (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .

D3dx10 verwendet die Windows-Abbild Erstellungs Komponente, um die Mehrzahl der unterstützten bitmapdateitypen zu implementieren. Weitere Informationen finden Sie unter [Übersicht über die Windows Imaging-Komponente](https://msdn.microsoft.com/library/ms737408.aspx) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 
