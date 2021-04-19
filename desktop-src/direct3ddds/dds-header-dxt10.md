---
title: DDS_HEADER_DXT10-Struktur (DDS. h)
description: DDS-Header Erweiterung zum Verarbeiten von Ressourcen Arrays, DXGI-Pixel Formate, die nicht den Legacy Strukturen des Microsoft DirectDraw-Pixel Formats zugeordnet sind, sowie zusätzliche Metadaten.
ms.assetid: 502d6943-8f25-446c-b990-8276f862c195
keywords:
- DDS_HEADER_DXT10 Struktur-DDS
topic_type:
- apiref
api_name:
- DDS_HEADER_DXT10
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a2f5dd4a6948d38b86b49584db81937ce5148b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364350"
---
# <a name="dds_header_dxt10-structure"></a><span data-ttu-id="ee8e6-104">DDS- \_ Header \_ DXT10 Struktur</span><span class="sxs-lookup"><span data-stu-id="ee8e6-104">DDS\_HEADER\_DXT10 structure</span></span>

<span data-ttu-id="ee8e6-105">DDS-Header Erweiterung zum Verarbeiten von Ressourcen Arrays, DXGI-Pixel Formate, die nicht den Legacy Strukturen des Microsoft DirectDraw-Pixel Formats zugeordnet sind, sowie zusätzliche Metadaten.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-105">DDS header extension to handle resource arrays, DXGI pixel formats that don't map to the legacy Microsoft DirectDraw pixel format structures, and additional metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee8e6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee8e6-106">Syntax</span></span>


```C++
typedef struct {
  DXGI_FORMAT              dxgiFormat;
  D3D10_RESOURCE_DIMENSION resourceDimension;
  UINT                     miscFlag;
  UINT                     arraySize;
  UINT                     miscFlags2;
} DDS_HEADER_DXT10;
```



## <a name="members"></a><span data-ttu-id="ee8e6-107">Member</span><span class="sxs-lookup"><span data-stu-id="ee8e6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ee8e6-108">**dxgiformat**</span><span class="sxs-lookup"><span data-stu-id="ee8e6-108">**dxgiFormat**</span></span>
</dt> <dd>

<span data-ttu-id="ee8e6-109">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="ee8e6-109">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="ee8e6-110">Das Surface-Pixel-Format (siehe [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="ee8e6-110">The surface pixel format (see [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span>

</dd> <dt>

<span data-ttu-id="ee8e6-111">**resourcedimension**</span><span class="sxs-lookup"><span data-stu-id="ee8e6-111">**resourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="ee8e6-112">Type: **[ **d3d10- \_ Ressourcen \_ Dimension**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="ee8e6-112">Type: **[**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="ee8e6-113">Identifiziert den Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-113">Identifies the type of resource.</span></span> <span data-ttu-id="ee8e6-114">Die folgenden Werte für diesen Member sind eine Teilmenge der Werte in der [**d3d10- \_ Ressourcen \_ Dimension**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) oder der [**D3D11- \_ ressourcendimensionsenumeration \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) :</span><span class="sxs-lookup"><span data-stu-id="ee8e6-114">The following values for this member are a subset of the values in the [**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) or [**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) enumeration:</span></span>



| <span data-ttu-id="ee8e6-115">type</span><span class="sxs-lookup"><span data-stu-id="ee8e6-115">Type</span></span>                                                              | <span data-ttu-id="ee8e6-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee8e6-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="ee8e6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ee8e6-117">Value</span></span> |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="ee8e6-118">DDS- \_ Dimension \_ TEXTURE1D (d3d10 \_ Resource \_ Dimension \_ TEXTURE1D)</span><span class="sxs-lookup"><span data-stu-id="ee8e6-118">DDS\_DIMENSION\_TEXTURE1D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE1D)</span></span> | <span data-ttu-id="ee8e6-119">Die Ressource ist eine [1D-Textur](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types).</span><span class="sxs-lookup"><span data-stu-id="ee8e6-119">Resource is a [1D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types).</span></span> <span data-ttu-id="ee8e6-120">Der **dwwidth** -Member des [**DDS- \_ Headers**](dds-header.md) gibt die Größe der Textur an.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-120">The **dwWidth** member of [**DDS\_HEADER**](dds-header.md) specifies the size of the texture.</span></span> <span data-ttu-id="ee8e6-121">In der Regel legen Sie den **dwheight** -Member des **DDS- \_ Headers** auf 1 fest. Außerdem müssen Sie das ddsd \_ height-Flag im **dwFlags** -Member des **DDS- \_ Headers** festlegen.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-121">Typically, you set the **dwHeight** member of **DDS\_HEADER** to 1; you also must set the DDSD\_HEIGHT flag in the **dwFlags** member of **DDS\_HEADER**.</span></span>                      | <span data-ttu-id="ee8e6-122">2</span><span class="sxs-lookup"><span data-stu-id="ee8e6-122">2</span></span>     |
| <span data-ttu-id="ee8e6-123">DDS- \_ Dimension \_ TEXTURE2D (d3d10 \_ Resource \_ Dimension \_ TEXTURE2D)</span><span class="sxs-lookup"><span data-stu-id="ee8e6-123">DDS\_DIMENSION\_TEXTURE2D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE2D)</span></span> | <span data-ttu-id="ee8e6-124">Ressource ist eine [2D-Textur](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) mit einem Bereich, der von den **dwwidth** -und **dwheight** -Membern des [**DDS- \_ Headers**](dds-header.md)angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-124">Resource is a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) with an area specified by the **dwWidth** and **dwHeight** members of [**DDS\_HEADER**](dds-header.md).</span></span> <span data-ttu-id="ee8e6-125">Sie können diesen Typ auch verwenden, um eine cubemaptextur zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-125">You can also use this type to identify a cube-map texture.</span></span> <span data-ttu-id="ee8e6-126">Weitere Informationen zum Identifizieren einer cubemaptextur finden Sie unter die Member " **fehlflag** " und " **arraySize** ".</span><span class="sxs-lookup"><span data-stu-id="ee8e6-126">For more information about how to identify a cube-map texture, see **miscFlag** and **arraySize** members.</span></span> | <span data-ttu-id="ee8e6-127">3</span><span class="sxs-lookup"><span data-stu-id="ee8e6-127">3</span></span>     |
| <span data-ttu-id="ee8e6-128">DDS- \_ Dimension \_ TEXTURE3D (d3d10 \_ Resource \_ Dimension \_ TEXTURE3D)</span><span class="sxs-lookup"><span data-stu-id="ee8e6-128">DDS\_DIMENSION\_TEXTURE3D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE3D)</span></span> | <span data-ttu-id="ee8e6-129">Ressource ist eine [3D-Textur](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) mit einem Volume, das durch die **dwwidth**-, **dwheight**-und **dwtiefe** -Member des [**DDS- \_ Headers**](dds-header.md)angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-129">Resource is a [3D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) with a volume specified by the **dwWidth**, **dwHeight**, and **dwDepth** members of [**DDS\_HEADER**](dds-header.md).</span></span> <span data-ttu-id="ee8e6-130">Sie müssen auch das ddsd- \_ tiefen Flag im **dwFlags** -Member des **DDS- \_ Headers** festlegen.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-130">You also must set the DDSD\_DEPTH flag in the **dwFlags** member of **DDS\_HEADER**.</span></span>                                                                   | <span data-ttu-id="ee8e6-131">4</span><span class="sxs-lookup"><span data-stu-id="ee8e6-131">4</span></span>     |



 

</dd> <dt>

<span data-ttu-id="ee8e6-132">**fehlflag**</span><span class="sxs-lookup"><span data-stu-id="ee8e6-132">**miscFlag**</span></span>
</dt> <dd>

<span data-ttu-id="ee8e6-133">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ee8e6-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ee8e6-134">Identifiziert andere, weniger häufig genutzte Optionen für Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-134">Identifies other, less common options for resources.</span></span> <span data-ttu-id="ee8e6-135">Der folgende Wert für diesen Member ist eine Teilmenge der Werte im [**d3d10 \_ \_ ressourcenmisc- \_ Flag**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) oder der [**D3D11 \_ Resource \_ misc \_ Flag**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) -Enumeration:</span><span class="sxs-lookup"><span data-stu-id="ee8e6-135">The following value for this member is a subset of the values in the [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) or [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) enumeration:</span></span>



| <span data-ttu-id="ee8e6-136">type</span><span class="sxs-lookup"><span data-stu-id="ee8e6-136">Type</span></span>                             | <span data-ttu-id="ee8e6-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee8e6-137">Description</span></span>                                                                                                  | <span data-ttu-id="ee8e6-138">Wert</span><span class="sxs-lookup"><span data-stu-id="ee8e6-138">Value</span></span> |
|----------------------------------|--------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="ee8e6-139">DDS- \_ Ressource \_ misc \_ texturecube</span><span class="sxs-lookup"><span data-stu-id="ee8e6-139">DDS\_RESOURCE\_MISC\_TEXTURECUBE</span></span> | <span data-ttu-id="ee8e6-140">Gibt an, dass eine [2D-Textur](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) eine cubemaptextur ist.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-140">Indicates a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) is a cube-map texture.</span></span> | <span data-ttu-id="ee8e6-141">0x4</span><span class="sxs-lookup"><span data-stu-id="ee8e6-141">0x4</span></span>   |



 

</dd> <dt>

<span data-ttu-id="ee8e6-142">**arraySize**</span><span class="sxs-lookup"><span data-stu-id="ee8e6-142">**arraySize**</span></span>
</dt> <dd>

<span data-ttu-id="ee8e6-143">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ee8e6-143">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ee8e6-144">Die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-144">The number of elements in the array.</span></span>

<span data-ttu-id="ee8e6-145">Bei einer [2D-Textur](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) , bei der es sich auch um eine cubemaptextur handelt, stellt diese Zahl die Anzahl der Cubes dar.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-145">For a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) that is also a cube-map texture, this number represents the number of cubes.</span></span> <span data-ttu-id="ee8e6-146">Diese Zahl entspricht der Zahl im **numcubes** -Member des [**d3d10 \_ Texcube- \_ Arrays \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) oder [**D3D11 \_ Texcube- \_ array \_ SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)).</span><span class="sxs-lookup"><span data-stu-id="ee8e6-146">This number is the same as the number in the **NumCubes** member of [**D3D10\_TEXCUBE\_ARRAY\_SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) or [**D3D11\_TEXCUBE\_ARRAY\_SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)).</span></span> <span data-ttu-id="ee8e6-147">In diesem Fall enthält die DDS-Datei **arraySize** \* 6 2D-Texturen.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-147">In this case, the DDS file contains **arraySize**\*6 2D textures.</span></span> <span data-ttu-id="ee8e6-148">Weitere Informationen zu diesem Fall finden Sie in der Beschreibung zu " **fehlflag** ".</span><span class="sxs-lookup"><span data-stu-id="ee8e6-148">For more information about this case, see the **miscFlag** description.</span></span>

<span data-ttu-id="ee8e6-149">Für eine [3D-Textur](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types)müssen Sie diese Zahl auf 1 festlegen.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-149">For a [3D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types), you must set this number to 1.</span></span>

</dd> <dt>

<span data-ttu-id="ee8e6-150">**miscFlags2**</span><span class="sxs-lookup"><span data-stu-id="ee8e6-150">**miscFlags2**</span></span>
</dt> <dd>

<span data-ttu-id="ee8e6-151">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ee8e6-151">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ee8e6-152">Enthält zusätzliche Metadaten (zuvor war reserviert).</span><span class="sxs-lookup"><span data-stu-id="ee8e6-152">Contains additional metadata (formerly was reserved).</span></span> <span data-ttu-id="ee8e6-153">Die unteren 3 Bits geben den Alpha Modus der zugeordneten Ressource an.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-153">The lower 3 bits indicate the alpha mode of the associated resource.</span></span> <span data-ttu-id="ee8e6-154">Die oberen 29 Bits sind reserviert und in der Regel 0.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-154">The upper 29 bits are reserved and are typically 0.</span></span>



| <span data-ttu-id="ee8e6-155">type</span><span class="sxs-lookup"><span data-stu-id="ee8e6-155">Type</span></span>                            | <span data-ttu-id="ee8e6-156">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee8e6-156">Description</span></span>                                                                                                                              | <span data-ttu-id="ee8e6-157">Wert</span><span class="sxs-lookup"><span data-stu-id="ee8e6-157">Value</span></span> |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="ee8e6-158">DDS- \_ alpha \_ Modus \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="ee8e6-158">DDS\_ALPHA\_MODE\_UNKNOWN</span></span>       | <span data-ttu-id="ee8e6-159">Der Alpha Kanal Inhalt ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-159">Alpha channel content is unknown.</span></span> <span data-ttu-id="ee8e6-160">Dies ist der Wert für Legacy Dateien, bei dem es sich in der Regel um einen "geraden" Alpha handelt.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-160">This is the value for legacy files, which typically is assumed to be 'straight' alpha.</span></span>                 | <span data-ttu-id="ee8e6-161">0x0</span><span class="sxs-lookup"><span data-stu-id="ee8e6-161">0x0</span></span>   |
| <span data-ttu-id="ee8e6-162">DDS- \_ alpha \_ Modus \_ direkt</span><span class="sxs-lookup"><span data-stu-id="ee8e6-162">DDS\_ALPHA\_MODE\_STRAIGHT</span></span>      | <span data-ttu-id="ee8e6-163">Der Inhalt des Alphakanals wird als "gerade Alpha" verwendet.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-163">Any alpha channel content is presumed to use straight alpha.</span></span>                                                                             | <span data-ttu-id="ee8e6-164">0x1</span><span class="sxs-lookup"><span data-stu-id="ee8e6-164">0x1</span></span>   |
| <span data-ttu-id="ee8e6-165">DDS- \_ alpha \_ Modus ist \_ vorab multipliziert.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-165">DDS\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="ee8e6-166">Für alle Alphakanal Inhalte wird ein prämultipliziertes Alpha verwendet.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-166">Any alpha channel content is using premultiplied alpha.</span></span> <span data-ttu-id="ee8e6-167">Die einzigen Legacy Dateiformate, die diese Informationen angeben, sind "DX2" und "DX4".</span><span class="sxs-lookup"><span data-stu-id="ee8e6-167">The only legacy file formats that indicate this information are 'DX2' and 'DX4'.</span></span> | <span data-ttu-id="ee8e6-168">0x2</span><span class="sxs-lookup"><span data-stu-id="ee8e6-168">0x2</span></span>   |
| <span data-ttu-id="ee8e6-169">DDS- \_ alpha \_ Modus nicht \_ transparent</span><span class="sxs-lookup"><span data-stu-id="ee8e6-169">DDS\_ALPHA\_MODE\_OPAQUE</span></span>        | <span data-ttu-id="ee8e6-170">Alle Alphakanal Inhalte sind auf vollständig deckend festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-170">Any alpha channel content is all set to fully opaque.</span></span>                                                                                    | <span data-ttu-id="ee8e6-171">0x3</span><span class="sxs-lookup"><span data-stu-id="ee8e6-171">0x3</span></span>   |
| <span data-ttu-id="ee8e6-172">benutzerdefinierter DDS- \_ alpha \_ Modus \_</span><span class="sxs-lookup"><span data-stu-id="ee8e6-172">DDS\_ALPHA\_MODE\_CUSTOM</span></span>        | <span data-ttu-id="ee8e6-173">Jeder Alphakanal Inhalt wird als 4. Kanal verwendet und ist nicht für die Darstellung von Transparenz (direkt oder vorab multipliziert) vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-173">Any alpha channel content is being used as a 4th channel and is not intended to represent transparency (straight or premultiplied).</span></span>      | <span data-ttu-id="ee8e6-174">0x4</span><span class="sxs-lookup"><span data-stu-id="ee8e6-174">0x4</span></span>   |



 

> [!Note]  
> <span data-ttu-id="ee8e6-175">Die Legacy Bibliotheken D3DX 10 und [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) können keine geladen werden. DDS-Datei mit **miscFlags2** ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ee8e6-175">The legacy D3DX 10 and [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) utility libraries will fail to load any .DDS file with **miscFlags2** not equal to zero.</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee8e6-176">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee8e6-176">Remarks</span></span>

<span data-ttu-id="ee8e6-177">Verwenden Sie diese Struktur in Verbindung mit einem [**DDS- \_ Header**](dds-header.md) , um ein Ressourcen Array in einer DDS-Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-177">Use this structure together with a [**DDS\_HEADER**](dds-header.md) to store a resource array in a DDS file.</span></span> <span data-ttu-id="ee8e6-178">Weitere Informationen finden Sie unter [Textur Arrays](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="ee8e6-178">For more info, see [texture arrays](dx-graphics-dds-pguide.md).</span></span>

<span data-ttu-id="ee8e6-179">Dieser Header ist vorhanden, wenn der **dwfourcc** -Member der [**DDS- \_ Pixel Format**](dds-pixelformat.md) -Struktur auf ' DX10 ' festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ee8e6-179">This header is present if the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](dds-pixelformat.md) structure is set to 'DX10'.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee8e6-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee8e6-180">Requirements</span></span>



| <span data-ttu-id="ee8e6-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee8e6-181">Requirement</span></span> | <span data-ttu-id="ee8e6-182">Wert</span><span class="sxs-lookup"><span data-stu-id="ee8e6-182">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ee8e6-183">Header</span><span class="sxs-lookup"><span data-stu-id="ee8e6-183">Header</span></span><br/> | <dl> <span data-ttu-id="ee8e6-184"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee8e6-184"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee8e6-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee8e6-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee8e6-186">Verweis für DDS</span><span class="sxs-lookup"><span data-stu-id="ee8e6-186">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

