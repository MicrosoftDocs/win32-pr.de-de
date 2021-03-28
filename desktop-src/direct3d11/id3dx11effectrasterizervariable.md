---
title: ID3DX11EffectRasterizerVariable-Schnittstelle (D3dx11effect. h)
description: Eine Raster-Variable-Schnittstelle greift auf den Status des Rasterizers zu.
ms.assetid: d039e3c5-c066-4658-bead-92a5d705ed89
keywords:
- ID3DX11EffectRasterizerVariable-Schnittstelle Direct3D 11
- ID3DX11EffectRasterizerVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a19c5d529d6134ebad238be6e7c6195dc628a7f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996259"
---
# <a name="id3dx11effectrasterizervariable-interface"></a><span data-ttu-id="1237e-105">ID3DX11EffectRasterizerVariable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1237e-105">ID3DX11EffectRasterizerVariable interface</span></span>

<span data-ttu-id="1237e-106">Eine Raster-Variable-Schnittstelle greift auf den Status des Rasterizers zu.</span><span class="sxs-lookup"><span data-stu-id="1237e-106">A rasterizer-variable interface accesses rasterizer state.</span></span>

## <a name="members"></a><span data-ttu-id="1237e-107">Member</span><span class="sxs-lookup"><span data-stu-id="1237e-107">Members</span></span>

<span data-ttu-id="1237e-108">Die **ID3DX11EffectRasterizerVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="1237e-108">The **ID3DX11EffectRasterizerVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="1237e-109">**ID3DX11EffectRasterizerVariable** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1237e-109">**ID3DX11EffectRasterizerVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="1237e-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="1237e-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1237e-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="1237e-111">Methods</span></span>

<span data-ttu-id="1237e-112">Die **ID3DX11EffectRasterizerVariable** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1237e-112">The **ID3DX11EffectRasterizerVariable** interface has these methods.</span></span>



| <span data-ttu-id="1237e-113">Methode</span><span class="sxs-lookup"><span data-stu-id="1237e-113">Method</span></span>                                                                                   | <span data-ttu-id="1237e-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1237e-114">Description</span></span>                                                            |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="1237e-115">**Getbackingstore**</span><span class="sxs-lookup"><span data-stu-id="1237e-115">**GetBackingStore**</span></span>](id3dx11effectrasterizervariable-getbackingstore.md)               | <span data-ttu-id="1237e-116">Ein Zeiger auf eine Variable, die den rasteriser-Zustand enthält, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1237e-116">Get a pointer to a variable that contains rasteriser state.</span></span><br/> |
| [<span data-ttu-id="1237e-117">**Getrasterizerstate**</span><span class="sxs-lookup"><span data-stu-id="1237e-117">**GetRasterizerState**</span></span>](id3dx11effectrasterizervariable-getrasterizerstate.md)         | <span data-ttu-id="1237e-118">Einen Zeiger auf eine Raster-Schnittstelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="1237e-118">Get a pointer to a rasterizer interface.</span></span><br/>                    |
| [<span data-ttu-id="1237e-119">**"Tartrasterizerstate"**</span><span class="sxs-lookup"><span data-stu-id="1237e-119">**SetRasterizerState**</span></span>](id3dx11effectrasterizervariable-setrasterizerstate.md)         | <span data-ttu-id="1237e-120">Legt den Status des Rasterizers fest.</span><span class="sxs-lookup"><span data-stu-id="1237e-120">Sets the rasterizer state.</span></span><br/>                                  |
| [<span data-ttu-id="1237e-121">**Undotartrasterizerstate**</span><span class="sxs-lookup"><span data-stu-id="1237e-121">**UndoSetRasterizerState**</span></span>](id3dx11effectrasterizervariable-undosetrasterizerstate.md) | <span data-ttu-id="1237e-122">Stellt einen zuvor festgelegten Raster-Zustand wieder her.</span><span class="sxs-lookup"><span data-stu-id="1237e-122">Reverts a previously set rasterizer state.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="1237e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1237e-123">Remarks</span></span>

<span data-ttu-id="1237e-124">Eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md) -Schnittstelle wird erstellt, wenn ein Effekt in den Arbeitsspeicher gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="1237e-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="1237e-125">Effekt Variablen werden im Sicherungs Speicher im Arbeitsspeicher gespeichert. Wenn eine Technik angewendet wird, werden die Werte im Sicherungs Speicher auf das Gerät kopiert.</span><span class="sxs-lookup"><span data-stu-id="1237e-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="1237e-126">Sie können eine dieser Methoden verwenden, um den Status zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="1237e-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="1237e-127">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="1237e-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1237e-128">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1237e-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1237e-129">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1237e-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1237e-130">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1237e-130">Requirements</span></span>



| <span data-ttu-id="1237e-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1237e-131">Requirement</span></span> | <span data-ttu-id="1237e-132">Wert</span><span class="sxs-lookup"><span data-stu-id="1237e-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1237e-133">Header</span><span class="sxs-lookup"><span data-stu-id="1237e-133">Header</span></span><br/>  | <dl> <span data-ttu-id="1237e-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1237e-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1237e-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1237e-135">Library</span></span><br/> | <dl> <span data-ttu-id="1237e-136"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="1237e-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1237e-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1237e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1237e-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="1237e-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="1237e-139">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1237e-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="1237e-140">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1237e-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





