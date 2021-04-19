---
description: Definiert die Speicher Klasse, die die Puffer für eine Ressource enthält.
ms.assetid: 29720b5f-16d7-4bd9-a7bd-e4dbfb00070b
title: D3DPOOL-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPOOL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc1d69d094b2f810855f9ce2116c472ba8ab605e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357244"
---
# <a name="d3dpool-enumeration"></a><span data-ttu-id="9d404-103">D3DPOOL-Enumeration</span><span class="sxs-lookup"><span data-stu-id="9d404-103">D3DPOOL enumeration</span></span>

<span data-ttu-id="9d404-104">Definiert die Speicher Klasse, die die Puffer für eine Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="9d404-104">Defines the memory class that holds the buffers for a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d404-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d404-105">Syntax</span></span>


```C++
typedef enum D3DPOOL { 
  D3DPOOL_DEFAULT      = 0,
  D3DPOOL_MANAGED      = 1,
  D3DPOOL_SYSTEMMEM    = 2,
  D3DPOOL_SCRATCH      = 3,
  D3DPOOL_FORCE_DWORD  = 0x7fffffff
} D3DPOOL, *LPD3DPOOL;
```



## <a name="constants"></a><span data-ttu-id="9d404-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="9d404-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9d404-107"><span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**D3DPOOL \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="9d404-107"><span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**D3DPOOL\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="9d404-108">Ressourcen werden in den Speicherpool eingefügt, der sich am besten für den Satz von Verwendungen eignet, die für die jeweilige Ressource angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="9d404-108">Resources are placed in the memory pool most appropriate for the set of usages requested for the given resource.</span></span> <span data-ttu-id="9d404-109">Dabei handelt es sich in der Regel um Videospeicher, einschließlich des lokalen Video Speichers und des AGP-Speichers.</span><span class="sxs-lookup"><span data-stu-id="9d404-109">This is usually video memory, including both local video memory and AGP memory.</span></span> <span data-ttu-id="9d404-110">Der D3DPOOL \_ -Standard Pool ist getrennt von D3DPOOL \_ Managed und D3DPOOL \_ SystemMem und gibt an, dass die Ressource für den Gerätezugriff im bevorzugten Speicher abgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="9d404-110">The D3DPOOL\_DEFAULT pool is separate from D3DPOOL\_MANAGED and D3DPOOL\_SYSTEMMEM, and it specifies that the resource is placed in the preferred memory for device access.</span></span> <span data-ttu-id="9d404-111">Beachten Sie, dass D3DPOOL \_ default niemals angibt, dass entweder D3DPOOL \_ Managed oder D3DPOOL \_ SystemMem als Speicher Pooltyp für diese Ressource ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d404-111">Note that D3DPOOL\_DEFAULT never indicates that either D3DPOOL\_MANAGED or D3DPOOL\_SYSTEMMEM should be chosen as the memory pool type for this resource.</span></span> <span data-ttu-id="9d404-112">Texturen, die im D3DPOOL- \_ Standard Pool platziert werden, können nicht gesperrt werden, es sei denn, Sie sind dynamische Texturen oder private, FourCC-Treiber Formate.</span><span class="sxs-lookup"><span data-stu-id="9d404-112">Textures placed in the D3DPOOL\_DEFAULT pool cannot be locked unless they are dynamic textures or they are private, FOURCC, driver formats.</span></span> <span data-ttu-id="9d404-113">Um auf nicht Sperr Bare Texturen zuzugreifen, müssen Sie Funktionen wie [**IDirect3DDevice9:: updatesurface**](/windows/desktop/api), [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9:: getfrontbufferdata**](/windows/desktop/api)und [**IDirect3DDevice9:: GetRenderTargetData**](/windows/desktop/api)verwenden.</span><span class="sxs-lookup"><span data-stu-id="9d404-113">To access unlockable textures, you must use functions such as [**IDirect3DDevice9::UpdateSurface**](/windows/desktop/api), [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9::GetFrontBufferData**](/windows/desktop/api), and [**IDirect3DDevice9::GetRenderTargetData**](/windows/desktop/api).</span></span> <span data-ttu-id="9d404-114">D3DPOOL \_ Managed ist für die meisten Anwendungen wahrscheinlich eine bessere Wahl als die D3DPOOL- \_ Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="9d404-114">D3DPOOL\_MANAGED is probably a better choice than D3DPOOL\_DEFAULT for most applications.</span></span> <span data-ttu-id="9d404-115">Beachten Sie, dass einige Texturen, die in den vom Treiber proprietären Pixel Formaten erstellt wurden, für die Direct3D-Laufzeit unbekannt sind, gesperrt werden können.</span><span class="sxs-lookup"><span data-stu-id="9d404-115">Note that some textures created in driver-proprietary pixel formats, unknown to the Direct3D runtime, can be locked.</span></span> <span data-ttu-id="9d404-116">Beachten Sie auch, dass im Gegensatz zu Texturen-SwapChain-Back-Puffer, Renderziele, Scheitelpunkt Puffer und Index Puffer gesperrt werden können.</span><span class="sxs-lookup"><span data-stu-id="9d404-116">Also note that - unlike textures - swap chain back buffers, render targets, vertex buffers, and index buffers can be locked.</span></span> <span data-ttu-id="9d404-117">Wenn ein Gerät verloren geht, müssen mit D3DPOOL default erstellte Ressourcen \_ freigegeben werden, [**bevor IDirect3DDevice9:: Reset**](/windows/desktop/api)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9d404-117">When a device is lost, resources created using D3DPOOL\_DEFAULT must be released before calling [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="9d404-118">Weitere Informationen finden Sie unter [verlorene Geräte (Direct3D 9)](lost-devices.md).</span><span class="sxs-lookup"><span data-stu-id="9d404-118">For more information, see [Lost Devices (Direct3D 9)](lost-devices.md).</span></span>

<span data-ttu-id="9d404-119">Wenn beim Erstellen von Ressourcen mit der D3DPOOL- \_ Standardeinstellung für den Grafikkartenspeicher bereits ein Commit ausgeführt wurde, werden verwaltete Ressourcen entfernt, um genügend Arbeitsspeicher zum erfüllen der Anforderung freizugeben.</span><span class="sxs-lookup"><span data-stu-id="9d404-119">When creating resources with D3DPOOL\_DEFAULT, if video card memory is already committed, managed resources will be evicted to free enough memory to satisfy the request.</span></span>

</dd> <dt>

<span data-ttu-id="9d404-120"><span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**D3DPOOL \_ verwaltet**</span><span class="sxs-lookup"><span data-stu-id="9d404-120"><span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**D3DPOOL\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="9d404-121">Ressourcen werden nach Bedarf automatisch in den Speicherzugriff auf das Gerät kopiert.</span><span class="sxs-lookup"><span data-stu-id="9d404-121">Resources are copied automatically to device-accessible memory as needed.</span></span> <span data-ttu-id="9d404-122">Verwaltete Ressourcen werden durch den System Arbeitsspeicher unterstützt und müssen nicht neu erstellt werden, wenn ein Gerät verloren geht.</span><span class="sxs-lookup"><span data-stu-id="9d404-122">Managed resources are backed by system memory and do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="9d404-123">Weitere Informationen finden Sie unter [Verwalten von Ressourcen (Direct3D 9)](managing-resources.md) .</span><span class="sxs-lookup"><span data-stu-id="9d404-123">See [Managing Resources (Direct3D 9)](managing-resources.md) for more information.</span></span> <span data-ttu-id="9d404-124">Verwaltete Ressourcen können gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="9d404-124">Managed resources can be locked.</span></span> <span data-ttu-id="9d404-125">Es wird nur die Systemspeicher Kopie direkt geändert.</span><span class="sxs-lookup"><span data-stu-id="9d404-125">Only the system-memory copy is directly modified.</span></span> <span data-ttu-id="9d404-126">Direct3D kopiert die Änderungen nach Bedarf in den vom Treiber zugänglichen Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="9d404-126">Direct3D copies your changes to driver-accessible memory as needed.</span></span>



|                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d404-127">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="9d404-127">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="9d404-128">D3DPOOL \_ Managed ist mit [**IDirect3DDevice9**](/windows/desktop/api)gültig, jedoch nicht mit [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).</span><span class="sxs-lookup"><span data-stu-id="9d404-128">D3DPOOL\_MANAGED is valid with [**IDirect3DDevice9**](/windows/desktop/api); however, it is not valid with [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9d404-129"><span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL \_ SystemMem**</span><span class="sxs-lookup"><span data-stu-id="9d404-129"><span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="9d404-130">Ressourcen werden in den Arbeitsspeicher eingefügt, der in der Regel nicht vom Direct3D-Gerät zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="9d404-130">Resources are placed in memory that is not typically accessible by the Direct3D device.</span></span> <span data-ttu-id="9d404-131">Diese Speicher Belegung beansprucht System-RAM, verringert jedoch nicht das kostenpflichtige RAM.</span><span class="sxs-lookup"><span data-stu-id="9d404-131">This memory allocation consumes system RAM but does not reduce pageable RAM.</span></span> <span data-ttu-id="9d404-132">Diese Ressourcen müssen nicht neu erstellt werden, wenn ein Gerät verloren geht.</span><span class="sxs-lookup"><span data-stu-id="9d404-132">These resources do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="9d404-133">Die Ressourcen in diesem Pool können gesperrt werden und können als Quelle für einen [**IDirect3DDevice9:: updatesurface**](/windows/desktop/api) -oder [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) -Vorgang zu einer Speicher Ressource verwendet werden, die mit D3DPOOL default erstellt wurde \_ .</span><span class="sxs-lookup"><span data-stu-id="9d404-133">Resources in this pool can be locked and can be used as the source for a [**IDirect3DDevice9::UpdateSurface**](/windows/desktop/api) or [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) operation to a memory resource created with D3DPOOL\_DEFAULT.</span></span>

</dd> <dt>

<span data-ttu-id="9d404-134"><span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL \_ Scratch**</span><span class="sxs-lookup"><span data-stu-id="9d404-134"><span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL\_SCRATCH**</span></span>
</dt> <dd>

<span data-ttu-id="9d404-135">Ressourcen werden im System-RAM abgelegt und müssen nicht neu erstellt werden, wenn ein Gerät verloren geht.</span><span class="sxs-lookup"><span data-stu-id="9d404-135">Resources are placed in system RAM and do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="9d404-136">Diese Ressourcen werden nicht durch die Größe von Geräten oder Formatierungs Beschränkungen gebunden.</span><span class="sxs-lookup"><span data-stu-id="9d404-136">These resources are not bound by device size or format restrictions.</span></span> <span data-ttu-id="9d404-137">Aus diesem Grund kann auf diese Ressourcen nicht durch das Direct3D-Gerät zugegriffen werden, und es wird nicht als Texturen oder Renderziele festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9d404-137">Because of this, these resources cannot be accessed by the Direct3D device nor set as textures or render targets.</span></span> <span data-ttu-id="9d404-138">Diese Ressourcen können jedoch immer erstellt, gesperrt und kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="9d404-138">However, these resources can always be created, locked, and copied.</span></span>

</dd> <dt>

<span data-ttu-id="9d404-139"><span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="9d404-139"><span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="9d404-140">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="9d404-140">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="9d404-141">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="9d404-141">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="9d404-142">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d404-142">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d404-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d404-143">Remarks</span></span>

<span data-ttu-id="9d404-144">Alle pooltypen sind mit allen Ressourcen gültig, einschließlich Scheitelpunkt Puffer, Index Puffer, Texturen und Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="9d404-144">All pool types are valid with all resources including: vertex buffers, index buffers, textures, and surfaces.</span></span>

<span data-ttu-id="9d404-145">In den folgenden Tabellen werden die Einschränkungen für die pooltypen für Renderziele, tiefen Schablonen und dynamische und MipMap-Verwendungen angegeben.</span><span class="sxs-lookup"><span data-stu-id="9d404-145">The following tables indicate restrictions on pool types for render targets, depth stencils, and dynamic and mipmap usages.</span></span> <span data-ttu-id="9d404-146">Ein x gibt eine kompatible Kombination an. das Fehlen von x deutet auf Inkompatibilität hin.</span><span class="sxs-lookup"><span data-stu-id="9d404-146">An x indicates a compatible combination; lack of an x indicates incompatibility.</span></span>



| <span data-ttu-id="9d404-147">Pool</span><span class="sxs-lookup"><span data-stu-id="9d404-147">Pool</span></span>               | <span data-ttu-id="9d404-148">D3DUSAGE \_ renderTarget</span><span class="sxs-lookup"><span data-stu-id="9d404-148">D3DUSAGE\_RENDERTARGET</span></span> | <span data-ttu-id="9d404-149">D3DUSAGE \_ depthstencil</span><span class="sxs-lookup"><span data-stu-id="9d404-149">D3DUSAGE\_DEPTHSTENCIL</span></span> |
|--------------------|------------------------|------------------------|
| <span data-ttu-id="9d404-150">D3DPOOL \_ Standard</span><span class="sxs-lookup"><span data-stu-id="9d404-150">D3DPOOL\_DEFAULT</span></span>   | <span data-ttu-id="9d404-151">x</span><span class="sxs-lookup"><span data-stu-id="9d404-151">x</span></span>                      | <span data-ttu-id="9d404-152">x</span><span class="sxs-lookup"><span data-stu-id="9d404-152">x</span></span>                      |
| <span data-ttu-id="9d404-153">D3DPOOL \_ verwaltet</span><span class="sxs-lookup"><span data-stu-id="9d404-153">D3DPOOL\_MANAGED</span></span>   |                        |                        |
| <span data-ttu-id="9d404-154">D3DPOOL \_ Scratch</span><span class="sxs-lookup"><span data-stu-id="9d404-154">D3DPOOL\_SCRATCH</span></span>   |                        |                        |
| <span data-ttu-id="9d404-155">D3DPOOL \_ SystemMem</span><span class="sxs-lookup"><span data-stu-id="9d404-155">D3DPOOL\_SYSTEMMEM</span></span> |                        |                        |



 



| <span data-ttu-id="9d404-156">Pool</span><span class="sxs-lookup"><span data-stu-id="9d404-156">Pool</span></span>               | <span data-ttu-id="9d404-157">D3DUSAGE \_ dynamisch</span><span class="sxs-lookup"><span data-stu-id="9d404-157">D3DUSAGE\_DYNAMIC</span></span> | <span data-ttu-id="9d404-158">D3DUSAGE \_ autogenmipmap</span><span class="sxs-lookup"><span data-stu-id="9d404-158">D3DUSAGE\_AUTOGENMIPMAP</span></span> |
|--------------------|-------------------|-------------------------|
| <span data-ttu-id="9d404-159">D3DPOOL \_ Standard</span><span class="sxs-lookup"><span data-stu-id="9d404-159">D3DPOOL\_DEFAULT</span></span>   | <span data-ttu-id="9d404-160">x</span><span class="sxs-lookup"><span data-stu-id="9d404-160">x</span></span>                 | <span data-ttu-id="9d404-161">x</span><span class="sxs-lookup"><span data-stu-id="9d404-161">x</span></span>                       |
| <span data-ttu-id="9d404-162">D3DPOOL \_ verwaltet</span><span class="sxs-lookup"><span data-stu-id="9d404-162">D3DPOOL\_MANAGED</span></span>   |                   | <span data-ttu-id="9d404-163">x</span><span class="sxs-lookup"><span data-stu-id="9d404-163">x</span></span>                       |
| <span data-ttu-id="9d404-164">D3DPOOL \_ Scratch</span><span class="sxs-lookup"><span data-stu-id="9d404-164">D3DPOOL\_SCRATCH</span></span>   |                   |                         |
| <span data-ttu-id="9d404-165">D3DPOOL \_ SystemMem</span><span class="sxs-lookup"><span data-stu-id="9d404-165">D3DPOOL\_SYSTEMMEM</span></span> | <span data-ttu-id="9d404-166">x</span><span class="sxs-lookup"><span data-stu-id="9d404-166">x</span></span>                 |                         |



 

<span data-ttu-id="9d404-167">Weitere Informationen zu Verwendungs Typen finden Sie unter [**D3DUSAGE**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="9d404-167">For more information about usage types, see [**D3DUSAGE**](d3dusage.md).</span></span>

<span data-ttu-id="9d404-168">Pools können nicht für verschiedene Objekte gemischt werden, die in einer Ressource (MIP-Ebenen in einer MipMap) enthalten sind, und wenn ein Pool ausgewählt wird, kann er nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="9d404-168">Pools cannot be mixed for different objects contained within one resource (mip levels in a mipmap) and, when a pool is chosen, it cannot be changed.</span></span>

<span data-ttu-id="9d404-169">Anwendungen sollten D3DPOOL \_ für die meisten statischen Ressourcen verwenden, da dadurch die Anwendung nicht mehr mit verlorenen Geräten verarbeitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="9d404-169">Applications should use D3DPOOL\_MANAGED for most static resources because this saves the application from having to deal with lost devices.</span></span> <span data-ttu-id="9d404-170">(Verwaltete Ressourcen werden von der Laufzeit wieder hergestellt.) Dies ist besonders für die Systeme mit einheitlicher Speicherarchitektur (Unified Memory Architecture, Uma) vorteilhaft.</span><span class="sxs-lookup"><span data-stu-id="9d404-170">(Managed resources are restored by the runtime.) This is especially beneficial for unified memory architecture (UMA) systems.</span></span> <span data-ttu-id="9d404-171">Andere dynamische Ressourcen sind für D3DPOOL nicht gut geeignet \_ .</span><span class="sxs-lookup"><span data-stu-id="9d404-171">Other dynamic resources are not a good match for D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="9d404-172">Tatsächlich können Index Puffer und Vertex-Puffer nicht mit D3DPOOL erstellt werden, die \_ mit D3DUSAGE \_ Dynamic verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="9d404-172">In fact, index buffers and vertex buffers cannot be created using D3DPOOL\_MANAGED together with D3DUSAGE\_DYNAMIC.</span></span>

<span data-ttu-id="9d404-173">Bei dynamischen Texturen ist es manchmal wünschenswert, ein paar von Grafikspeicher-und Systemspeicher Texturen zu verwenden und den Videospeicher mithilfe von D3DPOOL \_ default und dem Systemspeicher mithilfe von D3DPOOL \_ SystemMem zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="9d404-173">For dynamic textures, it is sometimes desirable to use a pair of video memory and system memory textures, allocating the video memory using D3DPOOL\_DEFAULT and the system memory using D3DPOOL\_SYSTEMMEM.</span></span> <span data-ttu-id="9d404-174">Sie können die Bits der Systemspeicher Textur mithilfe einer Sperr Methode sperren und ändern.</span><span class="sxs-lookup"><span data-stu-id="9d404-174">You can lock and modify the bits of the system memory texture using a locking method.</span></span> <span data-ttu-id="9d404-175">Anschließend können Sie die Grafikspeicher Textur mithilfe von [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture)aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9d404-175">Then you can update the video memory texture using [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d404-176">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d404-176">Requirements</span></span>



| <span data-ttu-id="9d404-177">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d404-177">Requirement</span></span> | <span data-ttu-id="9d404-178">Wert</span><span class="sxs-lookup"><span data-stu-id="9d404-178">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d404-179">Header</span><span class="sxs-lookup"><span data-stu-id="9d404-179">Header</span></span><br/> | <dl> <span data-ttu-id="9d404-180"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d404-180"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d404-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d404-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d404-182">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="9d404-182">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="9d404-183">**D3DUSAGE**</span><span class="sxs-lookup"><span data-stu-id="9d404-183">**D3DUSAGE**</span></span>](d3dusage.md)
</dt> <dt>

[<span data-ttu-id="9d404-184">**IDirect3DDevice9:: kreatecubetexture**</span><span class="sxs-lookup"><span data-stu-id="9d404-184">**IDirect3DDevice9::CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
</dt> <dt>

[<span data-ttu-id="9d404-185">**IDirect3DDevice9:: kreateingedexbuffer**</span><span class="sxs-lookup"><span data-stu-id="9d404-185">**IDirect3DDevice9::CreateIndexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
</dt> <dt>

[<span data-ttu-id="9d404-186">**IDirect3DDevice9:: kreatetexture**</span><span class="sxs-lookup"><span data-stu-id="9d404-186">**IDirect3DDevice9::CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
</dt> <dt>

[<span data-ttu-id="9d404-187">**IDirect3DDevice9:: kreatevolumetexture**</span><span class="sxs-lookup"><span data-stu-id="9d404-187">**IDirect3DDevice9::CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
</dt> <dt>

[<span data-ttu-id="9d404-188">**IDirect3DDevice9:: kreatevertexbuffer**</span><span class="sxs-lookup"><span data-stu-id="9d404-188">**IDirect3DDevice9::CreateVertexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
</dt> <dt>

[<span data-ttu-id="9d404-189">**D3DINDEXBUFFER- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="9d404-189">**D3DINDEXBUFFER\_DESC**</span></span>](d3dindexbuffer-desc.md)
</dt> <dt>

[<span data-ttu-id="9d404-190">**D3DSURFACE- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="9d404-190">**D3DSURFACE\_DESC**</span></span>](d3dsurface-desc.md)
</dt> <dt>

[<span data-ttu-id="9d404-191">**D3DVERTEXBUFFER- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="9d404-191">**D3DVERTEXBUFFER\_DESC**</span></span>](d3dvertexbuffer-desc.md)
</dt> <dt>

[<span data-ttu-id="9d404-192">**D3DVOLUME- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="9d404-192">**D3DVOLUME\_DESC**</span></span>](d3dvolume-desc.md)
</dt> </dl>

 

 
