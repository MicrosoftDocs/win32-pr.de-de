---
description: Anwendungen verwenden die Methoden der idirectxfileobject-Schnittstelle zum Abrufen von Informationen zu Microsoft DirectX-Datei Objekten. Veraltet.
ms.assetid: 015d2c4e-4a25-40da-b88a-bad0c4e20e09
title: Idirectxfileobject-Schnittstelle (dxfile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: e03f4a80c0cff25fa9416d35c20f2d60d17b206b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361859"
---
# <a name="idirectxfileobject-interface"></a><span data-ttu-id="22b68-104">Idirectxfileobject-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="22b68-104">IDirectXFileObject interface</span></span>

<span data-ttu-id="22b68-105">Anwendungen verwenden die Methoden der idirectxfileobject-Schnittstelle zum Abrufen von Informationen zu Microsoft DirectX-Datei Objekten.</span><span class="sxs-lookup"><span data-stu-id="22b68-105">Applications use the methods of the IDirectXFileObject interface to retrieve information about Microsoft DirectX file objects.</span></span> <span data-ttu-id="22b68-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="22b68-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="22b68-107">Member</span><span class="sxs-lookup"><span data-stu-id="22b68-107">Members</span></span>

<span data-ttu-id="22b68-108">Die **idirectxfileobject** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="22b68-108">The **IDirectXFileObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="22b68-109">**Idirectxfileobject** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="22b68-109">**IDirectXFileObject** also has these types of members:</span></span>

-   [<span data-ttu-id="22b68-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="22b68-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="22b68-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="22b68-111">Methods</span></span>

<span data-ttu-id="22b68-112">Die **idirectxfileobject** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="22b68-112">The **IDirectXFileObject** interface has these methods.</span></span>



| <span data-ttu-id="22b68-113">Methode</span><span class="sxs-lookup"><span data-stu-id="22b68-113">Method</span></span>                                         | <span data-ttu-id="22b68-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22b68-114">Description</span></span>                                                                                   |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22b68-115">**GetId**</span><span class="sxs-lookup"><span data-stu-id="22b68-115">**GetId**</span></span>](idirectxfileobject--getid.md)     | <span data-ttu-id="22b68-116">Ruft einen Zeiger auf die GUID ab, mit der ein DirectX-Datei Objekt identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="22b68-116">Retrieves a pointer to the GUID that identifies a DirectX file object.</span></span> <span data-ttu-id="22b68-117">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="22b68-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="22b68-118">**GetName**</span><span class="sxs-lookup"><span data-stu-id="22b68-118">**GetName**</span></span>](idirectxfileobject--getname.md) | <span data-ttu-id="22b68-119">Ruft einen Zeiger auf den Namen eines DirectX-Datei Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="22b68-119">Retrieves a pointer to a DirectX file object's name.</span></span> <span data-ttu-id="22b68-120">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="22b68-120">Deprecated.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="22b68-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22b68-121">Remarks</span></span>

<span data-ttu-id="22b68-122">Die GUID für die idirectxfileobject-Schnittstelle ist IID \_ idirectxfileobject.</span><span class="sxs-lookup"><span data-stu-id="22b68-122">The GUID for the IDirectXFileObject interface is IID\_IDirectXFileObject.</span></span>

<span data-ttu-id="22b68-123">Der lpdirectxfileobject-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="22b68-123">The LPDIRECTXFILEOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileObject *LPDIRECTXFILEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="22b68-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22b68-124">Requirements</span></span>



| <span data-ttu-id="22b68-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22b68-125">Requirement</span></span> | <span data-ttu-id="22b68-126">Wert</span><span class="sxs-lookup"><span data-stu-id="22b68-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22b68-127">Header</span><span class="sxs-lookup"><span data-stu-id="22b68-127">Header</span></span><br/>  | <dl> <span data-ttu-id="22b68-128"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="22b68-128"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="22b68-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="22b68-129">Library</span></span><br/> | <dl> <span data-ttu-id="22b68-130"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22b68-130"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22b68-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22b68-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22b68-132">X-Datei Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="22b68-132">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
