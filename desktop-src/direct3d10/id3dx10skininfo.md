---
description: Mit ID3DX10SkinInfo können Sie die Beziehung zwischen den Knochen und Scheitel Punkten in ihren Netzen optimieren, verarbeiten und manuell festlegen (siehe "Skelett Animation" auf Wikipedia).
ms.assetid: bea0fe71-c201-45c6-8036-d0d76d5851fd
title: ID3DX10SkinInfo-Schnittstelle (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3216765ab9ef2ba9f2b0883c31a878a7eae6861f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354927"
---
# <a name="id3dx10skininfo-interface"></a><span data-ttu-id="d2fab-103">ID3DX10SkinInfo-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d2fab-103">ID3DX10SkinInfo interface</span></span>

<span data-ttu-id="d2fab-104">Mit ID3DX10SkinInfo können Sie die Beziehung zwischen den Knochen und Scheitel Punkten in ihren Netzen optimieren, verarbeiten und manuell festlegen (siehe " [Skelett Animation" auf Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)).</span><span class="sxs-lookup"><span data-stu-id="d2fab-104">ID3DX10SkinInfo allows you to optimize, process, and manually set the relationship between bones and vertices in your meshes (see [Skeletal Animation on Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)).</span></span> <span data-ttu-id="d2fab-105">Es ist besonders nützlich, wenn Sie x-Dateien, die von DCC-apps exportiert werden (z. b. 3ds Max und Maya), flexibler gestalten und die renderinggeschwindigkeit der im Software-Rendermodus gespritzelten Netze verbessern.</span><span class="sxs-lookup"><span data-stu-id="d2fab-105">It is most useful for making .x files exported by DCC Apps (such as 3DS Max and Maya) more hardware-friendly, and for improving the render speed of your skinned meshes in software render mode.</span></span>

## <a name="members"></a><span data-ttu-id="d2fab-106">Member</span><span class="sxs-lookup"><span data-stu-id="d2fab-106">Members</span></span>

<span data-ttu-id="d2fab-107">Die **ID3DX10SkinInfo** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d2fab-107">The **ID3DX10SkinInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d2fab-108">**ID3DX10SkinInfo** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d2fab-108">**ID3DX10SkinInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="d2fab-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="d2fab-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d2fab-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="d2fab-110">Methods</span></span>

<span data-ttu-id="d2fab-111">Die **ID3DX10SkinInfo** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d2fab-111">The **ID3DX10SkinInfo** interface has these methods.</span></span>



| <span data-ttu-id="d2fab-112">Methode</span><span class="sxs-lookup"><span data-stu-id="d2fab-112">Method</span></span>                                                                   | <span data-ttu-id="d2fab-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2fab-113">Description</span></span>                                                                                                                        |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2fab-114">**Addboneinfluences**</span><span class="sxs-lookup"><span data-stu-id="d2fab-114">**AddBoneInfluences**</span></span>](id3dx10skininfo-addboneinfluences.md)           | <span data-ttu-id="d2fab-115">Ermöglicht, dass ein vorhandener Arbeitsspeicher eine Gruppe von Scheitel Punkten beeinflusst und festlegt, wie viel Einfluss der Knochen auf jeden Scheitelpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="d2fab-115">Enable an existing bone to influence a group of vertices and define how much influence the bone has on each vertex.</span></span><br/>     |
| [<span data-ttu-id="d2fab-116">**Addbones**</span><span class="sxs-lookup"><span data-stu-id="d2fab-116">**AddBones**</span></span>](id3dx10skininfo-addbones.md)                             | <span data-ttu-id="d2fab-117">Speicherplatz für weitere Knochen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="d2fab-117">Allocate space for more bones.</span></span><br/>                                                                                          |
| [<span data-ttu-id="d2fab-118">**Addvertices**</span><span class="sxs-lookup"><span data-stu-id="d2fab-118">**AddVertices**</span></span>](id3dx10skininfo-addvertices.md)                       | <span data-ttu-id="d2fab-119">Zuweisen von Speicherplatz für weitere Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="d2fab-119">Allocate space for additional vertices.</span></span><br/>                                                                                 |
| [<span data-ttu-id="d2fab-120">**Clearboneingefluences**</span><span class="sxs-lookup"><span data-stu-id="d2fab-120">**ClearBoneInfluences**</span></span>](id3dx10skininfo-clearboneinfluences.md)       | <span data-ttu-id="d2fab-121">Löschen Sie die Liste der Scheitel Punkte, auf die sich die Schnittstelle auswirkt.</span><span class="sxs-lookup"><span data-stu-id="d2fab-121">Clear a bone's list of vertices that it influences.</span></span><br/>                                                                     |
| [<span data-ttu-id="d2fab-122">**Kompakt**</span><span class="sxs-lookup"><span data-stu-id="d2fab-122">**Compact**</span></span>](id3dx10skininfo-compact.md)                               | <span data-ttu-id="d2fab-123">Begrenzen Sie die Anzahl der Knochen, die einen Scheitelpunkt beeinflussen können, und/oder schränken Sie die Menge der Auswirkungen ein, die ein Knochen auf einen Scheitelpunkt aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="d2fab-123">Limit the number of bones that can influence a vertex and/or limit the amount of influence a bone can have on a vertex.</span></span><br/> |
| [<span data-ttu-id="d2fab-124">**Dosoftwareskinning**</span><span class="sxs-lookup"><span data-stu-id="d2fab-124">**DoSoftwareSkinning**</span></span>](id3dx10skininfo-dosoftwareskinning.md)         | <span data-ttu-id="d2fab-125">Führt die Software in einem Array von Vertices aus.</span><span class="sxs-lookup"><span data-stu-id="d2fab-125">Do software skinning on an array of vertices.</span></span><br/>                                                                           |
| [<span data-ttu-id="d2fab-126">**Findboneinfluumceindex**</span><span class="sxs-lookup"><span data-stu-id="d2fab-126">**FindBoneInfluenceIndex**</span></span>](id3dx10skininfo-findboneinfluenceindex.md) | <span data-ttu-id="d2fab-127">Suchen Sie nach dem Index, der angibt, wo sich ein bestimmter Scheitelpunkt in der Liste der beeinflussten Scheitel Punkte eines bestimmten Knotens befindet.</span><span class="sxs-lookup"><span data-stu-id="d2fab-127">Find the index that indicates where a given vertex is in a given bone's list of influenced vertices.</span></span><br/>                    |
| [<span data-ttu-id="d2fab-128">**Getboneingefluence**</span><span class="sxs-lookup"><span data-stu-id="d2fab-128">**GetBoneInfluence**</span></span>](id3dx10skininfo-getboneinfluence.md)             | <span data-ttu-id="d2fab-129">Gibt die Menge der Auswirkung an, die ein bestimmter Knochen über einem bestimmten Scheitelpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="d2fab-129">Get the amount of influence a given bone has over a given vertex.</span></span><br/>                                                       |
| [<span data-ttu-id="d2fab-130">**Getboneinfluercecount**</span><span class="sxs-lookup"><span data-stu-id="d2fab-130">**GetBoneInfluenceCount**</span></span>](id3dx10skininfo-getboneinfluencecount.md)   | <span data-ttu-id="d2fab-131">Gibt die Anzahl der Scheitel Punkte an, die von einem bestimmten Knochen beeinflusst werden.</span><span class="sxs-lookup"><span data-stu-id="d2fab-131">Get the number of vertices that a given bone influences.</span></span><br/>                                                                |
| [<span data-ttu-id="d2fab-132">**Getboneingefluences**</span><span class="sxs-lookup"><span data-stu-id="d2fab-132">**GetBoneInfluences**</span></span>](id3dx10skininfo-getboneinfluences.md)           | <span data-ttu-id="d2fab-133">Eine Liste der Scheitel Punkte, die von einem bestimmten Knochen beeinflusst werden, und eine Liste der Auswirkungen von Bone auf jeden Scheitelpunkt erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2fab-133">Get a list of vertices that a given bone influences and a list of the amount of influence that bone has on each vertex.</span></span><br/> |
| [<span data-ttu-id="d2fab-134">**Getmaxboneingefluences**</span><span class="sxs-lookup"><span data-stu-id="d2fab-134">**GetMaxBoneInfluences**</span></span>](id3dx10skininfo-getmaxboneinfluences.md)     | <span data-ttu-id="d2fab-135">Holen Sie sich die Anzahl der Scheitel Punkte, die ein Knochen Maximum beeinflussen kann.</span><span class="sxs-lookup"><span data-stu-id="d2fab-135">Get the number of vertices a bone can maximally influence.</span></span><br/>                                                              |
| [<span data-ttu-id="d2fab-136">**Getnumbones**</span><span class="sxs-lookup"><span data-stu-id="d2fab-136">**GetNumBones**</span></span>](id3dx10skininfo-getnumbones.md)                       | <span data-ttu-id="d2fab-137">Gibt die Anzahl der Knochen in ID3DX10SkinInfo an.</span><span class="sxs-lookup"><span data-stu-id="d2fab-137">Get the number of bones in ID3DX10SkinInfo.</span></span><br/>                                                                             |
| [<span data-ttu-id="d2fab-138">**Getnumvertices**</span><span class="sxs-lookup"><span data-stu-id="d2fab-138">**GetNumVertices**</span></span>](id3dx10skininfo-getnumvertices.md)                 | <span data-ttu-id="d2fab-139">Holen Sie sich die Anzahl der Vertices in ID3DX10SkinInfo.</span><span class="sxs-lookup"><span data-stu-id="d2fab-139">Get the number of vertices in ID3DX10SkinInfo.</span></span><br/>                                                                          |
| [<span data-ttu-id="d2fab-140">**Neu zuordnen**</span><span class="sxs-lookup"><span data-stu-id="d2fab-140">**RemapBones**</span></span>](id3dx10skininfo-remapbones.md)                         | <span data-ttu-id="d2fab-141">Ändern Sie, welche Knochen welche Scheitel Punkte beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="d2fab-141">Change which bones influence which vertices.</span></span><br/>                                                                            |
| [<span data-ttu-id="d2fab-142">**Remapvertices**</span><span class="sxs-lookup"><span data-stu-id="d2fab-142">**RemapVertices**</span></span>](id3dx10skininfo-remapvertices.md)                   | <span data-ttu-id="d2fab-143">Ändern der zu ändernden Scheitel Punkte</span><span class="sxs-lookup"><span data-stu-id="d2fab-143">Change which vertices are influenced by which bones.</span></span><br/>                                                                    |
| [<span data-ttu-id="d2fab-144">**Removebone**</span><span class="sxs-lookup"><span data-stu-id="d2fab-144">**RemoveBone**</span></span>](id3dx10skininfo-removebone.md)                         | <span data-ttu-id="d2fab-145">Entfernt einen Knochen.</span><span class="sxs-lookup"><span data-stu-id="d2fab-145">Remove a bone.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="d2fab-146">**Setboneingefluence**</span><span class="sxs-lookup"><span data-stu-id="d2fab-146">**SetBoneInfluence**</span></span>](id3dx10skininfo-setboneinfluence.md)             | <span data-ttu-id="d2fab-147">Legen Sie den Umfang der Auswirkung fest, den ein bestimmter Knochen über einem bestimmten Scheitelpunkt hat.</span><span class="sxs-lookup"><span data-stu-id="d2fab-147">Set the amount of influence a given bone has over a given vertex.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="d2fab-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2fab-148">Remarks</span></span>

<span data-ttu-id="d2fab-149">Erstellen Sie eine ID3DX10SkinInfo-Schnittstelle mit [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh** oder **D3DX10CreateSkinInfoFVF**.</span><span class="sxs-lookup"><span data-stu-id="d2fab-149">Create a ID3DX10SkinInfo interface with [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh**, or **D3DX10CreateSkinInfoFVF**.</span></span>

<span data-ttu-id="d2fab-150">Der LPD3DX10SKININFO-Typ wird als Zeiger auf die **ID3DX10SkinInfo** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="d2fab-150">The LPD3DX10SKININFO type is defined as a pointer to the **ID3DX10SkinInfo** interface.</span></span>


```
typedef struct ID3DX10SkinInfo *LPD3DX10SKININFO;
```



## <a name="requirements"></a><span data-ttu-id="d2fab-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2fab-151">Requirements</span></span>



| <span data-ttu-id="d2fab-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2fab-152">Requirement</span></span> | <span data-ttu-id="d2fab-153">Wert</span><span class="sxs-lookup"><span data-stu-id="d2fab-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2fab-154">Header</span><span class="sxs-lookup"><span data-stu-id="d2fab-154">Header</span></span><br/>  | <dl> <span data-ttu-id="d2fab-155"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2fab-155"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2fab-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d2fab-156">Library</span></span><br/> | <dl> <span data-ttu-id="d2fab-157"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2fab-157"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2fab-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2fab-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2fab-159">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d2fab-159">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
