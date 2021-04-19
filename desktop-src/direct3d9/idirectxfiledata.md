---
description: Anwendungen verwenden die Methoden der idirectxfiledata-Schnittstelle, um die unmittelbare Hierarchie des Datenobjekts zu erstellen oder darauf zuzugreifen.
ms.assetid: 8810162f-76a8-45ba-b069-7910fd611a60
title: Idirectxfiledata-Schnittstelle (dxfile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 30d2fb26e3752e302726edce51354369f3b067eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361233"
---
# <a name="idirectxfiledata-interface"></a><span data-ttu-id="ea80f-103">Idirectxfiledata-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ea80f-103">IDirectXFileData interface</span></span>

<span data-ttu-id="ea80f-104">Anwendungen verwenden die Methoden der idirectxfiledata-Schnittstelle, um die unmittelbare Hierarchie des Datenobjekts zu erstellen oder darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ea80f-104">Applications use the methods of the IDirectXFileData interface to build or to access the immediate hierarchy of the data object.</span></span> <span data-ttu-id="ea80f-105">Durch Vorlagen Einschränkungen wird die Hierarchie bestimmt.</span><span class="sxs-lookup"><span data-stu-id="ea80f-105">Template restrictions determine the hierarchy.</span></span> <span data-ttu-id="ea80f-106">Die von der Vorlage zugelassenen Datentypen werden als optionale Member bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ea80f-106">Data types allowed by the template are called optional members.</span></span> <span data-ttu-id="ea80f-107">Die optionalen Member sind nicht erforderlich, aber in einem Objekt werden möglicherweise wichtige Informationen übersehen.</span><span class="sxs-lookup"><span data-stu-id="ea80f-107">The optional members are not required, but an object might miss important information without them.</span></span> <span data-ttu-id="ea80f-108">Diese optionalen Member werden als untergeordnete Elemente des Datenobjekts gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ea80f-108">These optional members are saved as children of the data object.</span></span> <span data-ttu-id="ea80f-109">Die untergeordneten Elemente können ein anderes Datenobjekt, ein Verweis auf ein früheres Datenobjekt oder ein binäres Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="ea80f-109">The children can be another data object, a reference to an earlier data object, or a binary object.</span></span> <span data-ttu-id="ea80f-110">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ea80f-110">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="ea80f-111">Member</span><span class="sxs-lookup"><span data-stu-id="ea80f-111">Members</span></span>

<span data-ttu-id="ea80f-112">Die **idirectxfiledata** -Schnittstelle erbt von [**idirectxfileobject**](idirectxfileobject.md).</span><span class="sxs-lookup"><span data-stu-id="ea80f-112">The **IDirectXFileData** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="ea80f-113">**Idirectxfiledata** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ea80f-113">**IDirectXFileData** also has these types of members:</span></span>

-   [<span data-ttu-id="ea80f-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="ea80f-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ea80f-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="ea80f-115">Methods</span></span>

<span data-ttu-id="ea80f-116">Die **idirectxfiledata** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ea80f-116">The **IDirectXFileData** interface has these methods.</span></span>



| <span data-ttu-id="ea80f-117">Methode</span><span class="sxs-lookup"><span data-stu-id="ea80f-117">Method</span></span>                                                         | <span data-ttu-id="ea80f-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea80f-118">Description</span></span>                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea80f-119">**Addbinaryobject**</span><span class="sxs-lookup"><span data-stu-id="ea80f-119">**AddBinaryObject**</span></span>](idirectxfiledata--addbinaryobject.md)   | <span data-ttu-id="ea80f-120">Erstellt ein binäres Objekt und fügt es als untergeordnetes Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="ea80f-120">Creates a binary object and adds it as a child object.</span></span> <span data-ttu-id="ea80f-121">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ea80f-121">Deprecated.</span></span><br/>                                             |
| [<span data-ttu-id="ea80f-122">**Adddataobject**</span><span class="sxs-lookup"><span data-stu-id="ea80f-122">**AddDataObject**</span></span>](idirectxfiledata--adddataobject.md)       | <span data-ttu-id="ea80f-123">Fügt ein Datenobjekt als untergeordnetes Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="ea80f-123">Adds a data object as a child object.</span></span> <span data-ttu-id="ea80f-124">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ea80f-124">Deprecated.</span></span><br/>                                                              |
| [<span data-ttu-id="ea80f-125">**Adddatareferenzierung**</span><span class="sxs-lookup"><span data-stu-id="ea80f-125">**AddDataReference**</span></span>](idirectxfiledata--adddatareference.md) | <span data-ttu-id="ea80f-126">Erstellt ein Daten Verweis Objekt als untergeordnetes Objekt und fügt es hinzu.</span><span class="sxs-lookup"><span data-stu-id="ea80f-126">Creates and adds a data reference object as a child object.</span></span> <span data-ttu-id="ea80f-127">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ea80f-127">Deprecated.</span></span><br/>                                        |
| [<span data-ttu-id="ea80f-128">**GetData**</span><span class="sxs-lookup"><span data-stu-id="ea80f-128">**GetData**</span></span>](idirectxfiledata--getdata.md)                   | <span data-ttu-id="ea80f-129">Ruft die Daten für eines der Member des Objekts oder die Daten für alle Elemente ab.</span><span class="sxs-lookup"><span data-stu-id="ea80f-129">Retrieves the data for one of the object's members or the data for all members.</span></span> <span data-ttu-id="ea80f-130">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ea80f-130">Deprecated.</span></span><br/>                    |
| [<span data-ttu-id="ea80f-131">**Getnextobject**</span><span class="sxs-lookup"><span data-stu-id="ea80f-131">**GetNextObject**</span></span>](idirectxfiledata--getnextobject.md)       | <span data-ttu-id="ea80f-132">Ruft das nächste untergeordnete Datenobjekt, das Daten Verweis Objekt oder das binäre Objekt in der DirectX-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="ea80f-132">Retrieves the next child data object, data reference object, or binary object in the DirectX file.</span></span> <span data-ttu-id="ea80f-133">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ea80f-133">Deprecated.</span></span><br/> |
| [<span data-ttu-id="ea80f-134">**GetType**</span><span class="sxs-lookup"><span data-stu-id="ea80f-134">**GetType**</span></span>](idirectxfiledata--gettype.md)                   | <span data-ttu-id="ea80f-135">Ruft die GUID der Objekt Vorlage ab.</span><span class="sxs-lookup"><span data-stu-id="ea80f-135">Retrieves the GUID of the object's template.</span></span> <span data-ttu-id="ea80f-136">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ea80f-136">Deprecated.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="ea80f-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea80f-137">Remarks</span></span>

<span data-ttu-id="ea80f-138">Die GUID für die idirectxfiledata-Schnittstelle ist IID \_ idirectxfiledata.</span><span class="sxs-lookup"><span data-stu-id="ea80f-138">The GUID for the IDirectXFileData interface is IID\_IDirectXFileData.</span></span>

<span data-ttu-id="ea80f-139">Der lpdirectxfiledata-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="ea80f-139">The LPDIRECTXFILEDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileData *LPDIRECTXFILEDATA;
```



## <a name="requirements"></a><span data-ttu-id="ea80f-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea80f-140">Requirements</span></span>



| <span data-ttu-id="ea80f-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea80f-141">Requirement</span></span> | <span data-ttu-id="ea80f-142">Wert</span><span class="sxs-lookup"><span data-stu-id="ea80f-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea80f-143">Header</span><span class="sxs-lookup"><span data-stu-id="ea80f-143">Header</span></span><br/>  | <dl> <span data-ttu-id="ea80f-144"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea80f-144"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea80f-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ea80f-145">Library</span></span><br/> | <dl> <span data-ttu-id="ea80f-146"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea80f-146"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea80f-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea80f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea80f-148">**Idirectxfileobject**</span><span class="sxs-lookup"><span data-stu-id="ea80f-148">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="ea80f-149">X-Datei Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ea80f-149">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




