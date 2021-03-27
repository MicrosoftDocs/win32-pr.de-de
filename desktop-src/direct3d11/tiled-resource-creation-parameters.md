---
title: Parameter für die Kachel Ressourcen Erstellung
description: Es gibt einige Einschränkungen für den Typ der Direct3D-Ressourcen, die Sie mit dem D3D11 \_ - \_ ressourcenmisc-Kachel Kennzeichen erstellen können \_ . Dieser Abschnitt enthält die gültigen Parameter zum Erstellen von gekachelten Ressourcen.
ms.assetid: 19A0EA7F-888D-4102-A5D2-F3B54775EDE8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b912325371c59bd46a6cc4245289b2fe5d32a924
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/13/2019
ms.locfileid: "103719331"
---
# <a name="tiled-resource-creation-parameters"></a><span data-ttu-id="73f18-104">Parameter für die Kachel Ressourcen Erstellung</span><span class="sxs-lookup"><span data-stu-id="73f18-104">Tiled resource creation parameters</span></span>

<span data-ttu-id="73f18-105">Es gibt einige Einschränkungen für den Typ der Direct3D-Ressourcen, die Sie mit dem [**D3D11 \_ - \_ ressourcenmisc- \_ Kachel**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) Kennzeichen erstellen können.</span><span class="sxs-lookup"><span data-stu-id="73f18-105">There are some constraints on the type of Direct3D resources that you can create with the [**D3D11\_RESOURCE\_MISC\_TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span> <span data-ttu-id="73f18-106">Dieser Abschnitt enthält die gültigen Parameter zum Erstellen von gekachelten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="73f18-106">This section provides the valid parameters for creating tiled resources.</span></span>

<dl> <dt>

<span data-ttu-id="73f18-107"><span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Unterstützter Ressourcentyp**</span><span class="sxs-lookup"><span data-stu-id="73f18-107"><span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Supported Resource Type**</span></span>
</dt> <dd>

<span data-ttu-id="73f18-108">Texture2D \[ array \] (einschließlich texturecube- \[ array \] , das eine Variante des Texture2D- \[ Arrays ist \] ) oder Puffer.</span><span class="sxs-lookup"><span data-stu-id="73f18-108">Texture2D\[Array\] (including TextureCube\[Array\], which is a variant of Texture2D\[Array\]) or Buffer.</span></span>

<span data-ttu-id="73f18-109">**Nicht unterstützt:** Texture1D \[ array \] oder Texture3D, aber Texture3D wird in Zukunft möglicherweise unterstützt.</span><span class="sxs-lookup"><span data-stu-id="73f18-109">**NOT supported:** Texture1D\[Array\] or Texture3D, but Texture3D might be supported in the future.</span></span>

</dd> <dt>

<span data-ttu-id="73f18-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Unterstützte Ressourcenverwendung**</span><span class="sxs-lookup"><span data-stu-id="73f18-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Supported Resource Usage**</span></span>
</dt> <dd>

<span data-ttu-id="73f18-111">D3D11 \_ Verwendungs \_ Standard.</span><span class="sxs-lookup"><span data-stu-id="73f18-111">D3D11\_USAGE\_DEFAULT.</span></span>

<span data-ttu-id="73f18-112">**Nicht unterstützt:** D3D11 \_ use \_ Dynamic, D3D11 \_ Usage \_ Staging oder D3D11 \_ Usage \_ unmutable.</span><span class="sxs-lookup"><span data-stu-id="73f18-112">**NOT supported:** D3D11\_USAGE\_DYNAMIC, D3D11\_USAGE\_STAGING, or D3D11\_USAGE\_IMMUTABLE.</span></span>

</dd> <dt>

<span data-ttu-id="73f18-113"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Unterstützte ressourcenmisc-Flags**</span><span class="sxs-lookup"><span data-stu-id="73f18-113"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Supported Resource Misc Flags**</span></span>
</dt> <dd>

<span data-ttu-id="73f18-114">D3D11 \_ Resource \_ misc \_ (definitionsgemäß), \_ misc \_ texturecube, \_ DrawIndirect \_ args, \_ buffer \_ Allow \_ RAW \_ views, \_ buffer \_ strukturierte, \_ Resource \_ Clamp oder \_ Generate \_ mips.</span><span class="sxs-lookup"><span data-stu-id="73f18-114">D3D11\_RESOURCE\_MISC\_TILED (by definition), \_MISC\_TEXTURECUBE, \_DRAWINDIRECT\_ARGS, \_BUFFER\_ALLOW\_RAW\_VIEWS, \_BUFFER\_STRUCTURED, \_RESOURCE\_CLAMP, or \_GENERATE\_MIPS.</span></span>

<span data-ttu-id="73f18-115">**Nicht unterstützt:** \_ Freigegebene, frei \_ gegebene \_ keyedmutex-, \_ GDI- \_ kompatible, frei \_ gegebene \_ nthandle, \_ eingeschränkte \_ Inhalte, frei \_ \_ gegebene \_ Ressource einschränken, Treiber für frei \_ gegebene Ressourcen einschränken, geschützter \_ \_ \_ \_ oder \_ Kachel \_ Pool.</span><span class="sxs-lookup"><span data-stu-id="73f18-115">**NOT supported:** \_SHARED, \_SHARED\_KEYEDMUTEX, \_GDI\_COMPATIBLE, \_SHARED\_NTHANDLE, \_RESTRICTED\_CONTENT, \_RESTRICT\_SHARED\_RESOURCE, \_RESTRICT\_SHARED\_RESOURCE\_DRIVER, \_GUARDED, or \_TILE\_POOL.</span></span>

</dd> <dt>

<span data-ttu-id="73f18-116"><span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Unterstützte Bindungsflags**</span><span class="sxs-lookup"><span data-stu-id="73f18-116"><span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Supported Bind Flags**</span></span>
</dt> <dd>

<span data-ttu-id="73f18-117">D3D11 \_ Bind- \_ Shader- \_ Ressource, \_ \_ Renderziel, \_ tiefen \_ Schablone oder \_ unsortierter \_ Zugriff.</span><span class="sxs-lookup"><span data-stu-id="73f18-117">D3D11\_BIND\_SHADER\_RESOURCE, \_RENDER\_TARGET, \_DEPTH\_STENCIL, or \_UNORDERED\_ACCESS.</span></span>

<span data-ttu-id="73f18-118">**Nicht unterstützt:** \_ Konstanter \_ Puffer: \_ Vertex \_ \[ -Puffer beachten Sie, dass die Bindung eines Kachel Puffers als SRV/UAV/RTV weiterhin in Ordnung ist \] , \_ Index \_ Puffer, \_ \_ Streamausgabe, \_ Bindungs \_ Decoder oder \_ Bind \_ Video \_ Encoder.</span><span class="sxs-lookup"><span data-stu-id="73f18-118">**NOT supported:** \_CONSTANT\_BUFFER, \_VERTEX\_BUFFER \[note that binding a tiled Buffer as an SRV/UAV/RTV is still ok\], \_INDEX\_BUFFER, \_STREAM\_OUTPUT, \_BIND\_DECODER, or \_BIND\_VIDEO\_ENCODER.</span></span>

</dd> <dt>

<span data-ttu-id="73f18-119"><span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Unterstützte Formate**</span><span class="sxs-lookup"><span data-stu-id="73f18-119"><span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Supported Formats**</span></span>
</dt> <dd>

<span data-ttu-id="73f18-120">Alle Formate, die für die angegebene Konfiguration verfügbar sind, und zwar unabhängig davon, ob Sie gekachelt werden, mit einigen Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="73f18-120">All formats that would be available for the given configuration regardless of it being tiled, with some exceptions.</span></span>

</dd> <dt>

<span data-ttu-id="73f18-121"><span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**Unterstützte samplede SC (Multisample count, Quality)**</span><span class="sxs-lookup"><span data-stu-id="73f18-121"><span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**Supported SampleDesc (Multisample count, quality)**</span></span>
</dt> <dd>

<span data-ttu-id="73f18-122">Unabhängig davon, was für die jeweilige Konfiguration unterstützt wird, mit einigen Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="73f18-122">Whatever would be supported for the given configuration regardless of it being tiled, with some exceptions.</span></span>

</dd> <dt>

<span data-ttu-id="73f18-123"><span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Unterstützte Breite/Höhe/miplevels/arraySize**</span><span class="sxs-lookup"><span data-stu-id="73f18-123"><span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Supported Width/Height/MipLevels/ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="73f18-124">Vollständige Blöcke, die von Direct3D 11 unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="73f18-124">Full extents supported by Direct3D 11.</span></span> <span data-ttu-id="73f18-125">Bei gekachelten Ressourcen gibt es keine Einschränkung der Gesamtspeicher Größe, die für nicht gekachelte Ressourcen erhoben wird.</span><span class="sxs-lookup"><span data-stu-id="73f18-125">Tiled resources don't have the restriction on total memory size imposed on non-tiled resources.</span></span> <span data-ttu-id="73f18-126">Gekachelte Ressourcen werden nur durch die Grenzen des gesamten virtuellen Adressraums eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="73f18-126">Tiled resources are only constrained by overall virtual address space limits.</span></span> <span data-ttu-id="73f18-127">Weitere Informationen finden Sie unter [Adressraum verfügbar für Kachel Ressourcen](address-space-available-for-tiled-resources.md).</span><span class="sxs-lookup"><span data-stu-id="73f18-127">For info, see [Address space available for tiled resources](address-space-available-for-tiled-resources.md).</span></span>

</dd> </dl>

<span data-ttu-id="73f18-128">Der ursprüngliche Inhalt des Kachel Pool Arbeitsspeichers ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="73f18-128">The initial contents of tile pool memory are undefined.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73f18-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="73f18-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73f18-130">Erstellen von Kachel Ressourcen</span><span class="sxs-lookup"><span data-stu-id="73f18-130">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




