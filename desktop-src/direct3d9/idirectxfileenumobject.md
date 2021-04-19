---
description: Anwendungen verwenden die Methoden der idirectxfileenumubject-Schnittstelle, um die Datenobjekte in der Datei zu durchlaufen und ein Datenobjekt anhand seiner Globally Unique Identifier (GUID) oder anhand seines Namens abzurufen. Veraltet.
ms.assetid: 9eefda2a-5b17-4330-8245-63a38c1b1469
title: Idirectxfileendumubject-Schnittstelle (dxfile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: f9220f6e0a406cb4143798787276d7aa6cb5f5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366454"
---
# <a name="idirectxfileenumobject-interface"></a><span data-ttu-id="252a5-104">Idirectxfile-umubject-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="252a5-104">IDirectXFileEnumObject interface</span></span>

<span data-ttu-id="252a5-105">Anwendungen verwenden die Methoden der idirectxfileenumubject-Schnittstelle, um die Datenobjekte in der Datei zu durchlaufen und ein Datenobjekt anhand seiner Globally Unique Identifier (GUID) oder anhand seines Namens abzurufen.</span><span class="sxs-lookup"><span data-stu-id="252a5-105">Applications use the methods of the IDirectXFileEnumObject interface to cycle through the data objects in the file and to retrieve a data object by its globally unique identifier (GUID) or by its name.</span></span> <span data-ttu-id="252a5-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="252a5-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="252a5-107">Member</span><span class="sxs-lookup"><span data-stu-id="252a5-107">Members</span></span>

<span data-ttu-id="252a5-108">Die **idirectxfileendumuject** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="252a5-108">The **IDirectXFileEnumObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="252a5-109">**Idirectxfileenumubject** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="252a5-109">**IDirectXFileEnumObject** also has these types of members:</span></span>

-   [<span data-ttu-id="252a5-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="252a5-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="252a5-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="252a5-111">Methods</span></span>

<span data-ttu-id="252a5-112">Die **idirectxfileerumuject** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="252a5-112">The **IDirectXFileEnumObject** interface has these methods.</span></span>



| <span data-ttu-id="252a5-113">Methode</span><span class="sxs-lookup"><span data-stu-id="252a5-113">Method</span></span>                                                                     | <span data-ttu-id="252a5-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="252a5-114">Description</span></span>                                                                     |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="252a5-115">**Getdataobjectbyid**</span><span class="sxs-lookup"><span data-stu-id="252a5-115">**GetDataObjectById**</span></span>](idirectxfileenumobject--getdataobjectbyid.md)     | <span data-ttu-id="252a5-116">Ruft das Datenobjekt ab, das über die angegebene GUID verfügt.</span><span class="sxs-lookup"><span data-stu-id="252a5-116">Retrieves the data object that has the specified GUID.</span></span> <span data-ttu-id="252a5-117">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="252a5-117">Deprecated.</span></span><br/>   |
| [<span data-ttu-id="252a5-118">**Getdataobjectbyname**</span><span class="sxs-lookup"><span data-stu-id="252a5-118">**GetDataObjectByName**</span></span>](idirectxfileenumobject--getdataobjectbyname.md) | <span data-ttu-id="252a5-119">Ruft das Datenobjekt ab, das über den angegebenen Namen verfügt.</span><span class="sxs-lookup"><span data-stu-id="252a5-119">Retrieves the data object that has the specified name.</span></span> <span data-ttu-id="252a5-120">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="252a5-120">Deprecated.</span></span><br/>   |
| [<span data-ttu-id="252a5-121">**Getnextdataobject**</span><span class="sxs-lookup"><span data-stu-id="252a5-121">**GetNextDataObject**</span></span>](idirectxfileenumobject--getnextdataobject.md)     | <span data-ttu-id="252a5-122">Ruft das nächste Objekt der obersten Ebene in der DirectX-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="252a5-122">Retrieves the next top-level object in the DirectX file.</span></span> <span data-ttu-id="252a5-123">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="252a5-123">Deprecated.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="252a5-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="252a5-124">Remarks</span></span>

<span data-ttu-id="252a5-125">Die GUID für die idirectxfileeinumuject-Schnittstelle ist IID \_ idirectxfileeinumubject.</span><span class="sxs-lookup"><span data-stu-id="252a5-125">The GUID for the IDirectXFileEnumObject interface is IID\_IDirectXFileEnumObject.</span></span>

<span data-ttu-id="252a5-126">Der lpdirectxfileendumubject-Typ ist als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="252a5-126">The LPDIRECTXFILEENUMOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileEnumObject *LPDIRECTXFILEENUMOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="252a5-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="252a5-127">Requirements</span></span>



| <span data-ttu-id="252a5-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="252a5-128">Requirement</span></span> | <span data-ttu-id="252a5-129">Wert</span><span class="sxs-lookup"><span data-stu-id="252a5-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="252a5-130">Header</span><span class="sxs-lookup"><span data-stu-id="252a5-130">Header</span></span><br/>  | <dl> <span data-ttu-id="252a5-131"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="252a5-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="252a5-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="252a5-132">Library</span></span><br/> | <dl> <span data-ttu-id="252a5-133"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="252a5-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="252a5-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="252a5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="252a5-135">X-Datei Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="252a5-135">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
