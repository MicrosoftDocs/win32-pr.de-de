---
description: Verwenden von komprimierten Texturen (Direct3D 9)
ms.assetid: 60892a8b-93f4-43ba-87ef-d5c7cc6fb8c6
title: Verwenden von komprimierten Texturen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 643b0618043f12ff3e1a84b806c86edb780ad929
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747601"
---
# <a name="using-compressed-textures-direct3d-9"></a><span data-ttu-id="5d3b1-103">Verwenden von komprimierten Texturen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5d3b1-103">Using Compressed Textures (Direct3D 9)</span></span>

## <a name="determining-support-for-compressed-textures"></a><span data-ttu-id="5d3b1-104">Festlegen der Unterstützung für komprimierte Texturen</span><span class="sxs-lookup"><span data-stu-id="5d3b1-104">Determining Support for Compressed Textures</span></span>

<span data-ttu-id="5d3b1-105">Wenn Sie den Adapter testen möchten, geben Sie ein beliebiges Pixel Format an, das DXT1, DXT2, DXT3, DXT4 oder DXT5 verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-105">To test the adapter, specify any pixel format that uses the DXT1, DXT2, DXT3, DXT4, or DXT5.</span></span> <span data-ttu-id="5d3b1-106">Wenn [**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) D3D OK zurückgibt \_ , kann das Gerät Textur direkt aus einer komprimierten Textur Oberfläche erstellen, die das Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-106">If [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) returns D3D\_OK, the device can create texture directly from a compressed texture surface that uses that format.</span></span> <span data-ttu-id="5d3b1-107">Wenn dies der Fall ist, können Sie komprimierte Textur Oberflächen direkt mit Direct3D verwenden, indem Sie die [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-107">If so, you can use compressed texture surfaces directly with Direct3D by calling the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span> <span data-ttu-id="5d3b1-108">Im folgenden Codebeispiel wird veranschaulicht, wie bestimmt wird, ob der Adapter ein komprimiertes Textur Format unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-108">The following code example shows how to determine if the adapter supports a compressed texture format.</span></span>


```
BOOL IsCompressedTextureFormatOk( D3DFORMAT TextureFormat, 
                                  D3DFORMAT AdapterFormat ) 
{
    HRESULT hr = pD3D->CheckDeviceFormat( D3DADAPTER_DEFAULT,
                                          D3DDEVTYPE_HAL,
                                          AdapterFormat,
                                          0,
                                          D3DRTYPE_TEXTURE,
                                          TextureFormat);

    return SUCCEEDED( hr );
}
```



<span data-ttu-id="5d3b1-109">Wenn das Gerät Texturierung von komprimierten Textur Oberflächen nicht unterstützt, können Sie Textur Daten trotzdem in einer komprimierten Formatierungs Oberfläche speichern, aber Sie müssen alle komprimierten Texturen in ein unterstütztes Format konvertieren, bevor Sie für die Texturierung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-109">If the device does not support texturing from compressed texture surfaces, you can still store texture data in a compressed format surface, but you must convert any compressed textures to a supported format before they can be used for texturing.</span></span>

## <a name="creating-compressed-textures"></a><span data-ttu-id="5d3b1-110">Erstellen komprimierter Texturen</span><span class="sxs-lookup"><span data-stu-id="5d3b1-110">Creating Compressed Textures</span></span>

<span data-ttu-id="5d3b1-111">Nachdem Sie ein Gerät erstellt haben, das ein komprimiertes Textur Format auf dem Adapter unterstützt, können Sie eine komprimierte Textur Ressource erstellen.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-111">After creating a device that supports a compressed texture format on the adapter, you can create a compressed texture resource.</span></span> <span data-ttu-id="5d3b1-112">Aufrufen von [**IDirect3DDevice9:: kreatetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) und Angeben eines komprimierten Textur Formats für den Format-Parameter.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-112">Call [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) and specify a compressed texture format for the Format parameter.</span></span>

<span data-ttu-id="5d3b1-113">Bevor Sie ein Bild in ein Textur Objekt laden, rufen Sie einen Zeiger auf die Textur Oberfläche ab, indem Sie die [**IDirect3DTexture9:: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-113">Before loading an image into a texture object, retrieve a pointer to the texture surface by calling the [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) method.</span></span>

<span data-ttu-id="5d3b1-114">Nun können Sie eine beliebige D3DXLoadSurfacexxx-Funktion verwenden, um ein Bild auf die-Oberfläche zu laden, die mit [**IDirect3DTexture9:: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-114">Now you can use any D3DXLoadSurfacexxx function to load an image to the surface that was retrieved by using [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel).</span></span> <span data-ttu-id="5d3b1-115">Diese Funktionen behandeln die Konvertierung in und aus komprimierten Textur Formaten.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-115">These functions handle conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="5d3b1-116">Sie können komprimierte Textur Dateien (DDS) mit dem DirectX-Textur-Editor (Dxtex.exe) erstellen und konvertieren, der mit dem DirectX SDK bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-116">You can create and convert compressed texture (DDS) files using the DirectX Texture Editor (Dxtex.exe) supplied with the DirectX SDK.</span></span> <span data-ttu-id="5d3b1-117">Sie erhalten Dxtex.exe und erfahren mehr über das DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-117">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="5d3b1-118">Weitere Informationen zum DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="5d3b1-118">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="5d3b1-119">Der Vorteil dieses Verhaltens besteht darin, dass eine Anwendung den Inhalt einer komprimierten Oberfläche in eine Datei kopieren kann, ohne zu berechnen, wie viel Speicher für eine Oberfläche einer bestimmten Breite und Höhe im jeweiligen Format erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-119">The advantage of this behavior is that an application can copy the contents of a compressed surface to a file without calculating how much storage is required for a surface of a particular width and height in the specific format.</span></span>

<span data-ttu-id="5d3b1-120">In der folgenden Tabelle sind die fünf Typen komprimierter Texturen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-120">The following table shows the five types of compressed textures.</span></span> <span data-ttu-id="5d3b1-121">Weitere Informationen zum Speichern der Daten finden Sie unter [komprimierte Textur Formate (Direct3D 9)](compressed-texture-formats.md).</span><span class="sxs-lookup"><span data-stu-id="5d3b1-121">For more information about how the data is stored, see [Compressed Texture Formats (Direct3D 9)](compressed-texture-formats.md).</span></span> <span data-ttu-id="5d3b1-122">Diese Informationen sind nur erforderlich, wenn Sie eigene Komprimierungs Routinen schreiben.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-122">You only need this information if you are writing your own compression routines.</span></span>



| <span data-ttu-id="5d3b1-123">FOURCC</span><span class="sxs-lookup"><span data-stu-id="5d3b1-123">FOURCC</span></span> | <span data-ttu-id="5d3b1-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d3b1-124">Description</span></span>        | <span data-ttu-id="5d3b1-125">Alpha in der Vorschau?</span><span class="sxs-lookup"><span data-stu-id="5d3b1-125">Alpha premultiplied?</span></span> |
|--------|--------------------|----------------------|
| <span data-ttu-id="5d3b1-126">DXT1</span><span class="sxs-lookup"><span data-stu-id="5d3b1-126">DXT1</span></span>   | <span data-ttu-id="5d3b1-127">Undurchsichtiges/1-Bit-Alpha</span><span class="sxs-lookup"><span data-stu-id="5d3b1-127">Opaque/1-bit alpha</span></span> | <span data-ttu-id="5d3b1-128">–</span><span class="sxs-lookup"><span data-stu-id="5d3b1-128">N/A</span></span>                  |
| <span data-ttu-id="5d3b1-129">DXT2</span><span class="sxs-lookup"><span data-stu-id="5d3b1-129">DXT2</span></span>   | <span data-ttu-id="5d3b1-130">Explizites Alpha</span><span class="sxs-lookup"><span data-stu-id="5d3b1-130">Explicit alpha</span></span>     | <span data-ttu-id="5d3b1-131">Ja</span><span class="sxs-lookup"><span data-stu-id="5d3b1-131">Yes</span></span>                  |
| <span data-ttu-id="5d3b1-132">DXT3</span><span class="sxs-lookup"><span data-stu-id="5d3b1-132">DXT3</span></span>   | <span data-ttu-id="5d3b1-133">Explizites Alpha</span><span class="sxs-lookup"><span data-stu-id="5d3b1-133">Explicit alpha</span></span>     | <span data-ttu-id="5d3b1-134">Nein</span><span class="sxs-lookup"><span data-stu-id="5d3b1-134">No</span></span>                   |
| <span data-ttu-id="5d3b1-135">DXT4</span><span class="sxs-lookup"><span data-stu-id="5d3b1-135">DXT4</span></span>   | <span data-ttu-id="5d3b1-136">Interpoliert Alpha</span><span class="sxs-lookup"><span data-stu-id="5d3b1-136">Interpolated alpha</span></span> | <span data-ttu-id="5d3b1-137">Ja</span><span class="sxs-lookup"><span data-stu-id="5d3b1-137">Yes</span></span>                  |
| <span data-ttu-id="5d3b1-138">DXT5</span><span class="sxs-lookup"><span data-stu-id="5d3b1-138">DXT5</span></span>   | <span data-ttu-id="5d3b1-139">Interpoliert Alpha</span><span class="sxs-lookup"><span data-stu-id="5d3b1-139">Interpolated alpha</span></span> | <span data-ttu-id="5d3b1-140">Nein</span><span class="sxs-lookup"><span data-stu-id="5d3b1-140">No</span></span>                   |



 

<span data-ttu-id="5d3b1-141">Wenn Sie Daten aus einem nicht vorab multiplizierten Format in ein vorab multipliziertes Format übertragen, skaliert Direct3D die Farben auf der Grundlage der Alpha Werte.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-141">When you transfer data from a nonpremultiplied format to a premultiplied format, Direct3D scales the colors based on the alpha values.</span></span> <span data-ttu-id="5d3b1-142">Das Übertragen von Daten aus einem prämultiplizierten Format in ein nicht vorab multipliziertes Format wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-142">Transferring data from a premultiplied format to a nonpremultiplied format is not supported.</span></span> <span data-ttu-id="5d3b1-143">Wenn Sie versuchen, Daten aus einer vorab multiplizierten Alpha Quelle in ein nicht prämultipliziertes Alpha Ziel zu übertragen, gibt die Methode D3DERR \_ invalidcallzurück.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-143">If you try to transfer data from a premultiplied alpha source to a nonpremultiplied alpha destination, the method returns D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="5d3b1-144">Wenn Sie Daten aus einer vormultiplizierten Alpha Quelle an ein Ziel mit keinem Alpha übertragen, werden die Quell Farbkomponenten, die durch Alpha skaliert wurden, unverändert kopiert.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-144">If you transfer data from a premultiplied alpha source to a destination that has no alpha, the source color components, which have been scaled by alpha, are copied as is.</span></span>

## <a name="decompressing-compressed-texture-surfaces"></a><span data-ttu-id="5d3b1-145">Komprimieren komprimierter Textur Oberflächen</span><span class="sxs-lookup"><span data-stu-id="5d3b1-145">Decompressing Compressed Texture Surfaces</span></span>

<span data-ttu-id="5d3b1-146">Wie beim Komprimieren einer Textur Oberfläche wird die Komprimierung einer komprimierten Textur über Direct3D-Kopierdienste durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-146">As with compressing a texture surface, decompressing a compressed texture is performed through Direct3D copying services.</span></span>

<span data-ttu-id="5d3b1-147">Um eine komprimierte Textur Oberfläche in eine nicht komprimierte Textur Oberfläche zu kopieren, verwenden Sie die [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)-Funktion.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-147">To copy a compressed texture surface to a uncompressed texture surface, use the function [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md).</span></span> <span data-ttu-id="5d3b1-148">Diese Funktionen verarbeiten die Komprimierung zu und von komprimierten und unkomprimierten Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="5d3b1-148">This functions handles compression to and from compressed and uncompressed surfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d3b1-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5d3b1-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d3b1-150">Komprimierte Textur Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5d3b1-150">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 
