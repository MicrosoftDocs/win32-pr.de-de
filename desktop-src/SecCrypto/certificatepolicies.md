---
description: Eine Auflistung von policyinformation-Objekten.
ms.assetid: 2abdd070-82ae-47fd-afbc-6d4361e5a3f1
title: Certificatepolicies-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8ec217276b5d038f85f33887b771b0afa0c6e40a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369697"
---
# <a name="certificatepolicies-object"></a><span data-ttu-id="0987f-103">Certificatepolicies-Objekt</span><span class="sxs-lookup"><span data-stu-id="0987f-103">CertificatePolicies object</span></span>

<span data-ttu-id="0987f-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0987f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0987f-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um die Zertifikat Richtlinien abzurufen.\]</span><span class="sxs-lookup"><span data-stu-id="0987f-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="0987f-106">Das **certificatepolicies** -Objekt stellt eine Auflistung von [**policyinformation**](policyinformation.md) -Objekten dar.</span><span class="sxs-lookup"><span data-stu-id="0987f-106">The **CertificatePolicies** object represents a collection of [**PolicyInformation**](policyinformation.md) objects.</span></span> <span data-ttu-id="0987f-107">Jedes [**policyinformation**](policyinformation.md) -Objekt stellt eine einzelne Zertifikat Richtlinie dar.</span><span class="sxs-lookup"><span data-stu-id="0987f-107">Each [**PolicyInformation**](policyinformation.md) object represents a single certificate policy.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="0987f-108">Verwendung</span><span class="sxs-lookup"><span data-stu-id="0987f-108">When to use</span></span>

<span data-ttu-id="0987f-109">Das **certificatepolicies** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="0987f-109">The **CertificatePolicies** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="0987f-110">Abrufen der Anzahl der Zertifikat Richtlinien in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="0987f-110">Retrieve the number of certificate policies in the collection.</span></span>
-   <span data-ttu-id="0987f-111">Rufen Sie ein bestimmtes [**policyinformation**](policyinformation.md) -Objekt aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="0987f-111">Retrieve a specific [**PolicyInformation**](policyinformation.md) object from the collection.</span></span>
-   <span data-ttu-id="0987f-112">Iterieren Sie die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="0987f-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="0987f-113">Member</span><span class="sxs-lookup"><span data-stu-id="0987f-113">Members</span></span>

<span data-ttu-id="0987f-114">Das **certificatepolicies** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0987f-114">The **CertificatePolicies** object has these types of members:</span></span>

-   [<span data-ttu-id="0987f-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0987f-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0987f-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0987f-116">Properties</span></span>

<span data-ttu-id="0987f-117">Das **certificatepolicies** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0987f-117">The **CertificatePolicies** object has these properties.</span></span>



| <span data-ttu-id="0987f-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0987f-118">Property</span></span>                                                    | <span data-ttu-id="0987f-119">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="0987f-119">Access type</span></span>          | <span data-ttu-id="0987f-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0987f-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0987f-121">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="0987f-121">**\_NewEnum**</span></span>](certificatepolicies-newenum.md)<br/> | <span data-ttu-id="0987f-122">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0987f-122">Read-only</span></span><br/> | <span data-ttu-id="0987f-123">Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0987f-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="0987f-124">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="0987f-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="0987f-125">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="0987f-125">**Count**</span></span>](certificatepolicies-count.md)<br/>       | <span data-ttu-id="0987f-126">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0987f-126">Read-only</span></span><br/> | <span data-ttu-id="0987f-127">Ruft die Anzahl der [**policyinformation**](policyinformation.md) -Objekte in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="0987f-127">Retrieves the number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="0987f-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="0987f-128">**Item**</span></span>](certificatepolicies-item.md)<br/>         | <span data-ttu-id="0987f-129">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0987f-129">Read-only</span></span><br/> | <span data-ttu-id="0987f-130">Ruft ein [**policyinformation**](policyinformation.md) -Objekt ab, das die indizierte Zertifikat Richtlinie der Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="0987f-130">Retrieves a [**PolicyInformation**](policyinformation.md) object that represents the indexed certificate policy of the collection.</span></span> <span data-ttu-id="0987f-131">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0987f-131">This is the default property.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="0987f-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0987f-132">Remarks</span></span>

<span data-ttu-id="0987f-133">Das **certificatepolicies** -Objekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0987f-133">The **CertificatePolicies** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="0987f-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0987f-134">Requirements</span></span>



| <span data-ttu-id="0987f-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0987f-135">Requirement</span></span> | <span data-ttu-id="0987f-136">Wert</span><span class="sxs-lookup"><span data-stu-id="0987f-136">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0987f-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0987f-137">End of client support</span></span><br/> | <span data-ttu-id="0987f-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0987f-138">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0987f-139">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="0987f-139">End of server support</span></span><br/> | <span data-ttu-id="0987f-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0987f-140">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0987f-141">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="0987f-141">Redistributable</span></span><br/>       | <span data-ttu-id="0987f-142">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="0987f-142">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0987f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="0987f-143">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0987f-144"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0987f-144"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
