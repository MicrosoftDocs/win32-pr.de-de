---
description: 'ID3DXSaveUserData-Schnittstelle: Diese Schnittstelle wird von der Anwendung implementiert, um zusätzliche Benutzerdaten zu speichern, die in X-Dateien eingebettet sind.'
ms.assetid: 6294f942-9c14-4eed-92a8-af2821fd7e13
title: ID3DXSaveUserData-Schnittstelle (D3dx9anim.h)
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
ms.openlocfilehash: 5dbdc71239455772809e44f535634a0d06cc0653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107178"
---
# <a name="id3dxsaveuserdata-interface"></a><span data-ttu-id="7af45-103">ID3DXSaveUserData-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7af45-103">ID3DXSaveUserData interface</span></span>

<span data-ttu-id="7af45-104">Diese Schnittstelle wird von der Anwendung implementiert, um zusätzliche Benutzerdaten zu speichern, die in X-Dateien eingebettet sind.</span><span class="sxs-lookup"><span data-stu-id="7af45-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="7af45-105">Eine Instanz dieser Schnittstelle wird an [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md)übergeben, und D3DX ruft jedes Mal die entsprechende Methode auf dieser Schnittstelle auf, wenn die entsprechenden Daten gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="7af45-105">An instance of this interface is passed to [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="7af45-106">Beispielsweise wird für jedes Frameobjekt in der X-Datei [**ID3DXSaveUserData::AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) aufgerufen und die untergeordneten Daten übergeben.</span><span class="sxs-lookup"><span data-stu-id="7af45-106">For example, for each frame object in the .x file, [**ID3DXSaveUserData::AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="7af45-107">Member</span><span class="sxs-lookup"><span data-stu-id="7af45-107">Members</span></span>

<span data-ttu-id="7af45-108">Die **ID3DXSaveUserData-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="7af45-108">The **ID3DXSaveUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7af45-109">**ID3DXSaveUserData** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7af45-109">**ID3DXSaveUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="7af45-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="7af45-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7af45-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="7af45-111">Methods</span></span>

<span data-ttu-id="7af45-112">Die **ID3DXSaveUserData-Schnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7af45-112">The **ID3DXSaveUserData** interface has these methods.</span></span>



| <span data-ttu-id="7af45-113">Methode</span><span class="sxs-lookup"><span data-stu-id="7af45-113">Method</span></span>                                                                              | <span data-ttu-id="7af45-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7af45-114">Description</span></span>                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="7af45-115">**AddFrameChildData**</span><span class="sxs-lookup"><span data-stu-id="7af45-115">**AddFrameChildData**</span></span>](id3dxsaveuserdata--addframechilddata.md)                   | <span data-ttu-id="7af45-116">Fügen Sie dem Frame untergeordnete Daten hinzu.</span><span class="sxs-lookup"><span data-stu-id="7af45-116">Add child data to the frame.</span></span><br/>                            |
| [<span data-ttu-id="7af45-117">**AddMeshChildData**</span><span class="sxs-lookup"><span data-stu-id="7af45-117">**AddMeshChildData**</span></span>](id3dxsaveuserdata--addmeshchilddata.md)                     | <span data-ttu-id="7af45-118">Fügen Sie dem Gitternetz untergeordnete Daten hinzu.</span><span class="sxs-lookup"><span data-stu-id="7af45-118">Add child data to the mesh.</span></span><br/>                             |
| [<span data-ttu-id="7af45-119">**AddTopLevelDataObjectsPost**</span><span class="sxs-lookup"><span data-stu-id="7af45-119">**AddTopLevelDataObjectsPost**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspost.md) | <span data-ttu-id="7af45-120">Fügen Sie nach der Framehierarchie ein Objekt der obersten Ebene hinzu.</span><span class="sxs-lookup"><span data-stu-id="7af45-120">Add a top level object after the frame hierarchy.</span></span><br/>       |
| [<span data-ttu-id="7af45-121">**AddTopLevelDataObjectsPre**</span><span class="sxs-lookup"><span data-stu-id="7af45-121">**AddTopLevelDataObjectsPre**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | <span data-ttu-id="7af45-122">Fügen Sie vor der Framehierarchie ein Objekt der obersten Ebene hinzu.</span><span class="sxs-lookup"><span data-stu-id="7af45-122">Add a top level object before the frame hierarchy.</span></span><br/>      |
| [<span data-ttu-id="7af45-123">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="7af45-123">**RegisterTemplates**</span></span>](id3dxsaveuserdata--registertemplates.md)                   | <span data-ttu-id="7af45-124">Ein Rückruf für den Benutzer zum Registrieren einer X-Dateivorlage.</span><span class="sxs-lookup"><span data-stu-id="7af45-124">A callback for the user to register a .x file template.</span></span><br/> |
| [<span data-ttu-id="7af45-125">**SaveTemplates**</span><span class="sxs-lookup"><span data-stu-id="7af45-125">**SaveTemplates**</span></span>](id3dxsaveuserdata--savetemplates.md)                           | <span data-ttu-id="7af45-126">Ein Rückruf für den Benutzer zum Speichern einer X-Dateivorlage.</span><span class="sxs-lookup"><span data-stu-id="7af45-126">A callback for the user to save a .x file template.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="7af45-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7af45-127">Remarks</span></span>

<span data-ttu-id="7af45-128">Der LPD3DXSAVEUSERDATA-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="7af45-128">The LPD3DXSAVEUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="7af45-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7af45-129">Requirements</span></span>



| <span data-ttu-id="7af45-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7af45-130">Requirement</span></span> | <span data-ttu-id="7af45-131">Wert</span><span class="sxs-lookup"><span data-stu-id="7af45-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7af45-132">Header</span><span class="sxs-lookup"><span data-stu-id="7af45-132">Header</span></span><br/>  | <dl> <span data-ttu-id="7af45-133"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="7af45-133"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="7af45-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7af45-134">Library</span></span><br/> | <dl> <span data-ttu-id="7af45-135"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7af45-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7af45-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7af45-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7af45-137">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="7af45-137">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
