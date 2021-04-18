---
description: Anwendungen verwenden die Methoden der ID3DXFileSaveObject-Schnittstelle, um eine x-Datei auf den Datenträger zu schreiben und Datenobjekte und Vorlagen hinzuzufügen und zu speichern.
ms.assetid: 1131c151-fa21-4654-9776-484922d58487
title: ID3DXFileSaveObject-Schnittstelle (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f8d657c327c75045cf4feb2080a2e57d80f752df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361200"
---
# <a name="id3dxfilesaveobject-interface"></a><span data-ttu-id="803ca-103">ID3DXFileSaveObject-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="803ca-103">ID3DXFileSaveObject interface</span></span>

<span data-ttu-id="803ca-104">Anwendungen verwenden die Methoden der ID3DXFileSaveObject-Schnittstelle, um eine x-Datei auf den Datenträger zu schreiben und Datenobjekte und Vorlagen hinzuzufügen und zu speichern.</span><span class="sxs-lookup"><span data-stu-id="803ca-104">Applications use the methods of the ID3DXFileSaveObject interface to write a .x file to disk, and to add and save data objects and templates.</span></span>

## <a name="members"></a><span data-ttu-id="803ca-105">Member</span><span class="sxs-lookup"><span data-stu-id="803ca-105">Members</span></span>

<span data-ttu-id="803ca-106">Die **ID3DXFileSaveObject** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="803ca-106">The **ID3DXFileSaveObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="803ca-107">**ID3DXFileSaveObject** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="803ca-107">**ID3DXFileSaveObject** also has these types of members:</span></span>

-   [<span data-ttu-id="803ca-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="803ca-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="803ca-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="803ca-109">Methods</span></span>

<span data-ttu-id="803ca-110">Die **ID3DXFileSaveObject** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="803ca-110">The **ID3DXFileSaveObject** interface has these methods.</span></span>



| <span data-ttu-id="803ca-111">Methode</span><span class="sxs-lookup"><span data-stu-id="803ca-111">Method</span></span>                                                      | <span data-ttu-id="803ca-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="803ca-112">Description</span></span>                                                                                                                  |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="803ca-113">**Adddataobject**</span><span class="sxs-lookup"><span data-stu-id="803ca-113">**AddDataObject**</span></span>](id3dxfilesaveobject--adddataobject.md) | <span data-ttu-id="803ca-114">Fügt ein Datenobjekt als untergeordnetes Element des [**ID3DXFileSaveData**](id3dxfilesavedata.md) -Objekts hinzu.</span><span class="sxs-lookup"><span data-stu-id="803ca-114">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span><br/>                       |
| [<span data-ttu-id="803ca-115">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="803ca-115">**GetFile**</span></span>](id3dxfilesaveobject--getfile.md)             | <span data-ttu-id="803ca-116">Ruft die [**ID3DXFile**](id3dxfile.md) -Schnittstelle des-Objekts ab, das dieses **ID3DXFileSaveObject** -Objekt erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="803ca-116">Gets the [**ID3DXFile**](id3dxfile.md) interface of the object that created this **ID3DXFileSaveObject** object.</span></span><br/> |
| [<span data-ttu-id="803ca-117">**Speichern**</span><span class="sxs-lookup"><span data-stu-id="803ca-117">**Save**</span></span>](id3dxfilesaveobject--save.md)                   | <span data-ttu-id="803ca-118">Speichert ein Datenobjekt und seine untergeordneten Elemente in einer x-Datei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="803ca-118">Saves a data object and its children to a .x file on disk.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="803ca-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="803ca-119">Remarks</span></span>

<span data-ttu-id="803ca-120">In jeder Datei sind keine Vorlagen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="803ca-120">Templates are not required in every file.</span></span> <span data-ttu-id="803ca-121">Beispielsweise können Sie alle Vorlagen in eine einzelne x-Datei einfügen, anstatt Sie in jeder. x-Datei zu duplizieren.</span><span class="sxs-lookup"><span data-stu-id="803ca-121">For example, you could put all templates into a single .x file rather than duplicating them in every .x file.</span></span>

<span data-ttu-id="803ca-122">Die ID3DXFileSaveObject-Schnittstelle wird durch Aufrufen der [**ID3DXFile:: createsaveobject**](id3dxfile--createsaveobject.md) -Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="803ca-122">The ID3DXFileSaveObject interface is obtained by calling the [**ID3DXFile::CreateSaveObject**](id3dxfile--createsaveobject.md) method.</span></span>

<span data-ttu-id="803ca-123">Die Globally Unique Identifier (GUID) für die ID3DXFileSaveObject-Schnittstelle ist IID \_ ID3DXFileSaveObject.</span><span class="sxs-lookup"><span data-stu-id="803ca-123">The globally unique identifier (GUID) for the ID3DXFileSaveObject interface is IID\_ID3DXFileSaveObject.</span></span>

<span data-ttu-id="803ca-124">Der LPD3DXFILESAVEOBJECT-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="803ca-124">The LPD3DXFILESAVEOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileSaveObject *LPD3DXFILESAVEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="803ca-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="803ca-125">Requirements</span></span>



| <span data-ttu-id="803ca-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="803ca-126">Requirement</span></span> | <span data-ttu-id="803ca-127">Wert</span><span class="sxs-lookup"><span data-stu-id="803ca-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="803ca-128">Header</span><span class="sxs-lookup"><span data-stu-id="803ca-128">Header</span></span><br/>  | <dl> <span data-ttu-id="803ca-129"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="803ca-129"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="803ca-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="803ca-130">Library</span></span><br/> | <dl> <span data-ttu-id="803ca-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="803ca-131"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="803ca-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="803ca-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="803ca-133">D3DX X-Datei Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="803ca-133">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
