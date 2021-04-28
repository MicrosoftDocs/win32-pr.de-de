---
description: 'ID3DXLoadUserData-Schnittstelle: Diese Schnittstelle wird von der Anwendung implementiert, um zusätzliche Benutzerdaten zu speichern, die in X-Dateien eingebettet sind.'
ms.assetid: 0d656f99-c24c-4326-bc6f-c0e7874c0fb2
title: ID3DXLoadUserData-Schnittstelle (D3dx9anim.h)
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
ms.openlocfilehash: 83d603d2ec5fde00ef0b29d84368e04a1276f992
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093628"
---
# <a name="id3dxloaduserdata-interface"></a><span data-ttu-id="b58f4-103">ID3DXLoadUserData-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b58f4-103">ID3DXLoadUserData interface</span></span>

<span data-ttu-id="b58f4-104">Diese Schnittstelle wird von der Anwendung implementiert, um zusätzliche Benutzerdaten zu speichern, die in X-Dateien eingebettet sind.</span><span class="sxs-lookup"><span data-stu-id="b58f4-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="b58f4-105">Eine Instanz dieser Schnittstelle wird [**an D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md)übergeben, und D3DX ruft jedes Mal die entsprechende Methode auf dieser Schnittstelle auf, wenn die entsprechenden Daten gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="b58f4-105">An instance of this interface is passed to [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="b58f4-106">Beispielsweise wird für jedes Frameobjekt in der X-Datei [**ID3DXLoadUserData::LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) aufgerufen und die untergeordneten Daten übergeben.</span><span class="sxs-lookup"><span data-stu-id="b58f4-106">For example, for each frame object in the .x file, [**ID3DXLoadUserData::LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="b58f4-107">Member</span><span class="sxs-lookup"><span data-stu-id="b58f4-107">Members</span></span>

<span data-ttu-id="b58f4-108">Die **ID3DXLoadUserData-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="b58f4-108">The **ID3DXLoadUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b58f4-109">**ID3DXLoadUserData** verfügt auch über diese Membertypen:</span><span class="sxs-lookup"><span data-stu-id="b58f4-109">**ID3DXLoadUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="b58f4-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="b58f4-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b58f4-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="b58f4-111">Methods</span></span>

<span data-ttu-id="b58f4-112">Die **ID3DXLoadUserData-Schnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b58f4-112">The **ID3DXLoadUserData** interface has these methods.</span></span>



| <span data-ttu-id="b58f4-113">Methode</span><span class="sxs-lookup"><span data-stu-id="b58f4-113">Method</span></span>                                                              | <span data-ttu-id="b58f4-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b58f4-114">Description</span></span>                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="b58f4-115">**LoadFrameChildData**</span><span class="sxs-lookup"><span data-stu-id="b58f4-115">**LoadFrameChildData**</span></span>](id3dxloaduserdata--loadframechilddata.md) | <span data-ttu-id="b58f4-116">Laden sie untergeordnete Framedaten aus einer X-Datei.</span><span class="sxs-lookup"><span data-stu-id="b58f4-116">Load frame child data from a .x file.</span></span><br/> |
| [<span data-ttu-id="b58f4-117">**LoadMeshChildData**</span><span class="sxs-lookup"><span data-stu-id="b58f4-117">**LoadMeshChildData**</span></span>](id3dxloaduserdata--loadmeshchilddata.md)   | <span data-ttu-id="b58f4-118">Laden von untergeordneten Meshdaten aus einer X-Datei.</span><span class="sxs-lookup"><span data-stu-id="b58f4-118">Load mesh child data from a .x file.</span></span><br/>  |
| [<span data-ttu-id="b58f4-119">**LoadTopLevelData**</span><span class="sxs-lookup"><span data-stu-id="b58f4-119">**LoadTopLevelData**</span></span>](id3dxloaduserdata--loadtopleveldata.md)     | <span data-ttu-id="b58f4-120">Laden sie Daten der obersten Ebene aus einer X-Datei.</span><span class="sxs-lookup"><span data-stu-id="b58f4-120">Load top level data from a .x file.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="b58f4-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b58f4-121">Remarks</span></span>

<span data-ttu-id="b58f4-122">Der LPD3DXLOADUSERDATA-Typ ist als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="b58f4-122">The LPD3DXLOADUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="b58f4-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b58f4-123">Requirements</span></span>



| <span data-ttu-id="b58f4-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b58f4-124">Requirement</span></span> | <span data-ttu-id="b58f4-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b58f4-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b58f4-126">Header</span><span class="sxs-lookup"><span data-stu-id="b58f4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b58f4-127"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="b58f4-127"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b58f4-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b58f4-128">Library</span></span><br/> | <dl> <span data-ttu-id="b58f4-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b58f4-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b58f4-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b58f4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b58f4-131">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b58f4-131">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
