---
title: ID3DX11EffectDepthStencilVariable-Schnittstelle (D3dx11effect. h)
description: Eine tiefen Schablone-Variablen-Schnittstelle greift auf den Status der tiefen Schablone zu.
ms.assetid: 8fb1be19-eed4-4d69-bbbe-94484531eba2
keywords:
- ID3DX11EffectDepthStencilVariable-Schnittstelle Direct3D 11
- ID3DX11EffectDepthStencilVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d7aa520df0c13c81435421d5f605f901a61da6e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961717"
---
# <a name="id3dx11effectdepthstencilvariable-interface"></a><span data-ttu-id="300c6-105">ID3DX11EffectDepthStencilVariable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="300c6-105">ID3DX11EffectDepthStencilVariable interface</span></span>

<span data-ttu-id="300c6-106">Eine tiefen Schablone-Variablen-Schnittstelle greift auf den Status der tiefen Schablone zu.</span><span class="sxs-lookup"><span data-stu-id="300c6-106">A depth-stencil-variable interface accesses depth-stencil state.</span></span>

## <a name="members"></a><span data-ttu-id="300c6-107">Member</span><span class="sxs-lookup"><span data-stu-id="300c6-107">Members</span></span>

<span data-ttu-id="300c6-108">Die **ID3DX11EffectDepthStencilVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="300c6-108">The **ID3DX11EffectDepthStencilVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="300c6-109">**ID3DX11EffectDepthStencilVariable** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="300c6-109">**ID3DX11EffectDepthStencilVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="300c6-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="300c6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="300c6-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="300c6-111">Methods</span></span>

<span data-ttu-id="300c6-112">Die **ID3DX11EffectDepthStencilVariable** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="300c6-112">The **ID3DX11EffectDepthStencilVariable** interface has these methods.</span></span>



| <span data-ttu-id="300c6-113">Methode</span><span class="sxs-lookup"><span data-stu-id="300c6-113">Method</span></span>                                                                                         | <span data-ttu-id="300c6-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="300c6-114">Description</span></span>                                                               |
|:-----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="300c6-115">**Getbackingstore**</span><span class="sxs-lookup"><span data-stu-id="300c6-115">**GetBackingStore**</span></span>](id3dx11effectdepthstencilvariable-getbackingstore.md)                   | <span data-ttu-id="300c6-116">Einen Zeiger auf eine Variable mit dem Status der tiefen Schablone erhalten.</span><span class="sxs-lookup"><span data-stu-id="300c6-116">Get a pointer to a variable that contains depth-stencil state.</span></span><br/> |
| [<span data-ttu-id="300c6-117">**Getdepthstencilstate**</span><span class="sxs-lookup"><span data-stu-id="300c6-117">**GetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-getdepthstencilstate.md)         | <span data-ttu-id="300c6-118">Einen Zeiger auf eine tiefen Schablone-Schnittstelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="300c6-118">Get a pointer to a depth-stencil interface.</span></span><br/>                    |
| [<span data-ttu-id="300c6-119">**Setdepthstencilstate**</span><span class="sxs-lookup"><span data-stu-id="300c6-119">**SetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)         | <span data-ttu-id="300c6-120">Legt den Status der tiefen Schablone fest.</span><span class="sxs-lookup"><span data-stu-id="300c6-120">Sets the depth stencil state.</span></span><br/>                                  |
| [<span data-ttu-id="300c6-121">**Undosetdepthstencilstate**</span><span class="sxs-lookup"><span data-stu-id="300c6-121">**UndoSetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md) | <span data-ttu-id="300c6-122">Stellt einen zuvor festgelegten tiefen Schablone Zustand wieder her.</span><span class="sxs-lookup"><span data-stu-id="300c6-122">Reverts a previously set depth stencil state.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="300c6-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="300c6-123">Remarks</span></span>

<span data-ttu-id="300c6-124">Eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md) -Schnittstelle wird erstellt, wenn ein Effekt in den Arbeitsspeicher gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="300c6-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="300c6-125">Effekt Variablen werden im Sicherungs Speicher im Arbeitsspeicher gespeichert. Wenn eine Technik angewendet wird, werden die Werte im Sicherungs Speicher auf das Gerät kopiert.</span><span class="sxs-lookup"><span data-stu-id="300c6-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="300c6-126">Sie können eine dieser Methoden verwenden, um den Status zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="300c6-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="300c6-127">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="300c6-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="300c6-128">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="300c6-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="300c6-129">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="300c6-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="300c6-130">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="300c6-130">Requirements</span></span>



| <span data-ttu-id="300c6-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="300c6-131">Requirement</span></span> | <span data-ttu-id="300c6-132">Wert</span><span class="sxs-lookup"><span data-stu-id="300c6-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="300c6-133">Header</span><span class="sxs-lookup"><span data-stu-id="300c6-133">Header</span></span><br/>  | <dl> <span data-ttu-id="300c6-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="300c6-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="300c6-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="300c6-135">Library</span></span><br/> | <dl> <span data-ttu-id="300c6-136"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="300c6-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="300c6-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="300c6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="300c6-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="300c6-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="300c6-139">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="300c6-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="300c6-140">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="300c6-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





