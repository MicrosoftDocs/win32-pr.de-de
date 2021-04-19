---
description: Die ID3DXRenderToEnvMap-Schnittstelle wird verwendet, um den Renderingvorgang in Umgebungs Zuordnungen zu generalisieren.
ms.assetid: d72db260-5493-4381-9269-521ad333f0b2
title: ID3DXRenderToEnvMap-Schnittstelle (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c3fdfc37c206b6360fc0b7296bbf90c319652e28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106369330"
---
# <a name="id3dxrendertoenvmap-interface"></a><span data-ttu-id="02e1e-103">ID3DXRenderToEnvMap-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="02e1e-103">ID3DXRenderToEnvMap interface</span></span>

<span data-ttu-id="02e1e-104">Die ID3DXRenderToEnvMap-Schnittstelle wird verwendet, um den Renderingvorgang in Umgebungs Zuordnungen zu generalisieren.</span><span class="sxs-lookup"><span data-stu-id="02e1e-104">The ID3DXRenderToEnvMap interface is used to generalize the process of rendering to environment maps.</span></span>

## <a name="members"></a><span data-ttu-id="02e1e-105">Member</span><span class="sxs-lookup"><span data-stu-id="02e1e-105">Members</span></span>

<span data-ttu-id="02e1e-106">Die **ID3DXRenderToEnvMap** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="02e1e-106">The **ID3DXRenderToEnvMap** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="02e1e-107">**ID3DXRenderToEnvMap** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="02e1e-107">**ID3DXRenderToEnvMap** also has these types of members:</span></span>

-   [<span data-ttu-id="02e1e-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="02e1e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="02e1e-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="02e1e-109">Methods</span></span>

<span data-ttu-id="02e1e-110">Die **ID3DXRenderToEnvMap** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="02e1e-110">The **ID3DXRenderToEnvMap** interface has these methods.</span></span>



| <span data-ttu-id="02e1e-111">Methode</span><span class="sxs-lookup"><span data-stu-id="02e1e-111">Method</span></span>                                                          | <span data-ttu-id="02e1e-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02e1e-112">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02e1e-113">**Begincube**</span><span class="sxs-lookup"><span data-stu-id="02e1e-113">**BeginCube**</span></span>](id3dxrendertoenvmap--begincube.md)             | <span data-ttu-id="02e1e-114">Initiieren Sie das Rendering einer kubischen Umgebungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="02e1e-114">Initiate the rendering of a cubic environment map.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="02e1e-115">**Beginhemisphäre**</span><span class="sxs-lookup"><span data-stu-id="02e1e-115">**BeginHemisphere**</span></span>](id3dxrendertoenvmap--beginhemisphere.md) | <span data-ttu-id="02e1e-116">Initiieren Sie das Rendering einer Hemispheric-Umgebungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="02e1e-116">Initiate the rendering of a hemispheric environment map.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="02e1e-117">**Beginparser**</span><span class="sxs-lookup"><span data-stu-id="02e1e-117">**BeginParabolic**</span></span>](id3dxrendertoenvmap--beginparabolic.md)   | <span data-ttu-id="02e1e-118">Initiieren des Renderings einer paramegigramm-Umgebungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="02e1e-118">Initiate the rendering of a parabolic environment map.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="02e1e-119">**Beginsphere**</span><span class="sxs-lookup"><span data-stu-id="02e1e-119">**BeginSphere**</span></span>](id3dxrendertoenvmap--beginsphere.md)         | <span data-ttu-id="02e1e-120">Initiieren des Renderings einer kugelförmigen Umgebungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="02e1e-120">Initiate the rendering of a spherical environment map.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="02e1e-121">**ENDE**</span><span class="sxs-lookup"><span data-stu-id="02e1e-121">**End**</span></span>](id3dxrendertoenvmap--end.md)                         | <span data-ttu-id="02e1e-122">Stellen Sie alle Renderziele wieder her, und erstellen Sie, falls erforderlich, alle gerenderten Gesichter in der Umgebungs Zuordnungs Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="02e1e-122">Restore all render targets and, if needed, compose all the rendered faces into the environment map surface.</span></span><br/>                                                                           |
| [<span data-ttu-id="02e1e-123">**Gesichtserkennung**</span><span class="sxs-lookup"><span data-stu-id="02e1e-123">**Face**</span></span>](id3dxrendertoenvmap--face.md)                       | <span data-ttu-id="02e1e-124">Initiieren Sie die Zeichnung der einzelnen Gesichter einer Umgebungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="02e1e-124">Initiate the drawing of each face of an environment map.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="02e1e-125">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="02e1e-125">**GetDesc**</span></span>](id3dxrendertoenvmap--getdesc.md)                 | <span data-ttu-id="02e1e-126">Ruft die Beschreibung der Renderoberfläche ab.</span><span class="sxs-lookup"><span data-stu-id="02e1e-126">Retrieves the description of the render surface.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="02e1e-127">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="02e1e-127">**GetDevice**</span></span>](id3dxrendertoenvmap--getdevice.md)             | <span data-ttu-id="02e1e-128">Ruft das Direct3D-Gerät ab, das der Umgebungs Zuordnung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="02e1e-128">Retrieves the Direct3D device associated with the environment map.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="02e1e-129">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="02e1e-129">**OnLostDevice**</span></span>](id3dxrendertoenvmap--onlostdevice.md)       | <span data-ttu-id="02e1e-130">Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen.</span><span class="sxs-lookup"><span data-stu-id="02e1e-130">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="02e1e-131">Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="02e1e-131">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="02e1e-132">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="02e1e-132">**OnResetDevice**</span></span>](id3dxrendertoenvmap--onresetdevice.md)     | <span data-ttu-id="02e1e-133">Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.</span><span class="sxs-lookup"><span data-stu-id="02e1e-133">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="02e1e-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02e1e-134">Remarks</span></span>

<span data-ttu-id="02e1e-135">Eine Umgebungs Zuordnung wird für Textur kartogramm verwendet, um eine anspruchsvollere Szene ohne komplexe Geometrie bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="02e1e-135">An environment map is used to texture-map scene geometry to provide a more sophisticated scene without using complex geometry.</span></span> <span data-ttu-id="02e1e-136">Diese Schnittstelle unterstützt das Erstellen von Oberflächen für die folgenden Arten von Geometrie: Cube, Halbkugel oder Hemispheric, Parser oder Kugel.</span><span class="sxs-lookup"><span data-stu-id="02e1e-136">This interface supports creating surfaces for the following kinds of geometry: cube, half sphere or hemispheric, parabolic, or sphere.</span></span>

<span data-ttu-id="02e1e-137">Die **ID3DXRenderToEnvMap** -Schnittstelle wird durch Aufrufen der [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) -Funktion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="02e1e-137">The **ID3DXRenderToEnvMap** interface is obtained by calling the [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) function.</span></span>

<span data-ttu-id="02e1e-138">Der LPD3DXRenderToEnvMap-Typ wird als Zeiger auf die **ID3DXRenderToEnvMap** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="02e1e-138">The LPD3DXRenderToEnvMap type is defined as a pointer to the **ID3DXRenderToEnvMap** interface.</span></span>


```
typedef interface ID3DXRenderToEnvMap ID3DXRenderToEnvMap;
typedef interface ID3DXRenderToEnvMap *LPD3DXRenderToEnvMap;
```



## <a name="requirements"></a><span data-ttu-id="02e1e-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02e1e-139">Requirements</span></span>



| <span data-ttu-id="02e1e-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02e1e-140">Requirement</span></span> | <span data-ttu-id="02e1e-141">Wert</span><span class="sxs-lookup"><span data-stu-id="02e1e-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02e1e-142">Header</span><span class="sxs-lookup"><span data-stu-id="02e1e-142">Header</span></span><br/>  | <dl> <span data-ttu-id="02e1e-143"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="02e1e-143"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="02e1e-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="02e1e-144">Library</span></span><br/> | <dl> <span data-ttu-id="02e1e-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02e1e-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="02e1e-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02e1e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e1e-147">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="02e1e-147">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
