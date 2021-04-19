---
description: Anwendungen verwenden die Methoden der ID3DXFileSaveData-Schnittstelle zum Hinzufügen von Datenobjekten als untergeordnete Elemente eines x-Datei Daten Knotens.
ms.assetid: ab5bdd9a-496a-4ae1-b93a-fe5856bd97d4
title: ID3DXFileSaveData-Schnittstelle (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d42f431dbb2f9108c5e503aea07ba6b11915f0ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353719"
---
# <a name="id3dxfilesavedata-interface"></a><span data-ttu-id="8a59c-103">ID3DXFileSaveData-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8a59c-103">ID3DXFileSaveData interface</span></span>

<span data-ttu-id="8a59c-104">Anwendungen verwenden die Methoden der ID3DXFileSaveData-Schnittstelle zum Hinzufügen von Datenobjekten als untergeordnete Elemente eines x-Datei Daten Knotens.</span><span class="sxs-lookup"><span data-stu-id="8a59c-104">Applications use the methods of the ID3DXFileSaveData interface to add data objects as children of a .x file data node.</span></span>

## <a name="members"></a><span data-ttu-id="8a59c-105">Member</span><span class="sxs-lookup"><span data-stu-id="8a59c-105">Members</span></span>

<span data-ttu-id="8a59c-106">Die **ID3DXFileSaveData** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8a59c-106">The **ID3DXFileSaveData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8a59c-107">**ID3DXFileSaveData** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8a59c-107">**ID3DXFileSaveData** also has these types of members:</span></span>

-   [<span data-ttu-id="8a59c-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="8a59c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8a59c-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="8a59c-109">Methods</span></span>

<span data-ttu-id="8a59c-110">Die **ID3DXFileSaveData** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8a59c-110">The **ID3DXFileSaveData** interface has these methods.</span></span>



| <span data-ttu-id="8a59c-111">Methode</span><span class="sxs-lookup"><span data-stu-id="8a59c-111">Method</span></span>                                                          | <span data-ttu-id="8a59c-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a59c-112">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a59c-113">**Adddataobject**</span><span class="sxs-lookup"><span data-stu-id="8a59c-113">**AddDataObject**</span></span>](id3dxfilesavedata--adddataobject.md)       | <span data-ttu-id="8a59c-114">Fügt ein Datenobjekt als untergeordnetes Element des **ID3DXFileSaveData** -Datei Daten Knotens hinzu.</span><span class="sxs-lookup"><span data-stu-id="8a59c-114">Adds a data object as a child of the **ID3DXFileSaveData** file data node.</span></span><br/>                                                      |
| [<span data-ttu-id="8a59c-115">**Adddatareferenzierung**</span><span class="sxs-lookup"><span data-stu-id="8a59c-115">**AddDataReference**</span></span>](id3dxfilesavedata--adddatareference.md) | <span data-ttu-id="8a59c-116">Fügt einen Daten Verweis als untergeordnetes Element dieses **ID3DXFileSaveData** File Data-Knotens hinzu.</span><span class="sxs-lookup"><span data-stu-id="8a59c-116">Adds a data reference as a child of this **ID3DXFileSaveData** file data node.</span></span> <span data-ttu-id="8a59c-117">Der Daten Verweis verweist auf ein Datei Datenobjekt.</span><span class="sxs-lookup"><span data-stu-id="8a59c-117">The data reference points to a file data object.</span></span><br/> |
| [<span data-ttu-id="8a59c-118">**GetId**</span><span class="sxs-lookup"><span data-stu-id="8a59c-118">**GetId**</span></span>](id3dxfilesavedata--getid.md)                       | <span data-ttu-id="8a59c-119">Ruft die GUID dieses **ID3DXFileSaveData** File Data-Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="8a59c-119">Retrieves the GUID of this **ID3DXFileSaveData** file data node.</span></span><br/>                                                                |
| [<span data-ttu-id="8a59c-120">**GetName**</span><span class="sxs-lookup"><span data-stu-id="8a59c-120">**GetName**</span></span>](id3dxfilesavedata--getname.md)                   | <span data-ttu-id="8a59c-121">Ruft den Namen dieses **ID3DXFileSaveData** File Data-Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="8a59c-121">Retrieves the name of this **ID3DXFileSaveData** file data node.</span></span><br/>                                                                |
| [<span data-ttu-id="8a59c-122">**Getsave**</span><span class="sxs-lookup"><span data-stu-id="8a59c-122">**GetSave**</span></span>](id3dxfilesavedata--getsave.md)                   | <span data-ttu-id="8a59c-123">Ruft einen Zeiger auf diesen [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) File Data-Knoten ab.</span><span class="sxs-lookup"><span data-stu-id="8a59c-123">Retrieves a pointer to this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) file data node.</span></span><br/>                                  |
| [<span data-ttu-id="8a59c-124">**GetType**</span><span class="sxs-lookup"><span data-stu-id="8a59c-124">**GetType**</span></span>](id3dxfilesavedata--gettype.md)                   | <span data-ttu-id="8a59c-125">Ruft die Vorlagen-ID dieses Datei Daten Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="8a59c-125">Retrieves the template ID of this file data node.</span></span><br/>                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="8a59c-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a59c-126">Remarks</span></span>

<span data-ttu-id="8a59c-127">Die GUID für die ID3DXFileSaveObject-Schnittstelle ist IID \_ ID3DXFileSaveObject.</span><span class="sxs-lookup"><span data-stu-id="8a59c-127">The GUID for the ID3DXFileSaveObject interface is IID\_ID3DXFileSaveObject.</span></span>

<span data-ttu-id="8a59c-128">Der LPD3DXFileSaveData-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="8a59c-128">The LPD3DXFileSaveData type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileSaveData *LPD3DXFILESAVEDATA;
```



## <a name="requirements"></a><span data-ttu-id="8a59c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a59c-129">Requirements</span></span>



| <span data-ttu-id="8a59c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a59c-130">Requirement</span></span> | <span data-ttu-id="8a59c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="8a59c-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a59c-132">Header</span><span class="sxs-lookup"><span data-stu-id="8a59c-132">Header</span></span><br/>  | <dl> <span data-ttu-id="8a59c-133"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a59c-133"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="8a59c-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8a59c-134">Library</span></span><br/> | <dl> <span data-ttu-id="8a59c-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a59c-135"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8a59c-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a59c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a59c-137">D3DX X-Datei Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8a59c-137">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
