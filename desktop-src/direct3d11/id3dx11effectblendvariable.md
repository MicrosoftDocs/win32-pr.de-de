---
title: ID3DX11EffectBlendVariable-Schnittstelle (D3dx11effect. h)
description: Die Blend-Variable-Schnittstelle greift auf Blend-Status zu.
ms.assetid: 8a6e6e7e-2f1e-4e16-8d28-ffc7f3f018d6
keywords:
- ID3DX11EffectBlendVariable-Schnittstelle Direct3D 11
- ID3DX11EffectBlendVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a0a8a3ec0c2a3d92dfc9579fff8b3769dcfc5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961761"
---
# <a name="id3dx11effectblendvariable-interface"></a><span data-ttu-id="f5b86-105">ID3DX11EffectBlendVariable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f5b86-105">ID3DX11EffectBlendVariable interface</span></span>

<span data-ttu-id="f5b86-106">Die Blend-Variable-Schnittstelle greift auf Blend-Status zu.</span><span class="sxs-lookup"><span data-stu-id="f5b86-106">The blend-variable interface accesses blend state.</span></span>

## <a name="members"></a><span data-ttu-id="f5b86-107">Member</span><span class="sxs-lookup"><span data-stu-id="f5b86-107">Members</span></span>

<span data-ttu-id="f5b86-108">Die **ID3DX11EffectBlendVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="f5b86-108">The **ID3DX11EffectBlendVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="f5b86-109">**ID3DX11EffectBlendVariable** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f5b86-109">**ID3DX11EffectBlendVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="f5b86-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="f5b86-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f5b86-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="f5b86-111">Methods</span></span>

<span data-ttu-id="f5b86-112">Die **ID3DX11EffectBlendVariable** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f5b86-112">The **ID3DX11EffectBlendVariable** interface has these methods.</span></span>



| <span data-ttu-id="f5b86-113">Methode</span><span class="sxs-lookup"><span data-stu-id="f5b86-113">Method</span></span>                                                                    | <span data-ttu-id="f5b86-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5b86-114">Description</span></span>                                          |
|:--------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="f5b86-115">**Getbackingstore**</span><span class="sxs-lookup"><span data-stu-id="f5b86-115">**GetBackingStore**</span></span>](id3dx11effectblendvariable-getbackingstore.md)     | <span data-ttu-id="f5b86-116">Einen Zeiger auf eine Blend-State-Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="f5b86-116">Get a pointer to a blend-state variable.</span></span><br/>  |
| [<span data-ttu-id="f5b86-117">**Getblendstate**</span><span class="sxs-lookup"><span data-stu-id="f5b86-117">**GetBlendState**</span></span>](id3dx11effectblendvariable-getblendstate.md)         | <span data-ttu-id="f5b86-118">Einen Zeiger auf eine Blend-State-Schnittstelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="f5b86-118">Get a pointer to a blend-state interface.</span></span><br/> |
| [<span data-ttu-id="f5b86-119">**Setblendstate**</span><span class="sxs-lookup"><span data-stu-id="f5b86-119">**SetBlendState**</span></span>](id3dx11effectblendvariable-setblendstate.md)         | <span data-ttu-id="f5b86-120">Legt den Blend-Status eines Effekts fest.</span><span class="sxs-lookup"><span data-stu-id="f5b86-120">Sets an effect's blend-state.</span></span><br/>             |
| [<span data-ttu-id="f5b86-121">**Undosetblendstate**</span><span class="sxs-lookup"><span data-stu-id="f5b86-121">**UndoSetBlendState**</span></span>](id3dx11effectblendvariable-undosetblendstate.md) | <span data-ttu-id="f5b86-122">Kehrt einen zuvor festgelegten Blend-Status zurück.</span><span class="sxs-lookup"><span data-stu-id="f5b86-122">Reverts a previously set blend-state.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="f5b86-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5b86-123">Remarks</span></span>

<span data-ttu-id="f5b86-124">Eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md) -Schnittstelle wird erstellt, wenn ein Effekt in den Arbeitsspeicher gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="f5b86-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="f5b86-125">Effekt Variablen werden im Sicherungs Speicher im Arbeitsspeicher gespeichert. Wenn eine Technik angewendet wird, werden die Werte im Sicherungs Speicher auf das Gerät kopiert.</span><span class="sxs-lookup"><span data-stu-id="f5b86-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="f5b86-126">Sie können eine dieser Methoden verwenden, um den Status zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="f5b86-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="f5b86-127">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="f5b86-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f5b86-128">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f5b86-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f5b86-129">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f5b86-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5b86-130">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f5b86-130">Requirements</span></span>



| <span data-ttu-id="f5b86-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5b86-131">Requirement</span></span> | <span data-ttu-id="f5b86-132">Wert</span><span class="sxs-lookup"><span data-stu-id="f5b86-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b86-133">Header</span><span class="sxs-lookup"><span data-stu-id="f5b86-133">Header</span></span><br/>  | <dl> <span data-ttu-id="f5b86-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5b86-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f5b86-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f5b86-135">Library</span></span><br/> | <dl> <span data-ttu-id="f5b86-136"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="f5b86-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5b86-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f5b86-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5b86-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="f5b86-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="f5b86-139">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f5b86-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f5b86-140">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f5b86-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





