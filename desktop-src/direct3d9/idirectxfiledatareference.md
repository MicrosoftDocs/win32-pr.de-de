---
description: Anwendungen verwenden die Methoden der idirectxfiledatareferenzierungsschnittstelle, um Daten Verweis Objekte zu unterstützen.
ms.assetid: e0f6046f-36d9-4a13-9a0c-0738ebb2e569
title: Idirectxfiledatareferenzierungsschnittstelle (dxfile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: d04d2367f914c2e8d64a3c9c64fb55df1e51e47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132425"
---
# <a name="idirectxfiledatareference-interface"></a><span data-ttu-id="616f0-103">Idirectxfiledatareferenzierungsschnittstelle</span><span class="sxs-lookup"><span data-stu-id="616f0-103">IDirectXFileDataReference interface</span></span>

<span data-ttu-id="616f0-104">Anwendungen verwenden die Methoden der idirectxfiledatareferenzierungsschnittstelle, um Daten Verweis Objekte zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="616f0-104">Applications use the methods of the IDirectXFileDataReference interface to support data reference objects.</span></span> <span data-ttu-id="616f0-105">Ein Daten Verweis Objekt verweist auf ein Datenobjekt, das zuvor in der Datei definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="616f0-105">A data reference object refers to a data object that is defined earlier in the file.</span></span> <span data-ttu-id="616f0-106">Dies ermöglicht es Ihnen, das gleiche Objekt mehrmals zu verwenden, ohne es in der Datei wiederholen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="616f0-106">This enables you to use the same object multiple times without repeating it in the file.</span></span> <span data-ttu-id="616f0-107">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="616f0-107">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="616f0-108">Member</span><span class="sxs-lookup"><span data-stu-id="616f0-108">Members</span></span>

<span data-ttu-id="616f0-109">Die **idirectxfiledatareferenzierungsschnittstelle** erbt von [**idirectxfileobject**](idirectxfileobject.md).</span><span class="sxs-lookup"><span data-stu-id="616f0-109">The **IDirectXFileDataReference** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="616f0-110">**Idirectxfiledatareferenziert** auch diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="616f0-110">**IDirectXFileDataReference** also has these types of members:</span></span>

-   [<span data-ttu-id="616f0-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="616f0-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="616f0-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="616f0-112">Methods</span></span>

<span data-ttu-id="616f0-113">Die **idirectxfiledatareferenzierungsschnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="616f0-113">The **IDirectXFileDataReference** interface has these methods.</span></span>



| <span data-ttu-id="616f0-114">Methode</span><span class="sxs-lookup"><span data-stu-id="616f0-114">Method</span></span>                                                | <span data-ttu-id="616f0-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="616f0-115">Description</span></span>                                      |
|:------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="616f0-116">**Beheben**</span><span class="sxs-lookup"><span data-stu-id="616f0-116">**Resolve**</span></span>](idirectxfiledatareference--resolve.md) | <span data-ttu-id="616f0-117">Löst Daten Verweise auf.</span><span class="sxs-lookup"><span data-stu-id="616f0-117">Resolves data references.</span></span> <span data-ttu-id="616f0-118">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="616f0-118">Deprecated.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="616f0-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="616f0-119">Remarks</span></span>

<span data-ttu-id="616f0-120">Nachdem Sie festgestellt haben, dass ein Objekt ein Daten Verweis Objekt ist, verwenden Sie die [**idirectxfiledatareferen:: Resolve**](idirectxfiledatareference--resolve.md) -Methode, um das Objekt abzurufen, auf das verwiesen wird, das zuvor in der Datei definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="616f0-120">After you have determined that an object is a data reference object, use the [**IDirectXFileDataReference::Resolve**](idirectxfiledatareference--resolve.md) method to retrieve the referenced object defined earlier in the file.</span></span> <span data-ttu-id="616f0-121">Weitere Informationen zum Identifizieren eines Daten Verweis Objekts finden Sie unter [**idirectxfiledata**](idirectxfiledata.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="616f0-121">For information about how to identify a data reference object, see the [**IDirectXFileData**](idirectxfiledata.md) interface.</span></span>

<span data-ttu-id="616f0-122">Die GUID für die idirectxfiledatareferenzierungsschnittstelle ist IID \_ idirectxfiledatareferenziert.</span><span class="sxs-lookup"><span data-stu-id="616f0-122">The GUID for the IDirectXFileDataReference interface is IID\_IDirectXFileDataReference.</span></span>

<span data-ttu-id="616f0-123">Der lpdirectxfiledatareferenzierungstyp ist als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="616f0-123">The LPDIRECTXFILEDataReference type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileDataReference *LPDIRECTXFILEDATAREFERENCE;
```



## <a name="requirements"></a><span data-ttu-id="616f0-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="616f0-124">Requirements</span></span>



| <span data-ttu-id="616f0-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="616f0-125">Requirement</span></span> | <span data-ttu-id="616f0-126">Wert</span><span class="sxs-lookup"><span data-stu-id="616f0-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="616f0-127">Header</span><span class="sxs-lookup"><span data-stu-id="616f0-127">Header</span></span><br/>  | <dl> <span data-ttu-id="616f0-128"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="616f0-128"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="616f0-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="616f0-129">Library</span></span><br/> | <dl> <span data-ttu-id="616f0-130"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="616f0-130"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="616f0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="616f0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="616f0-132">**Idirectxfileobject**</span><span class="sxs-lookup"><span data-stu-id="616f0-132">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="616f0-133">X-Datei Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="616f0-133">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




