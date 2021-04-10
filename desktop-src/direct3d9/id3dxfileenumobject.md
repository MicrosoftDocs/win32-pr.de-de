---
description: Anwendungen verwenden die Methoden der ID3DXFileEnumObject-Schnittstelle, um die untergeordneten Datei Datenobjekte in der Datei zu durchlaufen und ein untergeordnetes Objekt anhand seiner Globally Unique Identifier (GUID) oder anhand seines Namens abzurufen.
ms.assetid: 23b28f07-5832-4163-953b-615d20e781f6
title: ID3DXFileEnumObject-Schnittstelle (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f9b28f94c8d514f81aaa51426557c825da91c4bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961657"
---
# <a name="id3dxfileenumobject-interface"></a><span data-ttu-id="8b423-103">ID3DXFileEnumObject-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8b423-103">ID3DXFileEnumObject interface</span></span>

<span data-ttu-id="8b423-104">Anwendungen verwenden die Methoden der ID3DXFileEnumObject-Schnittstelle, um die untergeordneten Datei Datenobjekte in der Datei zu durchlaufen und ein untergeordnetes Objekt anhand seiner Globally Unique Identifier (GUID) oder anhand seines Namens abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8b423-104">Applications use the methods of the ID3DXFileEnumObject interface to cycle through the child file data objects in the file and to retrieve a child object by its globally unique identifier (GUID) or by its name.</span></span>

## <a name="members"></a><span data-ttu-id="8b423-105">Member</span><span class="sxs-lookup"><span data-stu-id="8b423-105">Members</span></span>

<span data-ttu-id="8b423-106">Die **ID3DXFileEnumObject** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8b423-106">The **ID3DXFileEnumObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8b423-107">**ID3DXFileEnumObject** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8b423-107">**ID3DXFileEnumObject** also has these types of members:</span></span>

-   [<span data-ttu-id="8b423-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="8b423-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8b423-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="8b423-109">Methods</span></span>

<span data-ttu-id="8b423-110">Die **ID3DXFileEnumObject** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8b423-110">The **ID3DXFileEnumObject** interface has these methods.</span></span>



| <span data-ttu-id="8b423-111">Methode</span><span class="sxs-lookup"><span data-stu-id="8b423-111">Method</span></span>                                                                  | <span data-ttu-id="8b423-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b423-112">Description</span></span>                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="8b423-113">**GetChild**</span><span class="sxs-lookup"><span data-stu-id="8b423-113">**GetChild**</span></span>](id3dxfileenumobject--getchild.md)                       | <span data-ttu-id="8b423-114">Ruft ein untergeordnetes-Objekt in diesem Datei Datenobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="8b423-114">Retrieves a child object in this file data object.</span></span><br/>              |
| [<span data-ttu-id="8b423-115">**GetChildren**</span><span class="sxs-lookup"><span data-stu-id="8b423-115">**GetChildren**</span></span>](id3dxfileenumobject--getchildren.md)                 | <span data-ttu-id="8b423-116">Ruft die Anzahl der untergeordneten Objekte in diesem Datei Datenobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="8b423-116">Retrieves the number of child objects in this file data object.</span></span><br/> |
| [<span data-ttu-id="8b423-117">**Getdataobjectbyid**</span><span class="sxs-lookup"><span data-stu-id="8b423-117">**GetDataObjectById**</span></span>](id3dxfileenumobject--getdataobjectbyid.md)     | <span data-ttu-id="8b423-118">Ruft das Datenobjekt ab, das über die angegebene GUID verfügt.</span><span class="sxs-lookup"><span data-stu-id="8b423-118">Retrieves the data object that has the specified GUID.</span></span><br/>          |
| [<span data-ttu-id="8b423-119">**Getdataobjectbyname**</span><span class="sxs-lookup"><span data-stu-id="8b423-119">**GetDataObjectByName**</span></span>](id3dxfileenumobject--getdataobjectbyname.md) | <span data-ttu-id="8b423-120">Ruft das Datenobjekt ab, das über den angegebenen Namen verfügt.</span><span class="sxs-lookup"><span data-stu-id="8b423-120">Retrieves the data object that has the specified name.</span></span><br/>          |
| [<span data-ttu-id="8b423-121">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="8b423-121">**GetFile**</span></span>](id3dxfileenumobject--getfile.md)                         | <span data-ttu-id="8b423-122">Ruft das [**ID3DXFile**](id3dxfile.md) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="8b423-122">Retrieves the [**ID3DXFile**](id3dxfile.md) object.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="8b423-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b423-123">Remarks</span></span>

<span data-ttu-id="8b423-124">Die GUID für die ID3DXFileEnumObject-Schnittstelle ist IID \_ ID3DXFileEnumObject.</span><span class="sxs-lookup"><span data-stu-id="8b423-124">The GUID for the ID3DXFileEnumObject interface is IID\_ID3DXFileEnumObject.</span></span>

<span data-ttu-id="8b423-125">Der LPD3DXFILEENUMOBJECT-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="8b423-125">The LPD3DXFILEENUMOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileEnumObject *LPD3DXFILEENUMOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="8b423-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b423-126">Requirements</span></span>



| <span data-ttu-id="8b423-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b423-127">Requirement</span></span> | <span data-ttu-id="8b423-128">Wert</span><span class="sxs-lookup"><span data-stu-id="8b423-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b423-129">Header</span><span class="sxs-lookup"><span data-stu-id="8b423-129">Header</span></span><br/>  | <dl> <span data-ttu-id="8b423-130"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b423-130"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="8b423-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8b423-131">Library</span></span><br/> | <dl> <span data-ttu-id="8b423-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b423-132"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8b423-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b423-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b423-134">D3DX X-Datei Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8b423-134">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
