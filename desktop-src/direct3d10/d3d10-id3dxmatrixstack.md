---
description: Anwendungen verwenden die Methoden der ID3DXMATRIXStack-Schnittstelle, um einen Matrix Stapel zu bearbeiten.
ms.assetid: 6c76f9e0-5f59-4cf3-b34a-2475536af6c7
title: ID3DXMatrixStack-Schnittstelle (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMatrixStack
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3d6956a6764683378c732c4ed859bfa13e537422
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355637"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="6c331-103">ID3DXMatrixStack-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6c331-103">ID3DXMatrixStack interface</span></span>

<span data-ttu-id="6c331-104">Anwendungen verwenden die Methoden der ID3DXMATRIXStack-Schnittstelle, um einen Matrix Stapel zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6c331-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="6c331-105">Member</span><span class="sxs-lookup"><span data-stu-id="6c331-105">Members</span></span>

<span data-ttu-id="6c331-106">Die **ID3DXMatrixStack** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6c331-106">The **ID3DXMatrixStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6c331-107">**ID3DXMatrixStack** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6c331-107">**ID3DXMatrixStack** also has these types of members:</span></span>

-   [<span data-ttu-id="6c331-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="6c331-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6c331-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="6c331-109">Methods</span></span>

<span data-ttu-id="6c331-110">Die **ID3DXMatrixStack** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6c331-110">The **ID3DXMatrixStack** interface has these methods.</span></span>



| <span data-ttu-id="6c331-111">Methode</span><span class="sxs-lookup"><span data-stu-id="6c331-111">Method</span></span>                                                                      | <span data-ttu-id="6c331-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c331-112">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c331-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="6c331-113">**GetTop**</span></span>](id3dxmatrixstack-gettop.md)                                   | <span data-ttu-id="6c331-114">Ruft die aktuelle Matrix am Anfang des Stapels ab.</span><span class="sxs-lookup"><span data-stu-id="6c331-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="6c331-115">**Loadidentity**</span><span class="sxs-lookup"><span data-stu-id="6c331-115">**LoadIdentity**</span></span>](id3dxmatrixstack-loadidentity.md)                       | <span data-ttu-id="6c331-116">Lädt die Identität in der aktuellen Matrix.</span><span class="sxs-lookup"><span data-stu-id="6c331-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="6c331-117">**Loadmatrix**</span><span class="sxs-lookup"><span data-stu-id="6c331-117">**LoadMatrix**</span></span>](id3dxmatrixstack-loadmatrix.md)                           | <span data-ttu-id="6c331-118">Lädt die angegebene Matrix in die aktuelle Matrix.</span><span class="sxs-lookup"><span data-stu-id="6c331-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="6c331-119">**Multmatrix**</span><span class="sxs-lookup"><span data-stu-id="6c331-119">**MultMatrix**</span></span>](id3dxmatrixstack-multmatrix.md)                           | <span data-ttu-id="6c331-120">Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.</span><span class="sxs-lookup"><span data-stu-id="6c331-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="6c331-121">**Multmatrixlocal**</span><span class="sxs-lookup"><span data-stu-id="6c331-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack-multmatrixlocal.md)                 | <span data-ttu-id="6c331-122">Bestimmt das Produkt der angegebenen Matrix und der aktuellen Matrix.</span><span class="sxs-lookup"><span data-stu-id="6c331-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="6c331-123">**Chor**</span><span class="sxs-lookup"><span data-stu-id="6c331-123">**Pop**</span></span>](id3dxmatrixstack-pop.md)                                         | <span data-ttu-id="6c331-124">Entfernt die aktuelle Matrix vom oberen Rand des Stapels.</span><span class="sxs-lookup"><span data-stu-id="6c331-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="6c331-125">**Push**</span><span class="sxs-lookup"><span data-stu-id="6c331-125">**Push**</span></span>](id3dxmatrixstack-push.md)                                       | <span data-ttu-id="6c331-126">Fügt dem Stapel eine Matrix hinzu.</span><span class="sxs-lookup"><span data-stu-id="6c331-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="6c331-127">**Rotateaxis**</span><span class="sxs-lookup"><span data-stu-id="6c331-127">**RotateAxis**</span></span>](id3dxmatrixstack-rotateaxis.md)                           | <span data-ttu-id="6c331-128">Rotiert (relativ zum globalen Koordinaten Bereich) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="6c331-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="6c331-129">**Rotateaxislocal**</span><span class="sxs-lookup"><span data-stu-id="6c331-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack-rotateaxislocal.md)                 | <span data-ttu-id="6c331-130">Rotiert (relativ zum lokalen Koordinaten Bereich des Objekts) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="6c331-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="6c331-131">**Rotateyawpitchroll**</span><span class="sxs-lookup"><span data-stu-id="6c331-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack-rotateyawpitchroll.md)           | <span data-ttu-id="6c331-132">Rotiert (relativ zum globalen Koordinaten Bereich) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="6c331-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="6c331-133">**Rotateyawpitchrolllocal**</span><span class="sxs-lookup"><span data-stu-id="6c331-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack-rotateyawpitchrolllocal.md) | <span data-ttu-id="6c331-134">Rotiert (relativ zum lokalen Koordinaten Bereich des Objekts) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="6c331-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="6c331-135">**Migen**</span><span class="sxs-lookup"><span data-stu-id="6c331-135">**Scale**</span></span>](id3dxmatrixstack-scale.md)                                     | <span data-ttu-id="6c331-136">Skalieren Sie die aktuelle Matrix über den Ursprung der Welt Koordinate.</span><span class="sxs-lookup"><span data-stu-id="6c331-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="6c331-137">**Skalelocal**</span><span class="sxs-lookup"><span data-stu-id="6c331-137">**ScaleLocal**</span></span>](id3dxmatrixstack-scalelocal.md)                           | <span data-ttu-id="6c331-138">Skalieren Sie die aktuelle Matrix über den Objekt Ursprung.</span><span class="sxs-lookup"><span data-stu-id="6c331-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="6c331-139">**Übersetzen**</span><span class="sxs-lookup"><span data-stu-id="6c331-139">**Translate**</span></span>](id3dxmatrixstack-translate.md)                             | <span data-ttu-id="6c331-140">Bestimmt das Produkt der aktuellen Matrix und die berechnete Übersetzungs Matrix, die durch die angegebenen Faktoren (x, y und z) bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="6c331-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="6c331-141">**Translatelocal**</span><span class="sxs-lookup"><span data-stu-id="6c331-141">**TranslateLocal**</span></span>](id3dxmatrixstack-translatelocal.md)                   | <span data-ttu-id="6c331-142">Bestimmt das Produkt der berechneten Übersetzungs Matrix, die durch die angegebenen Faktoren (x, y und z) und die aktuelle Matrix bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="6c331-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6c331-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c331-143">Remarks</span></span>

<span data-ttu-id="6c331-144">Die ID3DX10MATRIXStack-Schnittstelle wird durch Aufrufen der [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) -Funktion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6c331-144">The ID3DX10MATRIXStack interface is obtained by calling the [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="6c331-145">Der LPD3DX10MATRIXSTACK-Typ wird als Zeiger auf die **ID3DXMatrixStack** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="6c331-145">The LPD3DX10MATRIXSTACK type is defined as a pointer to the **ID3DXMatrixStack** interface.</span></span>


```
typedef interface ID3DXMatrixStack ID3DXMatrixStack;
typedef interface ID3DXMatrixStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="6c331-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c331-146">Requirements</span></span>



| <span data-ttu-id="6c331-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c331-147">Requirement</span></span> | <span data-ttu-id="6c331-148">Wert</span><span class="sxs-lookup"><span data-stu-id="6c331-148">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c331-149">Header</span><span class="sxs-lookup"><span data-stu-id="6c331-149">Header</span></span><br/>  | <dl> <span data-ttu-id="6c331-150"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c331-150"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c331-151">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6c331-151">Library</span></span><br/> | <dl> <span data-ttu-id="6c331-152"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c331-152"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c331-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c331-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c331-154">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6c331-154">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
