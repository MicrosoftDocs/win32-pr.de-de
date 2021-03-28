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
# <a name="d3dx11_image_file_format-enumeration"></a><span data-ttu-id="2e3f2-106">Bibliothek d3dx11 \_ Image \_ file \_ Format-Enumeration</span><span class="sxs-lookup"><span data-stu-id="2e3f2-106">D3DX11\_IMAGE\_FILE\_FORMAT enumeration</span></span>

> [!Note]  
> <span data-ttu-id="2e3f2-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="2e3f2-108">Bild Dateiformate, die von den Funktionen D3DX11Createxxx und D3DX11Savexxx unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-108">Image file formats supported by D3DX11Createxxx and D3DX11Savexxx functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e3f2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e3f2-109">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="2e3f2-110">Konstanten</span><span class="sxs-lookup"><span data-stu-id="2e3f2-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2e3f2-111"><span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**Bibliothek d3dx11 \_ IFF- \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="2e3f2-111"><span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11\_IFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="2e3f2-112">Windows-Bitmap-Dateiformat (BMP).</span><span class="sxs-lookup"><span data-stu-id="2e3f2-112">Windows bitmap (BMP) file format.</span></span> <span data-ttu-id="2e3f2-113">Enthält einen Header, der die Auflösung des Geräts, auf dem das Rechteck von Pixeln erstellt wurde, die Abmessungen des Rechtecks, die Größe des Bits-Arrays, eine logische Palette und ein Array von Bits beschreibt, das die Beziehung zwischen Pixeln im bitzugeordneten Bild und Einträgen in der logischen Palette definiert.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-113">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> <span data-ttu-id="2e3f2-114">Die Dateierweiterung für dieses Format ist BMP.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-114">The file extension for this format is .bmp.</span></span>

</dd> <dt>

<span data-ttu-id="2e3f2-115"><span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**Bibliothek d3dx11 \_ IFF \_ JPG**</span><span class="sxs-lookup"><span data-stu-id="2e3f2-115"><span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11\_IFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="2e3f2-116">Joint Photographic Experts Group (JPEG) komprimiertes Dateiformat.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-116">Joint Photographic Experts Group (JPEG) compressed file format.</span></span> <span data-ttu-id="2e3f2-117">Gibt die Variablen Komprimierung von 24-Bit-RGB-Farb-und 8-Bit-Bilddokument Dateien mit Graustufen Tagged Image File Format (TIFF) an.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-117">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span> <span data-ttu-id="2e3f2-118">Die Dateierweiterung für dieses Format ist. jpg.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-118">The file extension for this format is .jpg.</span></span>

</dd> <dt>

<span data-ttu-id="2e3f2-119"><span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**Bibliothek d3dx11 \_ IFF \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="2e3f2-119"><span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**D3DX11\_IFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="2e3f2-120">Das Dateiformat Portable Network Graphics (PNG).</span><span class="sxs-lookup"><span data-stu-id="2e3f2-120">Portable Network Graphics (PNG) file format.</span></span> <span data-ttu-id="2e3f2-121">Ein nicht proprietäres Bitmap-Format, das die Verlust lose Komprimierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-121">A non-proprietary bitmap format using lossless compression.</span></span> <span data-ttu-id="2e3f2-122">Die Dateierweiterung für dieses Format ist PNG.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-122">The file extension for this format is .png.</span></span>

</dd> <dt>

<span data-ttu-id="2e3f2-123"><span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**Bibliothek d3dx11 \_ IFF- \_ DDS**</span><span class="sxs-lookup"><span data-stu-id="2e3f2-123"><span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11\_IFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="2e3f2-124">Das DDS-Dateiformat (DirectDraw Surface).</span><span class="sxs-lookup"><span data-stu-id="2e3f2-124">DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="2e3f2-125">Speichert Texturen, volumetexturen und kubische Umgebungs Zuordnungen mit oder ohne MipMap-Ebenen und mit oder ohne Pixel Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-125">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="2e3f2-126">Die Dateierweiterung für dieses Format lautet. DDS.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-126">The file extension for this format is .dds.</span></span>

</dd> <dt>

<span data-ttu-id="2e3f2-127"><span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**Bibliothek d3dx11 \_ IFF \_ TIFF**</span><span class="sxs-lookup"><span data-stu-id="2e3f2-127"><span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**D3DX11\_IFF\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="2e3f2-128">Tagged Image File Format (TIFF).</span><span class="sxs-lookup"><span data-stu-id="2e3f2-128">Tagged Image File Format (TIFF).</span></span> <span data-ttu-id="2e3f2-129">Die Dateierweiterungen für dieses Format sind. TIF und. TIFF.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-129">The file extensions for this format are .tif and .tiff.</span></span>

</dd> <dt>

<span data-ttu-id="2e3f2-130"><span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**Bibliothek d3dx11 \_ IFF- \_ GIF**</span><span class="sxs-lookup"><span data-stu-id="2e3f2-130"><span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**D3DX11\_IFF\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="2e3f2-131">Graphics Interchange Format (GIF).</span><span class="sxs-lookup"><span data-stu-id="2e3f2-131">Graphics Interchange Format (GIF).</span></span> <span data-ttu-id="2e3f2-132">Die Dateierweiterung für dieses Format ist GIF.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-132">The file extension for this format is .gif.</span></span>

</dd> <dt>

<span data-ttu-id="2e3f2-133"><span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**Bibliothek d3dx11 \_ IFF- \_ WMP**</span><span class="sxs-lookup"><span data-stu-id="2e3f2-133"><span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11\_IFF\_WMP**</span></span>
</dt> <dd>

<span data-ttu-id="2e3f2-134">Windows Media Photo Format (WMP).</span><span class="sxs-lookup"><span data-stu-id="2e3f2-134">Windows Media Photo format (WMP).</span></span> <span data-ttu-id="2e3f2-135">Dieses Format wird auch als HD-Foto und JPEG XR bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-135">This format is also known as HD Photo and JPEG XR.</span></span> <span data-ttu-id="2e3f2-136">Die Dateierweiterungen für dieses Format sind. HDP,. jxr und. WDP.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-136">The file extensions for this format are .hdp, .jxr, and .wdp.</span></span>

<span data-ttu-id="2e3f2-137">Um ordnungsgemäß zu funktionieren, erfordert **Bibliothek d3dx11 \_ IFF \_ WMP** , dass Sie com initialisieren.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-137">To work properly, **D3DX11\_IFF\_WMP** requires that you initialize COM.</span></span> <span data-ttu-id="2e3f2-138">Daher müssen Sie [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) oder [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) in Ihrer Anwendung aufrufen, bevor Sie D3DX aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-138">Therefore, call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) in your application before you call D3DX.</span></span>

</dd> <dt>

<span data-ttu-id="2e3f2-139"><span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**Bibliothek d3dx11 \_ IFF \_ \_ DWORD erzwingen**</span><span class="sxs-lookup"><span data-stu-id="2e3f2-139"><span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11\_IFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="2e3f2-140">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-140">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="2e3f2-141">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-141">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="2e3f2-142">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e3f2-142">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e3f2-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e3f2-143">Remarks</span></span>

<span data-ttu-id="2e3f2-144">Weitere Informationen zu einigen dieser Formate finden Sie unter [Bitmaps-Typen (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .</span><span class="sxs-lookup"><span data-stu-id="2e3f2-144">See [Types of Bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e3f2-145">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2e3f2-145">Requirements</span></span>



| <span data-ttu-id="2e3f2-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e3f2-146">Requirement</span></span> | <span data-ttu-id="2e3f2-147">Wert</span><span class="sxs-lookup"><span data-stu-id="2e3f2-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e3f2-148">Header</span><span class="sxs-lookup"><span data-stu-id="2e3f2-148">Header</span></span><br/> | <dl> <span data-ttu-id="2e3f2-149"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e3f2-149"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e3f2-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2e3f2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e3f2-151">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="2e3f2-151">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

