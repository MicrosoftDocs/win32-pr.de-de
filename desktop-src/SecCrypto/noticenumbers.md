---
description: 'NoticeNumbers-Objekt: Stellt eine Auflistung von Extension-Objekten dar.'
ms.assetid: b0d69df9-12c4-4872-b883-b029c4350502
title: NoticeNumbers-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b2bd6e653eabe9b25588fd29517ac94e0c878fdb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090758"
---
# <a name="noticenumbers-object"></a><span data-ttu-id="46c2e-103">NoticeNumbers-Objekt</span><span class="sxs-lookup"><span data-stu-id="46c2e-103">NoticeNumbers object</span></span>

<span data-ttu-id="46c2e-104">\[Das **NoticeNumbers-Objekt** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="46c2e-104">\[The **NoticeNumbers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="46c2e-105">Weitere Informationen finden Sie unter [**Qualifizierer**](qualifier.md).\]</span><span class="sxs-lookup"><span data-stu-id="46c2e-105">For more information, see [**Qualifier**](qualifier.md).\]</span></span>

<span data-ttu-id="46c2e-106">Das **NoticeNumbers-Objekt** stellt eine Auflistung von [**Extension-Objekten**](extension.md) dar.</span><span class="sxs-lookup"><span data-stu-id="46c2e-106">The **NoticeNumbers** object represents a collection of [**Extension**](extension.md) objects.</span></span> <span data-ttu-id="46c2e-107">Jedes [**Extension-Objekt**](extension.md) stellt eine Benutzerhinweisnummer dar.</span><span class="sxs-lookup"><span data-stu-id="46c2e-107">Each [**Extension**](extension.md) object represents a user notice number.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="46c2e-108">Verwendung</span><span class="sxs-lookup"><span data-stu-id="46c2e-108">When to use</span></span>

<span data-ttu-id="46c2e-109">Das **NoticeNumbers-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="46c2e-109">The **NoticeNumbers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="46c2e-110">Ruft die Anzahl der [**Extension-Objekte**](extension.md) in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="46c2e-110">Retrieve the number of [**Extension**](extension.md) objects in the collection.</span></span>
-   <span data-ttu-id="46c2e-111">Ruft ein bestimmtes [**Extension-Objekt**](extension.md) aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="46c2e-111">Retrieve a specific [**Extension**](extension.md) object from the collection.</span></span>
-   <span data-ttu-id="46c2e-112">Iterieren Sie die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="46c2e-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="46c2e-113">Member</span><span class="sxs-lookup"><span data-stu-id="46c2e-113">Members</span></span>

<span data-ttu-id="46c2e-114">Das **NoticeNumbers-Objekt** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="46c2e-114">The **NoticeNumbers** object has these types of members:</span></span>

-   [<span data-ttu-id="46c2e-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="46c2e-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46c2e-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="46c2e-116">Properties</span></span>

<span data-ttu-id="46c2e-117">Das **NoticeNumbers-Objekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="46c2e-117">The **NoticeNumbers** object has these properties.</span></span>



| <span data-ttu-id="46c2e-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="46c2e-118">Property</span></span>                                              | <span data-ttu-id="46c2e-119">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="46c2e-119">Access type</span></span>          | <span data-ttu-id="46c2e-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46c2e-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46c2e-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="46c2e-121">**\_NewEnum**</span></span>](noticenumbers-newenum.md)<br/> | <span data-ttu-id="46c2e-122">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46c2e-122">Read-only</span></span><br/> | <span data-ttu-id="46c2e-123">Ruft eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="46c2e-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="46c2e-124">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="46c2e-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="46c2e-125">**Anzahl**</span><span class="sxs-lookup"><span data-stu-id="46c2e-125">**Count**</span></span>](noticenumbers-count.md)<br/>       | <span data-ttu-id="46c2e-126">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46c2e-126">Read-only</span></span><br/> | <span data-ttu-id="46c2e-127">Ruft die Anzahl der [**Extension-Objekte**](extension.md) in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="46c2e-127">Retrieves the number of [**Extension**](extension.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="46c2e-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="46c2e-128">**Item**</span></span>](noticenumbers-item.md)<br/>         | <span data-ttu-id="46c2e-129">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46c2e-129">Read-only</span></span><br/> | <span data-ttu-id="46c2e-130">Ruft das [**Extension-Objekt**](extension.md) ab, das die indizierte Hinweisnummer der Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="46c2e-130">Retrieves the [**Extension**](extension.md) object that represents the indexed notice number of the collection.</span></span><br/> <span data-ttu-id="46c2e-131">Dies ist die Standardeigenschaft.</span><span class="sxs-lookup"><span data-stu-id="46c2e-131">This is the default property.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="46c2e-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46c2e-132">Remarks</span></span>

<span data-ttu-id="46c2e-133">Das **NoticeNumbers-Objekt** kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="46c2e-133">The **NoticeNumbers** object cannot be created.</span></span>

<span data-ttu-id="46c2e-134">Das NoticeNumbers-Objekt wird in der [**Qualifier.NoticeNumbers-Eigenschaft**](qualifier-noticenumbers.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="46c2e-134">The NoticeNumbers object is used in the [**Qualifier.NoticeNumbers**](qualifier-noticenumbers.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="46c2e-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46c2e-135">Requirements</span></span>



| <span data-ttu-id="46c2e-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46c2e-136">Requirement</span></span> | <span data-ttu-id="46c2e-137">Wert</span><span class="sxs-lookup"><span data-stu-id="46c2e-137">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46c2e-138">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="46c2e-138">Redistributable</span></span><br/> | <span data-ttu-id="46c2e-139">CAPICOM 2.0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="46c2e-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="46c2e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="46c2e-140">DLL</span></span><br/>             | <dl> <span data-ttu-id="46c2e-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46c2e-141"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
