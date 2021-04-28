---
description: 'ID3DXMatrixStack-Schnittstelle: Anwendungen verwenden die Methoden der ID3DXMATRIXStack-Schnittstelle, um einen Matrixstapel zu bearbeiten.'
ms.assetid: 6c76f9e0-5f59-4cf3-b34a-2475536af6c7
title: ID3DXMatrixStack-Schnittstelle (D3DX10.h)
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
ms.openlocfilehash: 65e9a5cd041431e1939346fec79dcf94fccd4ae9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094408"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="eac22-103">ID3DXMatrixStack-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="eac22-103">ID3DXMatrixStack interface</span></span>

<span data-ttu-id="eac22-104">Anwendungen verwenden die Methoden der ID3DXMATRIXStack-Schnittstelle, um einen Matrixstapel zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="eac22-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="eac22-105">Member</span><span class="sxs-lookup"><span data-stu-id="eac22-105">Members</span></span>

<span data-ttu-id="eac22-106">Die **ID3DXMatrixStack-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="eac22-106">The **ID3DXMatrixStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="eac22-107">**ID3DXMatrixStack** verfügt auch über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="eac22-107">**ID3DXMatrixStack** also has these types of members:</span></span>

-   [<span data-ttu-id="eac22-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="eac22-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eac22-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="eac22-109">Methods</span></span>

<span data-ttu-id="eac22-110">Die **ID3DXMatrixStack-Schnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="eac22-110">The **ID3DXMatrixStack** interface has these methods.</span></span>



| <span data-ttu-id="eac22-111">Methode</span><span class="sxs-lookup"><span data-stu-id="eac22-111">Method</span></span>                                                                      | <span data-ttu-id="eac22-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eac22-112">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eac22-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="eac22-113">**GetTop**</span></span>](id3dxmatrixstack-gettop.md)                                   | <span data-ttu-id="eac22-114">Ruft die aktuelle Matrix am anfang des Stapels ab.</span><span class="sxs-lookup"><span data-stu-id="eac22-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="eac22-115">**LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="eac22-115">**LoadIdentity**</span></span>](id3dxmatrixstack-loadidentity.md)                       | <span data-ttu-id="eac22-116">Lädt die Identität in der aktuellen Matrix.</span><span class="sxs-lookup"><span data-stu-id="eac22-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="eac22-117">**LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="eac22-117">**LoadMatrix**</span></span>](id3dxmatrixstack-loadmatrix.md)                           | <span data-ttu-id="eac22-118">Lädt die gegebene Matrix in die aktuelle Matrix.</span><span class="sxs-lookup"><span data-stu-id="eac22-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="eac22-119">**MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="eac22-119">**MultMatrix**</span></span>](id3dxmatrixstack-multmatrix.md)                           | <span data-ttu-id="eac22-120">Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.</span><span class="sxs-lookup"><span data-stu-id="eac22-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="eac22-121">**MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="eac22-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack-multmatrixlocal.md)                 | <span data-ttu-id="eac22-122">Bestimmt das Produkt der angegebenen Matrix und der aktuellen Matrix.</span><span class="sxs-lookup"><span data-stu-id="eac22-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="eac22-123">**Pop**</span><span class="sxs-lookup"><span data-stu-id="eac22-123">**Pop**</span></span>](id3dxmatrixstack-pop.md)                                         | <span data-ttu-id="eac22-124">Entfernt die aktuelle Matrix vom anfang des Stapels.</span><span class="sxs-lookup"><span data-stu-id="eac22-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="eac22-125">**Drücken**</span><span class="sxs-lookup"><span data-stu-id="eac22-125">**Push**</span></span>](id3dxmatrixstack-push.md)                                       | <span data-ttu-id="eac22-126">Fügt dem Stapel eine Matrix hinzu.</span><span class="sxs-lookup"><span data-stu-id="eac22-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="eac22-127">**RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="eac22-127">**RotateAxis**</span></span>](id3dxmatrixstack-rotateaxis.md)                           | <span data-ttu-id="eac22-128">Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="eac22-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="eac22-129">**RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="eac22-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack-rotateaxislocal.md)                 | <span data-ttu-id="eac22-130">Rotiert (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="eac22-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="eac22-131">**RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="eac22-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack-rotateyawpitchroll.md)           | <span data-ttu-id="eac22-132">Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="eac22-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="eac22-133">**RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="eac22-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack-rotateyawpitchrolllocal.md) | <span data-ttu-id="eac22-134">Rotiert (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="eac22-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="eac22-135">**Skalieren**</span><span class="sxs-lookup"><span data-stu-id="eac22-135">**Scale**</span></span>](id3dxmatrixstack-scale.md)                                     | <span data-ttu-id="eac22-136">Skalieren Sie die aktuelle Matrix über den Ursprung der Weltkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="eac22-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="eac22-137">**ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="eac22-137">**ScaleLocal**</span></span>](id3dxmatrixstack-scalelocal.md)                           | <span data-ttu-id="eac22-138">Skalieren Sie die aktuelle Matrix über den Objektursprung.</span><span class="sxs-lookup"><span data-stu-id="eac22-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="eac22-139">**Übersetzen**</span><span class="sxs-lookup"><span data-stu-id="eac22-139">**Translate**</span></span>](id3dxmatrixstack-translate.md)                             | <span data-ttu-id="eac22-140">Bestimmt das Produkt der aktuellen Matrix und der berechneten Übersetzungsmatrix, die durch die angegebenen Faktoren (x, y und z) bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="eac22-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="eac22-141">**TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="eac22-141">**TranslateLocal**</span></span>](id3dxmatrixstack-translatelocal.md)                   | <span data-ttu-id="eac22-142">Bestimmt das Produkt der berechneten Übersetzungsmatrix, das durch die angegebenen Faktoren (x, y und z) und die aktuelle Matrix bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="eac22-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eac22-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eac22-143">Remarks</span></span>

<span data-ttu-id="eac22-144">Die ID3DX10MATRIXStack-Schnittstelle wird durch Aufrufen der [**D3DXCreateMatrixStack-Funktion**](d3d10-d3dxcreatematrixstack.md) abgerufen.</span><span class="sxs-lookup"><span data-stu-id="eac22-144">The ID3DX10MATRIXStack interface is obtained by calling the [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="eac22-145">Der LPD3DX10MATRIXSTACK-Typ wird als Zeiger auf die **ID3DXMatrixStack-Schnittstelle** definiert.</span><span class="sxs-lookup"><span data-stu-id="eac22-145">The LPD3DX10MATRIXSTACK type is defined as a pointer to the **ID3DXMatrixStack** interface.</span></span>


```
typedef interface ID3DXMatrixStack ID3DXMatrixStack;
typedef interface ID3DXMatrixStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="eac22-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eac22-146">Requirements</span></span>



| <span data-ttu-id="eac22-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eac22-147">Requirement</span></span> | <span data-ttu-id="eac22-148">Wert</span><span class="sxs-lookup"><span data-stu-id="eac22-148">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eac22-149">Header</span><span class="sxs-lookup"><span data-stu-id="eac22-149">Header</span></span><br/>  | <dl> <span data-ttu-id="eac22-150"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="eac22-150"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="eac22-151">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eac22-151">Library</span></span><br/> | <dl> <span data-ttu-id="eac22-152"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="eac22-152"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eac22-153">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eac22-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eac22-154">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="eac22-154">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
