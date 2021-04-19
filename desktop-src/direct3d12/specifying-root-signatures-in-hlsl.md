---
title: Festlegen von Stammsignaturen in HLSL
description: Die Angabe von Stammsignaturen im HLSL-Shadermodell 5.1 ist eine Alternative zur Angabe in C++-Code.
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dad0da9f84d68fc1acbf53332d1cae4075f0faa
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492282"
---
# <a name="specifying-root-signatures-in-hlsl"></a><span data-ttu-id="4989e-103">Festlegen von Stammsignaturen in HLSL</span><span class="sxs-lookup"><span data-stu-id="4989e-103">Specifying Root Signatures in HLSL</span></span>

<span data-ttu-id="4989e-104">Das Angeben von Stammsignaturen im HLSL-Shadermodell 5.1 ist eine Alternative zur Angabe in C++-Code.</span><span class="sxs-lookup"><span data-stu-id="4989e-104">Specifying root signatures in HLSL Shader Model 5.1 is an alternative to specifying them in C++ code.</span></span>

-   [<span data-ttu-id="4989e-105">Ein Beispiel für eine HLSL-Stammsignatur</span><span class="sxs-lookup"><span data-stu-id="4989e-105">An example HLSL Root Signature</span></span>](#an-example-hlsl-root-signature)
    -   [<span data-ttu-id="4989e-106">Root Signature Version 1.0</span><span class="sxs-lookup"><span data-stu-id="4989e-106">Root Signature Version 1.0</span></span>](#root-signature-version-10)
    -   [<span data-ttu-id="4989e-107">Stammsignatur, Version 1.1</span><span class="sxs-lookup"><span data-stu-id="4989e-107">Root Signature Version 1.1</span></span>](#root-signature-version-11)
-   [<span data-ttu-id="4989e-108">RootFlags</span><span class="sxs-lookup"><span data-stu-id="4989e-108">RootFlags</span></span>](#rootflags)
-   [<span data-ttu-id="4989e-109">Stammkonst constants</span><span class="sxs-lookup"><span data-stu-id="4989e-109">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="4989e-110">Sichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="4989e-110">Visibility</span></span>](#visibility)
-   [<span data-ttu-id="4989e-111">CBV auf Stammebene</span><span class="sxs-lookup"><span data-stu-id="4989e-111">Root-level CBV</span></span>](#root-level-cbv)
-   [<span data-ttu-id="4989e-112">SRV auf Stammebene</span><span class="sxs-lookup"><span data-stu-id="4989e-112">Root-level SRV</span></span>](#root-level-srv)
-   [<span data-ttu-id="4989e-113">UAV auf Stammebene</span><span class="sxs-lookup"><span data-stu-id="4989e-113">Root-level UAV</span></span>](#root-level-uav)
-   [<span data-ttu-id="4989e-114">Deskriptortabelle</span><span class="sxs-lookup"><span data-stu-id="4989e-114">Descriptor Table</span></span>](#descriptor-table)
-   [<span data-ttu-id="4989e-115">Statischer Sampler</span><span class="sxs-lookup"><span data-stu-id="4989e-115">Static Sampler</span></span>](#static-sampler)
-   [<span data-ttu-id="4989e-116">Kompilieren einer HLSL-Stammsignatur</span><span class="sxs-lookup"><span data-stu-id="4989e-116">Compiling an HLSL root signature</span></span>](#compiling-an-hlsl-root-signature)
-   [<span data-ttu-id="4989e-117">Bearbeiten von Stammsignaturen mit dem FXC-Compiler</span><span class="sxs-lookup"><span data-stu-id="4989e-117">Manipulating root signatures with the FXC compiler</span></span>](#manipulating-root-signatures-with-the-fxc-compiler)
-   [<span data-ttu-id="4989e-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4989e-118">Notes</span></span>](#notes)
-   [<span data-ttu-id="4989e-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4989e-119">Related topics</span></span>](#related-topics)

## <a name="an-example-hlsl-root-signature"></a><span data-ttu-id="4989e-120">Beispiel für eine HLSL-Stammsignatur</span><span class="sxs-lookup"><span data-stu-id="4989e-120">An example HLSL Root Signature</span></span>

<span data-ttu-id="4989e-121">Eine Stammsignatur kann in HLSL als Zeichenfolge angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4989e-121">A root signature can be specified in HLSL as a string.</span></span> <span data-ttu-id="4989e-122">Die Zeichenfolge enthält eine Auflistung von durch Komma getrennten Klauseln, die die Komponenten der Stammsignatur beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4989e-122">The string contains a collection of comma-separated clauses that describe root signature constituent components.</span></span> <span data-ttu-id="4989e-123">Die Stammsignatur sollte über Shader hinweg für jedes Pipelinezustandsobjekt (PSO) identisch sein.</span><span class="sxs-lookup"><span data-stu-id="4989e-123">The root signature should be identical across shaders for any one pipeline state object (PSO).</span></span> <span data-ttu-id="4989e-124">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4989e-124">Here is an example:</span></span>

### <a name="root-signature-version-10"></a><span data-ttu-id="4989e-125">Root Signature Version 1.0</span><span class="sxs-lookup"><span data-stu-id="4989e-125">Root Signature Version 1.0</span></span>

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1), " \
              "SRV(t0), " \
              "UAV(u0, visibility = SHADER_VISIBILITY_GEOMETRY), " \
              "DescriptorTable( CBV(b0), " \
                               "UAV(u1, numDescriptors = 2), " \
                               "SRV(t1, numDescriptors = unbounded)), " \
              "DescriptorTable(Sampler(s0, numDescriptors = 2)), " \
              "RootConstants(num32BitConstants=1, b9), " \
              "DescriptorTable( UAV(u3), " \
                               "UAV(u4), " \
                               "UAV(u5, offset=1)), " \

              "StaticSampler(s2)," \
              "StaticSampler(s3, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

<span data-ttu-id="4989e-126">Diese Definition würde die folgende Stammsignatur enthalten, und es wird Folgendes notieren:</span><span class="sxs-lookup"><span data-stu-id="4989e-126">This definition would give the following root signature, noting:</span></span>

-   <span data-ttu-id="4989e-127">Die Verwendung von Standardparametern.</span><span class="sxs-lookup"><span data-stu-id="4989e-127">The use of default parameters.</span></span>
-   <span data-ttu-id="4989e-128">b0 und (b0, space=1) verursachen keinen Konflikt</span><span class="sxs-lookup"><span data-stu-id="4989e-128">b0 and (b0, space=1) do not conflict</span></span>
-   <span data-ttu-id="4989e-129">u0 ist nur für den Geometrie-Shader sichtbar.</span><span class="sxs-lookup"><span data-stu-id="4989e-129">u0 is only visible to the geometry shader</span></span>
-   <span data-ttu-id="4989e-130">u4 und u5 werden mit dem gleichen Deskriptor in einem Heap als Alias verwendet.</span><span class="sxs-lookup"><span data-stu-id="4989e-130">u4 and u5 are aliased to the same descriptor in a heap</span></span>

![Eine Stammsignatur, die mithilfe der Shadersprache auf hoher Ebene angegeben wird](images/hlsl-root-signature.png)

### <a name="root-signature-version-11"></a><span data-ttu-id="4989e-132">Stammsignatur, Version 1.1</span><span class="sxs-lookup"><span data-stu-id="4989e-132">Root Signature Version 1.1</span></span>

<span data-ttu-id="4989e-133">[Root Signature Version 1.1](root-signature-version-1-1.md) ermöglicht Treiberoptimierungen für Stammsignaturdeskriptoren und -daten.</span><span class="sxs-lookup"><span data-stu-id="4989e-133">[Root Signature Version 1.1](root-signature-version-1-1.md) enables driver optimizations on root signature descriptors and data.</span></span>

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1, flags = DATA_STATIC), " \
              "SRV(t0), " \
              "UAV(u0), " \
              "DescriptorTable( CBV(b1), " \
                               "SRV(t1, numDescriptors = 8, " \
                               "        flags = DESCRIPTORS_VOLATILE), " \
                               "UAV(u1, numDescriptors = unbounded, " \
                               "        flags = DESCRIPTORS_VOLATILE)), " \
              "DescriptorTable(Sampler(s0, space=1, numDescriptors = 4)), " \
              "RootConstants(num32BitConstants=3, b10), " \
              "StaticSampler(s1)," \
              "StaticSampler(s2, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

<span data-ttu-id="4989e-134">Die HLSL-Stammsignatursprache entspricht eng den C++-Stammsignatur-APIs und verfügt über eine entsprechende Ausdrucksstärke.</span><span class="sxs-lookup"><span data-stu-id="4989e-134">The HLSL root signature language closely corresponds to the C++ root signature APIs and has equivalent expressive power.</span></span> <span data-ttu-id="4989e-135">Die Stammsignatur wird als Sequenz von Klauseln angegeben, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="4989e-135">The root signature is specified as a sequence of clauses, separated by comma.</span></span> <span data-ttu-id="4989e-136">Die Reihenfolge der Klauseln ist wichtig, da die Reihenfolge der Analyse die Slotposition in der Stammsignatur bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4989e-136">The order of clauses is important, as the order of parsing determines the slot position in the root signature.</span></span> <span data-ttu-id="4989e-137">Jede Klausel nimmt einen oder mehrere benannte Parameter an.</span><span class="sxs-lookup"><span data-stu-id="4989e-137">Each clause takes one or more named parameters.</span></span> <span data-ttu-id="4989e-138">Die Reihenfolge der Parameter ist jedoch nicht wichtig.</span><span class="sxs-lookup"><span data-stu-id="4989e-138">The order of parameters is not important, however.</span></span>

## <a name="rootflags"></a><span data-ttu-id="4989e-139">RootFlags</span><span class="sxs-lookup"><span data-stu-id="4989e-139">RootFlags</span></span>

<span data-ttu-id="4989e-140">Die optionale *RootFlags-Klausel* verwendet entweder 0 (der Standardwert, um keine Flags anzugeben) oder einen oder mehrere vordefinierte Stammflagswerte, die über den \| OR ''-Operator verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="4989e-140">The optional *RootFlags* clause takes either 0 (the default value to indicate no flags), or one or several of predefined root flags values, connected via the OR ‘\|’ operator.</span></span> <span data-ttu-id="4989e-141">Die zulässigen Stammflagwerte werden durch [**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)definiert.</span><span class="sxs-lookup"><span data-stu-id="4989e-141">The allowed root flag values are defined by [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

<span data-ttu-id="4989e-142">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4989e-142">For example:</span></span>

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a><span data-ttu-id="4989e-143">Stammkonstanten</span><span class="sxs-lookup"><span data-stu-id="4989e-143">Root Constants</span></span>

<span data-ttu-id="4989e-144">Die *RootConstants-Klausel* gibt Stammkonstanten in der Stammsignatur an.</span><span class="sxs-lookup"><span data-stu-id="4989e-144">The *RootConstants* clause specifies root constants in the root signature.</span></span> <span data-ttu-id="4989e-145">Zwei obligatorische Parameter sind: *num32BitConstants* und *bReg* (das Register, das *BaseShaderRegister* in C++-APIs entspricht) des *Cbuffers*.</span><span class="sxs-lookup"><span data-stu-id="4989e-145">Two mandatory parameters are: *num32BitConstants* and *bReg* (the register corresponding to *BaseShaderRegister* in C++ APIs) of the *cbuffer*.</span></span> <span data-ttu-id="4989e-146">Die Parameter space (*RegisterSpace* in C++-APIs) und visibility (*ShaderVisibility* in C++) sind optional, und die Standardwerte lauten:</span><span class="sxs-lookup"><span data-stu-id="4989e-146">The space (*RegisterSpace* in C++ APIs) and visibility (*ShaderVisibility* in C++) parameters are optional, and the default values are:</span></span>

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

<span data-ttu-id="4989e-147">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4989e-147">For example:</span></span>

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a><span data-ttu-id="4989e-148">Sicht</span><span class="sxs-lookup"><span data-stu-id="4989e-148">Visibility</span></span>

<span data-ttu-id="4989e-149">Visibility ist ein optionaler Parameter, der einen der Werte aus [**D3D12 \_ SHADER \_ VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="4989e-149">Visibility is an optional parameter that can have one of the values from [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

<span data-ttu-id="4989e-150">SHADER \_ VISIBILITY \_ ALL überträgt die Stammargumente an alle Shader.</span><span class="sxs-lookup"><span data-stu-id="4989e-150">SHADER\_VISIBILITY\_ALL broadcasts the root arguments to all shaders.</span></span> <span data-ttu-id="4989e-151">Bei einigen Hardwarekomponenten sind dies keine Kosten, aber auf anderer Hardware entstehen Kosten für das Verzweigen der Daten in alle Shaderstufen.</span><span class="sxs-lookup"><span data-stu-id="4989e-151">On some hardware this has no cost, but on other hardware there is a cost to fork the data to all the shader stages.</span></span> <span data-ttu-id="4989e-152">Durch festlegen einer der Optionen, z. B. SHADER VISIBILITY VERTEX, wird das Stammargument auf \_ \_ eine einzelne Shaderstufe beschränkt.</span><span class="sxs-lookup"><span data-stu-id="4989e-152">Setting one of the options, such as SHADER\_VISIBILITY\_VERTEX, limits the root argument to a single shader stage.</span></span>

<span data-ttu-id="4989e-153">Das Festlegen von Stammargumenten auf einzelne Shaderstufen ermöglicht die Verwendung desselben Bindungsnamens in verschiedenen Phasen.</span><span class="sxs-lookup"><span data-stu-id="4989e-153">Setting root arguments to single shader stages allows the same bind name to be used at different stages.</span></span> <span data-ttu-id="4989e-154">Beispielsweise wäre eine SRV-Bindung von `t0,SHADER_VISIBILITY_VERTEX` und eine SRV-Bindung `t0,SHADER_VISIBILITY_PIXEL` von gültig.</span><span class="sxs-lookup"><span data-stu-id="4989e-154">For example, an SRV binding of `t0,SHADER_VISIBILITY_VERTEX` and SRV binding of `t0,SHADER_VISIBILITY_PIXEL` would be valid.</span></span> <span data-ttu-id="4989e-155">Wenn die Sichtbarkeitseinstellung jedoch `t0,SHADER_VISIBILITY_ALL` für eine der Bindungen verwendet wird, wäre die Stammsignatur ungültig.</span><span class="sxs-lookup"><span data-stu-id="4989e-155">But if the visibility setting was `t0,SHADER_VISIBILITY_ALL` for one of the bindings, the root signature would be invalid.</span></span>

## <a name="root-level-cbv"></a><span data-ttu-id="4989e-156">CBV auf Stammebene</span><span class="sxs-lookup"><span data-stu-id="4989e-156">Root-level CBV</span></span>

<span data-ttu-id="4989e-157">Die `CBV` -Klausel (konstante Pufferansicht) gibt einen konstanten Puffer auf Stammebene an, der den Reg-Eintrag b-register enthält.</span><span class="sxs-lookup"><span data-stu-id="4989e-157">The `CBV` (constant buffer view) clause specifies a root-level constant buffer b-register Reg entry.</span></span> <span data-ttu-id="4989e-158">Beachten Sie, dass dies ein skalarer Eintrag ist. Es ist nicht möglich, einen Bereich für die Stammebene anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4989e-158">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a><span data-ttu-id="4989e-159">SRV auf Stammebene</span><span class="sxs-lookup"><span data-stu-id="4989e-159">Root-level SRV</span></span>

<span data-ttu-id="4989e-160">Die `SRV` -Klausel (Shaderressourcenansicht) gibt einen SRV-Eintrag auf Stammebene t-register Reg an.</span><span class="sxs-lookup"><span data-stu-id="4989e-160">The `SRV` (shader resource view) clause specifies a root-level SRV t-register Reg entry.</span></span> <span data-ttu-id="4989e-161">Beachten Sie, dass dies ein skalarer Eintrag ist. Es ist nicht möglich, einen Bereich für die Stammebene anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4989e-161">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a><span data-ttu-id="4989e-162">UAV auf Stammebene</span><span class="sxs-lookup"><span data-stu-id="4989e-162">Root-level UAV</span></span>

<span data-ttu-id="4989e-163">Die `UAV` -Klausel (ungeordnete Zugriffsansicht) gibt einen UAV-u-register Reg-Eintrag auf Stammebene an.</span><span class="sxs-lookup"><span data-stu-id="4989e-163">The `UAV` (unordered access view) clause specifies a root-level UAV u-register Reg entry.</span></span> <span data-ttu-id="4989e-164">Beachten Sie, dass dies ein skalarer Eintrag ist. Es ist nicht möglich, einen Bereich für die Stammebene anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4989e-164">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="4989e-165">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4989e-165">For example:</span></span>

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a><span data-ttu-id="4989e-166">Deskriptortabelle</span><span class="sxs-lookup"><span data-stu-id="4989e-166">Descriptor Table</span></span>

<span data-ttu-id="4989e-167">Die -Klausel selbst ist eine Liste von durch Komma getrennten Deskriptortabellenklauseln sowie ein `DescriptorTable` optionaler Sichtbarkeitsparameter.</span><span class="sxs-lookup"><span data-stu-id="4989e-167">The `DescriptorTable` clause is itself a list of comma-separated descriptor table clauses, as well as an optional visibility parameter.</span></span> <span data-ttu-id="4989e-168">Die *DescriptorTable-Klauseln* umfassen CBV, SRV, UAV und Sampler.</span><span class="sxs-lookup"><span data-stu-id="4989e-168">The *DescriptorTable* clauses include CBV, SRV, UAV, and Sampler.</span></span> <span data-ttu-id="4989e-169">Beachten Sie, dass sich ihre Parameter von denen der Klauseln auf Stammebene unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="4989e-169">Note that their parameters differ from those of the root-level clauses.</span></span>

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

<span data-ttu-id="4989e-170">Die Deskriptortabelle `CBV` hat die folgende Syntax:</span><span class="sxs-lookup"><span data-stu-id="4989e-170">The Descriptor Table `CBV` has the following syntax:</span></span>

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="4989e-171">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4989e-171">For example:</span></span>

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

<span data-ttu-id="4989e-172">Der obligatorische Parameter *bReg* gibt den Start-Reg des cbuffer-Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="4989e-172">The mandatory parameter *bReg* specifies the start Reg of the cbuffer range.</span></span> <span data-ttu-id="4989e-173">Der *numDescriptors-Parameter* gibt die Anzahl der Deskriptoren im zusammenhängenden Cbufferbereich an. Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="4989e-173">The *numDescriptors* parameter specifies the number of descriptors in the contiguous cbuffer range; the default value being 1.</span></span> <span data-ttu-id="4989e-174">Der Eintrag deklariert einen Cbufferbereich, ` [Reg, Reg + numDescriptors - 1]` wenn *numDescriptors* eine Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="4989e-174">The entry declares a cbuffer range` [Reg, Reg + numDescriptors - 1]`, when *numDescriptors* is a number.</span></span> <span data-ttu-id="4989e-175">Wenn *numDescriptors* gleich "unbounded" ist, lautet der Bereich `[Reg, UINT_MAX]` , was bedeutet, dass die App sicherstellen muss, dass sie nicht auf einen Bereich außerhalb der Grenzen verweist.</span><span class="sxs-lookup"><span data-stu-id="4989e-175">If *numDescriptors* is equal to "unbounded", the range is `[Reg, UINT_MAX]`, which means the app must ensure it is not referencing an out-of-bounds area.</span></span> <span data-ttu-id="4989e-176">Das *Offsetfeld* stellt den *OffsetInDescriptorsFromTableStart-Parameter* in den C++-APIs dar, d. h. den Offset (in Deskriptoren) vom Anfang der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4989e-176">The *offset* field represents the *OffsetInDescriptorsFromTableStart* parameter in the C++ APIs, that is, the offset (in descriptors) from the start of the table.</span></span> <span data-ttu-id="4989e-177">Wenn der Offset auf DESCRIPTOR \_ RANGE \_ OFFSET APPEND \_ (Standardeinstellung) festgelegt ist, bedeutet dies, dass der Bereich direkt nach dem vorherigen Bereich liegt.</span><span class="sxs-lookup"><span data-stu-id="4989e-177">If the offset is set to DESCRIPTOR\_RANGE\_OFFSET\_APPEND (the default), it means the range is directly after the previous range.</span></span> <span data-ttu-id="4989e-178">Durch die Eingabe bestimmter Offsets können sich Bereiche jedoch überlappen, sodass Registeraliasing möglich ist.</span><span class="sxs-lookup"><span data-stu-id="4989e-178">However, entering specific offsets does allow for ranges to overlap each other, allowing register aliasing.</span></span>

<span data-ttu-id="4989e-179">Die Deskriptortabelle `SRV` weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="4989e-179">The Descriptor Table `SRV` has the following syntax:</span></span>

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="4989e-180">Dies ähnelt dem `CBV` Deskriptortabelleneintrag, mit dem Unterschied, dass der angegebene Bereich für Shaderressourcenansichten gilt.</span><span class="sxs-lookup"><span data-stu-id="4989e-180">This is similar to the descriptor table `CBV` entry, except the specified range is for shader resource views.</span></span>

<span data-ttu-id="4989e-181">Die Deskriptortabelle `UAV` weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="4989e-181">The Descriptor Table `UAV` has the following syntax:</span></span>

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="4989e-182">Dies ähnelt dem `CBV` Deskriptortabelleneintrag, mit dem Unterschied, dass der angegebene Bereich für unsortierte Zugriffsansichten gilt.</span><span class="sxs-lookup"><span data-stu-id="4989e-182">This is similar to the descriptor table `CBV` entry, except the specified range is for unordered access views.</span></span>

<span data-ttu-id="4989e-183">Die Deskriptortabelle `Sampler` weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="4989e-183">The Descriptor Table `Sampler` has the following syntax:</span></span>

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

<span data-ttu-id="4989e-184">Dies ähnelt dem `CBV` Deskriptortabelleneintrag, mit dem Unterschied, dass der angegebene Bereich für Shader-Sampler gilt.</span><span class="sxs-lookup"><span data-stu-id="4989e-184">This is similar to the descriptor table `CBV` entry, except the specified range is for shader samplers.</span></span> <span data-ttu-id="4989e-185">Beachten Sie, dass Sampler nicht mit anderen Deskriptortypen in derselben Deskriptortabelle kombiniert werden können (da sie sich in einem separaten Deskriptorheap befinden).</span><span class="sxs-lookup"><span data-stu-id="4989e-185">Note that Samplers can’t be mixed with other types of descriptors in the same descriptor table (since they are in a separate descriptor heap).</span></span>

## <a name="static-sampler"></a><span data-ttu-id="4989e-186">Statischer Sampler</span><span class="sxs-lookup"><span data-stu-id="4989e-186">Static Sampler</span></span>

<span data-ttu-id="4989e-187">Der statische Sampler stellt die [**D3D12 \_ STATIC \_ SAMPLER \_ DESC-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) dar.</span><span class="sxs-lookup"><span data-stu-id="4989e-187">The static sampler represents the [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span> <span data-ttu-id="4989e-188">Der obligatorische Parameter für *StaticSampler* ist ein Skalar, Sampler s-register Reg. Andere Parameter sind mit den unten gezeigten Standardwerten optional.</span><span class="sxs-lookup"><span data-stu-id="4989e-188">The mandatory parameter for *StaticSampler* is a scalar, sampler s-register Reg. Other parameters are optional with default values shown below.</span></span> <span data-ttu-id="4989e-189">Die meisten Felder akzeptieren einen Satz vordefinierter Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="4989e-189">Most fields accept a set of predefined enums.</span></span>

``` syntax
StaticSampler( sReg,
              [ filter = FILTER_ANISOTROPIC, 
                addressU = TEXTURE_ADDRESS_WRAP,
                addressV = TEXTURE_ADDRESS_WRAP,
                addressW = TEXTURE_ADDRESS_WRAP,
                mipLODBias = 0.f,
                maxAnisotropy = 16,
                comparisonFunc = COMPARISON_LESS_EQUAL,
                borderColor = STATIC_BORDER_COLOR_OPAQUE_WHITE,
                minLOD = 0.f,         
                maxLOD = 3.402823466e+38f,
                space = 0, 
                visibility = SHADER_VISIBILITY_ALL ])
```

<span data-ttu-id="4989e-190">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4989e-190">For example:</span></span>

``` syntax
StaticSampler(s4, filter=FILTER_MIN_MAG_MIP_LINEAR)
```

<span data-ttu-id="4989e-191">Die Parameteroptionen ähneln den C++-API-Aufrufen sehr, mit Ausnahme von *borderColor*, das auf eine Enumeration in HLSL beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="4989e-191">The parameter options are very similar to the C++ API calls, except for *borderColor*, which is restricted to an enum in HLSL.</span></span>

<span data-ttu-id="4989e-192">Das Filterfeld kann eines von [**D3D12 \_ FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)sein.</span><span class="sxs-lookup"><span data-stu-id="4989e-192">The filter field can be one of [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).</span></span>

<span data-ttu-id="4989e-193">Die Adressfelder können jeweils eines von [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode)sein.</span><span class="sxs-lookup"><span data-stu-id="4989e-193">The address fields can each be one of [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).</span></span>

<span data-ttu-id="4989e-194">Die Vergleichsfunktion kann eine von [**D3D12 \_ COMPARISON \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)sein.</span><span class="sxs-lookup"><span data-stu-id="4989e-194">The comparison function can be one of [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).</span></span>

<span data-ttu-id="4989e-195">Das Rahmenfarbfeld kann [**D3D12 \_ STATIC BORDER COLOR \_ \_ sein.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color)</span><span class="sxs-lookup"><span data-stu-id="4989e-195">The border color field can be one of [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).</span></span>

<span data-ttu-id="4989e-196">Sichtbarkeit kann [**D3D12 \_ SHADER \_ VISIBILITY sein.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)</span><span class="sxs-lookup"><span data-stu-id="4989e-196">Visibility can be one of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

## <a name="compiling-an-hlsl-root-signature"></a><span data-ttu-id="4989e-197">Kompilieren einer HLSL-Stammsignatur</span><span class="sxs-lookup"><span data-stu-id="4989e-197">Compiling an HLSL root signature</span></span>

<span data-ttu-id="4989e-198">Es gibt zwei Mechanismen zum Kompilieren einer HLSL-Stammsignatur.</span><span class="sxs-lookup"><span data-stu-id="4989e-198">There are two mechanisms to compile an HLSL root signature.</span></span> <span data-ttu-id="4989e-199">Erstens ist es möglich, eine Stammsignaturzeichenfolge über das *RootSignature-Attribut* an einen bestimmten Shader anfügen (im folgenden Beispiel mithilfe des **MyRS1-Einstiegspunkts):**</span><span class="sxs-lookup"><span data-stu-id="4989e-199">First, it is possible to attach a root signature string to a particular shader via the *RootSignature* attribute (in the following example, using the **MyRS1** entry point):</span></span>

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

<span data-ttu-id="4989e-200">Der Compiler erstellt und überprüft das Stammsignaturblob für den Shader und bettet es zusammen mit dem Shader-Bytecode in das Shaderblob ein.</span><span class="sxs-lookup"><span data-stu-id="4989e-200">The compiler will create and verify the root signature blob for the shader and embed it alongside the shader byte code into the shader blob.</span></span> <span data-ttu-id="4989e-201">Der Compiler unterstützt die Stammsignatursyntax für Shadermodell 5.0 und höher.</span><span class="sxs-lookup"><span data-stu-id="4989e-201">The compiler supports root signature syntax for shader model 5.0 and higher.</span></span> <span data-ttu-id="4989e-202">Wenn eine Stammsignatur in einen Shadermodell 5.0-Shader eingebettet ist und dieser Shader im Gegensatz zu D3D12 an die D3D11-Runtime gesendet wird, wird der Stammsignaturteil automatisch von D3D11 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="4989e-202">If a root signature is embedded in a shader model 5.0 shader and that shader is sent to the D3D11 runtime, as opposed to D3D12, the root signature portion will get silently ignored by D3D11.</span></span>

<span data-ttu-id="4989e-203">Der andere Mechanismus besteht in der Erstellung eines eigenständigen Stammsignaturblobs, um es möglicherweise mit einer großen Gruppe von Shadern wiederzuverwenden, um Speicherplatz zu sparen.</span><span class="sxs-lookup"><span data-stu-id="4989e-203">The other mechanism is to create a standalone root signature blob, perhaps to reuse it with a large set of shaders, saving space.</span></span> <span data-ttu-id="4989e-204">Das [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC) unterstützt **sowohl rootsig \_ 1 \_ 0-** als auch **rootsig \_ 1 1-Shadermodelle. \_**</span><span class="sxs-lookup"><span data-stu-id="4989e-204">The [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC) supports both **rootsig\_1\_0** and **rootsig\_1\_1** shader models.</span></span> <span data-ttu-id="4989e-205">Der Name der definierenden Zeichenfolge wird über das übliche /E-Argument angegeben.</span><span class="sxs-lookup"><span data-stu-id="4989e-205">The name of the define string is specified via the usual /E argument.</span></span> <span data-ttu-id="4989e-206">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4989e-206">For example:</span></span>

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

<span data-ttu-id="4989e-207">Beachten Sie, dass die Definition der Stammsignaturzeichenfolge auch über die Befehlszeile übergeben werden kann, z.B. /D MyRS1="...".</span><span class="sxs-lookup"><span data-stu-id="4989e-207">Note that the root signature string define can also be passed on the command line, e.g, /D MyRS1=”…”.</span></span>

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a><span data-ttu-id="4989e-208">Bearbeiten von Stammsignaturen mit dem FXC-Compiler</span><span class="sxs-lookup"><span data-stu-id="4989e-208">Manipulating root signatures with the FXC compiler</span></span>

<span data-ttu-id="4989e-209">Der FXC-Compiler erstellt Shader-Bytecode aus HLSL-Quelldateien.</span><span class="sxs-lookup"><span data-stu-id="4989e-209">The FXC compiler creates shader byte-code from HLSL source files.</span></span> <span data-ttu-id="4989e-210">Es gibt viele optionale Parameter für diesen Compiler. Weitere Informationen finden Sie im [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc).</span><span class="sxs-lookup"><span data-stu-id="4989e-210">There are a lot of optional parameters for this compiler, refer to the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc).</span></span>

<span data-ttu-id="4989e-211">Die folgende Tabelle enthält einige Beispiele für die Verwendung von FXC für die Verwaltung von von HLSL-Stammsignaturen.</span><span class="sxs-lookup"><span data-stu-id="4989e-211">For managing HLSL authored root signatures, the following table gives some examples of using FXC.</span></span>



| <span data-ttu-id="4989e-212">Linie</span><span class="sxs-lookup"><span data-stu-id="4989e-212">Line</span></span> | <span data-ttu-id="4989e-213">Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="4989e-213">Command line</span></span>                                                                 | <span data-ttu-id="4989e-214">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4989e-214">Description</span></span>                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4989e-215">1</span><span class="sxs-lookup"><span data-stu-id="4989e-215">1</span></span>    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | <span data-ttu-id="4989e-216">Kompiliert einen Shader für das Pixel-Shader 5.1-Ziel. Die Shaderquelle befindet sich in der Datei shaderWithRootSig.hlsl, die eine Stammsignatur enthält.</span><span class="sxs-lookup"><span data-stu-id="4989e-216">Compiles a shader for the pixel shader 5.1 target, the shader source is in the shaderWithRootSig.hlsl file, which includes a root signature.</span></span> <span data-ttu-id="4989e-217">Der Shader und die Stammsignatur werden als separate Blobs in der Binärdatei rs1.fxo kompiliert.</span><span class="sxs-lookup"><span data-stu-id="4989e-217">The shader and root signature are compiled as separate blobs in the rs1.fxo binary file.</span></span>    |
| <span data-ttu-id="4989e-218">2</span><span class="sxs-lookup"><span data-stu-id="4989e-218">2</span></span>    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | <span data-ttu-id="4989e-219">Extrahiert die Stammsignatur aus der von Zeile 1 erstellten Datei, sodass die Datei rs1.rs.fxo nur eine Stammsignatur enthält.</span><span class="sxs-lookup"><span data-stu-id="4989e-219">Extracts the root signature from the file created by line 1, so the rs1.rs.fxo file contains just a root signature.</span></span>                                                                                                                      |
| <span data-ttu-id="4989e-220">3</span><span class="sxs-lookup"><span data-stu-id="4989e-220">3</span></span>    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | <span data-ttu-id="4989e-221">Entfernt die Stammsignatur aus der durch Zeile 1 erstellten Datei, sodass die Datei rs1.stripped.fxo einen Shader ohne Stammsignatur enthält.</span><span class="sxs-lookup"><span data-stu-id="4989e-221">Removes the root signature from the file created by line 1, so the rs1.stripped.fxo file contains a shader with no root signature.</span></span>                                                                                                       |
| <span data-ttu-id="4989e-222">4</span><span class="sxs-lookup"><span data-stu-id="4989e-222">4</span></span>    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | <span data-ttu-id="4989e-223">Kombiniert einen Shader und eine Stammsignatur, die sich in separaten Dateien befinden, in einer Binärdatei, die beide Blobs enthält.</span><span class="sxs-lookup"><span data-stu-id="4989e-223">Combines a shader and root signature that are in separate files into a binary file containing both blobs.</span></span> <span data-ttu-id="4989e-224">In diesem Beispiel wäre rs1.new.fx0 mit rs1.fx0 in Zeile 1 identisch.</span><span class="sxs-lookup"><span data-stu-id="4989e-224">In this example rs1.new.fx0 would be identical to rs1.fx0 in line 1.</span></span>                                                           |
| <span data-ttu-id="4989e-225">5</span><span class="sxs-lookup"><span data-stu-id="4989e-225">5</span></span>    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | <span data-ttu-id="4989e-226">Erstellt eine eigenständige Stammsignaturbinärdatei aus einer Quelle, die mehr als nur eine Stammsignatur enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="4989e-226">Creates a stand-alone root signature binary file from a source that may contain more than just a root signature.</span></span> <span data-ttu-id="4989e-227">Beachten Sie das \_ Rootig 1 \_ 0-Ziel, und dass RS1 der Name der Stammsignatur \# (definieren) Makrozeichenfolge in der HLSL-Datei ist.</span><span class="sxs-lookup"><span data-stu-id="4989e-227">Note the rootsig\_1\_0 target, and that RS1 is the name of the root signature (\#define) macro string in the HLSL file.</span></span> |



 

<span data-ttu-id="4989e-228">Die über FXC verfügbare Funktionalität ist auch programmgesteuert mithilfe der [**D3DCompile-Funktion**](/windows/desktop/direct3dhlsl/d3dcompile) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4989e-228">The functionality available through FXC is also available programmatically using the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) function.</span></span> <span data-ttu-id="4989e-229">Mit diesem Aufruf wird ein Shader mit einer Stammsignatur oder einer eigenständigen Stammsignatur kompiliert (wobei das \_ Rootig-Ziel auf 1 0 festgelegt \_ wird).</span><span class="sxs-lookup"><span data-stu-id="4989e-229">This call compiles a shader with a root signature, or stand-alone root signature (setting the rootsig\_1\_0 target).</span></span> <span data-ttu-id="4989e-230">[**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) und [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) können Stammsignaturen extrahieren und an ein vorhandenes Blob anfügen.</span><span class="sxs-lookup"><span data-stu-id="4989e-230">[**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) and [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) can extract and attach root signatures to an existing blob.</span></span>  <span data-ttu-id="4989e-231">D3D \_ BLOB ROOT SIGNATURE wird \_ \_ verwendet, um den Stammsignatur-Blobteiltyp anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4989e-231">D3D\_BLOB\_ROOT\_SIGNATURE is used to specify the root signature blob part type.</span></span> <span data-ttu-id="4989e-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) entfernt die Stammsignatur (mithilfe des D3DCOMPILER \_ STRIP \_ ROOT \_ SIGNATURE-Flags) aus dem Blob.</span><span class="sxs-lookup"><span data-stu-id="4989e-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) removes the root signature (using the D3DCOMPILER\_STRIP\_ROOT\_SIGNATURE flag) from the blob.</span></span>

## <a name="notes"></a><span data-ttu-id="4989e-233">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4989e-233">Notes</span></span>

> [!Note]  
> <span data-ttu-id="4989e-234">Während die Offlinekompilierung von Shadern dringend empfohlen wird, wenn Shader zur Laufzeit kompiliert werden müssen, lesen Sie die Hinweise für [**D3DCompile2.**](/windows/desktop/direct3dhlsl/d3dcompile2)</span><span class="sxs-lookup"><span data-stu-id="4989e-234">Whereas the offline compilation of shaders is strongly recommended, if shaders have to be compiled at runtime, refer to the remarks for [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).</span></span>

 

> [!Note]  
> <span data-ttu-id="4989e-235">Vorhandene HLSL-Ressourcen müssen nicht geändert werden, um Stammsignaturen zu verarbeiten, die mit ihnen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4989e-235">Existing HLSL assets do not need to be changed to handle root signatures to be used with them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4989e-236">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4989e-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4989e-237">Dynamische Indizierung mit HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="4989e-237">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[<span data-ttu-id="4989e-238">HLSL Shader Model 5.1 Features for Direct3D 12 (HLSL-Shadermodell 5.1-Features für Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="4989e-238">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="4989e-239">Ressourcenbindung</span><span class="sxs-lookup"><span data-stu-id="4989e-239">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="4989e-240">Ressourcenbindung in HLSL</span><span class="sxs-lookup"><span data-stu-id="4989e-240">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="4989e-241">Stammsignaturen</span><span class="sxs-lookup"><span data-stu-id="4989e-241">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="4989e-242">Shadermodell 5.1</span><span class="sxs-lookup"><span data-stu-id="4989e-242">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="4989e-243">Von Shader festgelegter Schablonenreferenzwert</span><span class="sxs-lookup"><span data-stu-id="4989e-243">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
</dt> <dt>

[<span data-ttu-id="4989e-244">Typisiertes Laden von ungeordneten Zugriffsansichten</span><span class="sxs-lookup"><span data-stu-id="4989e-244">Typed Unordered Access View Loads</span></span>](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 
