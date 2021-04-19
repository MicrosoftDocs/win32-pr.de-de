---
description: Diese Schnittstelle wird von der Anwendung implementiert, um alle zusätzlichen in x-Dateien eingebetteten Benutzerdaten zu speichern.
ms.assetid: 6294f942-9c14-4eed-92a8-af2821fd7e13
title: ID3DXSaveUserData-Schnittstelle (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 77529a5a7b260dd27dc4af1752c88f55117bc974
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350677"
---
# <a name="id3dxsaveuserdata-interface"></a><span data-ttu-id="6422b-103">ID3DXSaveUserData-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6422b-103">ID3DXSaveUserData interface</span></span>

<span data-ttu-id="6422b-104">Diese Schnittstelle wird von der Anwendung implementiert, um alle zusätzlichen in x-Dateien eingebetteten Benutzerdaten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="6422b-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="6422b-105">Eine Instanz dieser Schnittstelle wird an [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md)und D3DX Ruft die entsprechende Methode für diese Schnittstelle immer dann auf, wenn die entsprechenden Daten gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="6422b-105">An instance of this interface is passed to [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="6422b-106">Beispielsweise wird für jedes Frame Objekt in der x-Datei [**ID3DXSaveUserData:: addframechilddata**](id3dxsaveuserdata--addframechilddata.md) aufgerufen und die untergeordneten Daten übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6422b-106">For example, for each frame object in the .x file, [**ID3DXSaveUserData::AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="6422b-107">Member</span><span class="sxs-lookup"><span data-stu-id="6422b-107">Members</span></span>

<span data-ttu-id="6422b-108">Die **ID3DXSaveUserData** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6422b-108">The **ID3DXSaveUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6422b-109">**ID3DXSaveUserData** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6422b-109">**ID3DXSaveUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="6422b-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="6422b-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6422b-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="6422b-111">Methods</span></span>

<span data-ttu-id="6422b-112">Die **ID3DXSaveUserData** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6422b-112">The **ID3DXSaveUserData** interface has these methods.</span></span>



| <span data-ttu-id="6422b-113">Methode</span><span class="sxs-lookup"><span data-stu-id="6422b-113">Method</span></span>                                                                              | <span data-ttu-id="6422b-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6422b-114">Description</span></span>                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="6422b-115">**Addframechilddata**</span><span class="sxs-lookup"><span data-stu-id="6422b-115">**AddFrameChildData**</span></span>](id3dxsaveuserdata--addframechilddata.md)                   | <span data-ttu-id="6422b-116">Fügen Sie dem Frame untergeordnete Daten hinzu.</span><span class="sxs-lookup"><span data-stu-id="6422b-116">Add child data to the frame.</span></span><br/>                            |
| [<span data-ttu-id="6422b-117">**Addmeshchilddata**</span><span class="sxs-lookup"><span data-stu-id="6422b-117">**AddMeshChildData**</span></span>](id3dxsaveuserdata--addmeshchilddata.md)                     | <span data-ttu-id="6422b-118">Fügen Sie dem Mesh untergeordnete Daten hinzu.</span><span class="sxs-lookup"><span data-stu-id="6422b-118">Add child data to the mesh.</span></span><br/>                             |
| [<span data-ttu-id="6422b-119">**Addtopleveldataobjectspost**</span><span class="sxs-lookup"><span data-stu-id="6422b-119">**AddTopLevelDataObjectsPost**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspost.md) | <span data-ttu-id="6422b-120">Fügen Sie ein Objekt der obersten Ebene nach der Frame Hierarchie hinzu.</span><span class="sxs-lookup"><span data-stu-id="6422b-120">Add a top level object after the frame hierarchy.</span></span><br/>       |
| [<span data-ttu-id="6422b-121">**Addtopleveldataobjectspre**</span><span class="sxs-lookup"><span data-stu-id="6422b-121">**AddTopLevelDataObjectsPre**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | <span data-ttu-id="6422b-122">Fügen Sie ein Objekt der obersten Ebene vor der Frame Hierarchie hinzu.</span><span class="sxs-lookup"><span data-stu-id="6422b-122">Add a top level object before the frame hierarchy.</span></span><br/>      |
| [<span data-ttu-id="6422b-123">**Register Templates**</span><span class="sxs-lookup"><span data-stu-id="6422b-123">**RegisterTemplates**</span></span>](id3dxsaveuserdata--registertemplates.md)                   | <span data-ttu-id="6422b-124">Ein Rückruf für den Benutzer zum Registrieren einer x-Datei Vorlage.</span><span class="sxs-lookup"><span data-stu-id="6422b-124">A callback for the user to register a .x file template.</span></span><br/> |
| [<span data-ttu-id="6422b-125">**Savetemplates**</span><span class="sxs-lookup"><span data-stu-id="6422b-125">**SaveTemplates**</span></span>](id3dxsaveuserdata--savetemplates.md)                           | <span data-ttu-id="6422b-126">Ein Rückruf für den Benutzer zum Speichern einer x-Datei Vorlage.</span><span class="sxs-lookup"><span data-stu-id="6422b-126">A callback for the user to save a .x file template.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="6422b-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6422b-127">Remarks</span></span>

<span data-ttu-id="6422b-128">Der LPD3DXSAVEUSERDATA-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="6422b-128">The LPD3DXSAVEUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="6422b-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6422b-129">Requirements</span></span>



| <span data-ttu-id="6422b-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6422b-130">Requirement</span></span> | <span data-ttu-id="6422b-131">Wert</span><span class="sxs-lookup"><span data-stu-id="6422b-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6422b-132">Header</span><span class="sxs-lookup"><span data-stu-id="6422b-132">Header</span></span><br/>  | <dl> <span data-ttu-id="6422b-133"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="6422b-133"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="6422b-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6422b-134">Library</span></span><br/> | <dl> <span data-ttu-id="6422b-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6422b-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6422b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6422b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6422b-137">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6422b-137">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
