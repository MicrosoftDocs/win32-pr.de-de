---
description: Eine Textur Ressource ist eine strukturierte Auflistung von Daten.
ms.assetid: 4c716be8-044e-4ed4-aeca-4379440826bd
title: Erstellen von Textur Ressourcen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f2ca200b566d17b02af56c48cb1227c41106ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958418"
---
# <a name="creating-texture-resources-direct3d-10"></a><span data-ttu-id="8254a-103">Erstellen von Textur Ressourcen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8254a-103">Creating Texture Resources (Direct3D 10)</span></span>

<span data-ttu-id="8254a-104">Eine [Textur](d3d10-graphics-programming-guide-resources-types.md) Ressource ist eine strukturierte Auflistung von Daten.</span><span class="sxs-lookup"><span data-stu-id="8254a-104">A [texture](d3d10-graphics-programming-guide-resources-types.md) resource is a structured collection of data.</span></span> <span data-ttu-id="8254a-105">Farbwerte werden in der Regel in Texturen gespeichert, und der Zugriff erfolgt während des Renderings durch die [Pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) in verschiedenen Phasen für Eingabe und Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="8254a-105">Typically, color values are stored in textures and accessed during rendering by the [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) at various stages for both input and output.</span></span> <span data-ttu-id="8254a-106">Das Erstellen von Texturen und deren Verwendung ist ein wichtiger Bestandteil des Renderings interessanter Szenen in Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="8254a-106">Creating textures and defining how they will be used is an important part of rendering interesting-looking scenes in Direct3D 10.</span></span>

<span data-ttu-id="8254a-107">Obwohl Texturen in der Regel Farbinformationen enthalten, ermöglicht das Erstellen von Texturen mit einem anderen [**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) es Ihnen, unterschiedliche Arten von Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8254a-107">Even though textures typically contain color information, creating textures using different [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enables them to store different kinds of data.</span></span> <span data-ttu-id="8254a-108">Diese Daten können dann von der Direct3D 10-Pipeline auf nicht herkömmliche Weise genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="8254a-108">This data can then be leveraged by the Direct3D 10 pipeline in non-traditional ways.</span></span>

<span data-ttu-id="8254a-109">Alle Texturen haben Beschränkungen hinsichtlich des genutzten Speichers und der Anzahl der darin enthaltenen texeln.</span><span class="sxs-lookup"><span data-stu-id="8254a-109">All textures have limits on how much memory they consume, and how many texels they contain.</span></span> <span data-ttu-id="8254a-110">Diese Grenzwerte werden von [Ressourcen Konstanten](d3d10-graphics-reference-resource-constants.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="8254a-110">These limits are specified by [resource constants](d3d10-graphics-reference-resource-constants.md).</span></span>

-   [<span data-ttu-id="8254a-111">Erstellen einer Textur aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="8254a-111">Create a Texture from a File</span></span>](#create-a-texture-from-a-file)
    -   [<span data-ttu-id="8254a-112">Separates Erstellen von Textur und Ansicht</span><span class="sxs-lookup"><span data-stu-id="8254a-112">Create Texture and View Separately</span></span>](#create-texture-and-view-separately)
    -   [<span data-ttu-id="8254a-113">Gleichzeitiges Erstellen von Textur und Ansicht</span><span class="sxs-lookup"><span data-stu-id="8254a-113">Create Texture and View Simultaneously</span></span>](#create-texture-and-view-simultaneously)
-   [<span data-ttu-id="8254a-114">Erstellen leerer Texturen</span><span class="sxs-lookup"><span data-stu-id="8254a-114">Creating Empty Textures</span></span>](#creating-empty-textures)
    -   [<span data-ttu-id="8254a-115">Rendering in eine Textur</span><span class="sxs-lookup"><span data-stu-id="8254a-115">Rendering to a texture</span></span>](#rendering-to-a-texture)
    -   [<span data-ttu-id="8254a-116">Manuelles Auffüllen von Texturen</span><span class="sxs-lookup"><span data-stu-id="8254a-116">Filling Textures Manually</span></span>](#filling-textures-manually)
-   [<span data-ttu-id="8254a-117">Mehrere Rendertargets</span><span class="sxs-lookup"><span data-stu-id="8254a-117">Multiple Rendertargets</span></span>](#multiple-rendertargets)
-   [<span data-ttu-id="8254a-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8254a-118">Related topics</span></span>](#related-topics)

## <a name="create-a-texture-from-a-file"></a><span data-ttu-id="8254a-119">Erstellen einer Textur aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="8254a-119">Create a Texture from a File</span></span>

> [!Note]  
> <span data-ttu-id="8254a-120">Die [D3DX Utility Library](d3d10-graphics-reference-d3dx10.md) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8254a-120">The [D3DX utility library](d3d10-graphics-reference-d3dx10.md) is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="8254a-121">Wenn Sie eine Textur in Direct3D 10 erstellen, müssen Sie auch eine [Ansicht](d3d10-graphics-programming-guide-resources-access-views.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="8254a-121">When you create a texture in Direct3D 10, you also need to create a [view](d3d10-graphics-programming-guide-resources-access-views.md).</span></span> <span data-ttu-id="8254a-122">Eine Sicht ist ein Objekt, das dem Gerät mitteilt, wie während des Renderings auf eine Textur zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8254a-122">A view is an object that tells the device how a texture should be accessed during rendering.</span></span> <span data-ttu-id="8254a-123">Die gängigste Methode, um auf eine Textur zuzugreifen, besteht darin, mithilfe eines [Shaders](../direct3dhlsl/dx-graphics-hlsl.md)aus ihr zu lesen.</span><span class="sxs-lookup"><span data-stu-id="8254a-123">The most common way to access a texture is to read from it using a [shader](../direct3dhlsl/dx-graphics-hlsl.md).</span></span> <span data-ttu-id="8254a-124">In einer Shader-Ressourcen Ansicht wird einem Shader mitgeteilt, wie während des Renderings aus einer Textur gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8254a-124">A shader-resource view will tell a shader how to read from a texture during rendering.</span></span> <span data-ttu-id="8254a-125">Die Art der Sicht, die von einer Textur verwendet wird, muss bei der Erstellung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8254a-125">The kind of view a texture will use must be specified when you create it.</span></span>

<span data-ttu-id="8254a-126">Das Erstellen einer Textur und das Laden der anfänglichen Daten kann auf zwei verschiedene Arten erfolgen: Erstellen Sie eine Textur und eine separate Ansicht, oder erstellen Sie die Textur und die Ansicht gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="8254a-126">Creating a texture and loading its initial data can be done in two different ways: create a texture and view separately, or create both the texture and the view at the same time.</span></span> <span data-ttu-id="8254a-127">Die API stellt beide Techniken bereit, sodass Sie auswählen können, welche für Ihre Anforderungen besser geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="8254a-127">The API provides both techniques so you can choose which better suits your needs.</span></span>

### <a name="create-texture-and-view-separately"></a><span data-ttu-id="8254a-128">Separates Erstellen von Textur und Ansicht</span><span class="sxs-lookup"><span data-stu-id="8254a-128">Create Texture and View Separately</span></span>

<span data-ttu-id="8254a-129">Die einfachste Möglichkeit zum Erstellen einer Textur besteht darin, Sie aus einer Bilddatei zu laden.</span><span class="sxs-lookup"><span data-stu-id="8254a-129">The easiest way to create a texture is to load it from an image file.</span></span> <span data-ttu-id="8254a-130">Um die Textur zu erstellen, füllen Sie einfach eine Struktur aus, und geben Sie den Namen der Textur an [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)an.</span><span class="sxs-lookup"><span data-stu-id="8254a-130">To create the texture, just fill in one structure and provide the texture's name to [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).</span></span>


```
ID3D10Device *pDevice = NULL;
// Initialize D3D10 device...

D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;

ID3D10Resource *pTexture = NULL;
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pTexture, NULL );
```



<span data-ttu-id="8254a-131">Die D3DX-Funktion [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) führt drei Dinge aus: zunächst erstellt Sie ein Direct3D 10-Textur Objekt. Zweitens wird die Eingabe Bilddatei gelesen. Drittens speichert Sie die Bilddaten im Textur Objekt.</span><span class="sxs-lookup"><span data-stu-id="8254a-131">The D3DX function [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) does three things: first, it creates a Direct3D 10 texture object; second, it reads the input image file; third, it stores the image data in the texture object.</span></span> <span data-ttu-id="8254a-132">Im obigen Beispiel wird eine BMP-Datei geladen, aber die Funktion kann eine Vielzahl von Dateitypen laden.</span><span class="sxs-lookup"><span data-stu-id="8254a-132">In the sample above, a BMP file is loaded, but the function can load a variety of file types.</span></span>

<span data-ttu-id="8254a-133">Das BIND-Flag gibt an, dass die Textur als Shaderressource erstellt wird, sodass eine Shader-Stufe während des Renderings aus der Textur gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="8254a-133">The bind flag indicates the texture will be created as a shader resource which allows a shader stage to read from the texture during rendering.</span></span>

<span data-ttu-id="8254a-134">Im obigen Beispiel werden nicht alle Lade Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="8254a-134">The above example does not specify all of the loading parameters.</span></span> <span data-ttu-id="8254a-135">In der Tat ist es häufig vorteilhaft, die Lade Parameter einfach Null auszuwerten, da dies D3DX die Auswahl geeigneter Werte basierend auf dem Eingabebild ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="8254a-135">In fact, it's often beneficial to simply zero out the loading parameters as this enables D3DX to choose appropriate values based on the input image.</span></span> <span data-ttu-id="8254a-136">Wenn das Eingabebild alle Parameter bestimmen soll, mit denen die Textur erstellt wird, geben Sie einfach **null** für den **loadinfo** -Parameter wie folgt an:</span><span class="sxs-lookup"><span data-stu-id="8254a-136">If you want the input image to determine all of the parameters the texture is created with, simply specify **NULL** for the **loadInfo** parameter like this:</span></span>


```
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", NULL, NULL, &pTexture, NULL );
```



<span data-ttu-id="8254a-137">Das Angeben von **null** für die ladeinformationen ist eine einfache, aber leistungsstarke Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="8254a-137">Specifying **NULL** for the loading information is a simple yet powerful shortcut.</span></span>

<span data-ttu-id="8254a-138">Nachdem Sie nun eine Textur erstellt haben, müssen Sie eine Shader-Ressourcen Ansicht erstellen, damit die Textur als Eingabe an einen Shader gebunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="8254a-138">Now that a texture has been created, you need to create a shader-resource view so that the texture can be bound as an input to a shader.</span></span> <span data-ttu-id="8254a-139">Da [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) einen Zeiger auf eine Ressource und keinen Zeiger auf eine Textur zurückgibt, müssen Sie den genauen Typ der Ressource ermitteln, die geladen wurde. Anschließend können Sie mithilfe von " [**kreateshaderresourceview**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview)" eine Shader-Ressourcen Ansicht erstellen.</span><span class="sxs-lookup"><span data-stu-id="8254a-139">Since [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) returns a pointer to a resource and not a pointer to a texture, you have to determine the exact type of resource that was loaded, and then you can create a shader-resource view using [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span></span>


```
D3D10_SHADER_RESOURCE_VIEW_DESC srvDesc;
D3D10_RESOURCE_DIMENSION type;
pTexture->GetType( &type );
switch( type )
{
    case D3D10_RESOURCE_DIMENSION_BUFFER:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE1D:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE2D:
    {
        D3D10_TEXTURE2D_DESC desc;
        ID3D10Texture2D *pTexture2D = (ID3D10Texture2D*)pTexture;
        pTexture2D->GetDesc( &desc );
        
        srvDesc.Format = desc.Format;
        srvDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Texture2D.MipLevels = desc.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = desc.MipLevels -1;

    }
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE3D:
    //...
    break;
    default:
    //...
    break;
}

ID3D10ShaderResourceView *pSRView = NULL;
pDevice->CreateShaderResourceView( pTexture, &srvDesc, &pSRView );
```



<span data-ttu-id="8254a-140">Obwohl das obige Beispiel eine 2D-Shader-Ressourcen Ansicht erstellt, ist der Code zum Erstellen anderer Shader-Resource-Ansichts Typen sehr ähnlich.</span><span class="sxs-lookup"><span data-stu-id="8254a-140">Although the above sample creates a 2D shader-resource view, the code to create other shader-resource view types is very similar.</span></span> <span data-ttu-id="8254a-141">Jede Shader-Stufe kann nun diese Textur als Eingabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="8254a-141">Any shader stage can now use this texture as an input.</span></span>

<span data-ttu-id="8254a-142">Die Verwendung von [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) und der Verwendung von " [**kreateshaderresourceview**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) " zum Erstellen einer Textur und der zugehörigen Ansicht ist eine Möglichkeit, eine Textur für die Bindung an eine Shader-Phase vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="8254a-142">Using [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) and [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) to create a texture and its associated view is one way to prepare a texture to be bound to a shader stage.</span></span> <span data-ttu-id="8254a-143">Eine andere Möglichkeit besteht darin, die Textur und ihre Ansicht gleichzeitig zu erstellen. Dies wird im nächsten Abschnitt erläutert.</span><span class="sxs-lookup"><span data-stu-id="8254a-143">Another way to do so is to create both the texture and its view at the same time, which is discussed in the next section.</span></span>

### <a name="create-texture-and-view-simultaneously"></a><span data-ttu-id="8254a-144">Gleichzeitiges Erstellen von Textur und Ansicht</span><span class="sxs-lookup"><span data-stu-id="8254a-144">Create Texture and View Simultaneously</span></span>

<span data-ttu-id="8254a-145">Direct3D 10 erfordert, dass sowohl eine Textur als auch eine Shader-Ressourcen Ansicht aus einer Textur während der Laufzeit gelesen werden muss.</span><span class="sxs-lookup"><span data-stu-id="8254a-145">Direct3D 10 requires both a texture and a shader-resource view to read from a texture during runtime.</span></span> <span data-ttu-id="8254a-146">Da die Erstellung einer Textur und einer Shader-Ressourcen Ansicht eine solche häufige Aufgabe ist, stellt D3DX die [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) bereit, um dies für Sie zu tun.</span><span class="sxs-lookup"><span data-stu-id="8254a-146">Since the creation of a texture and a shader-resource view is such a common task, D3DX provides the [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) to do it for you.</span></span>


```
D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;

ID3D10ShaderResourceView *pSRView = NULL;
D3DX10CreateShaderResourceViewFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pSRView, NULL );
```



<span data-ttu-id="8254a-147">Bei einem einzelnen D3DX-Befehl werden sowohl die Textur-als auch die Shader-Ressourcen Ansicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="8254a-147">With a single D3DX call, both the texture and shader-resource view are created.</span></span> <span data-ttu-id="8254a-148">Die Funktionalität des **loadinfo** -Parameters ist unverändert. Sie können damit anpassen, wie die Textur erstellt wird, oder die erforderlichen Parameter aus der Eingabedatei ableiten, indem Sie für den **loadinfo** -Parameter **null** angeben.</span><span class="sxs-lookup"><span data-stu-id="8254a-148">The functionality of the **loadInfo** parameter is unchanged; you can use it to customize how the texture is created, or derive the necessary parameters from the input file by specifying **NULL** for the **loadInfo** parameter.</span></span>

<span data-ttu-id="8254a-149">Das von der [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) -Funktion zurückgegebene [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) -Objekt kann später verwendet werden, um die ursprüngliche [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) -Schnittstelle abzurufen, wenn Sie benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="8254a-149">The [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) object returned by the [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) function can later be used to retrieve the original [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) interface if it is needed.</span></span> <span data-ttu-id="8254a-150">Dies kann durch Aufrufen der [**GetResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) -Methode erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="8254a-150">This can be done by calling the [**GetResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) method.</span></span>

<span data-ttu-id="8254a-151">D3DX bietet eine einzelne Funktion zum Erstellen einer Textur und einer Shader-Ressourcen Ansicht als über-und-Weise. Sie müssen entscheiden, welche Methode zum Erstellen einer Textur und Ansicht am besten den Anforderungen Ihrer Anwendung entspricht.</span><span class="sxs-lookup"><span data-stu-id="8254a-151">D3DX provides a single function to create a texture and shader-resource view as a convienience; it is up to you to decide which method of creating a texture and view best suits the needs of your application.</span></span>

<span data-ttu-id="8254a-152">Nachdem Sie nun wissen, wie eine Textur und die Shader-Ressourcen Ansicht erstellt werden, zeigt der nächste Abschnitt, wie Sie ein Beispiel (lesen) aus dieser Textur mithilfe eines Shaders erstellen können.</span><span class="sxs-lookup"><span data-stu-id="8254a-152">Now that you know how to create a texture and its shader-resource view, the next section will show you how you can sample (read) from that texture using a shader.</span></span>

## <a name="creating-empty-textures"></a><span data-ttu-id="8254a-153">Erstellen leerer Texturen</span><span class="sxs-lookup"><span data-stu-id="8254a-153">Creating Empty Textures</span></span>

<span data-ttu-id="8254a-154">Manchmal möchten Anwendungen eine Textur erstellen und die Daten berechnen, die in der Textur gespeichert werden sollen, oder die Grafik [Pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) verwenden, um diese Textur zu rendern und später die Ergebnisse in anderer Verarbeitung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8254a-154">Sometimes applications will want to create a texture and compute the data to be stored in the texture, or use the graphics [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) to render to this texture and later use the results in other processing.</span></span> <span data-ttu-id="8254a-155">Diese Texturen können von der Grafik Pipeline oder von der Anwendung selbst aktualisiert werden, je nachdem, welche Art von [**Verwendung**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) für die Textur bei der Erstellung angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8254a-155">These textures could be updated by the graphics pipeline or by the application itself, depending on what kind of [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) was specified for the texture when it was created.</span></span>

### <a name="rendering-to-a-texture"></a><span data-ttu-id="8254a-156">Rendering in eine Textur</span><span class="sxs-lookup"><span data-stu-id="8254a-156">Rendering to a texture</span></span>

<span data-ttu-id="8254a-157">Der häufigste Fall, eine leere Textur zu erstellen, die während der Laufzeit mit Daten aufgefüllt werden soll, ist der Fall, in dem eine Anwendung in eine Textur gerendert werden soll, und dann die Ergebnisse des Renderingvorgangs in einem nachfolgenden Durchlauf zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8254a-157">The most common case of creating an empty texture to be filled with data during runtime is the case where an application wants to render to a texture and then use the results of the rendering operation in a subsequent pass.</span></span> <span data-ttu-id="8254a-158">Mit diesem Zweck erstellte Texturen sollten die Standard [**Verwendung**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)angeben.</span><span class="sxs-lookup"><span data-stu-id="8254a-158">Textures created with this purpose should specify default [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span></span>

<span data-ttu-id="8254a-159">Im folgenden Codebeispiel wird eine leere Textur erstellt, die von der Pipeline zum Rendering und anschließend als Eingabe für einen [Shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md)verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8254a-159">The following code sample creates an empty texture that the pipeline can render to and subsequently use as an input to a [shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span></span>


```
// Create the render target texture
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = 1;
desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R32G32B32A32_FLOAT;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;

ID3D10Texture2D *pRenderTarget = NULL;
pDevice->CreateTexture2D( &desc, NULL, &pRenderTarget );
```



<span data-ttu-id="8254a-160">Das Erstellen der Textur erfordert, dass die Anwendung einige Informationen zu den Eigenschaften angibt, die die Textur enthalten wird.</span><span class="sxs-lookup"><span data-stu-id="8254a-160">Creating the texture requires the application to specify some information about the properties the texture will have.</span></span> <span data-ttu-id="8254a-161">Breite und Höhe der Textur in texeln werden auf 256 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8254a-161">The width and height of the texture in texels is set to 256.</span></span> <span data-ttu-id="8254a-162">Für dieses Renderziel ist nur eine einzelne MipMap-Ebene erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8254a-162">For this render target, a single mipmap level is all we need.</span></span> <span data-ttu-id="8254a-163">Es ist nur ein Renderziel erforderlich, damit die Array Größe auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8254a-163">Only one render target is required so the array size is set to 1.</span></span> <span data-ttu-id="8254a-164">Jedes Texttyp enthält 4 32-Bit-Gleit Komma Werte, die zum Speichern sehr präziser Informationen verwendet werden können (siehe [**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="8254a-164">Each texel contains four 32-bit floating point values, which can be used to store very precise information (see [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="8254a-165">Ein Beispiel pro Pixel ist alles, was benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="8254a-165">One sample per pixel is all that will be needed.</span></span> <span data-ttu-id="8254a-166">Die Verwendung wird auf Default festgelegt, da dies die effizienteste Platzierung des Renderziels im Arbeitsspeicher ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="8254a-166">The usage is set to default because this allows for the most efficient placement of the render target in memory.</span></span> <span data-ttu-id="8254a-167">Schließlich wird die Tatsache angegeben, dass die Textur als Renderziel und eine Shaderressource zu unterschiedlichen Zeitpunkten gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="8254a-167">Finally, the fact that the texture will be bound as a render target and a shader resource at different points in time is specified.</span></span>

<span data-ttu-id="8254a-168">Texturen können nicht direkt für das Rendering an die Pipeline gebunden werden. Verwenden Sie eine renderzielansicht, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8254a-168">Textures cannot be bound for rendering to the pipeline directly; use a render-target view as shown in the following code sample.</span></span>


```
D3D10_RENDER_TARGET_VIEW_DESC rtDesc;
rtDesc.Format = desc.Format;
rtDesc.ViewDimension = D3D10_RTV_DIMENSION_TEXTURE2D;
rtDesc.Texture2D.MipSlice = 0;

ID3D10RenderTargetView *pRenderTargetView = NULL;
pDevice->CreateRenderTargetView( pRenderTarget, &rtDesc, &pRenderTargetView );
```



<span data-ttu-id="8254a-169">Das Format der renderzielansicht wird einfach auf das Format der ursprünglichen Textur festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8254a-169">The format of the render-target view is simply set to the format of the original texture.</span></span> <span data-ttu-id="8254a-170">Die Informationen in der Ressource sollten als 2D-Textur interpretiert werden, und wir möchten nur die erste MipMap-Ebene des Renderziels verwenden.</span><span class="sxs-lookup"><span data-stu-id="8254a-170">The information in the resource should be interpreted as a 2D texture, and we only want to use the first mipmap level of the render target.</span></span>

<span data-ttu-id="8254a-171">Ähnlich wie eine renderzielansicht erstellt werden muss, damit das Renderziel für die Ausgabe an die Pipeline gebunden werden kann, muss eine Shader-Ressourcen Ansicht erstellt werden, sodass das Renderziel als Eingabe an die Pipeline gebunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="8254a-171">Similarly to how a render-target view must be created so that the render target can be bound for output to the pipeline, a shader-resource view must be created so that the render target can be bound to the pipeline as an input.</span></span> <span data-ttu-id="8254a-172">Dies wird im folgenden Codebeispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="8254a-172">The following code sample demonstrates this.</span></span>


```
// Create the shader-resource view
D3D10_SHADER_RESOURCE_VIEW_DESC srDesc;
srDesc.Format = desc.Format;
srDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
srDesc.Texture2D.MostDetailedMip = 0;
srDesc.Texture2D.MipLevels = 1;

ID3D10ShaderResourceView *pShaderResView = NULL;
pDevice->CreateShaderResourceView( pRenderTarget, &srDesc, &pShaderResView );
```



<span data-ttu-id="8254a-173">Die Parameter von Beschreibungen der Shader-Ressourcen Ansicht ähneln denen der Beschreibungen der renderzielsichten und wurden aus denselben Gründen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="8254a-173">The parameters of shader-resource view descriptions are very similar to those of render-target view descriptions and were chosen for the same reasons.</span></span>

### <a name="filling-textures-manually"></a><span data-ttu-id="8254a-174">Manuelles Auffüllen von Texturen</span><span class="sxs-lookup"><span data-stu-id="8254a-174">Filling Textures Manually</span></span>

<span data-ttu-id="8254a-175">Manchmal möchten Anwendungen Werte zur Laufzeit berechnen, Sie manuell in eine Textur einfügen und dann die Grafik [Pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) in späteren Renderingvorgängen verwenden.</span><span class="sxs-lookup"><span data-stu-id="8254a-175">Sometimes applications would like to compute values at runtime, put them into a texture manually and then have the graphics [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) use this texture in later rendering operations.</span></span> <span data-ttu-id="8254a-176">Hierzu muss die Anwendung eine leere Textur erstellen, damit die CPU auf den zugrunde liegenden Speicher zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="8254a-176">To do this, the application must create an empty texture in such a way to allow the CPU to access the underlying memory.</span></span> <span data-ttu-id="8254a-177">Dies erfolgt durch das Erstellen einer dynamischen Textur und das Erlangen des Zugriffs auf den zugrunde liegenden Speicher, indem eine bestimmte Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8254a-177">This is done by creating a dynamic texture and gaining access to the underlying memory by calling a particular method.</span></span> <span data-ttu-id="8254a-178">Die erforderliche Vorgehensweise wird im folgenden Codebeispiel veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="8254a-178">The following code sample demonstrates how to do this.</span></span>


```
D3D10_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DYNAMIC;
desc.BindFlags = D3D10_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
ID3D10Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



<span data-ttu-id="8254a-179">Beachten Sie, dass das Format auf 32 Bits pro Pixel festgelegt ist, wobei jede Komponente durch 8 Bits definiert wird.</span><span class="sxs-lookup"><span data-stu-id="8254a-179">Note that the format is set to a 32 bits per pixel where each component is defined by 8 bits.</span></span> <span data-ttu-id="8254a-180">Der Usage-Parameter ist auf Dynamic festgelegt, während die Bindungsflags festgelegt werden, um anzugeben, dass ein Shader auf die Textur zugreift.</span><span class="sxs-lookup"><span data-stu-id="8254a-180">The usage parameter is set to dynamic while the bind flags are set to specify the texture will be accessed by a shader.</span></span> <span data-ttu-id="8254a-181">Der Rest der Textur Beschreibung ähnelt der Erstellung eines Renderziels.</span><span class="sxs-lookup"><span data-stu-id="8254a-181">The rest of the texture description is similar to creating a render target.</span></span>

<span data-ttu-id="8254a-182">Durch Aufrufen von [**map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) kann die Anwendung auf den zugrunde liegenden Speicher der Textur zugreifen.</span><span class="sxs-lookup"><span data-stu-id="8254a-182">Calling [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) enables the application to access the underlying memory of the texture.</span></span> <span data-ttu-id="8254a-183">Der abgerufene Zeiger wird dann verwendet, um die Textur mit Daten zu füllen.</span><span class="sxs-lookup"><span data-stu-id="8254a-183">The pointer retrieved is then used to fill the texture with data.</span></span> <span data-ttu-id="8254a-184">Dies ist im folgenden Codebeispiel zu sehen.</span><span class="sxs-lookup"><span data-stu-id="8254a-184">This can be seen in the following code sample.</span></span>


```
D3D10_MAPPED_TEXTURE2D mappedTex;
pTexture->Map( D3D10CalcSubresource(0, 0, 1), D3D10_MAP_WRITE_DISCARD, 0, &mappedTex );

UCHAR* pTexels = (UCHAR*)mappedTex.pData;
for( UINT row = 0; row < desc.Height; row++ )
{
    UINT rowStart = row * mappedTex.RowPitch;
    for( UINT col = 0; col < desc.Width; col++ )
    {
        UINT colStart = col * 4;
        pTexels[rowStart + colStart + 0] = 255; // Red
        pTexels[rowStart + colStart + 1] = 128; // Green
        pTexels[rowStart + colStart + 2] = 64;  // Blue
        pTexels[rowStart + colStart + 3] = 32;  // Alpha
    }
}

pTexture->Unmap( D3D10CalcSubresource(0, 0, 1) );
```



## <a name="multiple-rendertargets"></a><span data-ttu-id="8254a-185">Mehrere Rendertargets</span><span class="sxs-lookup"><span data-stu-id="8254a-185">Multiple Rendertargets</span></span>

<span data-ttu-id="8254a-186">Bis zu acht renderzielsichten können gleichzeitig an die Pipeline gebunden werden (mit [**omantrendertargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)).</span><span class="sxs-lookup"><span data-stu-id="8254a-186">Up to eight render-target views can be bound to the pipeline at a time (with [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)).</span></span> <span data-ttu-id="8254a-187">Für jedes Pixel (oder jede Stichprobe, wenn multisamplinggrad aktiviert ist) erfolgt die Mischung unabhängig für jede renderzielansicht.</span><span class="sxs-lookup"><span data-stu-id="8254a-187">For each pixel (or each sample if multisampling is enabled), blending is done independently for each render-target view.</span></span> <span data-ttu-id="8254a-188">Zwei der Blend-Statusvariablen-blendenable und rendertargetschreitemask-sind Arrays von acht, wobei jedes Array Element einer renderzielansicht entspricht.</span><span class="sxs-lookup"><span data-stu-id="8254a-188">Two of the blend state variables - BlendEnable and RenderTargetWriteMask - are arrays of eight, each array member corresponds to a render-target view.</span></span> <span data-ttu-id="8254a-189">Wenn mehrere Renderziele verwendet werden, muss jedes Renderziel denselben [Ressourcentyp](d3d10-graphics-programming-guide-resources-types.md) aufweisen (Puffer, 1D-Textur, 2D-Textur Array usw.), und die gleiche Dimension (Breite, Höhe, Tiefe für 3D-Texturen und Array Größe für Textur Arrays) muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="8254a-189">When using multiple render targets, each render target must be the same [resource type](d3d10-graphics-programming-guide-resources-types.md) (buffer, 1D texture, 2D texture array, etc.) and must have the same dimension (width, height, depth for 3D textures, and array size for texture arrays).</span></span> <span data-ttu-id="8254a-190">Wenn die Renderziele Multisampling aufweisen, müssen Sie alle über die gleiche Anzahl von Stichproben pro Pixel verfügen.</span><span class="sxs-lookup"><span data-stu-id="8254a-190">If the render targets are multisampled, then they must all have the same number of samples per pixel.</span></span>

<span data-ttu-id="8254a-191">Es kann nur ein tiefen Schablone-Puffer aktiv sein, unabhängig davon, wie viele Renderziele aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="8254a-191">There can only be one depth-stencil buffer active, regardless of how many render targets are active.</span></span> <span data-ttu-id="8254a-192">Wenn Textur Arrays als Renderziele verwendet werden, müssen alle Ansichts Dimensionen entsprechend identisch sein.</span><span class="sxs-lookup"><span data-stu-id="8254a-192">When using texture arrays as render targets, all view dimensions must match.</span></span> <span data-ttu-id="8254a-193">Die Renderziele müssen nicht das gleiche Textur Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8254a-193">The render targets do not need to have the same texture format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8254a-194">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8254a-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8254a-195">Ressourcen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8254a-195">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
