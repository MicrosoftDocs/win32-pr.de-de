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
# <a name="d3dx10_image_file_format-enumeration"></a><span data-ttu-id="3084e-103">D3dx10 \_ Image \_ file \_ Format-Enumeration</span><span class="sxs-lookup"><span data-stu-id="3084e-103">D3DX10\_IMAGE\_FILE\_FORMAT enumeration</span></span>

<span data-ttu-id="3084e-104">Bild Dateiformate, die von den Funktionen D3DXCreatexxx und D3DX10Savexxx unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3084e-104">Image file formats supported by D3DXCreatexxx and D3DX10Savexxx functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="3084e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3084e-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="3084e-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="3084e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3084e-107"><span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3dx10 \_ IFF- \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="3084e-107"><span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10\_IFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="3084e-108">Windows-Bitmap-Dateiformat (BMP).</span><span class="sxs-lookup"><span data-stu-id="3084e-108">Windows bitmap (BMP) file format.</span></span> <span data-ttu-id="3084e-109">Enthält einen Header, der die Auflösung des Geräts, auf dem das Rechteck von Pixeln erstellt wurde, die Abmessungen des Rechtecks, die Größe des Bits-Arrays, eine logische Palette und ein Array von Bits beschreibt, das die Beziehung zwischen Pixeln im bitzugeordneten Bild und Einträgen in der logischen Palette definiert.</span><span class="sxs-lookup"><span data-stu-id="3084e-109">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> <span data-ttu-id="3084e-110">Die Dateierweiterung für dieses Format ist BMP.</span><span class="sxs-lookup"><span data-stu-id="3084e-110">The file extension for this format is .bmp.</span></span>

</dd> <dt>

<span data-ttu-id="3084e-111"><span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3dx10 \_ IFF \_ JPG**</span><span class="sxs-lookup"><span data-stu-id="3084e-111"><span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10\_IFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="3084e-112">Joint Photographic Experts Group (JPEG) komprimiertes Dateiformat.</span><span class="sxs-lookup"><span data-stu-id="3084e-112">Joint Photographic Experts Group (JPEG) compressed file format.</span></span> <span data-ttu-id="3084e-113">Gibt die Variablen Komprimierung von 24-Bit-RGB-Farb-und 8-Bit-Bilddokument Dateien mit Graustufen Tagged Image File Format (TIFF) an.</span><span class="sxs-lookup"><span data-stu-id="3084e-113">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span> <span data-ttu-id="3084e-114">Die Dateierweiterung für dieses Format ist. jpg.</span><span class="sxs-lookup"><span data-stu-id="3084e-114">The file extension for this format is .jpg.</span></span>

</dd> <dt>

<span data-ttu-id="3084e-115"><span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3dx10 \_ IFF \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="3084e-115"><span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3DX10\_IFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="3084e-116">Das Dateiformat Portable Network Graphics (PNG).</span><span class="sxs-lookup"><span data-stu-id="3084e-116">Portable Network Graphics (PNG) file format.</span></span> <span data-ttu-id="3084e-117">Ein nicht proprietäres Bitmap-Format, das die Verlust lose Komprimierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="3084e-117">A non-proprietary bitmap format using lossless compression.</span></span> <span data-ttu-id="3084e-118">Die Dateierweiterung für dieses Format ist PNG.</span><span class="sxs-lookup"><span data-stu-id="3084e-118">The file extension for this format is .png.</span></span>

</dd> <dt>

<span data-ttu-id="3084e-119"><span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3dx10 \_ IFF- \_ DDS**</span><span class="sxs-lookup"><span data-stu-id="3084e-119"><span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10\_IFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="3084e-120">Das DDS-Dateiformat (DirectDraw Surface).</span><span class="sxs-lookup"><span data-stu-id="3084e-120">DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="3084e-121">Speichert Texturen, volumetexturen und kubische Umgebungs Zuordnungen mit oder ohne MipMap-Ebenen und mit oder ohne Pixel Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="3084e-121">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="3084e-122">Die Dateierweiterung für dieses Format lautet. DDS.</span><span class="sxs-lookup"><span data-stu-id="3084e-122">The file extension for this format is .dds.</span></span>

</dd> <dt>

<span data-ttu-id="3084e-123"><span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**D3dx10 \_ IFF \_ TIFF**</span><span class="sxs-lookup"><span data-stu-id="3084e-123"><span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**D3DX10\_IFF\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="3084e-124">Tagged Image File Format (TIFF).</span><span class="sxs-lookup"><span data-stu-id="3084e-124">Tagged Image File Format (TIFF).</span></span> <span data-ttu-id="3084e-125">Die Dateierweiterungen für dieses Format sind. TIF und. TIFF.</span><span class="sxs-lookup"><span data-stu-id="3084e-125">The file extensions for this format are .tif and .tiff.</span></span>

</dd> <dt>

<span data-ttu-id="3084e-126"><span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**D3dx10 \_ IFF- \_ GIF**</span><span class="sxs-lookup"><span data-stu-id="3084e-126"><span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**D3DX10\_IFF\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="3084e-127">Graphics Interchange Format (GIF). Die Dateierweiterung für dieses Format ist GIF.</span><span class="sxs-lookup"><span data-stu-id="3084e-127">Graphics Interchange Format (GIF).The file extension for this format is .gif.</span></span>

</dd> <dt>

<span data-ttu-id="3084e-128"><span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3dx10 \_ IFF- \_ WMP**</span><span class="sxs-lookup"><span data-stu-id="3084e-128"><span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10\_IFF\_WMP**</span></span>
</dt> <dd>

<span data-ttu-id="3084e-129">Windows Media Photo Format (WMP).</span><span class="sxs-lookup"><span data-stu-id="3084e-129">Windows Media Photo format (WMP).</span></span> <span data-ttu-id="3084e-130">Dieses Format wird auch als HD-Foto und JPEG XR bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3084e-130">This format is also known as HD Photo and JPEG XR.</span></span> <span data-ttu-id="3084e-131">Die Dateierweiterungen für dieses Format sind. HDP,. jxr und. WDP.</span><span class="sxs-lookup"><span data-stu-id="3084e-131">The file extensions for this format are .hdp, .jxr, and .wdp.</span></span>

<span data-ttu-id="3084e-132">Um ordnungsgemäß zu funktionieren, erfordert **d3dx10 \_ IFF \_ WMP** , dass Sie com initialisieren.</span><span class="sxs-lookup"><span data-stu-id="3084e-132">To work properly, **D3DX10\_IFF\_WMP** requires that you initialize COM.</span></span> <span data-ttu-id="3084e-133">Daher müssen Sie [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) oder [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in Ihrer Anwendung aufrufen, bevor Sie D3DX aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3084e-133">Therefore, call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in your application before you call D3DX.</span></span>

</dd> <dt>

<span data-ttu-id="3084e-134"><span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3dx10 \_ IFF \_ \_ DWORD erzwingen**</span><span class="sxs-lookup"><span data-stu-id="3084e-134"><span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10\_IFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="3084e-135">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="3084e-135">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="3084e-136">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="3084e-136">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="3084e-137">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3084e-137">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3084e-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3084e-138">Remarks</span></span>

<span data-ttu-id="3084e-139">Weitere Informationen zu einigen dieser Formate finden Sie unter [Bitmaps-Typen (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .</span><span class="sxs-lookup"><span data-stu-id="3084e-139">See [Types of Bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

<span data-ttu-id="3084e-140">D3dx10 verwendet die Windows-Abbild Erstellungs Komponente, um die Mehrzahl der unterstützten bitmapdateitypen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="3084e-140">D3DX10 makes use of the Windows Imaging Component to implement the majority of the supported bitmap file types.</span></span> <span data-ttu-id="3084e-141">Weitere Informationen finden Sie unter [Übersicht über die Windows Imaging-Komponente](https://msdn.microsoft.com/library/ms737408.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3084e-141">See [Windows Imaging Component Overview](https://msdn.microsoft.com/library/ms737408.aspx) for additional information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3084e-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3084e-142">Requirements</span></span>



| <span data-ttu-id="3084e-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3084e-143">Requirement</span></span> | <span data-ttu-id="3084e-144">Wert</span><span class="sxs-lookup"><span data-stu-id="3084e-144">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3084e-145">Header</span><span class="sxs-lookup"><span data-stu-id="3084e-145">Header</span></span><br/> | <dl> <span data-ttu-id="3084e-146"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="3084e-146"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3084e-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3084e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3084e-148">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="3084e-148">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 
