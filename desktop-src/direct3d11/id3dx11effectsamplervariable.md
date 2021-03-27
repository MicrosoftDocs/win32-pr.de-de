---
title: ID3DX11EffectSamplerVariable-Schnittstelle (D3dx11effect. h)
description: Eine samplerschnittstelle greift auf den samplerstatus
ms.assetid: 8d21f829-2145-45f2-a9b4-2fdc06e0a879
keywords:
- ID3DX11EffectSamplerVariable-Schnittstelle Direct3D 11
- ID3DX11EffectSamplerVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5019022cea823566611410cd6e8fd5013380b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132409"
---
# <a name="id3dx11effectsamplervariable-interface"></a><span data-ttu-id="a7a6e-105">ID3DX11EffectSamplerVariable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a7a6e-105">ID3DX11EffectSamplerVariable interface</span></span>

<span data-ttu-id="a7a6e-106">Eine samplerschnittstelle greift auf den samplerstatus</span><span class="sxs-lookup"><span data-stu-id="a7a6e-106">A sampler interface accesses sampler state.</span></span>

## <a name="members"></a><span data-ttu-id="a7a6e-107">Member</span><span class="sxs-lookup"><span data-stu-id="a7a6e-107">Members</span></span>

<span data-ttu-id="a7a6e-108">Die **ID3DX11EffectSamplerVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="a7a6e-108">The **ID3DX11EffectSamplerVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="a7a6e-109">**ID3DX11EffectSamplerVariable** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a7a6e-109">**ID3DX11EffectSamplerVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="a7a6e-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="a7a6e-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a7a6e-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="a7a6e-111">Methods</span></span>

<span data-ttu-id="a7a6e-112">Die **ID3DX11EffectSamplerVariable** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a7a6e-112">The **ID3DX11EffectSamplerVariable** interface has these methods.</span></span>



| <span data-ttu-id="a7a6e-113">Methode</span><span class="sxs-lookup"><span data-stu-id="a7a6e-113">Method</span></span>                                                                  | <span data-ttu-id="a7a6e-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7a6e-114">Description</span></span>                                                         |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="a7a6e-115">**Getbackingstore**</span><span class="sxs-lookup"><span data-stu-id="a7a6e-115">**GetBackingStore**</span></span>](id3dx11effectsamplervariable-getbackingstore.md) | <span data-ttu-id="a7a6e-116">Einen Zeiger auf eine Variable mit dem samplerstatus erhalten.</span><span class="sxs-lookup"><span data-stu-id="a7a6e-116">Get a pointer to a variable that contains sampler state.</span></span><br/> |
| [<span data-ttu-id="a7a6e-117">**Getsampler**</span><span class="sxs-lookup"><span data-stu-id="a7a6e-117">**GetSampler**</span></span>](id3dx11effectsamplervariable-getsampler.md)           | <span data-ttu-id="a7a6e-118">Einen Zeiger auf eine samplerschnittstelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="a7a6e-118">Get a pointer to a sampler interface.</span></span><br/>                    |
| [<span data-ttu-id="a7a6e-119">**Setsampler**</span><span class="sxs-lookup"><span data-stu-id="a7a6e-119">**SetSampler**</span></span>](id3dx11effectsamplervariable-setsampler.md)           | <span data-ttu-id="a7a6e-120">Festlegen des samplerstatus</span><span class="sxs-lookup"><span data-stu-id="a7a6e-120">Set sampler state.</span></span><br/>                                       |
| [<span data-ttu-id="a7a6e-121">**Undosetsampler**</span><span class="sxs-lookup"><span data-stu-id="a7a6e-121">**UndoSetSampler**</span></span>](id3dx11effectsamplervariable-undosetsampler.md)   | <span data-ttu-id="a7a6e-122">Einen zuvor festgelegten samplerstatus zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="a7a6e-122">Revert a previously set sampler state.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="a7a6e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7a6e-123">Remarks</span></span>

<span data-ttu-id="a7a6e-124">Eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md) -Schnittstelle wird erstellt, wenn ein Effekt in den Arbeitsspeicher gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="a7a6e-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="a7a6e-125">Effekt Variablen werden im Sicherungs Speicher im Arbeitsspeicher gespeichert. Wenn eine Technik angewendet wird, werden die Werte im Sicherungs Speicher auf das Gerät kopiert.</span><span class="sxs-lookup"><span data-stu-id="a7a6e-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="a7a6e-126">Sie können eine dieser Methoden verwenden, um den Status zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="a7a6e-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="a7a6e-127">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="a7a6e-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a7a6e-128">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a7a6e-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a7a6e-129">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a7a6e-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a7a6e-130">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a7a6e-130">Requirements</span></span>



| <span data-ttu-id="a7a6e-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7a6e-131">Requirement</span></span> | <span data-ttu-id="a7a6e-132">Wert</span><span class="sxs-lookup"><span data-stu-id="a7a6e-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a6e-133">Header</span><span class="sxs-lookup"><span data-stu-id="a7a6e-133">Header</span></span><br/>  | <dl> <span data-ttu-id="a7a6e-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7a6e-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a7a6e-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a7a6e-135">Library</span></span><br/> | <dl> <span data-ttu-id="a7a6e-136"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="a7a6e-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7a6e-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a7a6e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7a6e-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="a7a6e-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="a7a6e-139">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a7a6e-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a7a6e-140">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a7a6e-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





