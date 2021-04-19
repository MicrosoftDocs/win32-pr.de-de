---
description: Die iportabledevicepropvariantcollection-Schnittstelle enthält eine Auflistung von indizierten PROPVARIANT-Werten desselben VarType.
ms.assetid: 41224958-a5a0-4e09-8733-d0ae036f68b9
title: Iportabledevicepropvariantcollection-Schnittstelle (portableabvicetypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 14ba07894c74567487704bb1f63e7242542af313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373707"
---
# <a name="iportabledevicepropvariantcollection-interface"></a><span data-ttu-id="f00a5-103">Iportabledevicepropvariantcollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f00a5-103">IPortableDevicePropVariantCollection interface</span></span>

<span data-ttu-id="f00a5-104">Die **iportabledevicepropvariantcollection** -Schnittstelle enthält eine Auflistung von indizierten **PROPVARIANT** -Werten desselben VarType.</span><span class="sxs-lookup"><span data-stu-id="f00a5-104">The **IPortableDevicePropVariantCollection** interface holds a collection of indexed **PROPVARIANT** values of the same VARTYPE.</span></span> <span data-ttu-id="f00a5-105">Der VarType des ersten Elements, das der Auflistung hinzugefügt wird, bestimmt den VarType der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="f00a5-105">The VARTYPE of the first item that is added to the collection determines the VARTYPE of the collection.</span></span> <span data-ttu-id="f00a5-106">Der Versuch, ein Element eines anderen VarType hinzuzufügen, schlägt möglicherweise fehl, wenn der **PROPVARIANT** -Wert nicht in den aktuellen VarType der Auflistung geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f00a5-106">An attempt to add an item of a different VARTYPE may fail if the **PROPVARIANT** value cannot be changed to the collection's current VARTYPE.</span></span> <span data-ttu-id="f00a5-107">Um den VarType der Auflistung zu ändern, nennen Sie **ChangeType**.</span><span class="sxs-lookup"><span data-stu-id="f00a5-107">To change the VARTYPE of the collection, call **ChangeType**.</span></span>

<span data-ttu-id="f00a5-108">Diese Schnittstelle kann aus einer-Methode abgerufen werden. Wenn ein neues-Objekt erforderlich ist, rufen Sie **CoCreate** mit der **CLSID \_ portabledevicepropvariantcollection** auf.</span><span class="sxs-lookup"><span data-stu-id="f00a5-108">This interface can be retrieved from a method or, if a new object is required, call **CoCreate** with **CLSID\_PortableDevicePropVariantCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="f00a5-109">Member</span><span class="sxs-lookup"><span data-stu-id="f00a5-109">Members</span></span>

<span data-ttu-id="f00a5-110">Die **iportabledevicepropvariantcollection** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f00a5-110">The **IPortableDevicePropVariantCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f00a5-111">**Iportabledevicepropvariantcollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f00a5-111">**IPortableDevicePropVariantCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="f00a5-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="f00a5-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f00a5-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="f00a5-113">Methods</span></span>

<span data-ttu-id="f00a5-114">Die **iportabledevicepropvariantcollection** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f00a5-114">The **IPortableDevicePropVariantCollection** interface has these methods.</span></span>



| <span data-ttu-id="f00a5-115">Methode</span><span class="sxs-lookup"><span data-stu-id="f00a5-115">Method</span></span>                                                                | <span data-ttu-id="f00a5-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f00a5-116">Description</span></span>                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="f00a5-117">**Eren**</span><span class="sxs-lookup"><span data-stu-id="f00a5-117">**Add**</span></span>](iportabledevicepropvariantcollection-add.md)               | <span data-ttu-id="f00a5-118">Fügt der Auflistung ein Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="f00a5-118">Adds an item to the collection.</span></span><br/>                                          |
| [<span data-ttu-id="f00a5-119">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="f00a5-119">**ChangeType**</span></span>](iportabledevicepropvariantcollection-changetype.md) | <span data-ttu-id="f00a5-120">Konvertiert alle Elemente in der Auflistung in den angegebenen VarType.</span><span class="sxs-lookup"><span data-stu-id="f00a5-120">Converts all items in the collection to the specified VARTYPE.</span></span><br/>           |
| [<span data-ttu-id="f00a5-121">**Klartext**</span><span class="sxs-lookup"><span data-stu-id="f00a5-121">**Clear**</span></span>](iportabledevicepropvariantcollection-clear.md)           | <span data-ttu-id="f00a5-122">Gibt alle Elemente aus der Auflistung frei und entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="f00a5-122">Frees, and then removes, all items from the collection.</span></span><br/>                  |
| [<span data-ttu-id="f00a5-123">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="f00a5-123">**GetAt**</span></span>](iportabledevicepropvariantcollection-getat.md)           | <span data-ttu-id="f00a5-124">Ruft ein Element durch einen NULL basierten Index aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="f00a5-124">Retrieves an item from the collection by a zero-based index.</span></span><br/>             |
| [<span data-ttu-id="f00a5-125">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="f00a5-125">**GetCount**</span></span>](iportabledevicepropvariantcollection-getcount.md)     | <span data-ttu-id="f00a5-126">Ruft die Anzahl der Elemente in dieser Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="f00a5-126">Retrieves the number of items in this collection.</span></span><br/>                        |
| [<span data-ttu-id="f00a5-127">**GetType**</span><span class="sxs-lookup"><span data-stu-id="f00a5-127">**GetType**</span></span>](iportabledevicepropvariantcollection-gettype.md)       | <span data-ttu-id="f00a5-128">Ruft den Datentyp der Elemente in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="f00a5-128">Retrieves the data type of the items in the collection.</span></span><br/>                  |
| [<span data-ttu-id="f00a5-129">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="f00a5-129">**RemoveAt**</span></span>](iportabledevicepropvariantcollection-removeat.md)     | <span data-ttu-id="f00a5-130">Entfernt das Element, das an der durch den angegebenen Index angegebenen Position gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f00a5-130">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f00a5-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f00a5-131">Requirements</span></span>



| <span data-ttu-id="f00a5-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f00a5-132">Requirement</span></span> | <span data-ttu-id="f00a5-133">Wert</span><span class="sxs-lookup"><span data-stu-id="f00a5-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f00a5-134">Header</span><span class="sxs-lookup"><span data-stu-id="f00a5-134">Header</span></span><br/>  | <dl> <span data-ttu-id="f00a5-135"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="f00a5-135"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f00a5-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f00a5-136">Library</span></span><br/> | <dl> <span data-ttu-id="f00a5-137"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f00a5-137"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f00a5-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f00a5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f00a5-139">**Sammlungs Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="f00a5-139">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

