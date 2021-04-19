---
description: Anwendungen verwenden die Methoden der ID3DXMATRIXStack-Schnittstelle, um einen Matrix Stapel zu bearbeiten.
ms.assetid: 4d382d39-a9da-4a3b-b7b6-d6890357d467
title: ID3DXMATRIXStack-Schnittstelle (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9446301ce057e788b4039f8ea3a144fb1fa19024
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367484"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="96f17-103">ID3DXMATRIXStack-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="96f17-103">ID3DXMATRIXStack interface</span></span>

<span data-ttu-id="96f17-104">Anwendungen verwenden die Methoden der ID3DXMATRIXStack-Schnittstelle, um einen Matrix Stapel zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="96f17-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="96f17-105">Member</span><span class="sxs-lookup"><span data-stu-id="96f17-105">Members</span></span>

<span data-ttu-id="96f17-106">Die **ID3DXMATRIXStack** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="96f17-106">The **ID3DXMATRIXStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="96f17-107">**ID3DXMATRIXStack** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="96f17-107">**ID3DXMATRIXStack** also has these types of members:</span></span>

-   [<span data-ttu-id="96f17-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="96f17-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="96f17-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="96f17-109">Methods</span></span>

<span data-ttu-id="96f17-110">Die **ID3DXMATRIXStack** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="96f17-110">The **ID3DXMATRIXStack** interface has these methods.</span></span>



| <span data-ttu-id="96f17-111">Methode</span><span class="sxs-lookup"><span data-stu-id="96f17-111">Method</span></span>                                                                       | <span data-ttu-id="96f17-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96f17-112">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96f17-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="96f17-113">**GetTop**</span></span>](id3dxmatrixstack--gettop.md)                                   | <span data-ttu-id="96f17-114">Ruft die aktuelle Matrix am Anfang des Stapels ab.</span><span class="sxs-lookup"><span data-stu-id="96f17-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="96f17-115">**Loadidentity**</span><span class="sxs-lookup"><span data-stu-id="96f17-115">**LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)                       | <span data-ttu-id="96f17-116">Lädt die Identität in der aktuellen Matrix.</span><span class="sxs-lookup"><span data-stu-id="96f17-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="96f17-117">**Loadmatrix**</span><span class="sxs-lookup"><span data-stu-id="96f17-117">**LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)                           | <span data-ttu-id="96f17-118">Lädt die angegebene Matrix in die aktuelle Matrix.</span><span class="sxs-lookup"><span data-stu-id="96f17-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="96f17-119">**Multmatrix**</span><span class="sxs-lookup"><span data-stu-id="96f17-119">**MultMatrix**</span></span>](id3dxmatrixstack--multmatrix.md)                           | <span data-ttu-id="96f17-120">Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.</span><span class="sxs-lookup"><span data-stu-id="96f17-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="96f17-121">**Multmatrixlocal**</span><span class="sxs-lookup"><span data-stu-id="96f17-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack--multmatrixlocal.md)                 | <span data-ttu-id="96f17-122">Bestimmt das Produkt der angegebenen Matrix und der aktuellen Matrix.</span><span class="sxs-lookup"><span data-stu-id="96f17-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="96f17-123">**Chor**</span><span class="sxs-lookup"><span data-stu-id="96f17-123">**Pop**</span></span>](id3dxmatrixstack--pop.md)                                         | <span data-ttu-id="96f17-124">Entfernt die aktuelle Matrix vom oberen Rand des Stapels.</span><span class="sxs-lookup"><span data-stu-id="96f17-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="96f17-125">**Push**</span><span class="sxs-lookup"><span data-stu-id="96f17-125">**Push**</span></span>](id3dxmatrixstack--push.md)                                       | <span data-ttu-id="96f17-126">Fügt dem Stapel eine Matrix hinzu.</span><span class="sxs-lookup"><span data-stu-id="96f17-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="96f17-127">**Rotateaxis**</span><span class="sxs-lookup"><span data-stu-id="96f17-127">**RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)                           | <span data-ttu-id="96f17-128">Rotiert (relativ zum globalen Koordinaten Bereich) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="96f17-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="96f17-129">**Rotateaxislocal**</span><span class="sxs-lookup"><span data-stu-id="96f17-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)                 | <span data-ttu-id="96f17-130">Rotiert (relativ zum lokalen Koordinaten Bereich des Objekts) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="96f17-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="96f17-131">**Rotateyawpitchroll**</span><span class="sxs-lookup"><span data-stu-id="96f17-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)           | <span data-ttu-id="96f17-132">Rotiert (relativ zum globalen Koordinaten Bereich) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="96f17-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="96f17-133">**Rotateyawpitchrolllocal**</span><span class="sxs-lookup"><span data-stu-id="96f17-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md) | <span data-ttu-id="96f17-134">Rotiert (relativ zum lokalen Koordinaten Bereich des Objekts) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="96f17-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="96f17-135">**Migen**</span><span class="sxs-lookup"><span data-stu-id="96f17-135">**Scale**</span></span>](id3dxmatrixstack--scale.md)                                     | <span data-ttu-id="96f17-136">Skalieren Sie die aktuelle Matrix über den Ursprung der Welt Koordinate.</span><span class="sxs-lookup"><span data-stu-id="96f17-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="96f17-137">**Skalelocal**</span><span class="sxs-lookup"><span data-stu-id="96f17-137">**ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)                           | <span data-ttu-id="96f17-138">Skalieren Sie die aktuelle Matrix über den Objekt Ursprung.</span><span class="sxs-lookup"><span data-stu-id="96f17-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="96f17-139">**Übersetzen**</span><span class="sxs-lookup"><span data-stu-id="96f17-139">**Translate**</span></span>](id3dxmatrixstack--translate.md)                             | <span data-ttu-id="96f17-140">Bestimmt das Produkt der aktuellen Matrix und die berechnete Übersetzungs Matrix, die durch die angegebenen Faktoren (x, y und z) bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="96f17-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="96f17-141">**Translatelocal**</span><span class="sxs-lookup"><span data-stu-id="96f17-141">**TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)                   | <span data-ttu-id="96f17-142">Bestimmt das Produkt der berechneten Übersetzungs Matrix, die durch die angegebenen Faktoren (x, y und z) und die aktuelle Matrix bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="96f17-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="96f17-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96f17-143">Remarks</span></span>

<span data-ttu-id="96f17-144">Die **ID3DXMATRIXStack** -Schnittstelle wird durch Aufrufen der [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) -Funktion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="96f17-144">The **ID3DXMATRIXStack** interface is obtained by calling the [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="96f17-145">Der LPD3DXMATRIXSTACK-Typ wird als Zeiger auf die **ID3DXMATRIXStack** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="96f17-145">The LPD3DXMATRIXSTACK type is defined as a pointer to the **ID3DXMATRIXStack** interface.</span></span>


```
typedef interface ID3DXMATRIXStack ID3DXMATRIXStack;
typedef interface ID3DXMATRIXStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="96f17-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96f17-146">Requirements</span></span>



| <span data-ttu-id="96f17-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96f17-147">Requirement</span></span> | <span data-ttu-id="96f17-148">Wert</span><span class="sxs-lookup"><span data-stu-id="96f17-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96f17-149">Header</span><span class="sxs-lookup"><span data-stu-id="96f17-149">Header</span></span><br/>  | <dl> <span data-ttu-id="96f17-150"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="96f17-150"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="96f17-151">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="96f17-151">Library</span></span><br/> | <dl> <span data-ttu-id="96f17-152"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96f17-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="96f17-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96f17-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96f17-154">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="96f17-154">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
