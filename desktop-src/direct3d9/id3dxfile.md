---
description: Anwendungen verwenden die Methoden der ID3DXFile-Schnittstelle, um Instanzen der ID3DXFileEnumObject-und ID3DXFileSaveObject-Schnittstellen zu erstellen und um Vorlagen zu registrieren.
ms.assetid: 472d45b1-5c03-4417-a005-91f802667919
title: ID3DXFile-Schnittstelle (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 45af79c4fb01c95b25803788f79588a3880fe264
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361219"
---
# <a name="id3dxfile-interface"></a><span data-ttu-id="1e00e-103">ID3DXFile-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1e00e-103">ID3DXFile interface</span></span>

<span data-ttu-id="1e00e-104">Anwendungen verwenden die Methoden der ID3DXFile-Schnittstelle, um Instanzen der [**ID3DXFileEnumObject**](id3dxfileenumobject.md) -und [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) -Schnittstellen zu erstellen und um Vorlagen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="1e00e-104">Applications use the methods of the ID3DXFile interface to create instances of the [**ID3DXFileEnumObject**](id3dxfileenumobject.md) and [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interfaces, and to register templates.</span></span>

## <a name="members"></a><span data-ttu-id="1e00e-105">Member</span><span class="sxs-lookup"><span data-stu-id="1e00e-105">Members</span></span>

<span data-ttu-id="1e00e-106">Die **ID3DXFile** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1e00e-106">The **ID3DXFile** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1e00e-107">**ID3DXFile** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1e00e-107">**ID3DXFile** also has these types of members:</span></span>

-   [<span data-ttu-id="1e00e-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="1e00e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1e00e-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="1e00e-109">Methods</span></span>

<span data-ttu-id="1e00e-110">Die **ID3DXFile** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1e00e-110">The **ID3DXFile** interface has these methods.</span></span>



| <span data-ttu-id="1e00e-111">Methode</span><span class="sxs-lookup"><span data-stu-id="1e00e-111">Method</span></span>                                                            | <span data-ttu-id="1e00e-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e00e-112">Description</span></span>                                                                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e00e-113">**"Kreateendumuject"**</span><span class="sxs-lookup"><span data-stu-id="1e00e-113">**CreateEnumObject**</span></span>](id3dxfile--createenumobject.md)           | <span data-ttu-id="1e00e-114">Erstellt ein Enumeratorobjekt, das eine x-Datei liest.</span><span class="sxs-lookup"><span data-stu-id="1e00e-114">Creates an enumerator object that will read a .x file.</span></span><br/>                                                      |
| [<span data-ttu-id="1e00e-115">**"Kreatesaveobject"**</span><span class="sxs-lookup"><span data-stu-id="1e00e-115">**CreateSaveObject**</span></span>](id3dxfile--createsaveobject.md)           | <span data-ttu-id="1e00e-116">Erstellt ein Speicher Objekt, das zum Speichern von Daten in einer x-Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1e00e-116">Creates a save object that will be used to save data to a .x file.</span></span><br/>                                          |
| [<span data-ttu-id="1e00e-117">**Registerenumtemplates**</span><span class="sxs-lookup"><span data-stu-id="1e00e-117">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md) | <span data-ttu-id="1e00e-118">Registriert benutzerdefinierte Vorlagen bei Angabe eines [**ID3DXFileEnumObject**](id3dxfileenumobject.md) -Enumerationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="1e00e-118">Registers custom templates, given an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object.</span></span><br/> |
| [<span data-ttu-id="1e00e-119">**Register Templates**</span><span class="sxs-lookup"><span data-stu-id="1e00e-119">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)         | <span data-ttu-id="1e00e-120">Registriert benutzerdefinierte Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="1e00e-120">Registers custom templates.</span></span><br/>                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="1e00e-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e00e-121">Remarks</span></span>

<span data-ttu-id="1e00e-122">Ein ID3DXFile-Objekt enthält auch einen lokalen Vorlagen Speicher.</span><span class="sxs-lookup"><span data-stu-id="1e00e-122">An ID3DXFile object also contains a local template store.</span></span> <span data-ttu-id="1e00e-123">Dieser lokale Speicher kann nur mit den Methoden [**ID3DXFile:: registerenumtemplates**](id3dxfile--registerenumtemplates.md) und [**ID3DXFile:: registertemplates**](id3dxfile--registertemplates.md) hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1e00e-123">This local storage may be added to only with the [**ID3DXFile::RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) and [**ID3DXFile::RegisterTemplates**](id3dxfile--registertemplates.md) methods.</span></span>

<span data-ttu-id="1e00e-124">[**ID3DXFileEnumObject**](id3dxfileenumobject.md) -und [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) -Objekte, die mit [**ID3DXFile:: anateenumubject**](id3dxfile--createenumobject.md) und [**ID3DXFile:: anatesaveobject**](id3dxfile--createsaveobject.md) erstellt wurden, nutzen auch den Vorlagen Speicher des übergeordneten ID3DXFile-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1e00e-124">[**ID3DXFileEnumObject**](id3dxfileenumobject.md) and [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) objects created with [**ID3DXFile::CreateEnumObject**](id3dxfile--createenumobject.md) and [**ID3DXFile::CreateSaveObject**](id3dxfile--createsaveobject.md) also utilize the template store of the parent ID3DXFile object.</span></span>

<span data-ttu-id="1e00e-125">Die ID3DXFile-Schnittstelle wird durch Aufrufen der [**D3DXFileCreate**](d3dxfilecreate.md) -Funktion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1e00e-125">The ID3DXFile interface is obtained by calling the [**D3DXFileCreate**](d3dxfilecreate.md) function.</span></span>

<span data-ttu-id="1e00e-126">Die Globally Unique Identifier (GUID) für die ID3DXFile-Schnittstelle ist IID \_ ID3DXFile.</span><span class="sxs-lookup"><span data-stu-id="1e00e-126">The globally unique identifier (GUID) for the ID3DXFile interface is IID\_ID3DXFile.</span></span>

<span data-ttu-id="1e00e-127">Der LPD3DXFILE-Typ wird als Zeiger auf die ID3DXFile-Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="1e00e-127">The LPD3DXFILE type is defined as a pointer to the ID3DXFile interface.</span></span>


```
typedef interface ID3DXFile *LPD3DXFILE;
```



## <a name="requirements"></a><span data-ttu-id="1e00e-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e00e-128">Requirements</span></span>



| <span data-ttu-id="1e00e-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e00e-129">Requirement</span></span> | <span data-ttu-id="1e00e-130">Wert</span><span class="sxs-lookup"><span data-stu-id="1e00e-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e00e-131">Header</span><span class="sxs-lookup"><span data-stu-id="1e00e-131">Header</span></span><br/>  | <dl> <span data-ttu-id="1e00e-132"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e00e-132"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="1e00e-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1e00e-133">Library</span></span><br/> | <dl> <span data-ttu-id="1e00e-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e00e-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1e00e-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e00e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e00e-136">D3DX X-Datei Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1e00e-136">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
