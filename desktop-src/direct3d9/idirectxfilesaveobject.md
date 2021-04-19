---
description: Anwendungen verwenden die Methoden der idirectxfilesaveobject-Schnittstelle, um Datenobjekte zu erstellen und Vorlagen und Datenobjekte zu speichern.
ms.assetid: 7948a7d2-b150-45cf-a1fc-5dca21d74770
title: Idirectxfilesaveobject-Schnittstelle (dxfile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 4be69b10037381d4b06466d52483427b6d40499a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353356"
---
# <a name="idirectxfilesaveobject-interface"></a><span data-ttu-id="83f9c-103">Idirectxfilesaveobject-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="83f9c-103">IDirectXFileSaveObject interface</span></span>

<span data-ttu-id="83f9c-104">Anwendungen verwenden die Methoden der idirectxfilesaveobject-Schnittstelle, um Datenobjekte zu erstellen und Vorlagen und Datenobjekte zu speichern.</span><span class="sxs-lookup"><span data-stu-id="83f9c-104">Applications use the methods of the IDirectXFileSaveObject interface to create data objects and to save templates and data objects.</span></span> <span data-ttu-id="83f9c-105">Beachten Sie, dass in jeder Datei keine Vorlagen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="83f9c-105">Note that templates are not required in every file.</span></span> <span data-ttu-id="83f9c-106">Sie können z. b. alle Vorlagen in einer einzigen Microsoft DirectX-Datei ablegen, anstatt Sie in jeder DirectX-Datei zu duplizieren.</span><span class="sxs-lookup"><span data-stu-id="83f9c-106">For example, you could put all templates into a single Microsoft DirectX file rather than duplicating them in every DirectX file.</span></span> <span data-ttu-id="83f9c-107">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="83f9c-107">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="83f9c-108">Member</span><span class="sxs-lookup"><span data-stu-id="83f9c-108">Members</span></span>

<span data-ttu-id="83f9c-109">Die **idirectxfilesaveobject** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="83f9c-109">The **IDirectXFileSaveObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="83f9c-110">**Idirectxfilesaveobject** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="83f9c-110">**IDirectXFileSaveObject** also has these types of members:</span></span>

-   [<span data-ttu-id="83f9c-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="83f9c-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="83f9c-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="83f9c-112">Methods</span></span>

<span data-ttu-id="83f9c-113">Die **idirectxfilesaveobject** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="83f9c-113">The **IDirectXFileSaveObject** interface has these methods.</span></span>



| <span data-ttu-id="83f9c-114">Methode</span><span class="sxs-lookup"><span data-stu-id="83f9c-114">Method</span></span>                                                               | <span data-ttu-id="83f9c-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83f9c-115">Description</span></span>                                                                    |
|:---------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="83f9c-116">**"Kreatedataobject"**</span><span class="sxs-lookup"><span data-stu-id="83f9c-116">**CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md) | <span data-ttu-id="83f9c-117">Erstellt ein Datenobjekt.</span><span class="sxs-lookup"><span data-stu-id="83f9c-117">Creates a data object.</span></span> <span data-ttu-id="83f9c-118">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="83f9c-118">Deprecated.</span></span><br/>                                  |
| [<span data-ttu-id="83f9c-119">**SaveData**</span><span class="sxs-lookup"><span data-stu-id="83f9c-119">**SaveData**</span></span>](idirectxfilesaveobject--savedata.md)                 | <span data-ttu-id="83f9c-120">Speichert ein Datenobjekt und seine untergeordneten Elemente in einer DirectX-Datei.</span><span class="sxs-lookup"><span data-stu-id="83f9c-120">Saves a data object and its children to a DirectX file.</span></span> <span data-ttu-id="83f9c-121">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="83f9c-121">Deprecated.</span></span><br/> |
| [<span data-ttu-id="83f9c-122">**Savetemplates**</span><span class="sxs-lookup"><span data-stu-id="83f9c-122">**SaveTemplates**</span></span>](idirectxfilesaveobject--savetemplates.md)       | <span data-ttu-id="83f9c-123">Speichert Vorlagen in einer DirectX-Datei.</span><span class="sxs-lookup"><span data-stu-id="83f9c-123">Saves templates to a DirectX file.</span></span> <span data-ttu-id="83f9c-124">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="83f9c-124">Deprecated.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="83f9c-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83f9c-125">Remarks</span></span>

<span data-ttu-id="83f9c-126">Die Globally Unique Identifier (GUID) für die idirectxfilesaveobject-Schnittstelle ist **IID \_ idirectxfilesaveobject**.</span><span class="sxs-lookup"><span data-stu-id="83f9c-126">The globally unique identifier (GUID) for the IDirectXFileSaveObject interface is **IID\_IDirectXFileSaveObject**.</span></span>

<span data-ttu-id="83f9c-127">Die **idirectxfilesaveobject** -Schnittstelle wird durch Aufrufen der [**idirectxfile:: createsaveobject**](idirectxfile--createsaveobject.md) -Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="83f9c-127">The **IDirectXFileSaveObject** interface is obtained by calling the [**IDirectXFile::CreateSaveObject**](idirectxfile--createsaveobject.md) method.</span></span>

<span data-ttu-id="83f9c-128">Der **lpdirectxfilesaveobject** -Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="83f9c-128">The **LPDIRECTXFILESAVEOBJECT** type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileSaveObject *LPDIRECTXFILESAVEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="83f9c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83f9c-129">Requirements</span></span>



| <span data-ttu-id="83f9c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83f9c-130">Requirement</span></span> | <span data-ttu-id="83f9c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="83f9c-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83f9c-132">Header</span><span class="sxs-lookup"><span data-stu-id="83f9c-132">Header</span></span><br/>  | <dl> <span data-ttu-id="83f9c-133"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="83f9c-133"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="83f9c-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="83f9c-134">Library</span></span><br/> | <dl> <span data-ttu-id="83f9c-135"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83f9c-135"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83f9c-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83f9c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83f9c-137">X-Datei Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="83f9c-137">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
