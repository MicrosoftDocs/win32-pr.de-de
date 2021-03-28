---
title: ID3DX11EffectConstantBuffer-Schnittstelle (D3dx11effect. h)
description: Eine Konstante Puffer Schnittstelle greift auf Konstante Puffer oder Textur Puffer zu.
ms.assetid: 2106cb51-dc0a-4ab6-adb6-2deb06922af1
keywords:
- ID3DX11EffectConstantBuffer-Schnittstelle Direct3D 11
- ID3DX11EffectConstantBuffer Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfea2e8e67af30075990d6643b10bb86cf3021ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355256"
---
# <a name="id3dx11effectconstantbuffer-interface"></a><span data-ttu-id="970df-105">ID3DX11EffectConstantBuffer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="970df-105">ID3DX11EffectConstantBuffer interface</span></span>

<span data-ttu-id="970df-106">Eine Konstante Puffer Schnittstelle greift auf Konstante Puffer oder Textur Puffer zu.</span><span class="sxs-lookup"><span data-stu-id="970df-106">A constant-buffer interface accesses constant buffers or texture buffers.</span></span>

## <a name="members"></a><span data-ttu-id="970df-107">Member</span><span class="sxs-lookup"><span data-stu-id="970df-107">Members</span></span>

<span data-ttu-id="970df-108">Die **ID3DX11EffectConstantBuffer** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="970df-108">The **ID3DX11EffectConstantBuffer** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="970df-109">**ID3DX11EffectConstantBuffer** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="970df-109">**ID3DX11EffectConstantBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="970df-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="970df-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="970df-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="970df-111">Methods</span></span>

<span data-ttu-id="970df-112">Die **ID3DX11EffectConstantBuffer** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="970df-112">The **ID3DX11EffectConstantBuffer** interface has these methods.</span></span>



| <span data-ttu-id="970df-113">Methode</span><span class="sxs-lookup"><span data-stu-id="970df-113">Method</span></span>                                                                             | <span data-ttu-id="970df-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="970df-114">Description</span></span>                                          |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="970df-115">**Getconstantbuffer**</span><span class="sxs-lookup"><span data-stu-id="970df-115">**GetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-getconstantbuffer.md)         | <span data-ttu-id="970df-116">Einen konstanten Puffer erhalten.</span><span class="sxs-lookup"><span data-stu-id="970df-116">Get a constant-buffer.</span></span><br/>                    |
| [<span data-ttu-id="970df-117">**Gettexturebuffer**</span><span class="sxs-lookup"><span data-stu-id="970df-117">**GetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-gettexturebuffer.md)           | <span data-ttu-id="970df-118">Einen Textur Puffer erhalten.</span><span class="sxs-lookup"><span data-stu-id="970df-118">Get a texture-buffer.</span></span><br/>                     |
| [<span data-ttu-id="970df-119">**Setconstantbuffer**</span><span class="sxs-lookup"><span data-stu-id="970df-119">**SetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-setconstantbuffer.md)         | <span data-ttu-id="970df-120">Legen Sie einen konstanten Puffer fest.</span><span class="sxs-lookup"><span data-stu-id="970df-120">Set a constant-buffer.</span></span><br/>                    |
| [<span data-ttu-id="970df-121">**Settexturebuffer**</span><span class="sxs-lookup"><span data-stu-id="970df-121">**SetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-settexturebuffer.md)           | <span data-ttu-id="970df-122">Legen Sie einen Textur Puffer fest.</span><span class="sxs-lookup"><span data-stu-id="970df-122">Set a texture-buffer.</span></span><br/>                     |
| [<span data-ttu-id="970df-123">**Undosetconstantbuffer**</span><span class="sxs-lookup"><span data-stu-id="970df-123">**UndoSetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-undosetconstantbuffer.md) | <span data-ttu-id="970df-124">Stellt einen zuvor festgelegten Konstanten Puffer wieder her.</span><span class="sxs-lookup"><span data-stu-id="970df-124">Reverts a previously set constant buffer.</span></span><br/> |
| [<span data-ttu-id="970df-125">**Undosettexturebuffer**</span><span class="sxs-lookup"><span data-stu-id="970df-125">**UndoSetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-undosettexturebuffer.md)   | <span data-ttu-id="970df-126">Stellt einen zuvor festgelegten Textur Puffer wieder her.</span><span class="sxs-lookup"><span data-stu-id="970df-126">Reverts a previously set texture buffer.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="970df-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="970df-127">Remarks</span></span>

<span data-ttu-id="970df-128">Verwenden konstanter Puffer zum Speichern von zahlreichen Effekt Konstanten; Gruppieren von Konstanten in Puffer basierend auf Ihrer Aktualisierungshäufigkeit.</span><span class="sxs-lookup"><span data-stu-id="970df-128">Use constant buffers to store many effect constants; grouping constants into buffers based on their frequency of update.</span></span> <span data-ttu-id="970df-129">Auf diese Weise können Sie die Anzahl der Zustandsänderungen minimieren und die wenigsten API-Aufrufe aufrufen, um den Status zu ändern.</span><span class="sxs-lookup"><span data-stu-id="970df-129">This allows you to minimize the number of state changes as well as make the fewest API calls to change state.</span></span> <span data-ttu-id="970df-130">Beide Faktoren führen zu einer besseren Leistung.</span><span class="sxs-lookup"><span data-stu-id="970df-130">Both of these factors lead to better performance.</span></span>

> [!Note]  
> <span data-ttu-id="970df-131">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="970df-131">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="970df-132">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="970df-132">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="970df-133">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="970df-133">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="970df-134">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="970df-134">Requirements</span></span>



| <span data-ttu-id="970df-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="970df-135">Requirement</span></span> | <span data-ttu-id="970df-136">Wert</span><span class="sxs-lookup"><span data-stu-id="970df-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="970df-137">Header</span><span class="sxs-lookup"><span data-stu-id="970df-137">Header</span></span><br/>  | <dl> <span data-ttu-id="970df-138"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="970df-138"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="970df-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="970df-139">Library</span></span><br/> | <dl> <span data-ttu-id="970df-140"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="970df-140"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="970df-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="970df-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="970df-142">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="970df-142">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="970df-143">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="970df-143">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="970df-144">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="970df-144">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





