---
title: ID3DX11EffectScalarVariable-Schnittstelle (D3dx11effect. h)
description: Eine Effect-Skalarvariable-Schnittstelle greift auf skalare Werte zu.
ms.assetid: 52e3b856-aa1b-4ed2-b140-7ae96ec1c94b
keywords:
- ID3DX11EffectScalarVariable-Schnittstelle Direct3D 11
- ID3DX11EffectScalarVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d07f0d14ce37f9c84c20564189e1b8475e69887
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219446"
---
# <a name="id3dx11effectscalarvariable-interface"></a><span data-ttu-id="11105-105">ID3DX11EffectScalarVariable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="11105-105">ID3DX11EffectScalarVariable interface</span></span>

<span data-ttu-id="11105-106">Eine Effect-Skalarvariable-Schnittstelle greift auf skalare Werte zu.</span><span class="sxs-lookup"><span data-stu-id="11105-106">An effect-scalar-variable interface accesses scalar values.</span></span>

## <a name="members"></a><span data-ttu-id="11105-107">Member</span><span class="sxs-lookup"><span data-stu-id="11105-107">Members</span></span>

<span data-ttu-id="11105-108">Die **ID3DX11EffectScalarVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="11105-108">The **ID3DX11EffectScalarVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="11105-109">**ID3DX11EffectScalarVariable** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="11105-109">**ID3DX11EffectScalarVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="11105-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="11105-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="11105-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="11105-111">Methods</span></span>

<span data-ttu-id="11105-112">Die **ID3DX11EffectScalarVariable** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="11105-112">The **ID3DX11EffectScalarVariable** interface has these methods.</span></span>



| <span data-ttu-id="11105-113">Methode</span><span class="sxs-lookup"><span data-stu-id="11105-113">Method</span></span>                                                             | <span data-ttu-id="11105-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11105-114">Description</span></span>                                          |
|:-------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="11105-115">**GetBool**</span><span class="sxs-lookup"><span data-stu-id="11105-115">**GetBool**</span></span>](id3dx11effectscalarvariable-getbool.md)             | <span data-ttu-id="11105-116">Eine boolesche Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="11105-116">Get a boolean variable.</span></span><br/>                   |
| [<span data-ttu-id="11105-117">**Getboolarray**</span><span class="sxs-lookup"><span data-stu-id="11105-117">**GetBoolArray**</span></span>](id3dx11effectscalarvariable-getboolarray.md)   | <span data-ttu-id="11105-118">Ein Array von booleschen Variablen erhalten.</span><span class="sxs-lookup"><span data-stu-id="11105-118">Get an array of boolean variables.</span></span><br/>        |
| [<span data-ttu-id="11105-119">**GetFloat**</span><span class="sxs-lookup"><span data-stu-id="11105-119">**GetFloat**</span></span>](id3dx11effectscalarvariable-getfloat.md)           | <span data-ttu-id="11105-120">Eine Gleit Komma Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="11105-120">Get a floating-point variable.</span></span><br/>            |
| [<span data-ttu-id="11105-121">**Getfloatarray**</span><span class="sxs-lookup"><span data-stu-id="11105-121">**GetFloatArray**</span></span>](id3dx11effectscalarvariable-getfloatarray.md) | <span data-ttu-id="11105-122">Ein Array von Gleit Komma Variablen erhalten.</span><span class="sxs-lookup"><span data-stu-id="11105-122">Get an array of floating-point variables.</span></span><br/> |
| [<span data-ttu-id="11105-123">**GetInt**</span><span class="sxs-lookup"><span data-stu-id="11105-123">**GetInt**</span></span>](id3dx11effectscalarvariable-getint.md)               | <span data-ttu-id="11105-124">Eine ganzzahlige Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="11105-124">Get an integer variable.</span></span><br/>                  |
| [<span data-ttu-id="11105-125">**Getintarray**</span><span class="sxs-lookup"><span data-stu-id="11105-125">**GetIntArray**</span></span>](id3dx11effectscalarvariable-getintarray.md)     | <span data-ttu-id="11105-126">Ein Array von ganzzahligen Variablen erhalten.</span><span class="sxs-lookup"><span data-stu-id="11105-126">Get an array of integer variables.</span></span><br/>        |
| [<span data-ttu-id="11105-127">**SetBool**</span><span class="sxs-lookup"><span data-stu-id="11105-127">**SetBool**</span></span>](id3dx11effectscalarvariable-setbool.md)             | <span data-ttu-id="11105-128">Legen Sie eine boolesche Variable fest.</span><span class="sxs-lookup"><span data-stu-id="11105-128">Set a boolean variable.</span></span><br/>                   |
| [<span data-ttu-id="11105-129">**Setboolarray**</span><span class="sxs-lookup"><span data-stu-id="11105-129">**SetBoolArray**</span></span>](id3dx11effectscalarvariable-setboolarray.md)   | <span data-ttu-id="11105-130">Legen Sie ein Array von booleschen Variablen fest.</span><span class="sxs-lookup"><span data-stu-id="11105-130">Set an array of boolean variables.</span></span><br/>        |
| [<span data-ttu-id="11105-131">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="11105-131">**SetFloat**</span></span>](id3dx11effectscalarvariable-setfloat.md)           | <span data-ttu-id="11105-132">Legen Sie eine Gleit Komma Variable fest.</span><span class="sxs-lookup"><span data-stu-id="11105-132">Set a floating-point variable.</span></span><br/>            |
| [<span data-ttu-id="11105-133">**Setfloatarray**</span><span class="sxs-lookup"><span data-stu-id="11105-133">**SetFloatArray**</span></span>](id3dx11effectscalarvariable-setfloatarray.md) | <span data-ttu-id="11105-134">Legen Sie ein Array von Gleit Komma Variablen fest.</span><span class="sxs-lookup"><span data-stu-id="11105-134">Set an array of floating-point variables.</span></span><br/> |
| [<span data-ttu-id="11105-135">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="11105-135">**SetInt**</span></span>](id3dx11effectscalarvariable-setint.md)               | <span data-ttu-id="11105-136">Legen Sie eine Integer-Variable fest.</span><span class="sxs-lookup"><span data-stu-id="11105-136">Set an integer variable.</span></span><br/>                  |
| [<span data-ttu-id="11105-137">**"Tartintarray"**</span><span class="sxs-lookup"><span data-stu-id="11105-137">**SetIntArray**</span></span>](id3dx11effectscalarvariable-setintarray.md)     | <span data-ttu-id="11105-138">Legen Sie ein Array von ganzzahligen Variablen fest.</span><span class="sxs-lookup"><span data-stu-id="11105-138">Set an array of integer variables.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="11105-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11105-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="11105-140">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="11105-140">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="11105-141">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="11105-141">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="11105-142">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="11105-142">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="11105-143">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="11105-143">Requirements</span></span>



| <span data-ttu-id="11105-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11105-144">Requirement</span></span> | <span data-ttu-id="11105-145">Wert</span><span class="sxs-lookup"><span data-stu-id="11105-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11105-146">Header</span><span class="sxs-lookup"><span data-stu-id="11105-146">Header</span></span><br/>  | <dl> <span data-ttu-id="11105-147"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="11105-147"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="11105-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="11105-148">Library</span></span><br/> | <dl> <span data-ttu-id="11105-149"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="11105-149"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11105-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="11105-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11105-151">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="11105-151">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="11105-152">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="11105-152">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="11105-153">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="11105-153">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





