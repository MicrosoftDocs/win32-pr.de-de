---
title: Entpacken und Verpacken DXGI_FORMAT für die In-Place Bildbearbeitung
description: Die D3DX \_ dxgiformatconvert. INL-Datei enthält Funktionen für Inline Formatkonvertierungen, die Sie im COMPUTE-Shader oder Pixel-Shader auf Direct3D 11-Hardware verwenden können.
ms.assetid: 328c4488-9758-4359-a37b-ac50f20e2940
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04f3729bbeda5b0677da9d52e595e621523ff2d1
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106368283"
---
# <a name="unpacking-and-packing-dxgi_format-for-in-place-image-editing"></a><span data-ttu-id="56699-103">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="56699-103">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>

<span data-ttu-id="56699-104">Die D3DX \_ dxgiformatconvert. INL-Datei enthält Funktionen für Inline Formatkonvertierungen, die Sie im COMPUTE-Shader oder Pixel-Shader auf Direct3D 11-Hardware verwenden können.</span><span class="sxs-lookup"><span data-stu-id="56699-104">The D3DX\_DXGIFormatConvert.inl file contains inline format conversion functions that you can use in the compute shader or pixel shader on Direct3D 11 hardware.</span></span> <span data-ttu-id="56699-105">Sie können diese Funktionen in der Anwendung verwenden, um gleichzeitig Lese-und Schreibvorgänge für eine Textur auszuführen.</span><span class="sxs-lookup"><span data-stu-id="56699-105">You can use these functions in your application to simultaneously both read from and write to a texture.</span></span> <span data-ttu-id="56699-106">Das heißt, Sie können eine direkte Bildbearbeitung ausführen.</span><span class="sxs-lookup"><span data-stu-id="56699-106">That is, you can perform in-place image editing.</span></span> <span data-ttu-id="56699-107">Um diese Funktionen für die Inline Formatkonvertierung zu verwenden, schließen \_ Sie die Datei D3DX dxgiformatconvert. INL in Ihre Anwendung ein.</span><span class="sxs-lookup"><span data-stu-id="56699-107">To use these inline format conversion functions, include the D3DX\_DXGIFormatConvert.inl file in your application.</span></span>

> <span data-ttu-id="56699-108">Der D3DX \_ dxgiformatconvert. INL-Header wird im Legacy-DirectX-SDK ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="56699-108">The D3DX\_DXGIFormatConvert.inl header ships in the legacy DirectX SDK.</span></span> <span data-ttu-id="56699-109">Es ist auch im nuget-Paket [Microsoft. dxsdk. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) enthalten.</span><span class="sxs-lookup"><span data-stu-id="56699-109">It is also included in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet package.</span></span>

<span data-ttu-id="56699-110">Die unsortierter Zugriffs Ansicht (UAV) von Direct3D 11 einer Texture1D-, Texture2D-oder Texture3D-Ressource unterstützt den zufälligen Zugriff auf Lese-und Schreibvorgänge von einem Compute-Shader oder Pixel-Shader in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="56699-110">Direct3D 11's Unordered Access View (UAV) of a Texture1D, Texture2D, or Texture3D resource supports random access reads and writes to memory from a compute shader or pixel shader.</span></span> <span data-ttu-id="56699-111">Allerdings unterstützt Direct3D 11 gleichzeitige Lese-und Schreibvorgänge für das DXGI- \_ Format \_ R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="56699-111">However, Direct3D 11 supports simultaneously both reading from and writing to only the DXGI\_FORMAT\_R32\_UINT texture format.</span></span> <span data-ttu-id="56699-112">Beispielsweise unterstützt Direct3D 11 nicht gleichzeitiges Lesen von und Schreiben in andere, nützlichere Formate, wie z. b. DXGI- \_ Format \_ R8G8B8A8 \_ unorm.</span><span class="sxs-lookup"><span data-stu-id="56699-112">For example, Direct3D 11 does not support simultaneously both reading from and writing to other, more useful formats, such as DXGI\_FORMAT\_R8G8B8A8\_UNORM.</span></span> <span data-ttu-id="56699-113">Sie können nur einen UAV-Vorgang für den zufälligen Zugriff auf solche anderen Formate verwenden, oder Sie können nur einen Shader-Ressourcenansicht (SRV) für den zufälligen Zugriff verwenden, der aus solchen anderen Formaten gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="56699-113">You can use only a UAV to random access write to such other formats, or you can use only a Shader Resource View (SRV) to random access read from such other formats.</span></span> <span data-ttu-id="56699-114">Die Hardware für die Format Konvertierung ist nicht verfügbar, um gleichzeitig Lese-und Schreibvorgänge in solchen anderen Formaten auszuführen.</span><span class="sxs-lookup"><span data-stu-id="56699-114">Format conversion hardware is not available to simultaneously both read from and write to such other formats.</span></span>

<span data-ttu-id="56699-115">Sie können jedoch gleichzeitig sowohl aus solchen anderen Formaten lesen als auch schreiben, indem Sie die Textur in das DXGI- \_ Format \_ R32 \_ uint-Textur Format umwandeln, wenn Sie eine UAV erstellen, solange das ursprüngliche Format der Ressource eine Umwandlung in das DXGI- \_ Format \_ R32 \_ uint unterstützt.</span><span class="sxs-lookup"><span data-stu-id="56699-115">However, you can still simultaneously both read from and write to such other formats by casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format when you create a UAV, as long as the original format of the resource supports casting to DXGI\_FORMAT\_R32\_UINT.</span></span> <span data-ttu-id="56699-116">Die meisten 32 Bit pro Element Formate unterstützen die Umwandlung in das DXGI- \_ Format \_ R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="56699-116">Most 32 bit per element formats support casting to DXGI\_FORMAT\_R32\_UINT.</span></span> <span data-ttu-id="56699-117">Wenn Sie die Textur in das DXGI- \_ Format \_ R32 \_ uint-Textur Format umwandeln, wenn Sie eine UAV erstellen, können Sie dann gleichzeitig Lese-und Schreibvorgänge in die Textur ausführen, solange der Shader beim Schreiben beim Lesen und Verpacken das manuelle formatieren beim Schreiben durchführt.</span><span class="sxs-lookup"><span data-stu-id="56699-117">By casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format when you create a UAV, you can then simultaneous perform reads and writes to the texture as long as the shader performs manual format unpacking on read and packing on write.</span></span>

<span data-ttu-id="56699-118">Der Vorteil der Umwandlung der Textur in das DXGI- \_ Format von \_ R32 \_ uint ist, dass Sie später das entsprechende Format (z. b. DXGI- \_ Format \_ R16G16 \_ float) mit anderen Sichten in derselben Textur verwenden können, wie z. b. renderzielsichten (rtvs) oder Srvs.</span><span class="sxs-lookup"><span data-stu-id="56699-118">The benefit of casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format is that later on you can use the appropriate format (for example, DXGI\_FORMAT\_R16G16\_FLOAT) with other views on the same texture, such as Render Target Views (RTVs) or SRVs.</span></span> <span data-ttu-id="56699-119">Aus diesem Grund kann die Hardware das typische automatische Format entpacken und Verpacken, eine Textur Filterung durchführen usw., wenn keine Hardware Einschränkungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="56699-119">Therefore, the hardware can perform the typical automatic format unpack and pack, can perform texture filtering, and so on where there are no hardware limitations.</span></span>

<span data-ttu-id="56699-120">Das folgende Szenario erfordert, dass eine Anwendung die folgenden Aktionen ausführt, um eine direkte Bildbearbeitung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="56699-120">The following scenario requires that an application take the following sequence of actions to perform in-place image editing.</span></span>

<span data-ttu-id="56699-121">Angenommen, Sie möchten eine Textur erstellen, in der Sie einen PixelShader oder einen Compute-Shader verwenden können, um eine direkte Bearbeitung auszuführen, und Sie möchten, dass die Textur Daten in einem Format gespeichert werden, das einem der folgenden typlosen Formate untergeordnet ist:</span><span class="sxs-lookup"><span data-stu-id="56699-121">Suppose you want to make a texture on which you can use a pixel shader or compute shader to perform in-place editing, and you want the texture data to be stored in a format that is a descendant of one of the following TYPELESS formats:</span></span>

-   <span data-ttu-id="56699-122">DXGI- \_ Format \_ R10G10B10A2 \_ typlose</span><span class="sxs-lookup"><span data-stu-id="56699-122">DXGI\_FORMAT\_R10G10B10A2\_TYPELESS</span></span>
-   <span data-ttu-id="56699-123">DXGI- \_ Format \_ R8G8B8A8 \_ typlose</span><span class="sxs-lookup"><span data-stu-id="56699-123">DXGI\_FORMAT\_R8G8B8A8\_TYPELESS</span></span>
-   <span data-ttu-id="56699-124">DXGI- \_ Format \_ B8G8R8A8 \_ typlose</span><span class="sxs-lookup"><span data-stu-id="56699-124">DXGI\_FORMAT\_B8G8R8A8\_TYPELESS</span></span>
-   <span data-ttu-id="56699-125">DXGI- \_ Format \_ B8G8R8X8 \_ typlose</span><span class="sxs-lookup"><span data-stu-id="56699-125">DXGI\_FORMAT\_B8G8R8X8\_TYPELESS</span></span>
-   <span data-ttu-id="56699-126">DXGI- \_ Format \_ R16G16 \_ typlose</span><span class="sxs-lookup"><span data-stu-id="56699-126">DXGI\_FORMAT\_R16G16\_TYPELESS</span></span>

<span data-ttu-id="56699-127">Das DXGI- \_ Format \_ R10G10B10A2 \_ unorm-Format ist beispielsweise ein Nachfolger des DXGI-Formats \_ \_ R10G10B10A2 \_ typlose Format.</span><span class="sxs-lookup"><span data-stu-id="56699-127">For example, the DXGI\_FORMAT\_R10G10B10A2\_UNORM format is a descendant of the DXGI\_FORMAT\_R10G10B10A2\_TYPELESS format.</span></span> <span data-ttu-id="56699-128">Daher unterstützt das DXGI- \_ Format \_ R10G10B10A2 \_ unorm das Verwendungs Muster, das in der folgenden Reihenfolge beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="56699-128">Therefore, DXGI\_FORMAT\_R10G10B10A2\_UNORM supports the usage pattern that is described in the following sequence.</span></span> <span data-ttu-id="56699-129">Formate, die von einem typlosen DXGI-Format (z. b. \_ \_ \_ DXGI- \_ Format \_ R32 float) abgeleitet werden, \_ werden trivial unterstützt, ohne dass eine der in der folgenden Sequenz beschriebenen Format Konvertierungs Hilfe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="56699-129">Formats that descend from DXGI\_FORMAT\_R32\_TYPELESS, such as DXGI\_FORMAT\_R32\_FLOAT, are trivially supported without requiring any of the format conversion help that is described in the following sequence.</span></span>

<span data-ttu-id="56699-130">**So führen Sie eine direkte Bildbearbeitung aus**</span><span class="sxs-lookup"><span data-stu-id="56699-130">**To perform in-place image editing**</span></span>

1.  <span data-ttu-id="56699-131">Erstellen Sie eine Textur mit dem entsprechenden typlosen abhängigen Format, das im vorherigen Szenario angegeben ist, sowie die erforderlichen Bindungsflags, z \_ . b. D3D11 Bind \_ \_ unorderaccess \| D3D11 \_ Bind \_ Shader \_ Resource.</span><span class="sxs-lookup"><span data-stu-id="56699-131">Create a texture with the appropriate TYPELESS-dependent format that is specified in the previous scenario together with the required bind flags, such as D3D11\_BIND\_UNORDERED\_ACCESS \| D3D11\_BIND\_SHADER\_RESOURCE.</span></span>
2.  <span data-ttu-id="56699-132">Erstellen Sie für eine direkte Bildbearbeitung eine UAV mit dem DXGI- \_ Format \_ R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="56699-132">For in-place image editing, create a UAV with the DXGI\_FORMAT\_R32\_UINT format.</span></span> <span data-ttu-id="56699-133">Die Direct3D 11-API lässt in der Regel keine Umwandlung zwischen unterschiedlichen Format "Familien" zu.</span><span class="sxs-lookup"><span data-stu-id="56699-133">The Direct3D 11 API typically does not allow casting between different format "families."</span></span> <span data-ttu-id="56699-134">Die API Direct3D 11 gibt jedoch eine Ausnahme mit dem DXGI- \_ Format \_ R32 \_ uint aus.</span><span class="sxs-lookup"><span data-stu-id="56699-134">However, the Direct3D 11 API makes an exception with the DXGI\_FORMAT\_R32\_UINT format.</span></span>
3.  <span data-ttu-id="56699-135">Verwenden Sie im COMPUTE-Shader oder Pixel-Shader das entsprechende Inline Format Pack und die entpacken-Funktionen, die in der \_ Datei D3DX dxgiformatconvert. INL bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="56699-135">In the compute shader or pixel shader, use the appropriate inline format pack and unpack functions that are provided in the D3DX\_DXGIFormatConvert.inl file.</span></span> <span data-ttu-id="56699-136">Nehmen wir beispielsweise an, dass das DXGI- \_ Format \_ R32 \_ uint UAV der Textur tatsächlich das DXGI \_ \_ -Format R10G10B10A2 \_ unorm-formatierte Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="56699-136">For example, suppose the DXGI\_FORMAT\_R32\_UINT UAV of the texture really holds DXGI\_FORMAT\_R10G10B10A2\_UNORM-formatted data.</span></span> <span data-ttu-id="56699-137">Nachdem die Anwendung eine uint aus der UAV in den Shader gelesen hat, muss Sie die folgende Funktion aufrufen, um das Textur Format zu entpacken:</span><span class="sxs-lookup"><span data-stu-id="56699-137">After the application reads a uint from the UAV into the shader, it must call the following function to unpack the texture format:</span></span>

    ```
    XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
    ```

    

    <span data-ttu-id="56699-138">Wenn Sie dann im gleichen Shader in die UAV schreiben möchten, ruft die Anwendung die folgende Funktion auf, um Shader-Daten in einen uint zu packen, den die Anwendung in die UAV schreiben kann:</span><span class="sxs-lookup"><span data-stu-id="56699-138">Then, to write to the UAV in the same shader, the application calls the following function to pack shader data into a uint that the application can write to the UAV:</span></span>

    ```
    UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
    ```

    

4.  <span data-ttu-id="56699-139">Die Anwendung kann dann andere Ansichten, z. b. Srvs, mit dem erforderlichen Format erstellen.</span><span class="sxs-lookup"><span data-stu-id="56699-139">The application can then create other views, such as SRVs, with the required format.</span></span> <span data-ttu-id="56699-140">Die Anwendung kann z. b. einen SRV mit dem DXGI- \_ Format \_ R10G10B10A2 \_ unorm Format erstellen, wenn die Ressource als DXGI- \_ Format \_ R10G10B10A2 \_ typlose erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="56699-140">For example, the application can create a SRV with the DXGI\_FORMAT\_R10G10B10A2\_UNORM format if the resource was created as DXGI\_FORMAT\_R10G10B10A2\_TYPELESS.</span></span> <span data-ttu-id="56699-141">Wenn ein Shader auf diesen SRV zugreift, kann die Hardware wie üblich eine automatische Typkonvertierung durchführen.</span><span class="sxs-lookup"><span data-stu-id="56699-141">When a shader accesses that SRV, the hardware can perform automatic type conversion as usual.</span></span>

> [!Note]  
> <span data-ttu-id="56699-142">Wenn der Shader nur in eine UAV schreiben oder als SRV gelesen werden muss, ist keiner dieser Konvertierungs Aufgaben erforderlich, da Sie vollständig typisierte UAVs oder Srvs verwenden können.</span><span class="sxs-lookup"><span data-stu-id="56699-142">If the shader must write only to a UAV, or read as an SRV, none of this conversion work is needed because you can use fully typed UAVs or SRVs.</span></span> <span data-ttu-id="56699-143">Die in D3DX \_ dxgiformatconvert. INL bereitgestellten formatkonvertierungs Funktionen sind möglicherweise nur nützlich, wenn Sie gleichzeitige Lese-und Schreibvorgänge in eine UAV einer Textur durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="56699-143">The format conversion functions provided in D3DX\_DXGIFormatConvert.inl are potentially useful only if you want to perform simultaneous reading from and writing to a UAV of a texture.</span></span>

 

<span data-ttu-id="56699-144">Im folgenden finden Sie eine Liste der formatkonvertierungs Funktionen, die in der \_ Datei D3DX dxgiformatconvert. INL enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="56699-144">The following is the list of format conversion functions that are included in the D3DX\_DXGIFormatConvert.inl file.</span></span> <span data-ttu-id="56699-145">Diese Funktionen werden nach dem DXGI \_ -Format kategorisiert, das Sie entpacken und Verpacken.</span><span class="sxs-lookup"><span data-stu-id="56699-145">These functions are categorized by the DXGI\_FORMAT that they unpack and pack.</span></span> <span data-ttu-id="56699-146">Jedes der unterstützten Formate wird von einem der im vorherigen Szenario aufgelisteten typlosen Formate abgeleitet und unterstützt die Umwandlung in das DXGI- \_ Format \_ R32 \_ uint als UAV.</span><span class="sxs-lookup"><span data-stu-id="56699-146">Each of the supported formats descends from one of the TYPELESS formats listed in the preceding scenario and supports casting to DXGI\_FORMAT\_R32\_UINT as a UAV.</span></span>

<dl> <dt>

<span data-ttu-id="56699-147"><span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>DXGI- \_ Format \_ R10G10B10A2 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="56699-147"><span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>DXGI\_FORMAT\_R10G10B10A2\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="56699-148"><span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>DXGI- \_ Format \_ R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="56699-148"><span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>DXGI\_FORMAT\_R10G10B10A2\_UINT</span></span>
</dt> <dd>


```
XMUINT4 D3DX_R10G10B10A2_UINT_to_UINT4(UINT packedInput)
UINT    D3DX_UINT4_to_R10G10B10A2_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="56699-149"><span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>DXGI- \_ Format \_ R8G8B8A8 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="56699-149"><span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>DXGI\_FORMAT\_R8G8B8A8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="56699-150"><span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>DXGI- \_ Format \_ R8G8B8A8 \_ unorm \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="56699-150"><span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="56699-151">Die \_ inexact-Type-Funktion verwendet shaderanweisungen ohne hohe Genauigkeit, um die genaue Antwort zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="56699-151">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="56699-152">Die Alternative Funktion verwendet eine im Shader gespeicherte Nachschlage Tabelle, um eine exakte sRGB->float-Konvertierung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="56699-152">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="56699-153"><span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>DXGI- \_ Format \_ R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="56699-153"><span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>DXGI\_FORMAT\_R8G8B8A8\_UINT</span></span>
</dt> <dd>


```
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(UINT packedInput)
XMUINT  D3DX_UINT4_to_R8G8B8A8_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="56699-154"><span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>DXGI- \_ Format \_ R8G8B8A8 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="56699-154"><span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>DXGI\_FORMAT\_R8G8B8A8\_SNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_SNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="56699-155"><span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>DXGI- \_ Format \_ R8G8B8A8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="56699-155"><span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>DXGI\_FORMAT\_R8G8B8A8\_SINT</span></span>
</dt> <dd>


```
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(UINT packedInput)
UINT   D3DX_INT4_to_R8G8B8A8_SINT(XMINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="56699-156"><span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>DXGI- \_ Format \_ B8G8R8A8 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="56699-156"><span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_B8G8R8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="56699-157"><span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="56699-157"><span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="56699-158">Die \_ inexact-Type-Funktion verwendet shaderanweisungen ohne hohe Genauigkeit, um die genaue Antwort zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="56699-158">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="56699-159">Die Alternative Funktion verwendet eine im Shader gespeicherte Nachschlage Tabelle, um eine exakte sRGB->float-Konvertierung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="56699-159">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="56699-160"><span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>DXGI- \_ Format \_ B8G8R8X8 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="56699-160"><span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>DXGI\_FORMAT\_B8G8R8X8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM(hlsl_precise XMFLOAT3 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="56699-161"><span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>DXGI- \_ Format \_ B8G8R8X8 \_ unorm \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="56699-161"><span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(UINT packedInput) *
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(hlsl_precise XMFLOAT3 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="56699-162">Die \_ inexact-Type-Funktion verwendet shaderanweisungen ohne hohe Genauigkeit, um die genaue Antwort zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="56699-162">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="56699-163">Die Alternative Funktion verwendet eine im Shader gespeicherte Nachschlage Tabelle, um eine exakte sRGB->float-Konvertierung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="56699-163">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="56699-164"><span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>DXGI- \_ Format \_ R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="56699-164"><span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>DXGI\_FORMAT\_R16G16\_FLOAT</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_FLOAT(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="56699-165"><span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>DXGI- \_ Format \_ R16G16 \_ unorm</span><span class="sxs-lookup"><span data-stu-id="56699-165"><span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>DXGI\_FORMAT\_R16G16\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_UNORM(hlsl_precise FLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="56699-166"><span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>DXGI- \_ Format \_ R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="56699-166"><span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>DXGI\_FORMAT\_R16G16\_UINT</span></span>
</dt> <dd>


```
XMUINT2 D3DX_R16G16_UINT_to_UINT2(UINT packedInput)
UINT    D3DX_UINT2_to_R16G16_UINT(XMUINT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="56699-167"><span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>DXGI- \_ Format \_ R16G16 \_ snorm</span><span class="sxs-lookup"><span data-stu-id="56699-167"><span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>DXGI\_FORMAT\_R16G16\_SNORM</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_SNORM(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="56699-168"><span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>DXGI- \_ Format \_ R16G16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="56699-168"><span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>DXGI\_FORMAT\_R16G16\_SINT</span></span>
</dt> <dd>


```
XMINT2 D3DX_R16G16_SINT_to_INT2(UINT packedInput)
UINT   D3DX_INT2_to_R16G16_SINT(XMINT2 unpackedInput)
```



</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="56699-169">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="56699-169">Related Topics</span></span>

[<span data-ttu-id="56699-170">Programmieranleitung für HLSL</span><span class="sxs-lookup"><span data-stu-id="56699-170">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="56699-171">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56699-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56699-172">Programmieranleitung für HLSL</span><span class="sxs-lookup"><span data-stu-id="56699-172">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




