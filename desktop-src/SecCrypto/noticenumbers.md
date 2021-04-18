---
description: Stellt eine Auflistung von Erweiterungs Objekten dar.
ms.assetid: b0d69df9-12c4-4872-b883-b029c4350502
title: Noticenenumbers-Objekt
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
ms.openlocfilehash: 58d954fdeef66d6d0e5eadb3086cb549b59e5669
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361000"
---
# <a name="noticenumbers-object"></a><span data-ttu-id="b863b-103">Noticenenumbers-Objekt</span><span class="sxs-lookup"><span data-stu-id="b863b-103">NoticeNumbers object</span></span>

<span data-ttu-id="b863b-104">\[Das **noticenenumbers** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b863b-104">\[The **NoticeNumbers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b863b-105">Weitere Informationen finden Sie unter [**Qualifizierer**](qualifier.md).\]</span><span class="sxs-lookup"><span data-stu-id="b863b-105">For more information, see [**Qualifier**](qualifier.md).\]</span></span>

<span data-ttu-id="b863b-106">Das **noticenenumbers** -Objekt stellt eine Auflistung von [**Erweiterungs**](extension.md) Objekten dar.</span><span class="sxs-lookup"><span data-stu-id="b863b-106">The **NoticeNumbers** object represents a collection of [**Extension**](extension.md) objects.</span></span> <span data-ttu-id="b863b-107">Jedes [**Erweiterungs**](extension.md) Objekt stellt eine Benutzer-Benachrichtigungs Nummer dar.</span><span class="sxs-lookup"><span data-stu-id="b863b-107">Each [**Extension**](extension.md) object represents a user notice number.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b863b-108">Verwendung</span><span class="sxs-lookup"><span data-stu-id="b863b-108">When to use</span></span>

<span data-ttu-id="b863b-109">Das **noticenenumbers** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="b863b-109">The **NoticeNumbers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="b863b-110">Ruft die Anzahl der [**Erweiterungs**](extension.md) Objekte in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="b863b-110">Retrieve the number of [**Extension**](extension.md) objects in the collection.</span></span>
-   <span data-ttu-id="b863b-111">Ruft ein bestimmtes [**Erweiterungs**](extension.md) Objekt aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="b863b-111">Retrieve a specific [**Extension**](extension.md) object from the collection.</span></span>
-   <span data-ttu-id="b863b-112">Iterieren Sie die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="b863b-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="b863b-113">Member</span><span class="sxs-lookup"><span data-stu-id="b863b-113">Members</span></span>

<span data-ttu-id="b863b-114">Das benachrichtitenenumerationsobjekt enthält diese Typen von **Membern** :</span><span class="sxs-lookup"><span data-stu-id="b863b-114">The **NoticeNumbers** object has these types of members:</span></span>

-   [<span data-ttu-id="b863b-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b863b-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b863b-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b863b-116">Properties</span></span>

<span data-ttu-id="b863b-117">Das **noticenenumbers** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b863b-117">The **NoticeNumbers** object has these properties.</span></span>



| <span data-ttu-id="b863b-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b863b-118">Property</span></span>                                              | <span data-ttu-id="b863b-119">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="b863b-119">Access type</span></span>          | <span data-ttu-id="b863b-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b863b-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b863b-121">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="b863b-121">**\_NewEnum**</span></span>](noticenumbers-newenum.md)<br/> | <span data-ttu-id="b863b-122">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b863b-122">Read-only</span></span><br/> | <span data-ttu-id="b863b-123">Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b863b-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="b863b-124">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="b863b-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="b863b-125">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="b863b-125">**Count**</span></span>](noticenumbers-count.md)<br/>       | <span data-ttu-id="b863b-126">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b863b-126">Read-only</span></span><br/> | <span data-ttu-id="b863b-127">Ruft die Anzahl der [**Erweiterungs**](extension.md) Objekte in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="b863b-127">Retrieves the number of [**Extension**](extension.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="b863b-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="b863b-128">**Item**</span></span>](noticenumbers-item.md)<br/>         | <span data-ttu-id="b863b-129">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b863b-129">Read-only</span></span><br/> | <span data-ttu-id="b863b-130">Ruft das [**Erweiterungs**](extension.md) Objekt ab, das die indizierte Benachrichtigungs Nummer der Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="b863b-130">Retrieves the [**Extension**](extension.md) object that represents the indexed notice number of the collection.</span></span><br/> <span data-ttu-id="b863b-131">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b863b-131">This is the default property.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="b863b-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b863b-132">Remarks</span></span>

<span data-ttu-id="b863b-133">Das **noticenenumbers** -Objekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b863b-133">The **NoticeNumbers** object cannot be created.</span></span>

<span data-ttu-id="b863b-134">Das noticenenumbers-Objekt wird in der [**Qualifizierer. noticenumschlag**](qualifier-noticenumbers.md) -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="b863b-134">The NoticeNumbers object is used in the [**Qualifier.NoticeNumbers**](qualifier-noticenumbers.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b863b-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b863b-135">Requirements</span></span>



| <span data-ttu-id="b863b-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b863b-136">Requirement</span></span> | <span data-ttu-id="b863b-137">Wert</span><span class="sxs-lookup"><span data-stu-id="b863b-137">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b863b-138">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="b863b-138">Redistributable</span></span><br/> | <span data-ttu-id="b863b-139">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="b863b-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b863b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b863b-140">DLL</span></span><br/>             | <dl> <span data-ttu-id="b863b-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b863b-141"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
