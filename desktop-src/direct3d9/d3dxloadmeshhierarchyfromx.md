---
description: 'D3DXLoadMeshHierarchyFromX-Funktion: Lädt die erste Framehierarchie aus einer X-Datei.'
ms.assetid: 1d446b23-9028-4187-b97c-a61edfe68e39
title: D3DXLoadMeshHierarchyFromX-Funktion (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6f6f08e10155509df800cca3cb3788d6b27e520
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114358"
---
# <a name="d3dxloadmeshhierarchyfromx-function"></a><span data-ttu-id="cf417-103">D3DXLoadMeshHierarchyFromX-Funktion</span><span class="sxs-lookup"><span data-stu-id="cf417-103">D3DXLoadMeshHierarchyFromX function</span></span>

<span data-ttu-id="cf417-104">Lädt die erste Framehierarchie aus einer X-Datei.</span><span class="sxs-lookup"><span data-stu-id="cf417-104">Loads the first frame hierarchy from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf417-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf417-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshHierarchyFromX(
  _In_  LPCTSTR                   Filename,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHierarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="cf417-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf417-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf417-107">*Dateiname* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cf417-107">*Filename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf417-108">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cf417-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cf417-109">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="cf417-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="cf417-110">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen.</span><span class="sxs-lookup"><span data-stu-id="cf417-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="cf417-111">Andernfalls wird der Zeichenfolgendatentyp in LPCSTR auflösen.</span><span class="sxs-lookup"><span data-stu-id="cf417-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="cf417-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="cf417-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="cf417-113">*MeshOptions* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cf417-113">*MeshOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf417-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cf417-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cf417-115">Kombination von mindestens einem Flag aus der [**D3DXMESH-Enumeration,**](./d3dxmesh.md) die Erstellungsoptionen für das Gitternetz angeben.</span><span class="sxs-lookup"><span data-stu-id="cf417-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="cf417-116">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cf417-116">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf417-117">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="cf417-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="cf417-118">Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) das dem Gittermodell zugeordnete Geräteobjekt.</span><span class="sxs-lookup"><span data-stu-id="cf417-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="cf417-119">*pAlloc* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cf417-119">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf417-120">Typ: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="cf417-120">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="cf417-121">Zeiger auf eine [**ID3DXAllocateHierarchy-Schnittstelle.**](id3dxallocatehierarchy.md)</span><span class="sxs-lookup"><span data-stu-id="cf417-121">Pointer to an [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="cf417-122">*pUserDataLoader* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cf417-122">*pUserDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf417-123">Typ: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="cf417-123">Type: **[**LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span></span>

<span data-ttu-id="cf417-124">Von der Anwendung bereitgestellte Schnittstelle, die das Laden von Benutzerdaten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="cf417-124">Application provided interface that allows loading of user data.</span></span> <span data-ttu-id="cf417-125">Siehe [**ID3DXLoadUserData.**](id3dxloaduserdata.md)</span><span class="sxs-lookup"><span data-stu-id="cf417-125">See [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf417-126">*ppFrameHierarchy* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cf417-126">*ppFrameHierarchy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf417-127">Typ: **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="cf417-127">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="cf417-128">Gibt einen Zeiger auf die geladene Rahmenhierarchie zurück.</span><span class="sxs-lookup"><span data-stu-id="cf417-128">Returns a pointer to the loaded frame hierarchy.</span></span> <span data-ttu-id="cf417-129">Siehe [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="cf417-129">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf417-130">*ppAnimController* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cf417-130">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf417-131">Typ: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="cf417-131">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="cf417-132">Gibt einen Zeiger auf den Animationscontroller zurück, der der Animation in der X-Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="cf417-132">Returns a pointer to the animation controller corresponding to animation in the .x file.</span></span> <span data-ttu-id="cf417-133">Dies wird mit Standardspuren und Ereignissen erstellt.</span><span class="sxs-lookup"><span data-stu-id="cf417-133">This is created with default tracks and events.</span></span> <span data-ttu-id="cf417-134">Siehe [**ID3DXAnimationController.**](id3dxanimationcontroller.md)</span><span class="sxs-lookup"><span data-stu-id="cf417-134">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf417-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf417-135">Return value</span></span>

<span data-ttu-id="cf417-136">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cf417-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cf417-137">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cf417-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cf417-138">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cf417-138">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf417-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf417-139">Remarks</span></span>

<span data-ttu-id="cf417-140">Die Compilereinstellung bestimmt auch die Funktionsversion.</span><span class="sxs-lookup"><span data-stu-id="cf417-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="cf417-141">Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXLoadMeshHierarchyFromXW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="cf417-141">If Unicode is defined, the function call resolves to D3DXLoadMeshHierarchyFromXW.</span></span> <span data-ttu-id="cf417-142">Andernfalls wird der Funktionsaufruf in D3DXLoadMeshHierarchyFromXA aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="cf417-142">Otherwise, the function call resolves to D3DXLoadMeshHierarchyFromXA.</span></span>

<span data-ttu-id="cf417-143">Alle Gitternetze in der Datei werden in ein Ausgabegitternetz reduziert.</span><span class="sxs-lookup"><span data-stu-id="cf417-143">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="cf417-144">Wenn die Datei eine Rahmenhierarchie enthält, werden alle Transformationen auf das Gitternetz angewendet.</span><span class="sxs-lookup"><span data-stu-id="cf417-144">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="cf417-145">**D3DXLoadMeshHierarchyFromX** lädt die Animationsdaten und die Framehierarchie aus einer X-Datei.</span><span class="sxs-lookup"><span data-stu-id="cf417-145">**D3DXLoadMeshHierarchyFromX** loads the animation data and frame hierarchy from a .x file.</span></span> <span data-ttu-id="cf417-146">Sie scannt die X-Datei und erstellt eine Framehierarchie und einen Animationscontroller gemäß dem von [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)abgeleiteten Objekt, das über pAlloc an sie übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="cf417-146">It scans the .x file and builds a frame hierarchy and animation controller according to the [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)-derived object passed to it through pAlloc.</span></span> <span data-ttu-id="cf417-147">Das Laden der Daten erfordert mehrere Schritte wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cf417-147">Loading the data requires several steps as follows:</span></span>

1.  <span data-ttu-id="cf417-148">Leiten Sie [**ID3DXAllocateHierarchy ab,**](id3dxallocatehierarchy.md)und implementieren Sie jede Methode.</span><span class="sxs-lookup"><span data-stu-id="cf417-148">Derive [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), implementing each method.</span></span> <span data-ttu-id="cf417-149">Dies steuert, wie Frames und Gitternetze zugeordnet und frei werden.</span><span class="sxs-lookup"><span data-stu-id="cf417-149">This controls how frames and meshes are allocated and freed.</span></span>
2.  <span data-ttu-id="cf417-150">Leiten Sie [**ID3DXLoadUserData ab,**](id3dxloaduserdata.md)und implementieren Sie jede Methode.</span><span class="sxs-lookup"><span data-stu-id="cf417-150">Derive [**ID3DXLoadUserData**](id3dxloaduserdata.md), implementing each method.</span></span> <span data-ttu-id="cf417-151">Wenn Ihre X-Datei keine eingebetteten benutzerdefinierten Daten enthält oder Sie sie nicht benötigen, können Sie diesen Teil überspringen.</span><span class="sxs-lookup"><span data-stu-id="cf417-151">If your .x file has no embedded user-defined data, or if you do not need it, you can skip this part.</span></span>
3.  <span data-ttu-id="cf417-152">Erstellen Sie ein Objekt ihrer [**ID3DXAllocateHierarchy-Klasse**](id3dxallocatehierarchy.md) und optional Ihrer LoadUserData-Klasse.</span><span class="sxs-lookup"><span data-stu-id="cf417-152">Create an object of your [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) class, and optionally of your LoadUserData class.</span></span> <span data-ttu-id="cf417-153">Sie müssen keine Methoden dieser Objekte selbst aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cf417-153">You do not need to call any methods of these objects yourself.</span></span>
4.  <span data-ttu-id="cf417-154">Rufen **Sie D3DXLoadMeshHierarchyFromX** auf, und übergeben Sie ihr [**ID3DXAllocateHierarchy-Objekt**](id3dxallocatehierarchy.md) und Ihr [**ID3DXLoadUserData-Objekt**](id3dxloaduserdata.md) (oder **NULL),** um die Framehierarchie und den Animationscontroller zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cf417-154">Call **D3DXLoadMeshHierarchyFromX**, passing in your [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) object and your [**ID3DXLoadUserData**](id3dxloaduserdata.md) object (or **NULL**) to create the frame hierarchy and animation controller.</span></span> <span data-ttu-id="cf417-155">Alle Animationssätze und Frames werden automatisch beim Animationscontroller registriert.</span><span class="sxs-lookup"><span data-stu-id="cf417-155">All the animation sets and frames are automatically registered to the animation controller.</span></span>

<span data-ttu-id="cf417-156">Während des Ladevorgang werden [**CreateFrame**](id3dxallocatehierarchy--createframe.md) und [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) auf jedem Frame zurückgebewegt, um das Laden und die Zuordnung des Frames zu steuern.</span><span class="sxs-lookup"><span data-stu-id="cf417-156">During the load, [**CreateFrame**](id3dxallocatehierarchy--createframe.md) and [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) are called back on each frame to control loading and allocation of the frame.</span></span> <span data-ttu-id="cf417-157">Die Anwendung definiert diese Methoden, um zu steuern, wie Frames gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="cf417-157">The application defines these methods to control how frames are stored.</span></span> <span data-ttu-id="cf417-158">[**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) und [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) werden für jedes Gittermodellobjekt zurückgebewegt, um das Laden und die Zuordnung von Gittermodellobjekten zu steuern.</span><span class="sxs-lookup"><span data-stu-id="cf417-158">[**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) and [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) are called back on each mesh object to control loading and allocation of mesh objects.</span></span> <span data-ttu-id="cf417-159">[**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) wird für jedes Objekt der obersten Ebene zurückgewendet, das nicht von den anderen Methoden geladen wird.</span><span class="sxs-lookup"><span data-stu-id="cf417-159">[**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) is called back for each top level object that doesn't get loaded by the other methods.</span></span>

<span data-ttu-id="cf417-160">Um diese Daten frei zu geben, rufen Sie ID3DXAnimationController::Release auf, um die Animationssätze frei zu geben, und [**D3DXFRAMEDestroy**](d3dxframedestroy.md), indem Sie den Stammknoten der Framehierarchie und ein Objekt der abgeleiteten [**ID3DXAllocateHierarchy-Klasse**](id3dxallocatehierarchy.md) übergeben.</span><span class="sxs-lookup"><span data-stu-id="cf417-160">To free this data, call ID3DXAnimationController::Release to free the animation sets, and [**D3DXFRAMEDestroy**](d3dxframedestroy.md), passing in the root node of the frame hierarchy and an object of your derived [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) class.</span></span> <span data-ttu-id="cf417-161">[**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md) und [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) werden jeweils für jeden Frame und jedes Gittermodellobjekt in der Framehierarchie aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="cf417-161">[**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md) and [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) will each be called for every frame and mesh object in the frame hierarchy.</span></span> <span data-ttu-id="cf417-162">Ihre Implementierung von **DestroyFrame** sollte alles freigeben, was von [**CreateFrame**](id3dxallocatehierarchy--createframe.md)zugeordnet wird, und ebenso für die Meshcontainermethoden.</span><span class="sxs-lookup"><span data-stu-id="cf417-162">Your implementation of **DestroyFrame** should release everything allocated by [**CreateFrame**](id3dxallocatehierarchy--createframe.md), and likewise for the mesh container methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf417-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf417-163">Requirements</span></span>



| <span data-ttu-id="cf417-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf417-164">Requirement</span></span> | <span data-ttu-id="cf417-165">Wert</span><span class="sxs-lookup"><span data-stu-id="cf417-165">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf417-166">Header</span><span class="sxs-lookup"><span data-stu-id="cf417-166">Header</span></span><br/>  | <dl> <span data-ttu-id="cf417-167"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="cf417-167"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="cf417-168">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cf417-168">Library</span></span><br/> | <dl> <span data-ttu-id="cf417-169"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf417-169"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cf417-170">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cf417-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf417-171">Animationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="cf417-171">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
