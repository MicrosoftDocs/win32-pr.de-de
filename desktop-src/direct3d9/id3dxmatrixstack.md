---
description: 'ID3DXMATRIXStack-Schnittstelle: Anwendungen verwenden die Methoden der ID3DXMATRIXStack-Schnittstelle, um einen Matrixstapel zu bearbeiten.'
ms.assetid: 4d382d39-a9da-4a3b-b7b6-d6890357d467
title: ID3DXMATRIXStack-Schnittstelle (D3dx9math.h)
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
ms.openlocfilehash: 62681c468fa7e78e6fd08c458798d98b467b992e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093318"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="4ee52-103">ID3DXMATRIXStack-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4ee52-103">ID3DXMATRIXStack interface</span></span>

<span data-ttu-id="4ee52-104">Anwendungen verwenden die Methoden der ID3DXMATRIXStack-Schnittstelle, um einen Matrixstapel zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="4ee52-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="4ee52-105">Member</span><span class="sxs-lookup"><span data-stu-id="4ee52-105">Members</span></span>

<span data-ttu-id="4ee52-106">Die **ID3DXMATRIXStack-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="4ee52-106">The **ID3DXMATRIXStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4ee52-107">**ID3DXMATRIXStack** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4ee52-107">**ID3DXMATRIXStack** also has these types of members:</span></span>

-   [<span data-ttu-id="4ee52-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="4ee52-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4ee52-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="4ee52-109">Methods</span></span>

<span data-ttu-id="4ee52-110">Die **ID3DXMATRIXStack-Schnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4ee52-110">The **ID3DXMATRIXStack** interface has these methods.</span></span>



| <span data-ttu-id="4ee52-111">Methode</span><span class="sxs-lookup"><span data-stu-id="4ee52-111">Method</span></span>                                                                       | <span data-ttu-id="4ee52-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ee52-112">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ee52-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="4ee52-113">**GetTop**</span></span>](id3dxmatrixstack--gettop.md)                                   | <span data-ttu-id="4ee52-114">Ruft die aktuelle Matrix am anfang des Stapels ab.</span><span class="sxs-lookup"><span data-stu-id="4ee52-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="4ee52-115">**LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="4ee52-115">**LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)                       | <span data-ttu-id="4ee52-116">Lädt die Identität in der aktuellen Matrix.</span><span class="sxs-lookup"><span data-stu-id="4ee52-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="4ee52-117">**LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="4ee52-117">**LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)                           | <span data-ttu-id="4ee52-118">Lädt die gegebene Matrix in die aktuelle Matrix.</span><span class="sxs-lookup"><span data-stu-id="4ee52-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="4ee52-119">**MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="4ee52-119">**MultMatrix**</span></span>](id3dxmatrixstack--multmatrix.md)                           | <span data-ttu-id="4ee52-120">Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.</span><span class="sxs-lookup"><span data-stu-id="4ee52-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="4ee52-121">**MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="4ee52-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack--multmatrixlocal.md)                 | <span data-ttu-id="4ee52-122">Bestimmt das Produkt der angegebenen Matrix und der aktuellen Matrix.</span><span class="sxs-lookup"><span data-stu-id="4ee52-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="4ee52-123">**Pop**</span><span class="sxs-lookup"><span data-stu-id="4ee52-123">**Pop**</span></span>](id3dxmatrixstack--pop.md)                                         | <span data-ttu-id="4ee52-124">Entfernt die aktuelle Matrix vom anfang des Stapels.</span><span class="sxs-lookup"><span data-stu-id="4ee52-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="4ee52-125">**Drücken**</span><span class="sxs-lookup"><span data-stu-id="4ee52-125">**Push**</span></span>](id3dxmatrixstack--push.md)                                       | <span data-ttu-id="4ee52-126">Fügt dem Stapel eine Matrix hinzu.</span><span class="sxs-lookup"><span data-stu-id="4ee52-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="4ee52-127">**RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="4ee52-127">**RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)                           | <span data-ttu-id="4ee52-128">Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="4ee52-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="4ee52-129">**RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="4ee52-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)                 | <span data-ttu-id="4ee52-130">Rotiert (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="4ee52-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="4ee52-131">**RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="4ee52-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)           | <span data-ttu-id="4ee52-132">Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="4ee52-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="4ee52-133">**RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="4ee52-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md) | <span data-ttu-id="4ee52-134">Rotiert (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="4ee52-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="4ee52-135">**Skalieren**</span><span class="sxs-lookup"><span data-stu-id="4ee52-135">**Scale**</span></span>](id3dxmatrixstack--scale.md)                                     | <span data-ttu-id="4ee52-136">Skalieren Sie die aktuelle Matrix über den Ursprung der Weltkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="4ee52-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="4ee52-137">**ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="4ee52-137">**ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)                           | <span data-ttu-id="4ee52-138">Skalieren Sie die aktuelle Matrix über den Objektursprung.</span><span class="sxs-lookup"><span data-stu-id="4ee52-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="4ee52-139">**Übersetzen**</span><span class="sxs-lookup"><span data-stu-id="4ee52-139">**Translate**</span></span>](id3dxmatrixstack--translate.md)                             | <span data-ttu-id="4ee52-140">Bestimmt das Produkt der aktuellen Matrix und der berechneten Übersetzungsmatrix, die durch die angegebenen Faktoren (x, y und z) bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="4ee52-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="4ee52-141">**TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="4ee52-141">**TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)                   | <span data-ttu-id="4ee52-142">Bestimmt das Produkt der berechneten Übersetzungsmatrix, das durch die angegebenen Faktoren (x, y und z) und die aktuelle Matrix bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="4ee52-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4ee52-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ee52-143">Remarks</span></span>

<span data-ttu-id="4ee52-144">Die **ID3DXMATRIXStack-Schnittstelle** wird durch Aufrufen der [**D3DXCreateMatrixStack-Funktion**](d3dxcreatematrixstack.md) abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4ee52-144">The **ID3DXMATRIXStack** interface is obtained by calling the [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="4ee52-145">Der LPD3DXMATRIXSTACK-Typ wird als Zeiger auf die **ID3DXMATRIXStack-Schnittstelle** definiert.</span><span class="sxs-lookup"><span data-stu-id="4ee52-145">The LPD3DXMATRIXSTACK type is defined as a pointer to the **ID3DXMATRIXStack** interface.</span></span>


```
typedef interface ID3DXMATRIXStack ID3DXMATRIXStack;
typedef interface ID3DXMATRIXStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="4ee52-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ee52-146">Requirements</span></span>



| <span data-ttu-id="4ee52-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ee52-147">Requirement</span></span> | <span data-ttu-id="4ee52-148">Wert</span><span class="sxs-lookup"><span data-stu-id="4ee52-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee52-149">Header</span><span class="sxs-lookup"><span data-stu-id="4ee52-149">Header</span></span><br/>  | <dl> <span data-ttu-id="4ee52-150"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="4ee52-150"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4ee52-151">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4ee52-151">Library</span></span><br/> | <dl> <span data-ttu-id="4ee52-152"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ee52-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4ee52-153">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4ee52-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ee52-154">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4ee52-154">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
