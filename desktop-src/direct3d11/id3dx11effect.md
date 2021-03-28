---
title: ID3DX11Effect-Schnittstelle (D3dx11effect. h)
description: Eine ID3DX11Effect-Schnittstelle verwaltet einen Satz von Zustands Objekten, Ressourcen und Shadern zum Implementieren eines renderingeffekts.
ms.assetid: 34429d51-6b45-4a62-bce1-50c4da02edac
keywords:
- ID3DX11Effect-Schnittstelle Direct3D 11
- ID3DX11Effect Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11Effect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395946ea4276bc57595abdeb18e7d1755ca0ff1d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996082"
---
# <a name="id3dx11effect-interface"></a><span data-ttu-id="1b5f8-105">ID3DX11Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1b5f8-105">ID3DX11Effect interface</span></span>

<span data-ttu-id="1b5f8-106">Eine **ID3DX11Effect** -Schnittstelle verwaltet einen Satz von Zustands Objekten, Ressourcen und Shadern zum Implementieren eines renderingeffekts.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-106">An **ID3DX11Effect** interface manages a set of state objects, resources, and shaders for implementing a rendering effect.</span></span>

## <a name="members"></a><span data-ttu-id="1b5f8-107">Member</span><span class="sxs-lookup"><span data-stu-id="1b5f8-107">Members</span></span>

<span data-ttu-id="1b5f8-108">Die **ID3DX11Effect** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-108">The **ID3DX11Effect** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1b5f8-109">**ID3DX11Effect** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1b5f8-109">**ID3DX11Effect** also has these types of members:</span></span>

-   [<span data-ttu-id="1b5f8-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="1b5f8-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1b5f8-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="1b5f8-111">Methods</span></span>

<span data-ttu-id="1b5f8-112">Die **ID3DX11Effect** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-112">The **ID3DX11Effect** interface has these methods.</span></span>



| <span data-ttu-id="1b5f8-113">Methode</span><span class="sxs-lookup"><span data-stu-id="1b5f8-113">Method</span></span>                                                                     | <span data-ttu-id="1b5f8-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b5f8-114">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b5f8-115">**Cloneeffect**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-115">**CloneEffect**</span></span>](id3dx11effect-cloneeffect.md)                           | <span data-ttu-id="1b5f8-116">Erstellt eine Kopie einer Effect-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-116">Creates a copy of an effect interface.</span></span><br/>                                         |
| [<span data-ttu-id="1b5f8-117">**Getclassverknüpfung**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-117">**GetClassLinkage**</span></span>](id3dx11effect-getclasslinkage.md)                   | <span data-ttu-id="1b5f8-118">Ruft eine Schnittstelle für die Klassen Verknüpfung ab.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-118">Gets a class linkage interface.</span></span><br/>                                                |
| [<span data-ttu-id="1b5f8-119">**GetConstantBufferByIndex**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-119">**GetConstantBufferByIndex**</span></span>](id3dx11effect-getconstantbufferbyindex.md) | <span data-ttu-id="1b5f8-120">Einen konstanten Puffer nach Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-120">Get a constant buffer by index.</span></span><br/>                                                |
| [<span data-ttu-id="1b5f8-121">**GetConstantBufferByName**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-121">**GetConstantBufferByName**</span></span>](id3dx11effect-getconstantbufferbyname.md)   | <span data-ttu-id="1b5f8-122">Einen konstanten Puffer anhand des Namens erhalten.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-122">Get a constant buffer by name.</span></span><br/>                                                 |
| [<span data-ttu-id="1b5f8-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-123">**GetDesc**</span></span>](id3dx11effect-getdesc.md)                                   | <span data-ttu-id="1b5f8-124">Sie erhalten eine Beschreibung des Effekts.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-124">Get an effect description.</span></span><br/>                                                     |
| [<span data-ttu-id="1b5f8-125">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-125">**GetDevice**</span></span>](id3dx11effect-getdevice.md)                               | <span data-ttu-id="1b5f8-126">Holen Sie sich das Gerät, das den Effekt erzeugt hat.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-126">Get the device that created the effect.</span></span><br/>                                        |
| [<span data-ttu-id="1b5f8-127">**Getgroupbyindex**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-127">**GetGroupByIndex**</span></span>](id3dx11effect-getgroupbyindex.md)                   | <span data-ttu-id="1b5f8-128">Ruft eine Effekt Gruppe nach Index ab.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-128">Gets an effect group by index.</span></span><br/>                                                 |
| [<span data-ttu-id="1b5f8-129">**Getgroupbyname**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-129">**GetGroupByName**</span></span>](id3dx11effect-getgroupbyname.md)                     | <span data-ttu-id="1b5f8-130">Ruft eine Effekt Gruppe nach dem Namen ab.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-130">Gets an effect group by name.</span></span><br/>                                                  |
| [<span data-ttu-id="1b5f8-131">**Gettechniquebyindex**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-131">**GetTechniqueByIndex**</span></span>](id3dx11effect-gettechniquebyindex.md)           | <span data-ttu-id="1b5f8-132">Holen Sie sich eine Technik nach Index.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-132">Get a technique by index.</span></span><br/>                                                      |
| [<span data-ttu-id="1b5f8-133">**Gettechniquebyname**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-133">**GetTechniqueByName**</span></span>](id3dx11effect-gettechniquebyname.md)             | <span data-ttu-id="1b5f8-134">Holen Sie sich eine Technik anhand des Namens.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-134">Get a technique by name.</span></span><br/>                                                       |
| [<span data-ttu-id="1b5f8-135">**GetVariableByIndex**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-135">**GetVariableByIndex**</span></span>](id3dx11effect-getvariablebyindex.md)             | <span data-ttu-id="1b5f8-136">Eine Variable nach Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-136">Get a variable by index.</span></span><br/>                                                       |
| [<span data-ttu-id="1b5f8-137">**GetVariableByName**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-137">**GetVariableByName**</span></span>](id3dx11effect-getvariablebyname.md)               | <span data-ttu-id="1b5f8-138">Eine Variable anhand ihres Namens erhalten.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-138">Get a variable by name.</span></span><br/>                                                        |
| [<span data-ttu-id="1b5f8-139">**Getvariablebysemantic**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-139">**GetVariableBySemantic**</span></span>](id3dx11effect-getvariablebysemantic.md)       | <span data-ttu-id="1b5f8-140">Eine Variable nach Semantik erhalten.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-140">Get a variable by semantic.</span></span><br/>                                                    |
| [<span data-ttu-id="1b5f8-141">**Isoptimiert**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-141">**IsOptimized**</span></span>](id3dx11effect-isoptimized.md)                           | <span data-ttu-id="1b5f8-142">Testen eines Effekts, um zu ermitteln, ob die reflektionsintemetadaten aus dem Arbeitsspeicher entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-142">Test an effect to see if the reflection metadata has been removed from memory.</span></span><br/> |
| [<span data-ttu-id="1b5f8-143">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-143">**IsValid**</span></span>](id3dx11effect-isvalid.md)                                   | <span data-ttu-id="1b5f8-144">Testen Sie einen Effekt, um festzustellen, ob er eine gültige Syntax enthält.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-144">Test an effect to see if it contains valid syntax.</span></span><br/>                             |
| [<span data-ttu-id="1b5f8-145">**Optimieren**</span><span class="sxs-lookup"><span data-stu-id="1b5f8-145">**Optimize**</span></span>](id3dx11effect-optimize.md)                                 | <span data-ttu-id="1b5f8-146">Minimieren Sie den für einen Effekt benötigten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-146">Minimize the amount of memory required for an effect.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="1b5f8-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b5f8-147">Remarks</span></span>

<span data-ttu-id="1b5f8-148">Ein Effekt wird durch Aufrufen von [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md)erstellt.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-148">An effect is created by calling [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span></span>

<span data-ttu-id="1b5f8-149">Das Effect-System gruppiert die für das Rendering erforderlichen Informationen in einen Effekt, der Folgendes enthält: Zustands Objekte zum Zuweisen von Zustandsänderungen in Gruppen, Ressourcen zum Bereitstellen von Eingabedaten und Speichern von Ausgabedaten sowie Programme, die Steuern, wie das Rendering als Shader ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-149">The effect system groups the information required for rendering into an effect which contains: state objects for assigning state changes in groups, resources for supplying input data and storing output data, and programs that control how the rendering is done called shaders.</span></span>

> [!Note]  
> <span data-ttu-id="1b5f8-150">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-150">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1b5f8-151">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-151">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1b5f8-152">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1b5f8-152">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

> [!Note]
>
> <span data-ttu-id="1b5f8-153">Wenn Sie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für ein **ID3DX11Effect** -Objekt aufrufen, um die [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle abzurufen, gibt **QueryInterface** E \_ nointerface zurück.</span><span class="sxs-lookup"><span data-stu-id="1b5f8-153">If you call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on an **ID3DX11Effect** object to retrieve the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface, **QueryInterface** returns E\_NOINTERFACE.</span></span> <span data-ttu-id="1b5f8-154">Um dieses Problem zu umgehen, verwenden Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="1b5f8-154">To work around this issue, use the following code:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>    IUnknown* pIUnknown = (IUnknown*)pEffect;
>     pIUnknown->AddRef();</code></pre></td>
> </tr>
> </tbody>
> </table>
>  
>
> ## <a name="requirements"></a><span data-ttu-id="1b5f8-155">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1b5f8-155">Requirements</span></span>
>
> 
>
<span data-ttu-id="1b5f8-156">| Anforderung | Wert |</span><span class="sxs-lookup"><span data-stu-id="1b5f8-156">| Requirement | Value |</span></span>
> <span data-ttu-id="1b5f8-157">|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------| | Header</span><span class="sxs-lookup"><span data-stu-id="1b5f8-157">|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------| | Header</span></span><br/>  | <dl> <span data-ttu-id="1b5f8-158"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b5f8-158"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    <span data-ttu-id="1b5f8-159">| | Fern</span><span class="sxs-lookup"><span data-stu-id="1b5f8-159">| | Library</span></span><br/> | <dl> <span data-ttu-id="1b5f8-160"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="1b5f8-160"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |
>
> 
>
> ## <a name="see-also"></a><span data-ttu-id="1b5f8-161">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1b5f8-161">See also</span></span>
>
> <dl> <dt>

[<span data-ttu-id="1b5f8-162">Effekte 11-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1b5f8-162">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="1b5f8-163">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1b5f8-163">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>
>
>  
>
>  
>
