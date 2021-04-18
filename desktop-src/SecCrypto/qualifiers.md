---
description: Stellt eine Auflistung von Qualifizierern dar.
ms.assetid: 2f51404d-b26e-4153-b206-ab6b413363a1
title: Qualifiziererobjekt (IADs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e873019d6fbfb21de8be430d7960f697b39eeca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358348"
---
# <a name="qualifiers-object"></a><span data-ttu-id="03d66-103">Qualifiziererobjekt</span><span class="sxs-lookup"><span data-stu-id="03d66-103">Qualifiers object</span></span>

<span data-ttu-id="03d66-104">\[Das **qualifiziererobjekt** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="03d66-104">\[The **Qualifiers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="03d66-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung sind.\]</span><span class="sxs-lookup"><span data-stu-id="03d66-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="03d66-106">Das **qualifiziererobjekt** stellt eine Auflistung von Qualifizierern dar.</span><span class="sxs-lookup"><span data-stu-id="03d66-106">The **Qualifiers** object represents a collection of qualifiers.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="03d66-107">Verwendung</span><span class="sxs-lookup"><span data-stu-id="03d66-107">When to use</span></span>

<span data-ttu-id="03d66-108">Das **qualifiziererobjekt** wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="03d66-108">The **Qualifiers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="03d66-109">Ruft eine bestimmte erweiterte Eigenschaft aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="03d66-109">Retrieve a specific extended property from the collection.</span></span>
-   <span data-ttu-id="03d66-110">Ruft die Anzahl der erweiterten Eigenschaften in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="03d66-110">Retrieve the number of extended properties in the collection.</span></span>
-   <span data-ttu-id="03d66-111">Iterieren Sie die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="03d66-111">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="03d66-112">Member</span><span class="sxs-lookup"><span data-stu-id="03d66-112">Members</span></span>

<span data-ttu-id="03d66-113">Das **qualifiziererobjekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="03d66-113">The **Qualifiers** object has these types of members:</span></span>

-   [<span data-ttu-id="03d66-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03d66-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03d66-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03d66-115">Properties</span></span>

<span data-ttu-id="03d66-116">Das **qualifiziererobjekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="03d66-116">The **Qualifiers** object has these properties.</span></span>



| <span data-ttu-id="03d66-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="03d66-117">Property</span></span>                                           | <span data-ttu-id="03d66-118">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="03d66-118">Access type</span></span>          | <span data-ttu-id="03d66-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03d66-119">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03d66-120">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="03d66-120">**\_NewEnum**</span></span>](qualifiers-newenum.md)<br/> | <span data-ttu-id="03d66-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="03d66-121">Read-only</span></span><br/> | <span data-ttu-id="03d66-122">Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="03d66-122">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="03d66-123">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="03d66-123">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="03d66-124">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="03d66-124">**Count**</span></span>](qualifiers-count.md)<br/>       | <span data-ttu-id="03d66-125">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="03d66-125">Read-only</span></span><br/> | <span data-ttu-id="03d66-126">Ruft die Anzahl der Qualifizierer in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="03d66-126">Retrieves the number of qualifiers in the collection.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="03d66-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="03d66-127">**Item**</span></span>](qualifiers-item.md)<br/>         | <span data-ttu-id="03d66-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="03d66-128">Read-only</span></span><br/> | <span data-ttu-id="03d66-129">Ruft ein [**qualifiziererobjekt**](qualifier.md) ab, das den indizierten Qualifizierer der Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="03d66-129">Retrieves a [**Qualifier**](qualifier.md) object that represents the indexed qualifier of the collection.</span></span> <span data-ttu-id="03d66-130">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="03d66-130">This is the default property.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="03d66-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03d66-131">Remarks</span></span>

<span data-ttu-id="03d66-132">Das **qualifiziererobjekt** kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="03d66-132">The **Qualifiers** object cannot be created.</span></span>

<span data-ttu-id="03d66-133">Die [**policyinformation. Qualifizierer**](policyinformation-qualifiers.md) CAPICOM-Objekt Eigenschaft gibt ein **qualifiziererobjekt** zurück.</span><span class="sxs-lookup"><span data-stu-id="03d66-133">The [**PolicyInformation.Qualifiers**](policyinformation-qualifiers.md) CAPICOM object property returns a **Qualifiers** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="03d66-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03d66-134">Requirements</span></span>



| <span data-ttu-id="03d66-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03d66-135">Requirement</span></span> | <span data-ttu-id="03d66-136">Wert</span><span class="sxs-lookup"><span data-stu-id="03d66-136">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03d66-137">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="03d66-137">Redistributable</span></span><br/> | <span data-ttu-id="03d66-138">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="03d66-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="03d66-139">Header</span><span class="sxs-lookup"><span data-stu-id="03d66-139">Header</span></span><br/>          | <dl> <span data-ttu-id="03d66-140"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="03d66-140"><dt>Iads.h</dt></span></span> </dl>      |
| <span data-ttu-id="03d66-141">DLL</span><span class="sxs-lookup"><span data-stu-id="03d66-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="03d66-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03d66-142"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
