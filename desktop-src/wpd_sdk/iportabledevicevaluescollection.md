---
description: Die iportabledevicevaluescollection-Schnittstelle enthält eine Auflistung von Null basierten indizierten iportabledevicevalues-Schnittstellen.
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
title: Iportableabvicevaluescollection-Schnittstelle (portabledebug-YPES. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cebe15dc9a4f4347eb58563e9b43240464565a4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365904"
---
# <a name="iportabledevicevaluescollection-interface"></a><span data-ttu-id="34311-103">Iportableabvicevaluescollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="34311-103">IPortableDeviceValuesCollection interface</span></span>

<span data-ttu-id="34311-104">Die **iportabledevicevaluescollection** -Schnittstelle enthält eine Auflistung von Null basierten indizierten **iportabledevicevalues** -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="34311-104">The **IPortableDeviceValuesCollection** interface holds a collection of zero-based indexed **IPortableDeviceValues** interfaces.</span></span> <span data-ttu-id="34311-105">Diese Schnittstelle kann aus einer-Methode abgerufen werden, oder wenn ein neues-Objekt erforderlich ist, rufen Sie **CoCreate** mit der **CLSID \_ portabledevicevaluescollection** auf.</span><span class="sxs-lookup"><span data-stu-id="34311-105">This interface can be retrieved from a method, or if a new object is required, call **CoCreate** with **CLSID\_PortableDeviceValuesCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="34311-106">Member</span><span class="sxs-lookup"><span data-stu-id="34311-106">Members</span></span>

<span data-ttu-id="34311-107">Die **iportabledebug** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="34311-107">The **IPortableDeviceValuesCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="34311-108">**Iportabletovicevaluescollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="34311-108">**IPortableDeviceValuesCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="34311-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="34311-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="34311-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="34311-110">Methods</span></span>

<span data-ttu-id="34311-111">Die **iportabledevicevaluescollection** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="34311-111">The **IPortableDeviceValuesCollection** interface has these methods.</span></span>



| <span data-ttu-id="34311-112">Methode</span><span class="sxs-lookup"><span data-stu-id="34311-112">Method</span></span>                                                       | <span data-ttu-id="34311-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34311-113">Description</span></span>                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="34311-114">**Eren**</span><span class="sxs-lookup"><span data-stu-id="34311-114">**Add**</span></span>](iportabledevicevaluescollection-add.md)           | <span data-ttu-id="34311-115">Fügt der Auflistung ein Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="34311-115">Adds an item to the collection</span></span><br/>                                           |
| [<span data-ttu-id="34311-116">**Klartext**</span><span class="sxs-lookup"><span data-stu-id="34311-116">**Clear**</span></span>](iportabledevicevaluescollection-clear.md)       | <span data-ttu-id="34311-117">Gibt alle Elemente aus der Auflistung frei.</span><span class="sxs-lookup"><span data-stu-id="34311-117">Releases all items from the collection.</span></span><br/>                                  |
| [<span data-ttu-id="34311-118">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="34311-118">**GetAt**</span></span>](iportabledevicevaluescollection-getat.md)       | <span data-ttu-id="34311-119">Ruft ein Element durch einen NULL basierten Index aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="34311-119">Retrieves an item from the collection by a zero-based index.</span></span><br/>             |
| [<span data-ttu-id="34311-120">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="34311-120">**GetCount**</span></span>](iportabledevicevaluescollection-getcount.md) | <span data-ttu-id="34311-121">Ruft die Anzahl der Elemente in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="34311-121">Retrieves the number of items in the collection.</span></span><br/>                         |
| [<span data-ttu-id="34311-122">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="34311-122">**RemoveAt**</span></span>](iportabledevicevaluescollection-removeat.md) | <span data-ttu-id="34311-123">Entfernt das Element, das an der durch den angegebenen Index angegebenen Position gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="34311-123">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="34311-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34311-124">Requirements</span></span>



| <span data-ttu-id="34311-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34311-125">Requirement</span></span> | <span data-ttu-id="34311-126">Wert</span><span class="sxs-lookup"><span data-stu-id="34311-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34311-127">Header</span><span class="sxs-lookup"><span data-stu-id="34311-127">Header</span></span><br/>  | <dl> <span data-ttu-id="34311-128"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="34311-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="34311-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="34311-129">Library</span></span><br/> | <dl> <span data-ttu-id="34311-130"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34311-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34311-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34311-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34311-132">**Sammlungs Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="34311-132">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

