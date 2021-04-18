---
description: Die iportabledevicekeycollection-Schnittstelle enthält eine Auflistung von PropertyKey-Werten. Diese Schnittstelle kann aus einer-Methode abgerufen werden. Wenn ein neues-Objekt erforderlich ist, rufen Sie CoCreate mit der CLSID \_ portabledevicekeycollection auf.
ms.assetid: 2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd
title: Iportabledevicekeycollection-Schnittstelle (portableabvicetypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: c246fabe7ced72a5aad6d30101df8035a159a923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371627"
---
# <a name="iportabledevicekeycollection-interface"></a><span data-ttu-id="60c31-104">Iportabledevicekeycollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="60c31-104">IPortableDeviceKeyCollection interface</span></span>

<span data-ttu-id="60c31-105">Die **iportabledevicekeycollection** -Schnittstelle enthält eine Auflistung von **PropertyKey** -Werten.</span><span class="sxs-lookup"><span data-stu-id="60c31-105">The **IPortableDeviceKeyCollection** interface holds a collection of **PROPERTYKEY** values.</span></span> <span data-ttu-id="60c31-106">Diese Schnittstelle kann aus einer-Methode abgerufen werden. Wenn ein neues-Objekt erforderlich ist, rufen Sie **CoCreate** mit der **CLSID \_ portabledevicekeycollection** auf.</span><span class="sxs-lookup"><span data-stu-id="60c31-106">This interface can be retrieved from a method or, if a new object is required, call **CoCreate** with **CLSID\_PortableDeviceKeyCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="60c31-107">Member</span><span class="sxs-lookup"><span data-stu-id="60c31-107">Members</span></span>

<span data-ttu-id="60c31-108">Die **iportabledevicekeycollection** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="60c31-108">The **IPortableDeviceKeyCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="60c31-109">**Iportabledevicekeycollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="60c31-109">**IPortableDeviceKeyCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="60c31-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="60c31-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="60c31-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="60c31-111">Methods</span></span>

<span data-ttu-id="60c31-112">Die **iportabledevicekeycollection** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="60c31-112">The **IPortableDeviceKeyCollection** interface has these methods.</span></span>



| <span data-ttu-id="60c31-113">Methode</span><span class="sxs-lookup"><span data-stu-id="60c31-113">Method</span></span>                                                    | <span data-ttu-id="60c31-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60c31-114">Description</span></span>                                                                         |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="60c31-115">**Eren**</span><span class="sxs-lookup"><span data-stu-id="60c31-115">**Add**</span></span>](iportabledevicekeycollection-add.md)           | <span data-ttu-id="60c31-116">Fügt der Auflistung einen Eigenschafts Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="60c31-116">Adds a property key to the collection.</span></span><br/>                                   |
| [<span data-ttu-id="60c31-117">**Klartext**</span><span class="sxs-lookup"><span data-stu-id="60c31-117">**Clear**</span></span>](iportabledevicekeycollection-clear.md)       | <span data-ttu-id="60c31-118">Löscht alle Elemente aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="60c31-118">Deletes all items from the collection.</span></span><br/>                                   |
| [<span data-ttu-id="60c31-119">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="60c31-119">**GetAt**</span></span>](iportabledevicekeycollection-getat.md)       | <span data-ttu-id="60c31-120">Ruft einen **PropertyKey** aus der Auflistung nach Index ab.</span><span class="sxs-lookup"><span data-stu-id="60c31-120">Retrieves a **PROPERTYKEY** from the collection by index.</span></span><br/>                |
| [<span data-ttu-id="60c31-121">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="60c31-121">**GetCount**</span></span>](iportabledevicekeycollection-getcount.md) | <span data-ttu-id="60c31-122">Ruft die Anzahl der Schlüssel in dieser Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="60c31-122">Retrieves the number of keys in this collection.</span></span><br/>                         |
| [<span data-ttu-id="60c31-123">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="60c31-123">**RemoveAt**</span></span>](iportabledevicekeycollection-removeat.md) | <span data-ttu-id="60c31-124">Entfernt das Element, das an der durch den angegebenen Index angegebenen Position gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="60c31-124">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="60c31-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60c31-125">Requirements</span></span>



| <span data-ttu-id="60c31-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60c31-126">Requirement</span></span> | <span data-ttu-id="60c31-127">Wert</span><span class="sxs-lookup"><span data-stu-id="60c31-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60c31-128">Header</span><span class="sxs-lookup"><span data-stu-id="60c31-128">Header</span></span><br/>  | <dl> <span data-ttu-id="60c31-129"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="60c31-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="60c31-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="60c31-130">Library</span></span><br/> | <dl> <span data-ttu-id="60c31-131"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60c31-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60c31-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60c31-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60c31-133">**Sammlungs Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="60c31-133">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

