---
description: Anwendungen verwenden die Methoden der ID3DXFileData-Schnittstelle, um die unmittelbare Hierarchie des Datenobjekts zu erstellen oder darauf zuzugreifen. Durch Vorlagen Einschränkungen wird die Hierarchie bestimmt.
ms.assetid: ce291e2b-b926-4502-8bee-55fe6d6d3267
title: ID3DXFileData-Schnittstelle (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1764787864c059e9c7417525a1a5ab5ff862f7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219596"
---
# <a name="id3dxfiledata-interface"></a><span data-ttu-id="dcce2-104">ID3DXFileData-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="dcce2-104">ID3DXFileData interface</span></span>

<span data-ttu-id="dcce2-105">Anwendungen verwenden die Methoden der ID3DXFileData-Schnittstelle, um die unmittelbare Hierarchie des Datenobjekts zu erstellen oder darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="dcce2-105">Applications use the methods of the ID3DXFileData interface to build or to access the immediate hierarchy of the data object.</span></span> <span data-ttu-id="dcce2-106">Durch Vorlagen Einschränkungen wird die Hierarchie bestimmt.</span><span class="sxs-lookup"><span data-stu-id="dcce2-106">Template restrictions determine the hierarchy.</span></span>

## <a name="members"></a><span data-ttu-id="dcce2-107">Member</span><span class="sxs-lookup"><span data-stu-id="dcce2-107">Members</span></span>

<span data-ttu-id="dcce2-108">Die **ID3DXFileData** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="dcce2-108">The **ID3DXFileData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dcce2-109">**ID3DXFileData** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dcce2-109">**ID3DXFileData** also has these types of members:</span></span>

-   [<span data-ttu-id="dcce2-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="dcce2-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dcce2-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="dcce2-111">Methods</span></span>

<span data-ttu-id="dcce2-112">Die **ID3DXFileData** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="dcce2-112">The **ID3DXFileData** interface has these methods.</span></span>



| <span data-ttu-id="dcce2-113">Methode</span><span class="sxs-lookup"><span data-stu-id="dcce2-113">Method</span></span>                                            | <span data-ttu-id="dcce2-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dcce2-114">Description</span></span>                                                                                                          |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dcce2-115">**GetChild**</span><span class="sxs-lookup"><span data-stu-id="dcce2-115">**GetChild**</span></span>](id3dxfiledata--getchild.md)       | <span data-ttu-id="dcce2-116">Ruft ein untergeordnetes-Objekt in diesem Datei Datenobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="dcce2-116">Retrieves a child object in this file data object.</span></span><br/>                                                        |
| [<span data-ttu-id="dcce2-117">**GetChildren**</span><span class="sxs-lookup"><span data-stu-id="dcce2-117">**GetChildren**</span></span>](id3dxfiledata--getchildren.md) | <span data-ttu-id="dcce2-118">Ruft die Anzahl der untergeordneten Elemente in diesem Datei Datenobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="dcce2-118">Retrieves the number of children in this file data object.</span></span><br/>                                                |
| [<span data-ttu-id="dcce2-119">**Getenum**</span><span class="sxs-lookup"><span data-stu-id="dcce2-119">**GetEnum**</span></span>](id3dxfiledata--getenum.md)         | <span data-ttu-id="dcce2-120">Ruft das Enumerationsobjekt in diesem Datei Datenobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="dcce2-120">Retrieves the enumeration object in this file data object.</span></span><br/>                                                |
| [<span data-ttu-id="dcce2-121">**GetId**</span><span class="sxs-lookup"><span data-stu-id="dcce2-121">**GetId**</span></span>](id3dxfiledata--getid.md)             | <span data-ttu-id="dcce2-122">Ruft die GUID dieses Datei Datenobjekts ab.</span><span class="sxs-lookup"><span data-stu-id="dcce2-122">Retrieves the GUID of this file data object.</span></span><br/>                                                              |
| [<span data-ttu-id="dcce2-123">**GetName**</span><span class="sxs-lookup"><span data-stu-id="dcce2-123">**GetName**</span></span>](id3dxfiledata--getname.md)         | <span data-ttu-id="dcce2-124">Ruft den Namen dieses Datei Datenobjekts ab.</span><span class="sxs-lookup"><span data-stu-id="dcce2-124">Retrieves the name of this file data object.</span></span><br/>                                                              |
| [<span data-ttu-id="dcce2-125">**GetType**</span><span class="sxs-lookup"><span data-stu-id="dcce2-125">**GetType**</span></span>](id3dxfiledata--gettype.md)         | <span data-ttu-id="dcce2-126">Ruft die Vorlagen-ID in diesem Datei Datenobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="dcce2-126">Retrieves the template ID in this file data object.</span></span><br/>                                                       |
| [<span data-ttu-id="dcce2-127">**IsReference**</span><span class="sxs-lookup"><span data-stu-id="dcce2-127">**IsReference**</span></span>](id3dxfiledata--isreference.md) | <span data-ttu-id="dcce2-128">Gibt an, ob dieses Datei Datenobjekt ein Verweis Objekt ist, das auf ein anderes untergeordnetes Datenobjekt zeigt.</span><span class="sxs-lookup"><span data-stu-id="dcce2-128">Indicates whether this file data object is a reference object that points to another child data object.</span></span><br/>   |
| [<span data-ttu-id="dcce2-129">**Sperre**</span><span class="sxs-lookup"><span data-stu-id="dcce2-129">**Lock**</span></span>](id3dxfiledata--lock.md)               | <span data-ttu-id="dcce2-130">Greift auf die x-Datei Daten zu.</span><span class="sxs-lookup"><span data-stu-id="dcce2-130">Accesses the .x file data.</span></span><br/>                                                                                |
| [<span data-ttu-id="dcce2-131">**Entsperren**</span><span class="sxs-lookup"><span data-stu-id="dcce2-131">**Unlock**</span></span>](id3dxfiledata--unlock.md)           | <span data-ttu-id="dcce2-132">Beendet die Lebensdauer des *ppData* -Zeigers, der von [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="dcce2-132">Ends the lifespan of the *ppData* pointer returned by [**ID3DXFileData::Lock**](id3dxfiledata--lock.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dcce2-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dcce2-133">Remarks</span></span>

<span data-ttu-id="dcce2-134">Die von der Vorlage zugelassenen Datentypen werden als optionale Member bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="dcce2-134">Data types allowed by the template are called optional members.</span></span> <span data-ttu-id="dcce2-135">Die optionalen Member sind nicht erforderlich, aber in einem Objekt werden möglicherweise wichtige Informationen übersehen.</span><span class="sxs-lookup"><span data-stu-id="dcce2-135">The optional members are not required, but an object might miss important information without them.</span></span> <span data-ttu-id="dcce2-136">Diese optionalen Member werden als untergeordnete Elemente des Datenobjekts gespeichert.</span><span class="sxs-lookup"><span data-stu-id="dcce2-136">These optional members are saved as children of the data object.</span></span> <span data-ttu-id="dcce2-137">Ein untergeordnetes Element kann ein anderes Datenobjekt oder ein Verweis auf ein früheres Datenobjekt sein.</span><span class="sxs-lookup"><span data-stu-id="dcce2-137">A child can be another data object or a reference to an earlier data object.</span></span>

<span data-ttu-id="dcce2-138">Die GUID für die ID3DXFileData-Schnittstelle ist IID \_ ID3DXFileData.</span><span class="sxs-lookup"><span data-stu-id="dcce2-138">The GUID for the ID3DXFileData interface is IID\_ID3DXFileData.</span></span>

<span data-ttu-id="dcce2-139">Der LPD3DXFILEDATA-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="dcce2-139">The LPD3DXFILEDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileData *LPD3DXFILEDATA;
```



## <a name="requirements"></a><span data-ttu-id="dcce2-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dcce2-140">Requirements</span></span>



| <span data-ttu-id="dcce2-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dcce2-141">Requirement</span></span> | <span data-ttu-id="dcce2-142">Wert</span><span class="sxs-lookup"><span data-stu-id="dcce2-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dcce2-143">Header</span><span class="sxs-lookup"><span data-stu-id="dcce2-143">Header</span></span><br/>  | <dl> <span data-ttu-id="dcce2-144"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcce2-144"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="dcce2-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dcce2-145">Library</span></span><br/> | <dl> <span data-ttu-id="dcce2-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcce2-146"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="dcce2-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcce2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcce2-148">D3DX X-Datei Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="dcce2-148">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
