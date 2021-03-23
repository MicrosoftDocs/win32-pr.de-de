---
title: Angeben von Stamm Signaturen in HLSL
description: Das Angeben von Stamm Signaturen im HLSL-Shader-Modell 5,1 ist eine Alternative zur Angabe in C++-Code.
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236876e22c3e1e0bb849ec1e1bc7d45692c900d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548641"
---
# <a name="specifying-root-signatures-in-hlsl"></a><span data-ttu-id="82d68-103">Angeben von Stamm Signaturen in HLSL</span><span class="sxs-lookup"><span data-stu-id="82d68-103">Specifying Root Signatures in HLSL</span></span>

<span data-ttu-id="82d68-104">Das Angeben von Stamm Signaturen im HLSL-Shader-Modell 5,1 ist eine Alternative zur Angabe in C++-Code.</span><span class="sxs-lookup"><span data-stu-id="82d68-104">Specifying root signatures in HLSL Shader Model 5.1 is an alternative to specifying them in C++ code.</span></span>

-   [<span data-ttu-id="82d68-105">Ein Beispiel für eine HLSL-Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="82d68-105">An example HLSL Root Signature</span></span>](#an-example-hlsl-root-signature)
    -   [<span data-ttu-id="82d68-106">Stamm Signatur Version 1,0</span><span class="sxs-lookup"><span data-stu-id="82d68-106">Root Signature Version 1.0</span></span>](#root-signature-version-10)
    -   [<span data-ttu-id="82d68-107">Stamm Signatur Version 1,1</span><span class="sxs-lookup"><span data-stu-id="82d68-107">Root Signature Version 1.1</span></span>](#root-signature-version-11)
-   [<span data-ttu-id="82d68-108">RootFlags</span><span class="sxs-lookup"><span data-stu-id="82d68-108">RootFlags</span></span>](#rootflags)
-   [<span data-ttu-id="82d68-109">Stamm Konstanten</span><span class="sxs-lookup"><span data-stu-id="82d68-109">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="82d68-110">Sichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="82d68-110">Visibility</span></span>](#visibility)
-   [<span data-ttu-id="82d68-111">CBV auf Stamm Ebene</span><span class="sxs-lookup"><span data-stu-id="82d68-111">Root-level CBV</span></span>](#root-level-cbv)
-   [<span data-ttu-id="82d68-112">SRV auf Stamm Ebene</span><span class="sxs-lookup"><span data-stu-id="82d68-112">Root-level SRV</span></span>](#root-level-srv)
-   [<span data-ttu-id="82d68-113">UAV auf Stamm Ebene</span><span class="sxs-lookup"><span data-stu-id="82d68-113">Root-level UAV</span></span>](#root-level-uav)
-   [<span data-ttu-id="82d68-114">Deskriptortabelle</span><span class="sxs-lookup"><span data-stu-id="82d68-114">Descriptor Table</span></span>](#descriptor-table)
-   [<span data-ttu-id="82d68-115">Statischer Sampler</span><span class="sxs-lookup"><span data-stu-id="82d68-115">Static Sampler</span></span>](#static-sampler)
-   [<span data-ttu-id="82d68-116">Kompilieren einer HLSL-Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="82d68-116">Compiling an HLSL root signature</span></span>](#compiling-an-hlsl-root-signature)
-   [<span data-ttu-id="82d68-117">Manipulieren von Stamm Signaturen mit dem FXC-Compiler</span><span class="sxs-lookup"><span data-stu-id="82d68-117">Manipulating root signatures with the FXC compiler</span></span>](#manipulating-root-signatures-with-the-fxc-compiler)
-   [<span data-ttu-id="82d68-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="82d68-118">Notes</span></span>](#notes)
-   [<span data-ttu-id="82d68-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="82d68-119">Related topics</span></span>](#related-topics)

## <a name="an-example-hlsl-root-signature"></a><span data-ttu-id="82d68-120">Ein Beispiel für eine HLSL-Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="82d68-120">An example HLSL Root Signature</span></span>

<span data-ttu-id="82d68-121">Eine Stamm Signatur kann in HLSL als Zeichenfolge angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="82d68-121">A root signature can be specified in HLSL as a string.</span></span> <span data-ttu-id="82d68-122">Die Zeichenfolge enthält eine Auflistung von durch Kommas getrennten Klauseln, die Komponenten der Stamm Signatur Komponenten beschreiben.</span><span class="sxs-lookup"><span data-stu-id="82d68-122">The string contains a collection of comma-separated clauses that describe root signature constituent components.</span></span> <span data-ttu-id="82d68-123">Die Stamm Signatur sollte für alle einzelnen Pipeline Zustands Objekte (PSO) über Shader hinweg identisch sein.</span><span class="sxs-lookup"><span data-stu-id="82d68-123">The root signature should be identical across shaders for any one pipeline state object (PSO).</span></span> <span data-ttu-id="82d68-124">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="82d68-124">Here is an example:</span></span>

### <a name="root-signature-version-10"></a><span data-ttu-id="82d68-125">Stamm Signatur Version 1,0</span><span class="sxs-lookup"><span data-stu-id="82d68-125">Root Signature Version 1.0</span></span>

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

### <a name="root-signature-version-11"></a><span data-ttu-id="82d68-126">Stamm Signatur Version 1,1</span><span class="sxs-lookup"><span data-stu-id="82d68-126">Root Signature Version 1.1</span></span>

<span data-ttu-id="82d68-127">Die Stamm [Signatur Version 1,1](root-signature-version-1-1.md) ermöglicht Treiber Optimierungen für Stamm Signatur Deskriptoren und-Daten.</span><span class="sxs-lookup"><span data-stu-id="82d68-127">[Root Signature Version 1.1](root-signature-version-1-1.md) enables driver optimizations on root signature descriptors and data.</span></span>

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

<span data-ttu-id="82d68-128">Diese Definition hat die folgende Stamm Signatur:</span><span class="sxs-lookup"><span data-stu-id="82d68-128">This definition would give the following root signature, noting:</span></span>

-   <span data-ttu-id="82d68-129">Die Verwendung von Standardparametern.</span><span class="sxs-lookup"><span data-stu-id="82d68-129">The use of default parameters.</span></span>
-   <span data-ttu-id="82d68-130">B0 und (B0, Space = 1) treten nicht in Konflikt</span><span class="sxs-lookup"><span data-stu-id="82d68-130">b0 and (b0, space=1) do not conflict</span></span>
-   <span data-ttu-id="82d68-131">U0 ist nur für den Geometry-Shader sichtbar.</span><span class="sxs-lookup"><span data-stu-id="82d68-131">u0 is only visible to the geometry shader</span></span>
-   <span data-ttu-id="82d68-132">U4 und U5 werden mit dem gleichen Deskriptor in einem Heap versehen</span><span class="sxs-lookup"><span data-stu-id="82d68-132">u4 and u5 are aliased to the same descriptor in a heap</span></span>

![eine mit der High-Level-Shader-Sprache angegebene Stamm Signatur](images/hlsl-root-signature.png)

<span data-ttu-id="82d68-134">Die HLSL-Stamm Signatur Sprache entspricht eng den C++-Stamm Signatur-APIs und verfügt über äquivalente Ausdrucksstärke.</span><span class="sxs-lookup"><span data-stu-id="82d68-134">The HLSL root signature language closely corresponds to the C++ root signature APIs and has equivalent expressive power.</span></span> <span data-ttu-id="82d68-135">Die Stamm Signatur wird als Sequenz von Klauseln angegeben, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="82d68-135">The root signature is specified as a sequence of clauses, separated by comma.</span></span> <span data-ttu-id="82d68-136">Die Reihenfolge der Klauseln ist wichtig, da die Reihenfolge der Verarbeitung die slotposition in der Stamm Signatur bestimmt.</span><span class="sxs-lookup"><span data-stu-id="82d68-136">The order of clauses is important, as the order of parsing determines the slot position in the root signature.</span></span> <span data-ttu-id="82d68-137">Jede Klausel nimmt einen oder mehrere benannte Parameter an.</span><span class="sxs-lookup"><span data-stu-id="82d68-137">Each clause takes one or more named parameters.</span></span> <span data-ttu-id="82d68-138">Die Reihenfolge der Parameter ist jedoch nicht wichtig.</span><span class="sxs-lookup"><span data-stu-id="82d68-138">The order of parameters is not important, however.</span></span>

## <a name="rootflags"></a><span data-ttu-id="82d68-139">RootFlags</span><span class="sxs-lookup"><span data-stu-id="82d68-139">RootFlags</span></span>

<span data-ttu-id="82d68-140">Die optionale *rootFlags* -Klausel nimmt entweder 0 (der Standardwert, um keine Flags anzugeben) oder einen oder mehrere vordefinierte stammflags-Werte an, die über den-Operator oder den-Operator verbunden sind \| .</span><span class="sxs-lookup"><span data-stu-id="82d68-140">The optional *RootFlags* clause takes either 0 (the default value to indicate no flags), or one or several of predefined root flags values, connected via the OR ‘\|’ operator.</span></span> <span data-ttu-id="82d68-141">Die zulässigen stammflag-Werte werden durch [**D3D12 \_ root \_ Signature- \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)definiert.</span><span class="sxs-lookup"><span data-stu-id="82d68-141">The allowed root flag values are defined by [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

<span data-ttu-id="82d68-142">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="82d68-142">For example:</span></span>

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a><span data-ttu-id="82d68-143">Stamm Konstanten</span><span class="sxs-lookup"><span data-stu-id="82d68-143">Root Constants</span></span>

<span data-ttu-id="82d68-144">Die *rootconstants* -Klausel gibt Stamm Konstanten in der Stamm Signatur an.</span><span class="sxs-lookup"><span data-stu-id="82d68-144">The *RootConstants* clause specifies root constants in the root signature.</span></span> <span data-ttu-id="82d68-145">Zwei obligatorische Parameter sind: *num32BitConstants* und *Breg* (das Register, das *baseshaderregister* in C++-APIs entspricht) des *cBuffer*.</span><span class="sxs-lookup"><span data-stu-id="82d68-145">Two mandatory parameters are: *num32BitConstants* and *bReg* (the register corresponding to *BaseShaderRegister* in C++ APIs) of the *cbuffer*.</span></span> <span data-ttu-id="82d68-146">Die Parameter Space (*registerspace* in C++ APIs) und Visibility (*shadervisibility* in C++) sind optional, und die Standardwerte lauten:</span><span class="sxs-lookup"><span data-stu-id="82d68-146">The space (*RegisterSpace* in C++ APIs) and visibility (*ShaderVisibility* in C++) parameters are optional, and the default values are:</span></span>

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

<span data-ttu-id="82d68-147">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="82d68-147">For example:</span></span>

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a><span data-ttu-id="82d68-148">Sicht</span><span class="sxs-lookup"><span data-stu-id="82d68-148">Visibility</span></span>

<span data-ttu-id="82d68-149">Visibility ist ein optionaler Parameter, der einen der Werte aus [**D3D12 \_ Shader \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="82d68-149">Visibility is an optional parameter that can have one of the values from [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

<span data-ttu-id="82d68-150">Shader \_ Visibility \_ überträgt alle Stamm Argumente an alle Shader.</span><span class="sxs-lookup"><span data-stu-id="82d68-150">SHADER\_VISIBILITY\_ALL broadcasts the root arguments to all shaders.</span></span> <span data-ttu-id="82d68-151">Bei manchen Hardwarekosten fallen keine Kosten an, aber auf anderer Hardware entstehen Kosten für die Verzweigung der Daten in allen shaderphasen.</span><span class="sxs-lookup"><span data-stu-id="82d68-151">On some hardware this has no cost, but on other hardware there is a cost to fork the data to all the shader stages.</span></span> <span data-ttu-id="82d68-152">Wenn Sie eine der Optionen festlegen, z. b. Shader \_ Visibility \_ Vertex, schränkt das Root-Argument auf eine einzelne Shader-Stufe ein.</span><span class="sxs-lookup"><span data-stu-id="82d68-152">Setting one of the options, such as SHADER\_VISIBILITY\_VERTEX, limits the root argument to a single shader stage.</span></span>

<span data-ttu-id="82d68-153">Durch das Festlegen von Stamm Argumenten auf einzelne Shader-Stufen kann derselbe Bindungs Name in verschiedenen Phasen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82d68-153">Setting root arguments to single shader stages allows the same bind name to be used at different stages.</span></span> <span data-ttu-id="82d68-154">Beispielsweise wäre eine SRV-Bindung von `t0,SHADER_VISIBILITY_VERTEX` und SRV-Bindung von `t0,SHADER_VISIBILITY_PIXEL` gültig.</span><span class="sxs-lookup"><span data-stu-id="82d68-154">For example, an SRV binding of `t0,SHADER_VISIBILITY_VERTEX` and SRV binding of `t0,SHADER_VISIBILITY_PIXEL` would be valid.</span></span> <span data-ttu-id="82d68-155">Wenn die Sichtbarkeits Einstellung jedoch `t0,SHADER_VISIBILITY_ALL` für eine der Bindungen gilt, wäre die Stamm Signatur ungültig.</span><span class="sxs-lookup"><span data-stu-id="82d68-155">But if the visibility setting was `t0,SHADER_VISIBILITY_ALL` for one of the bindings, the root signature would be invalid.</span></span>

## <a name="root-level-cbv"></a><span data-ttu-id="82d68-156">CBV auf Stamm Ebene</span><span class="sxs-lookup"><span data-stu-id="82d68-156">Root-level CBV</span></span>

<span data-ttu-id="82d68-157">Die `CBV` (Konstante Puffer Ansicht)-Klausel gibt einen konstanten Puffer b-Register-reg-Eintrag auf Stamm Ebene an.</span><span class="sxs-lookup"><span data-stu-id="82d68-157">The `CBV` (constant buffer view) clause specifies a root-level constant buffer b-register Reg entry.</span></span> <span data-ttu-id="82d68-158">Beachten Sie, dass es sich hierbei um einen skalaren Eintrag handelt. Es ist nicht möglich, einen Bereich für die Stamm Ebene anzugeben.</span><span class="sxs-lookup"><span data-stu-id="82d68-158">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a><span data-ttu-id="82d68-159">SRV auf Stamm Ebene</span><span class="sxs-lookup"><span data-stu-id="82d68-159">Root-level SRV</span></span>

<span data-ttu-id="82d68-160">Die `SRV` (Shader Resource View)-Klausel gibt einen SRV t-Register-reg-Eintrag auf Stamm Ebene an.</span><span class="sxs-lookup"><span data-stu-id="82d68-160">The `SRV` (shader resource view) clause specifies a root-level SRV t-register Reg entry.</span></span> <span data-ttu-id="82d68-161">Beachten Sie, dass es sich hierbei um einen skalaren Eintrag handelt. Es ist nicht möglich, einen Bereich für die Stamm Ebene anzugeben.</span><span class="sxs-lookup"><span data-stu-id="82d68-161">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a><span data-ttu-id="82d68-162">UAV auf Stamm Ebene</span><span class="sxs-lookup"><span data-stu-id="82d68-162">Root-level UAV</span></span>

<span data-ttu-id="82d68-163">Die `UAV` (unsortierter Zugriffs Ansicht)-Klausel gibt einen UAV-Registrierungs Eintrag auf Stamm Ebene an.</span><span class="sxs-lookup"><span data-stu-id="82d68-163">The `UAV` (unordered access view) clause specifies a root-level UAV u-register Reg entry.</span></span> <span data-ttu-id="82d68-164">Beachten Sie, dass es sich hierbei um einen skalaren Eintrag handelt. Es ist nicht möglich, einen Bereich für die Stamm Ebene anzugeben.</span><span class="sxs-lookup"><span data-stu-id="82d68-164">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="82d68-165">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="82d68-165">For example:</span></span>

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a><span data-ttu-id="82d68-166">Deskriptortabelle</span><span class="sxs-lookup"><span data-stu-id="82d68-166">Descriptor Table</span></span>

<span data-ttu-id="82d68-167">Die- `DescriptorTable` Klausel ist selbst eine Liste von durch Trennzeichen getrennten deskriptortabellenklauseln und ein optionaler Visibility-Parameter.</span><span class="sxs-lookup"><span data-stu-id="82d68-167">The `DescriptorTable` clause is itself a list of comma-separated descriptor table clauses, as well as an optional visibility parameter.</span></span> <span data-ttu-id="82d68-168">Die *deskriptortable* -Klauseln umfassen CBV, SRV, UAV und Sampler.</span><span class="sxs-lookup"><span data-stu-id="82d68-168">The *DescriptorTable* clauses include CBV, SRV, UAV, and Sampler.</span></span> <span data-ttu-id="82d68-169">Beachten Sie, dass sich Ihre Parameter von denen der Klauseln der Stamm Ebene unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="82d68-169">Note that their parameters differ from those of the root-level clauses.</span></span>

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

<span data-ttu-id="82d68-170">Die Deskriptortabelle `CBV` weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="82d68-170">The Descriptor Table `CBV` has the following syntax:</span></span>

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="82d68-171">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="82d68-171">For example:</span></span>

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

<span data-ttu-id="82d68-172">Der obligatorische Parameter *Breg* gibt die Start-reg des cBuffer-Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="82d68-172">The mandatory parameter *bReg* specifies the start Reg of the cbuffer range.</span></span> <span data-ttu-id="82d68-173">Der *numdescriptors* -Parameter gibt die Anzahl der Deskriptoren im zusammenhängenden cBuffer-Bereich an. der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="82d68-173">The *numDescriptors* parameter specifies the number of descriptors in the contiguous cbuffer range; the default value being 1.</span></span> <span data-ttu-id="82d68-174">Der-Eintrag deklariert einen cBuffer-Bereich ` [Reg, Reg + numDescriptors - 1]` , wenn *numdescriptors* eine Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="82d68-174">The entry declares a cbuffer range` [Reg, Reg + numDescriptors - 1]`, when *numDescriptors* is a number.</span></span> <span data-ttu-id="82d68-175">Wenn *numdescriptors* gleich "unbegrenzt" ist, ist der Bereich. dies `[Reg, UINT_MAX]` bedeutet, dass die APP sicherstellen muss, dass Sie nicht auf einen Out-of-Bounds-Bereich verweist.</span><span class="sxs-lookup"><span data-stu-id="82d68-175">If *numDescriptors* is equal to "unbounded", the range is `[Reg, UINT_MAX]`, which means the app must ensure it is not referencing an out-of-bounds area.</span></span> <span data-ttu-id="82d68-176">Das *Offset* Feld stellt den *offsetindescriptorsfromtablestart* -Parameter in den C++-APIs dar, d. h. den Offset (in den Deskriptoren) vom Beginn der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="82d68-176">The *offset* field represents the *OffsetInDescriptorsFromTableStart* parameter in the C++ APIs, that is, the offset (in descriptors) from the start of the table.</span></span> <span data-ttu-id="82d68-177">Wenn der Offset auf den Wert des deskriptorbereichoffsets angefügt wird \_ \_ \_ (Standardeinstellung), bedeutet dies, dass sich der Bereich direkt hinter dem vorherigen Bereich befindet.</span><span class="sxs-lookup"><span data-stu-id="82d68-177">If the offset is set to DESCRIPTOR\_RANGE\_OFFSET\_APPEND (the default), it means the range is directly after the previous range.</span></span> <span data-ttu-id="82d68-178">Durch die Eingabe bestimmter Offsets können sich Bereiche jedoch untereinander überlappen, was das Registrieren von Aliasing ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="82d68-178">However, entering specific offsets does allow for ranges to overlap each other, allowing register aliasing.</span></span>

<span data-ttu-id="82d68-179">Die Deskriptortabelle `SRV` weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="82d68-179">The Descriptor Table `SRV` has the following syntax:</span></span>

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="82d68-180">Dies ähnelt dem `CBV` deskriptortabelleneintrag, mit dem Unterschied, dass der angegebene Bereich für Shader-Ressourcen Sichten gilt.</span><span class="sxs-lookup"><span data-stu-id="82d68-180">This is similar to the descriptor table `CBV` entry, except the specified range is for shader resource views.</span></span>

<span data-ttu-id="82d68-181">Die Deskriptortabelle `UAV` weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="82d68-181">The Descriptor Table `UAV` has the following syntax:</span></span>

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="82d68-182">Dies ähnelt dem `CBV` deskriptortabelleneintrag, mit dem Unterschied, dass der angegebene Bereich für ungeordnete Zugriffs Sichten gilt.</span><span class="sxs-lookup"><span data-stu-id="82d68-182">This is similar to the descriptor table `CBV` entry, except the specified range is for unordered access views.</span></span>

<span data-ttu-id="82d68-183">Die Deskriptortabelle `Sampler` weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="82d68-183">The Descriptor Table `Sampler` has the following syntax:</span></span>

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

<span data-ttu-id="82d68-184">Dies ähnelt dem `CBV` deskriptortabelleneintrag, mit dem Unterschied, dass der angegebene Bereich für Shader-Samplers ist.</span><span class="sxs-lookup"><span data-stu-id="82d68-184">This is similar to the descriptor table `CBV` entry, except the specified range is for shader samplers.</span></span> <span data-ttu-id="82d68-185">Beachten Sie, dass Samplers nicht mit anderen Typen von Deskriptoren in derselben Deskriptortabelle gemischt werden können (da Sie sich in einem separaten deskriptorheap befinden).</span><span class="sxs-lookup"><span data-stu-id="82d68-185">Note that Samplers can’t be mixed with other types of descriptors in the same descriptor table (since they are in a separate descriptor heap).</span></span>

## <a name="static-sampler"></a><span data-ttu-id="82d68-186">Statischer Sampler</span><span class="sxs-lookup"><span data-stu-id="82d68-186">Static Sampler</span></span>

<span data-ttu-id="82d68-187">Der statische Sampler stellt die [**statische D3D12- \_ \_ \_ samplerstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) dar.</span><span class="sxs-lookup"><span data-stu-id="82d68-187">The static sampler represents the [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span> <span data-ttu-id="82d68-188">Der obligatorische Parameter für *staticsampler* ist ein Skalar, Sampler s-Register reg. Andere Parameter sind optional, wobei die Standardwerte unten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="82d68-188">The mandatory parameter for *StaticSampler* is a scalar, sampler s-register Reg. Other parameters are optional with default values shown below.</span></span> <span data-ttu-id="82d68-189">Die meisten Felder akzeptieren eine Reihe vordefinierter enums.</span><span class="sxs-lookup"><span data-stu-id="82d68-189">Most fields accept a set of predefined enums.</span></span>

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

<span data-ttu-id="82d68-190">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="82d68-190">For example:</span></span>

``` syntax
StaticSampler(s4, filter=FILTER_MIN_MAG_MIP_LINEAR)
```

<span data-ttu-id="82d68-191">Die Parameter Optionen ähneln den C++-API-aufrufen, ausgenommen *BorderColor*, das auf eine Enumeration in HLSL beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="82d68-191">The parameter options are very similar to the C++ API calls, except for *borderColor*, which is restricted to an enum in HLSL.</span></span>

<span data-ttu-id="82d68-192">Das Filter Feld kann einen der [**\_ Filter "D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="82d68-192">The filter field can be one of [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).</span></span>

<span data-ttu-id="82d68-193">Die Adressfelder können jeweils einen der [**D3D12- \_ Textur \_ Adress \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode)aufweisen.</span><span class="sxs-lookup"><span data-stu-id="82d68-193">The address fields can each be one of [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).</span></span>

<span data-ttu-id="82d68-194">Bei der Vergleichsfunktion kann es sich um einen [**D3D12 \_ Vergleichs \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)handeln.</span><span class="sxs-lookup"><span data-stu-id="82d68-194">The comparison function can be one of [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).</span></span>

<span data-ttu-id="82d68-195">Das Rahmen Farbfeld kann eine der [**statischen Rahmen \_ \_ \_ Farben D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color)sein.</span><span class="sxs-lookup"><span data-stu-id="82d68-195">The border color field can be one of [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).</span></span>

<span data-ttu-id="82d68-196">Sichtbarkeit kann eine der [**D3D12- \_ Shader- \_ Sichtbarkeit**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)sein.</span><span class="sxs-lookup"><span data-stu-id="82d68-196">Visibility can be one of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

## <a name="compiling-an-hlsl-root-signature"></a><span data-ttu-id="82d68-197">Kompilieren einer HLSL-Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="82d68-197">Compiling an HLSL root signature</span></span>

<span data-ttu-id="82d68-198">Es gibt zwei Mechanismen zum Kompilieren einer HLSL-Stamm Signatur.</span><span class="sxs-lookup"><span data-stu-id="82d68-198">There are two mechanisms to compile an HLSL root signature.</span></span> <span data-ttu-id="82d68-199">Zunächst ist es möglich, eine Stamm Signatur Zeichenfolge über das *rootsignature* -Attribut an einen bestimmten Shader anzufügen (im folgenden Beispiel mit dem **MyRS1** -Einstiegspunkt):</span><span class="sxs-lookup"><span data-stu-id="82d68-199">First, it is possible to attach a root signature string to a particular shader via the *RootSignature* attribute (in the following example, using the **MyRS1** entry point):</span></span>

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

<span data-ttu-id="82d68-200">Der Compiler erstellt und überprüft das Stamm Signatur-BLOB für den Shader und bettet ihn zusammen mit dem Shader-Bytecode in das Shader-BLOB ein.</span><span class="sxs-lookup"><span data-stu-id="82d68-200">The compiler will create and verify the root signature blob for the shader and embed it alongside the shader byte code into the shader blob.</span></span> <span data-ttu-id="82d68-201">Der Compiler unterstützt die Stamm Signatur Syntax für das Shader-Modell 5,0 und höher.</span><span class="sxs-lookup"><span data-stu-id="82d68-201">The compiler supports root signature syntax for shader model 5.0 and higher.</span></span> <span data-ttu-id="82d68-202">Wenn eine Stamm Signatur in ein Shader-Modell 5,0-Shader eingebettet ist und dieser Shader an die D3D11-Laufzeit gesendet wird (im Gegensatz zu D3D12), wird der Stamm Signatur Teil von D3D11 automatisch ignoriert.</span><span class="sxs-lookup"><span data-stu-id="82d68-202">If a root signature is embedded in a shader model 5.0 shader and that shader is sent to the D3D11 runtime, as opposed to D3D12, the root signature portion will get silently ignored by D3D11.</span></span>

<span data-ttu-id="82d68-203">Der andere Mechanismus besteht darin, einen eigenständigen Stamm Signatur-BLOB zu erstellen, um ihn ggf. mit einem großen Satz von Shadern wiederzuverwenden und Speicherplatz zu sparen.</span><span class="sxs-lookup"><span data-stu-id="82d68-203">The other mechanism is to create a standalone root signature blob, perhaps to reuse it with a large set of shaders, saving space.</span></span> <span data-ttu-id="82d68-204">Das [Effekt-Compilertool](/windows/desktop/direct3dtools/fxc) (FXC) unterstützt sowohl **rootsig \_ 1 \_ 0** -als auch **rootsig \_ 1 \_ 1** -shadermodelle.</span><span class="sxs-lookup"><span data-stu-id="82d68-204">The [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC) supports both **rootsig\_1\_0** and **rootsig\_1\_1** shader models.</span></span> <span data-ttu-id="82d68-205">Der Name der definierenden Zeichenfolge wird über das übliche/E-Argument angegeben.</span><span class="sxs-lookup"><span data-stu-id="82d68-205">The name of the define string is specified via the usual /E argument.</span></span> <span data-ttu-id="82d68-206">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="82d68-206">For example:</span></span>

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

<span data-ttu-id="82d68-207">Beachten Sie, dass die Definition der Stamm Signatur Zeichenfolge auch in der Befehlszeile weitergegeben werden kann, z. b./D MyRS1 = "...".</span><span class="sxs-lookup"><span data-stu-id="82d68-207">Note that the root signature string define can also be passed on the command line, e.g, /D MyRS1=”…”.</span></span>

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a><span data-ttu-id="82d68-208">Manipulieren von Stamm Signaturen mit dem FXC-Compiler</span><span class="sxs-lookup"><span data-stu-id="82d68-208">Manipulating root signatures with the FXC compiler</span></span>

<span data-ttu-id="82d68-209">Der FXC-Compiler erstellt Shader-Bytecode aus HLSL-Quelldateien.</span><span class="sxs-lookup"><span data-stu-id="82d68-209">The FXC compiler creates shader byte-code from HLSL source files.</span></span> <span data-ttu-id="82d68-210">Es gibt zahlreiche optionale Parameter für diesen Compiler. Weitere Informationen finden Sie im [Tool "Effect-Compiler](/windows/desktop/direct3dtools/fxc)".</span><span class="sxs-lookup"><span data-stu-id="82d68-210">There are a lot of optional parameters for this compiler, refer to the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc).</span></span>

<span data-ttu-id="82d68-211">In der folgenden Tabelle finden Sie einige Beispiele für die Verwendung von FXC zum Verwalten von erstellten HLSL-Stamm Signaturen.</span><span class="sxs-lookup"><span data-stu-id="82d68-211">For managing HLSL authored root signatures, the following table gives some examples of using FXC.</span></span>



| <span data-ttu-id="82d68-212">Linie</span><span class="sxs-lookup"><span data-stu-id="82d68-212">Line</span></span> | <span data-ttu-id="82d68-213">Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="82d68-213">Command line</span></span>                                                                 | <span data-ttu-id="82d68-214">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="82d68-214">Description</span></span>                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82d68-215">1</span><span class="sxs-lookup"><span data-stu-id="82d68-215">1</span></span>    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | <span data-ttu-id="82d68-216">Kompiliert einen Shader für das Pixel-Shader 5,1-Ziel, die Shader-Quelle befindet sich in der Datei "shaderwithrootsig. HLSL", die eine Stamm Signatur enthält.</span><span class="sxs-lookup"><span data-stu-id="82d68-216">Compiles a shader for the pixel shader 5.1 target, the shader source is in the shaderWithRootSig.hlsl file, which includes a root signature.</span></span> <span data-ttu-id="82d68-217">Der Shader und die Stamm Signatur werden als separate BLOBs in der Binärdatei "RS1. FXO" kompiliert.</span><span class="sxs-lookup"><span data-stu-id="82d68-217">The shader and root signature are compiled as separate blobs in the rs1.fxo binary file.</span></span>    |
| <span data-ttu-id="82d68-218">2</span><span class="sxs-lookup"><span data-stu-id="82d68-218">2</span></span>    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | <span data-ttu-id="82d68-219">Extrahiert die Stamm Signatur aus der von Zeile 1 erstellten Datei, sodass die Datei "RS1. Rs. FXO" nur eine Stamm Signatur enthält.</span><span class="sxs-lookup"><span data-stu-id="82d68-219">Extracts the root signature from the file created by line 1, so the rs1.rs.fxo file contains just a root signature.</span></span>                                                                                                                      |
| <span data-ttu-id="82d68-220">3</span><span class="sxs-lookup"><span data-stu-id="82d68-220">3</span></span>    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | <span data-ttu-id="82d68-221">Entfernt die Stamm Signatur aus der von Zeile 1 erstellten Datei, sodass die Datei "RS1. entfernt. FXO" einen Shader ohne Stamm Signatur enthält.</span><span class="sxs-lookup"><span data-stu-id="82d68-221">Removes the root signature from the file created by line 1, so the rs1.stripped.fxo file contains a shader with no root signature.</span></span>                                                                                                       |
| <span data-ttu-id="82d68-222">4</span><span class="sxs-lookup"><span data-stu-id="82d68-222">4</span></span>    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | <span data-ttu-id="82d68-223">Kombiniert einen Shader und eine Stamm Signatur in separaten Dateien zu einer Binärdatei, die beide BLOB-Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="82d68-223">Combines a shader and root signature that are in separate files into a binary file containing both blobs.</span></span> <span data-ttu-id="82d68-224">In diesem Beispiel ist "RS1. New. fx0" mit "RS1. fx0" in Zeile 1 identisch.</span><span class="sxs-lookup"><span data-stu-id="82d68-224">In this example rs1.new.fx0 would be identical to rs1.fx0 in line 1.</span></span>                                                           |
| <span data-ttu-id="82d68-225">5</span><span class="sxs-lookup"><span data-stu-id="82d68-225">5</span></span>    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | <span data-ttu-id="82d68-226">Erstellt eine eigenständige Stamm Signatur-Binärdatei aus einer Quelle, die möglicherweise mehr als nur eine Stamm Signatur enthält.</span><span class="sxs-lookup"><span data-stu-id="82d68-226">Creates a stand-alone root signature binary file from a source that may contain more than just a root signature.</span></span> <span data-ttu-id="82d68-227">Beachten Sie das Ziel "rootsig \_ 1 \_ 0", und "RS1" ist der Name der Stamm Signatur ( \# define)-Makro Zeichenfolge in der HLSL-Datei.</span><span class="sxs-lookup"><span data-stu-id="82d68-227">Note the rootsig\_1\_0 target, and that RS1 is the name of the root signature (\#define) macro string in the HLSL file.</span></span> |



 

<span data-ttu-id="82d68-228">Die über FXC verfügbare Funktionalität ist auch Programm gesteuert mithilfe der [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) -Funktion verfügbar.</span><span class="sxs-lookup"><span data-stu-id="82d68-228">The functionality available through FXC is also available programmatically using the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) function.</span></span> <span data-ttu-id="82d68-229">Dieser Befehl kompiliert einen Shader mit einer Stamm Signatur oder einer eigenständigen Stamm Signatur (durch Festlegen des rootsig \_ 1 \_ 0-Ziels).</span><span class="sxs-lookup"><span data-stu-id="82d68-229">This call compiles a shader with a root signature, or stand-alone root signature (setting the rootsig\_1\_0 target).</span></span> <span data-ttu-id="82d68-230">[**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) und [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) können Stamm Signaturen extrahieren und an ein vorhandenes BLOB anfügen.</span><span class="sxs-lookup"><span data-stu-id="82d68-230">[**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) and [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) can extract and attach root signatures to an existing blob.</span></span><span data-ttu-id="82d68-231">Die D3D- \_ BLOB-Stamm \_ \_ Signatur wird verwendet, um den teittyp der Stamm Signatur-BLOB anzugeben.</span><span class="sxs-lookup"><span data-stu-id="82d68-231">  D3D\_BLOB\_ROOT\_SIGNATURE is used to specify the root signature blob part type.</span></span> <span data-ttu-id="82d68-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) entfernt die Stamm Signatur (mit dem D3DCOMPILER \_ Strip \_ root \_ Signature-Flag) aus dem BLOB.</span><span class="sxs-lookup"><span data-stu-id="82d68-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) removes the root signature (using the D3DCOMPILER\_STRIP\_ROOT\_SIGNATURE flag) from the blob.</span></span>

## <a name="notes"></a><span data-ttu-id="82d68-233">Hinweise</span><span class="sxs-lookup"><span data-stu-id="82d68-233">Notes</span></span>

> [!Note]  
> <span data-ttu-id="82d68-234">Die Offline Kompilierung von Shadern wird dringend empfohlen, wenn Shader zur Laufzeit kompiliert werden müssen, lesen Sie die Hinweise zu [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).</span><span class="sxs-lookup"><span data-stu-id="82d68-234">Whereas the offline compilation of shaders is strongly recommended, if shaders have to be compiled at runtime, refer to the remarks for [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).</span></span>

 

> [!Note]  
> <span data-ttu-id="82d68-235">Vorhandene HLSL-Assets müssen nicht geändert werden, um die zu verwendenden Stamm Signaturen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="82d68-235">Existing HLSL assets do not need to be changed to handle root signatures to be used with them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="82d68-236">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="82d68-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82d68-237">Dynamische Indizierung mit HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="82d68-237">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[<span data-ttu-id="82d68-238">HLSL-Shader-Modell 5,1 Features für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="82d68-238">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="82d68-239">Ressourcen Bindung</span><span class="sxs-lookup"><span data-stu-id="82d68-239">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="82d68-240">Ressourcen Bindung in HLSL</span><span class="sxs-lookup"><span data-stu-id="82d68-240">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="82d68-241">Stamm Signaturen</span><span class="sxs-lookup"><span data-stu-id="82d68-241">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="82d68-242">Shadermodell 5,1</span><span class="sxs-lookup"><span data-stu-id="82d68-242">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="82d68-243">Von Shader angegebener Schablone-Verweis Wert</span><span class="sxs-lookup"><span data-stu-id="82d68-243">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
</dt> <dt>

[<span data-ttu-id="82d68-244">Typisierte nicht geordnete zugriffsansichts Ladungen</span><span class="sxs-lookup"><span data-stu-id="82d68-244">Typed Unordered Access View Loads</span></span>](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 