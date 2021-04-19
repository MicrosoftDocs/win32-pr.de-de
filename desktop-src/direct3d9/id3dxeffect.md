---
description: Wird verwendet, um Effekte festzulegen und abzufragen und um Techniken auszuwählen. Ein Effect-Objekt kann mehrere Techniken enthalten, um denselben Effekt zu erzeugen.
ms.assetid: bffc64ab-12e7-44e9-b296-262b0459a68a
title: ID3DXEffect-Schnittstelle (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 275376234739964940d70381a34331ff5b89f2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354996"
---
# <a name="id3dxeffect-interface"></a><span data-ttu-id="81d08-104">ID3DXEffect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="81d08-104">ID3DXEffect interface</span></span>

<span data-ttu-id="81d08-105">Wird verwendet, um Effekte festzulegen und abzufragen und um Techniken auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="81d08-105">Used to set and query effects, and to choose techniques.</span></span> <span data-ttu-id="81d08-106">Ein Effect-Objekt kann mehrere Techniken enthalten, um denselben Effekt zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="81d08-106">An effect object can contain multiple techniques to render the same effect.</span></span>

## <a name="members"></a><span data-ttu-id="81d08-107">Member</span><span class="sxs-lookup"><span data-stu-id="81d08-107">Members</span></span>

<span data-ttu-id="81d08-108">Die **ID3DXEffect** -Schnittstelle erbt von [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span><span class="sxs-lookup"><span data-stu-id="81d08-108">The **ID3DXEffect** interface inherits from [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span> <span data-ttu-id="81d08-109">**ID3DXEffect** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="81d08-109">**ID3DXEffect** also has these types of members:</span></span>

-   [<span data-ttu-id="81d08-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="81d08-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="81d08-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="81d08-111">Methods</span></span>

<span data-ttu-id="81d08-112">Die **ID3DXEffect** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="81d08-112">The **ID3DXEffect** interface has these methods.</span></span>



| <span data-ttu-id="81d08-113">Methode</span><span class="sxs-lookup"><span data-stu-id="81d08-113">Method</span></span>                                                                | <span data-ttu-id="81d08-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81d08-114">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81d08-115">**Applyparameterblock**</span><span class="sxs-lookup"><span data-stu-id="81d08-115">**ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)       | <span data-ttu-id="81d08-116">Wenden Sie die Werte in einem Zustands Block auf den Systemstatus aktueller Effekt an.</span><span class="sxs-lookup"><span data-stu-id="81d08-116">Apply the values in a state block to the current effect system state.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="81d08-117">**Starten**</span><span class="sxs-lookup"><span data-stu-id="81d08-117">**Begin**</span></span>](id3dxeffect--begin.md)                                   | <span data-ttu-id="81d08-118">Startet ein aktives Verfahren.</span><span class="sxs-lookup"><span data-stu-id="81d08-118">Starts an active technique.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="81d08-119">**Beginparameterblock**</span><span class="sxs-lookup"><span data-stu-id="81d08-119">**BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)       | <span data-ttu-id="81d08-120">Starten Sie die Erfassung von Zustandsänderungen in einem Parameter Block.</span><span class="sxs-lookup"><span data-stu-id="81d08-120">Start capturing state changes in a parameter block.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="81d08-121">**Beginpass**</span><span class="sxs-lookup"><span data-stu-id="81d08-121">**BeginPass**</span></span>](id3dxeffect--beginpass.md)                           | <span data-ttu-id="81d08-122">Startet einen Durchlauf innerhalb der aktiven Technik.</span><span class="sxs-lookup"><span data-stu-id="81d08-122">Begins a pass, within the active technique.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="81d08-123">**Cloneeffect**</span><span class="sxs-lookup"><span data-stu-id="81d08-123">**CloneEffect**</span></span>](id3dxeffect--cloneeffect.md)                       | <span data-ttu-id="81d08-124">Erstellt eine Kopie eines Effekts.</span><span class="sxs-lookup"><span data-stu-id="81d08-124">Creates a copy of an effect.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="81d08-125">**CommitChanges**</span><span class="sxs-lookup"><span data-stu-id="81d08-125">**CommitChanges**</span></span>](id3dxeffect--commitchanges.md)                   | <span data-ttu-id="81d08-126">Weitergeben von Zustandsänderungen, die innerhalb eines aktiven Durchlaufs an das Gerät erfolgen, vor dem Rendering.</span><span class="sxs-lookup"><span data-stu-id="81d08-126">Propagate state changes that occur inside of an active pass to the device before rendering.</span></span><br/>                                                                                           |
| [<span data-ttu-id="81d08-127">**Deleteparameterblock**</span><span class="sxs-lookup"><span data-stu-id="81d08-127">**DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)     | <span data-ttu-id="81d08-128">Löschen Sie einen Parameter Block.</span><span class="sxs-lookup"><span data-stu-id="81d08-128">Delete a parameter block.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="81d08-129">**ENDE**</span><span class="sxs-lookup"><span data-stu-id="81d08-129">**End**</span></span>](id3dxeffect--end.md)                                       | <span data-ttu-id="81d08-130">Beendet eine aktive Technik.</span><span class="sxs-lookup"><span data-stu-id="81d08-130">Ends an active technique.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="81d08-131">**Endparameterblock**</span><span class="sxs-lookup"><span data-stu-id="81d08-131">**EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)           | <span data-ttu-id="81d08-132">Beendet die Erfassung von Effekt-Parameter Zustandsänderungen.</span><span class="sxs-lookup"><span data-stu-id="81d08-132">Stop capturing effect parameter state changes.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="81d08-133">**Endpass**</span><span class="sxs-lookup"><span data-stu-id="81d08-133">**EndPass**</span></span>](id3dxeffect--endpass.md)                               | <span data-ttu-id="81d08-134">Beenden eines aktiven Pass.</span><span class="sxs-lookup"><span data-stu-id="81d08-134">End an active pass.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="81d08-135">**Findnextvalidtechnique**</span><span class="sxs-lookup"><span data-stu-id="81d08-135">**FindNextValidTechnique**</span></span>](id3dxeffect--findnextvalidtechnique.md) | <span data-ttu-id="81d08-136">Sucht das nächste gültige Verfahren, beginnend bei der Technik nach der angegebenen Technik.</span><span class="sxs-lookup"><span data-stu-id="81d08-136">Searches for the next valid technique, starting at the technique after the specified technique.</span></span><br/>                                                                                       |
| [<span data-ttu-id="81d08-137">**Getcurrenttechnique**</span><span class="sxs-lookup"><span data-stu-id="81d08-137">**GetCurrentTechnique**</span></span>](id3dxeffect--getcurrenttechnique.md)       | <span data-ttu-id="81d08-138">Ruft die aktuelle Technik ab.</span><span class="sxs-lookup"><span data-stu-id="81d08-138">Gets the current technique.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="81d08-139">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="81d08-139">**GetDevice**</span></span>](id3dxeffect--getdevice.md)                           | <span data-ttu-id="81d08-140">Ruft das Gerät ab, das dem Effekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="81d08-140">Retrieves the device associated with the effect.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="81d08-141">**Getpool)**</span><span class="sxs-lookup"><span data-stu-id="81d08-141">**GetPool**</span></span>](id3dxeffect--getpool.md)                               | <span data-ttu-id="81d08-142">Ruft einen Zeiger auf den Pool von freigegebenen Parametern ab.</span><span class="sxs-lookup"><span data-stu-id="81d08-142">Gets a pointer to the pool of shared parameters.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="81d08-143">**GetStatus Manager**</span><span class="sxs-lookup"><span data-stu-id="81d08-143">**GetStateManager**</span></span>](id3dxeffect--getstatemanager.md)               | <span data-ttu-id="81d08-144">Holen Sie sich den Effekt Zustands-Manager.</span><span class="sxs-lookup"><span data-stu-id="81d08-144">Get the effect state manager.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="81d08-145">**Isparameterused**</span><span class="sxs-lookup"><span data-stu-id="81d08-145">**IsParameterUsed**</span></span>](id3dxeffect--isparameterused.md)               | <span data-ttu-id="81d08-146">Bestimmt, ob ein Parameter von der Technik verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="81d08-146">Determines if a parameter is used by the technique.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="81d08-147">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="81d08-147">**OnLostDevice**</span></span>](id3dxeffect--onlostdevice.md)                     | <span data-ttu-id="81d08-148">Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen.</span><span class="sxs-lookup"><span data-stu-id="81d08-148">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="81d08-149">Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="81d08-149">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="81d08-150">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="81d08-150">**OnResetDevice**</span></span>](id3dxeffect--onresetdevice.md)                   | <span data-ttu-id="81d08-151">Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.</span><span class="sxs-lookup"><span data-stu-id="81d08-151">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="81d08-152">**"Strawvalue"**</span><span class="sxs-lookup"><span data-stu-id="81d08-152">**SetRawValue**</span></span>](id3dxeffect--setrawvalue.md)                       | <span data-ttu-id="81d08-153">Legen Sie einen zusammenhängenden Bereich von shaderkonstanten mit einer Speicher Kopie fest.</span><span class="sxs-lookup"><span data-stu-id="81d08-153">Set a contiguous range of shader constants with a memory copy.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="81d08-154">**SetStatus Manager**</span><span class="sxs-lookup"><span data-stu-id="81d08-154">**SetStateManager**</span></span>](id3dxeffect--setstatemanager.md)               | <span data-ttu-id="81d08-155">Legen Sie den Effekt Zustands-Manager fest.</span><span class="sxs-lookup"><span data-stu-id="81d08-155">Set the effect state manager.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="81d08-156">**Settechnique**</span><span class="sxs-lookup"><span data-stu-id="81d08-156">**SetTechnique**</span></span>](id3dxeffect--settechnique.md)                     | <span data-ttu-id="81d08-157">Legt die aktive Technik fest.</span><span class="sxs-lookup"><span data-stu-id="81d08-157">Sets the active technique.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="81d08-158">**Validatetechnique**</span><span class="sxs-lookup"><span data-stu-id="81d08-158">**ValidateTechnique**</span></span>](id3dxeffect--validatetechnique.md)           | <span data-ttu-id="81d08-159">Überprüfen Sie eine Technik.</span><span class="sxs-lookup"><span data-stu-id="81d08-159">Validate a technique.</span></span><br/>                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="81d08-160">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81d08-160">Remarks</span></span>

<span data-ttu-id="81d08-161">Die ID3DXEffect-Schnittstelle wird durch Aufrufen von [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)oder [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="81d08-161">The ID3DXEffect interface is obtained by calling [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md), or [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md).</span></span>

<span data-ttu-id="81d08-162">Der LPD3DXEFFECT-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="81d08-162">The LPD3DXEFFECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffect ID3DXEffect;
typedef interface ID3DXEffect *LPD3DXEFFECT;
```



## <a name="requirements"></a><span data-ttu-id="81d08-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81d08-163">Requirements</span></span>



| <span data-ttu-id="81d08-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81d08-164">Requirement</span></span> | <span data-ttu-id="81d08-165">Wert</span><span class="sxs-lookup"><span data-stu-id="81d08-165">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="81d08-166">Header</span><span class="sxs-lookup"><span data-stu-id="81d08-166">Header</span></span><br/>  | <dl> <span data-ttu-id="81d08-167"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="81d08-167"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="81d08-168">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="81d08-168">Library</span></span><br/> | <dl> <span data-ttu-id="81d08-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81d08-169"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="81d08-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81d08-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81d08-171">**ID3DXBaseEffect**</span><span class="sxs-lookup"><span data-stu-id="81d08-171">**ID3DXBaseEffect**</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="81d08-172">Effekt Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="81d08-172">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[<span data-ttu-id="81d08-173">**D3DXCreateEffect**</span><span class="sxs-lookup"><span data-stu-id="81d08-173">**D3DXCreateEffect**</span></span>](d3dxcreateeffect.md)
</dt> <dt>

[<span data-ttu-id="81d08-174">**D3DXCreateEffectFromFile**</span><span class="sxs-lookup"><span data-stu-id="81d08-174">**D3DXCreateEffectFromFile**</span></span>](d3dxcreateeffectfromfile.md)
</dt> <dt>

[<span data-ttu-id="81d08-175">**D3DXCreateEffectFromResource**</span><span class="sxs-lookup"><span data-stu-id="81d08-175">**D3DXCreateEffectFromResource**</span></span>](d3dxcreateeffectfromresource.md)
</dt> </dl>

 

 




