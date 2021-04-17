---
description: Die ID3DXRenderToSurface-Schnittstelle wird verwendet, um den Renderingvorgang für-Oberflächen zu generalisieren.
ms.assetid: e9f2ca5e-faa3-45a8-94eb-16f354618e80
title: ID3DXRenderToSurface-Schnittstelle (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 577e729e4e1a510dd24dc981b2b90bdca27dc0f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355826"
---
# <a name="id3dxrendertosurface-interface"></a><span data-ttu-id="8e9fd-103">ID3DXRenderToSurface-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8e9fd-103">ID3DXRenderToSurface interface</span></span>

<span data-ttu-id="8e9fd-104">Die ID3DXRenderToSurface-Schnittstelle wird verwendet, um den Renderingvorgang für-Oberflächen zu generalisieren.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-104">The ID3DXRenderToSurface interface is used to generalize the process of rendering to surfaces.</span></span>

## <a name="members"></a><span data-ttu-id="8e9fd-105">Member</span><span class="sxs-lookup"><span data-stu-id="8e9fd-105">Members</span></span>

<span data-ttu-id="8e9fd-106">Die **ID3DXRenderToSurface** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-106">The **ID3DXRenderToSurface** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8e9fd-107">**ID3DXRenderToSurface** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8e9fd-107">**ID3DXRenderToSurface** also has these types of members:</span></span>

-   [<span data-ttu-id="8e9fd-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="8e9fd-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8e9fd-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="8e9fd-109">Methods</span></span>

<span data-ttu-id="8e9fd-110">Die **ID3DXRenderToSurface** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-110">The **ID3DXRenderToSurface** interface has these methods.</span></span>



| <span data-ttu-id="8e9fd-111">Methode</span><span class="sxs-lookup"><span data-stu-id="8e9fd-111">Method</span></span>                                                       | <span data-ttu-id="8e9fd-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e9fd-112">Description</span></span>                                                                                                                                                                                     |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e9fd-113">**BeginScene**</span><span class="sxs-lookup"><span data-stu-id="8e9fd-113">**BeginScene**</span></span>](id3dxrendertosurface--beginscene.md)       | <span data-ttu-id="8e9fd-114">Beginnt eine Szene.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-114">Begins a scene.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="8e9fd-115">**EndScene**</span><span class="sxs-lookup"><span data-stu-id="8e9fd-115">**EndScene**</span></span>](id3dxrendertosurface--endscene.md)           | <span data-ttu-id="8e9fd-116">Beendet eine Szene.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-116">Ends a scene.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="8e9fd-117">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="8e9fd-117">**GetDesc**</span></span>](id3dxrendertosurface--getdesc.md)             | <span data-ttu-id="8e9fd-118">Ruft die Parameter der Renderoberfläche ab.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-118">Retrieves the parameters of the render surface.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="8e9fd-119">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="8e9fd-119">**GetDevice**</span></span>](id3dxrendertosurface--getdevice.md)         | <span data-ttu-id="8e9fd-120">Ruft das Direct3D-Gerät ab, das der Renderoberfläche zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-120">Retrieves the Direct3D device associated with the render surface.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="8e9fd-121">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="8e9fd-121">**OnLostDevice**</span></span>](id3dxrendertosurface--onlostdevice.md)   | <span data-ttu-id="8e9fd-122">Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-122">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="8e9fd-123">Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-123">This method should be called whenever a device is lost or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="8e9fd-124">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="8e9fd-124">**OnResetDevice**</span></span>](id3dxrendertosurface--onresetdevice.md) | <span data-ttu-id="8e9fd-125">Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-125">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="8e9fd-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e9fd-126">Remarks</span></span>

<span data-ttu-id="8e9fd-127">Oberflächen können auf verschiedene Arten verwendet werden, z.b. Renderingziele, Offscreen-Rendering oder Rendering in Texturen.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-127">Surfaces can be used in a variety of ways including render targets, off-screen rendering, or rendering to textures.</span></span>

<span data-ttu-id="8e9fd-128">Eine Oberfläche kann mithilfe eines separaten Viewports konfiguriert werden, indem die [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md) -Methode verwendet wird, um eine benutzerdefinierte Renderansicht bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-128">A surface can be configured using a separate viewport using the [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md) method, to provide a custom render view.</span></span> <span data-ttu-id="8e9fd-129">Wenn es sich bei der-Oberfläche nicht um ein Renderziel handelt, wird ein kompatibles Renderziel verwendet, und das Ergebnis wird auf die-Oberfläche am Ende der Szene kopiert.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-129">If the surface is not a render target, a compatible render target is used, and the result is copied to the surface at the end of the scene.</span></span>

<span data-ttu-id="8e9fd-130">Die **ID3DXRenderToSurface** -Schnittstelle wird durch Aufrufen der [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) -Funktion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-130">The **ID3DXRenderToSurface** interface is obtained by calling the [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) function.</span></span>

<span data-ttu-id="8e9fd-131">Der LPD3DXRENDERTOSURFACE-Typ wird als Zeiger auf die **ID3DXRenderToSurface** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="8e9fd-131">The LPD3DXRENDERTOSURFACE type is defined as a pointer to the **ID3DXRenderToSurface** interface.</span></span>


```
typedef interface ID3DXRenderToSurface ID3DXRenderToSurface;
typedef interface ID3DXRenderToSurface *LPD3DXRENDERTOSURFACE;
```



## <a name="requirements"></a><span data-ttu-id="8e9fd-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e9fd-132">Requirements</span></span>



| <span data-ttu-id="8e9fd-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e9fd-133">Requirement</span></span> | <span data-ttu-id="8e9fd-134">Wert</span><span class="sxs-lookup"><span data-stu-id="8e9fd-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e9fd-135">Header</span><span class="sxs-lookup"><span data-stu-id="8e9fd-135">Header</span></span><br/>  | <dl> <span data-ttu-id="8e9fd-136"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e9fd-136"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="8e9fd-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8e9fd-137">Library</span></span><br/> | <dl> <span data-ttu-id="8e9fd-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e9fd-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8e9fd-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e9fd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e9fd-140">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8e9fd-140">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
