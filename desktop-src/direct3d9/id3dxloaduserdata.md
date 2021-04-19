---
description: Diese Schnittstelle wird von der Anwendung implementiert, um alle zusätzlichen in x-Dateien eingebetteten Benutzerdaten zu speichern.
ms.assetid: 0d656f99-c24c-4326-bc6f-c0e7874c0fb2
title: ID3DXLoadUserData-Schnittstelle (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fcb07ba9351e5f6c23dd86c8147151932b3972ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373493"
---
# <a name="id3dxloaduserdata-interface"></a><span data-ttu-id="33682-103">ID3DXLoadUserData-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="33682-103">ID3DXLoadUserData interface</span></span>

<span data-ttu-id="33682-104">Diese Schnittstelle wird von der Anwendung implementiert, um alle zusätzlichen in x-Dateien eingebetteten Benutzerdaten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="33682-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="33682-105">Eine Instanz dieser Schnittstelle wird an [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md)und D3DX Ruft die entsprechende Methode für diese Schnittstelle immer dann auf, wenn die entsprechenden Daten gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="33682-105">An instance of this interface is passed to [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="33682-106">Beispielsweise wird für jedes Frame Objekt in der x-Datei [**ID3DXLoadUserData:: loadframechilddata**](id3dxloaduserdata--loadframechilddata.md) aufgerufen und die untergeordneten Daten übermittelt.</span><span class="sxs-lookup"><span data-stu-id="33682-106">For example, for each frame object in the .x file, [**ID3DXLoadUserData::LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="33682-107">Member</span><span class="sxs-lookup"><span data-stu-id="33682-107">Members</span></span>

<span data-ttu-id="33682-108">Die **ID3DXLoadUserData** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="33682-108">The **ID3DXLoadUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="33682-109">**ID3DXLoadUserData** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="33682-109">**ID3DXLoadUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="33682-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="33682-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="33682-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="33682-111">Methods</span></span>

<span data-ttu-id="33682-112">Die **ID3DXLoadUserData** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="33682-112">The **ID3DXLoadUserData** interface has these methods.</span></span>



| <span data-ttu-id="33682-113">Methode</span><span class="sxs-lookup"><span data-stu-id="33682-113">Method</span></span>                                                              | <span data-ttu-id="33682-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33682-114">Description</span></span>                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="33682-115">**Loadframechilddata**</span><span class="sxs-lookup"><span data-stu-id="33682-115">**LoadFrameChildData**</span></span>](id3dxloaduserdata--loadframechilddata.md) | <span data-ttu-id="33682-116">Laden von untergeordneten Frame-Daten aus einer x-Datei.</span><span class="sxs-lookup"><span data-stu-id="33682-116">Load frame child data from a .x file.</span></span><br/> |
| [<span data-ttu-id="33682-117">**Loadmeshchilddata**</span><span class="sxs-lookup"><span data-stu-id="33682-117">**LoadMeshChildData**</span></span>](id3dxloaduserdata--loadmeshchilddata.md)   | <span data-ttu-id="33682-118">Laden von untergeordneten Mesh-Daten aus einer x-Datei.</span><span class="sxs-lookup"><span data-stu-id="33682-118">Load mesh child data from a .x file.</span></span><br/>  |
| [<span data-ttu-id="33682-119">**Loadtopleveldata**</span><span class="sxs-lookup"><span data-stu-id="33682-119">**LoadTopLevelData**</span></span>](id3dxloaduserdata--loadtopleveldata.md)     | <span data-ttu-id="33682-120">Laden von Daten der obersten Ebene aus einer x-Datei.</span><span class="sxs-lookup"><span data-stu-id="33682-120">Load top level data from a .x file.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="33682-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33682-121">Remarks</span></span>

<span data-ttu-id="33682-122">Der LPD3DXLOADUSERDATA-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="33682-122">The LPD3DXLOADUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="33682-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33682-123">Requirements</span></span>



| <span data-ttu-id="33682-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33682-124">Requirement</span></span> | <span data-ttu-id="33682-125">Wert</span><span class="sxs-lookup"><span data-stu-id="33682-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33682-126">Header</span><span class="sxs-lookup"><span data-stu-id="33682-126">Header</span></span><br/>  | <dl> <span data-ttu-id="33682-127"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="33682-127"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="33682-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="33682-128">Library</span></span><br/> | <dl> <span data-ttu-id="33682-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33682-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="33682-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33682-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33682-131">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="33682-131">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
