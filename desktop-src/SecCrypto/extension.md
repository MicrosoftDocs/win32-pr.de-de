---
description: Stellt eine einzelne Zertifikat Erweiterung dar.
ms.assetid: cca3121d-0f0f-4de2-a225-6dd3910078d7
title: Erweiterungs Objekt (mmcobj. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a048cd5f29825c2d96a9d924473159e93d3e0be1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369627"
---
# <a name="extension-object"></a><span data-ttu-id="4ae26-103">Erweiterungs Objekt</span><span class="sxs-lookup"><span data-stu-id="4ae26-103">Extension object</span></span>

<span data-ttu-id="4ae26-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4ae26-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4ae26-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="4ae26-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4ae26-106">Das **Erweiterungs** Objekt stellt eine einzelne Zertifikat Erweiterung dar.</span><span class="sxs-lookup"><span data-stu-id="4ae26-106">The **Extension** object represents a single certificate extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="4ae26-107">Verwendung</span><span class="sxs-lookup"><span data-stu-id="4ae26-107">When to use</span></span>

<span data-ttu-id="4ae26-108">Das **Erweiterungs** Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="4ae26-108">The **Extension** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="4ae26-109">Rufen Sie die OID der Zertifikat Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="4ae26-109">Retrieve the OID of the certificate extension.</span></span>
-   <span data-ttu-id="4ae26-110">Abrufen der von einem [**encodeddata**](encodeddata.md) -Objekt dargestellten Zertifikat Erweiterungs Daten.</span><span class="sxs-lookup"><span data-stu-id="4ae26-110">Retrieve the certificate extension data represented by an [**EncodedData**](encodeddata.md) object.</span></span>
-   <span data-ttu-id="4ae26-111">Bestimmen Sie, ob die Zertifikat Erweiterung als kritisch markiert ist.</span><span class="sxs-lookup"><span data-stu-id="4ae26-111">Determine whether the certificate extension is marked as critical.</span></span>

## <a name="members"></a><span data-ttu-id="4ae26-112">Member</span><span class="sxs-lookup"><span data-stu-id="4ae26-112">Members</span></span>

<span data-ttu-id="4ae26-113">Das **Erweiterungs** Objekt enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4ae26-113">The **Extension** object has these types of members:</span></span>

-   [<span data-ttu-id="4ae26-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ae26-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ae26-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ae26-115">Properties</span></span>

<span data-ttu-id="4ae26-116">Das **Erweiterungs** Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4ae26-116">The **Extension** object has these properties.</span></span>



| <span data-ttu-id="4ae26-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4ae26-117">Property</span></span>                                                | <span data-ttu-id="4ae26-118">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="4ae26-118">Access type</span></span>          | <span data-ttu-id="4ae26-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ae26-119">Description</span></span>                                                                                   |
|:--------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ae26-120">**Encoddata**</span><span class="sxs-lookup"><span data-stu-id="4ae26-120">**EncodedData**</span></span>](extension-encodeddata.md)<br/> | <span data-ttu-id="4ae26-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ae26-121">Read-only</span></span><br/> | <span data-ttu-id="4ae26-122">Ruft die codierten Daten für die Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="4ae26-122">Retrieves the encoded data for the extension.</span></span><br/>                                      |
| [<span data-ttu-id="4ae26-123">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="4ae26-123">**IsCritical**</span></span>](extension-iscritical.md)<br/>   | <span data-ttu-id="4ae26-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ae26-124">Read-only</span></span><br/> | <span data-ttu-id="4ae26-125">Ruft einen booleschen Wert ab, der angibt, ob die Erweiterung als kritisch markiert ist.</span><span class="sxs-lookup"><span data-stu-id="4ae26-125">Retrieves a Boolean value that indicates whether the extension is marked critical.</span></span><br/> |
| [<span data-ttu-id="4ae26-126">**OID**</span><span class="sxs-lookup"><span data-stu-id="4ae26-126">**OID**</span></span>](extension-oid.md)<br/>                 | <span data-ttu-id="4ae26-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ae26-127">Read-only</span></span><br/> | <span data-ttu-id="4ae26-128">Ruft den Objekt Bezeichner für die Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="4ae26-128">Retrieves the object identifier for the extension.</span></span> <span data-ttu-id="4ae26-129">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4ae26-129">This is the default property.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="4ae26-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ae26-130">Remarks</span></span>

<span data-ttu-id="4ae26-131">Das **Erweiterungs** Objekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4ae26-131">The **Extension** object cannot be created.</span></span>

<span data-ttu-id="4ae26-132">Das **Erweiterungs** Objekt wird vom Erweiterungs Objekt für [**Erweiterungen**](extensions.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ae26-132">The **Extension** object is used by the [**Extensions**](extensions.md) collection object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ae26-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ae26-133">Requirements</span></span>



| <span data-ttu-id="4ae26-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ae26-134">Requirement</span></span> | <span data-ttu-id="4ae26-135">Wert</span><span class="sxs-lookup"><span data-stu-id="4ae26-135">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae26-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4ae26-136">End of client support</span></span><br/> | <span data-ttu-id="4ae26-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ae26-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4ae26-138">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="4ae26-138">End of server support</span></span><br/> | <span data-ttu-id="4ae26-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ae26-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4ae26-140">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="4ae26-140">Redistributable</span></span><br/>       | <span data-ttu-id="4ae26-141">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="4ae26-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4ae26-142">Header</span><span class="sxs-lookup"><span data-stu-id="4ae26-142">Header</span></span><br/>                | <dl> <span data-ttu-id="4ae26-143"><dt>Mmcobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ae26-143"><dt>Mmcobj.h</dt></span></span> </dl>    |
| <span data-ttu-id="4ae26-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4ae26-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4ae26-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ae26-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
