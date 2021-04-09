---
description: Anwendungen verwenden die Methoden der idirectxfile-Schnittstelle zum Erstellen von Instanzen der Schnittstellen idirectxfileenumubject und idirectxfilesaveobject und zum Registrieren von Vorlagen. Veraltet.
ms.assetid: c4e800dc-72a9-4b91-9c89-ee76764b1bb9
title: Idirectxfile-Schnittstelle (dxfile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 0a1e084108580277432aaeb61086b43a97dbd9f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870176"
---
# <a name="idirectxfile-interface"></a><span data-ttu-id="3c31c-104">Idirectxfile-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3c31c-104">IDirectXFile interface</span></span>

<span data-ttu-id="3c31c-105">Anwendungen verwenden die Methoden der idirectxfile-Schnittstelle zum Erstellen von Instanzen der Schnittstellen [**idirectxfileenumubject**](idirectxfileenumobject.md) und [**idirectxfilesaveobject**](idirectxfilesaveobject.md) und zum Registrieren von Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="3c31c-105">Applications use the methods of the IDirectXFile interface to create instances of the [**IDirectXFileEnumObject**](idirectxfileenumobject.md) and [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interfaces, and to register templates.</span></span> <span data-ttu-id="3c31c-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3c31c-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="3c31c-107">Member</span><span class="sxs-lookup"><span data-stu-id="3c31c-107">Members</span></span>

<span data-ttu-id="3c31c-108">Die **idirectxfile** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3c31c-108">The **IDirectXFile** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3c31c-109">**Idirectxfile** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3c31c-109">**IDirectXFile** also has these types of members:</span></span>

-   [<span data-ttu-id="3c31c-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="3c31c-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3c31c-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="3c31c-111">Methods</span></span>

<span data-ttu-id="3c31c-112">Die **idirectxfile** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3c31c-112">The **IDirectXFile** interface has these methods.</span></span>



| <span data-ttu-id="3c31c-113">Methode</span><span class="sxs-lookup"><span data-stu-id="3c31c-113">Method</span></span>                                                       | <span data-ttu-id="3c31c-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c31c-114">Description</span></span>                                          |
|:-------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="3c31c-115">**"Kreateendumuject"**</span><span class="sxs-lookup"><span data-stu-id="3c31c-115">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)   | <span data-ttu-id="3c31c-116">Erstellt ein Enumeratorobjekt.</span><span class="sxs-lookup"><span data-stu-id="3c31c-116">Creates an enumerator object.</span></span> <span data-ttu-id="3c31c-117">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3c31c-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="3c31c-118">**"Kreatesaveobject"**</span><span class="sxs-lookup"><span data-stu-id="3c31c-118">**CreateSaveObject**</span></span>](idirectxfile--createsaveobject.md)   | <span data-ttu-id="3c31c-119">Erstellt ein Save-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3c31c-119">Creates a save object.</span></span> <span data-ttu-id="3c31c-120">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3c31c-120">Deprecated.</span></span><br/>        |
| [<span data-ttu-id="3c31c-121">**Register Templates**</span><span class="sxs-lookup"><span data-stu-id="3c31c-121">**RegisterTemplates**</span></span>](idirectxfile--registertemplates.md) | <span data-ttu-id="3c31c-122">Registriert benutzerdefinierte Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="3c31c-122">Registers custom templates.</span></span> <span data-ttu-id="3c31c-123">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3c31c-123">Deprecated.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="3c31c-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c31c-124">Remarks</span></span>

<span data-ttu-id="3c31c-125">Der Globally Unique Identifier (GUID) für die idirectxfile-Schnittstelle ist IID \_ idirectxfile.</span><span class="sxs-lookup"><span data-stu-id="3c31c-125">The globally unique identifier (GUID) for the IDirectXFile interface is IID\_IDirectXFile.</span></span>

<span data-ttu-id="3c31c-126">Die idirectxfile-Schnittstelle wird durch Aufrufen der [**directxfilecreate**](directxfilecreate.md) -Funktion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3c31c-126">The IDirectXFile interface is obtained by calling the [**DirectXFileCreate**](directxfilecreate.md) function.</span></span>

<span data-ttu-id="3c31c-127">Der lpdirectxfile-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="3c31c-127">The LPDIRECTXFILE type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFile *LPDIRECTXFILE;
```



## <a name="requirements"></a><span data-ttu-id="3c31c-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c31c-128">Requirements</span></span>



| <span data-ttu-id="3c31c-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c31c-129">Requirement</span></span> | <span data-ttu-id="3c31c-130">Wert</span><span class="sxs-lookup"><span data-stu-id="3c31c-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c31c-131">Header</span><span class="sxs-lookup"><span data-stu-id="3c31c-131">Header</span></span><br/>  | <dl> <span data-ttu-id="3c31c-132"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c31c-132"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c31c-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3c31c-133">Library</span></span><br/> | <dl> <span data-ttu-id="3c31c-134"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c31c-134"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c31c-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c31c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c31c-136">X-Datei Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="3c31c-136">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
