---
description: Stellt eine Auflistung von EKU-Objekten dar.
ms.assetid: 04b9f0bf-e1d4-4a2c-be5d-bae7c1090bdb
title: EKUs-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 56fd6eaeb5a00549cbb4ee659b99ece391e0ebed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371696"
---
# <a name="ekus-object"></a><span data-ttu-id="04778-103">EKUs-Objekt</span><span class="sxs-lookup"><span data-stu-id="04778-103">EKUs object</span></span>

<span data-ttu-id="04778-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="04778-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="04778-105">Verwenden Sie stattdessen die [**X509ExtensionCollection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="04778-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="04778-106">Das **EKUs** -Objekt stellt eine Auflistung von [**EKU**](eku.md) -Objekten dar.</span><span class="sxs-lookup"><span data-stu-id="04778-106">The **EKUs** object represents a collection of [**EKU**](eku.md) objects.</span></span> <span data-ttu-id="04778-107">Jedes [**EKU**](eku.md) -Objekt stellt eine einzelne EKU (Extended Key Usage)-Eigenschaft eines Zertifikats dar.</span><span class="sxs-lookup"><span data-stu-id="04778-107">Each [**EKU**](eku.md) object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="04778-108">Verwendung</span><span class="sxs-lookup"><span data-stu-id="04778-108">When to use</span></span>

<span data-ttu-id="04778-109">Die **EKUs** -Sammlung wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="04778-109">The **EKUs** collection is used to perform the following tasks:</span></span>

-   <span data-ttu-id="04778-110">Ruft die Anzahl der EKU-Eigenschaften in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="04778-110">Retrieve the number of EKU properties in the collection.</span></span>
-   <span data-ttu-id="04778-111">Rufen Sie ein bestimmtes [**EKU**](eku.md) -Objekt aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="04778-111">Retrieve a specific [**EKU**](eku.md) object from the collection.</span></span>
-   <span data-ttu-id="04778-112">Iterieren Sie die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="04778-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="04778-113">Member</span><span class="sxs-lookup"><span data-stu-id="04778-113">Members</span></span>

<span data-ttu-id="04778-114">Das **EKUs** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="04778-114">The **EKUs** object has these types of members:</span></span>

-   [<span data-ttu-id="04778-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="04778-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="04778-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="04778-116">Properties</span></span>

<span data-ttu-id="04778-117">Das **EKUs** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="04778-117">The **EKUs** object has these properties.</span></span>



| <span data-ttu-id="04778-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04778-118">Property</span></span>                                     | <span data-ttu-id="04778-119">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="04778-119">Access type</span></span>          | <span data-ttu-id="04778-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04778-120">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04778-121">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="04778-121">**\_NewEnum**</span></span>](ekus-newenum.md)<br/> | <span data-ttu-id="04778-122">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04778-122">Read-only</span></span><br/> | <span data-ttu-id="04778-123">Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="04778-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="04778-124">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="04778-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="04778-125">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="04778-125">**Count**</span></span>](ekus-count.md)<br/>       | <span data-ttu-id="04778-126">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04778-126">Read-only</span></span><br/> | <span data-ttu-id="04778-127">Ruft die Anzahl der [**EKU**](eku.md) -Objekte in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="04778-127">Retrieves the number of [**EKU**](eku.md) objects in the collection.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="04778-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="04778-128">**Item**</span></span>](ekus-item.md)<br/>         | <span data-ttu-id="04778-129">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04778-129">Read-only</span></span><br/> | <span data-ttu-id="04778-130">Ruft das [**EKU**](eku.md) -Objekt ab, das die indizierte EKU-Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="04778-130">Retrieves the [**EKU**](eku.md) object that represents the indexed EKU property.</span></span> <span data-ttu-id="04778-131">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="04778-131">This is the default property.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="04778-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04778-132">Remarks</span></span>

<span data-ttu-id="04778-133">Diese Auflistung wird von der [**extendedkeyusage. EKUs**](extendedkeyusage-ekus.md) -Eigenschaft abgerufen.</span><span class="sxs-lookup"><span data-stu-id="04778-133">This collection is retrieved by the [**ExtendedKeyUsage.EKUs**](extendedkeyusage-ekus.md) property.</span></span>

<span data-ttu-id="04778-134">Das **EKUs** -Objekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="04778-134">The **EKUs** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="04778-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04778-135">Requirements</span></span>



| <span data-ttu-id="04778-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04778-136">Requirement</span></span> | <span data-ttu-id="04778-137">Wert</span><span class="sxs-lookup"><span data-stu-id="04778-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04778-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="04778-138">End of client support</span></span><br/> | <span data-ttu-id="04778-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04778-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="04778-140">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="04778-140">End of server support</span></span><br/> | <span data-ttu-id="04778-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04778-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="04778-142">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="04778-142">Redistributable</span></span><br/>       | <span data-ttu-id="04778-143">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="04778-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="04778-144">DLL</span><span class="sxs-lookup"><span data-stu-id="04778-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="04778-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04778-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
