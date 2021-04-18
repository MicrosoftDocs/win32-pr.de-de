---
description: Bietet Zugriff auf die Richtlinien Informationen einer Erweiterung.
ms.assetid: 03d627b3-2d44-4637-97a4-85cdcaf3e4d3
title: Policyinformation-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d0cc89d6f993b72763083e69bb88e848134e8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364801"
---
# <a name="policyinformation-object"></a><span data-ttu-id="14109-103">Policyinformation-Objekt</span><span class="sxs-lookup"><span data-stu-id="14109-103">PolicyInformation object</span></span>

<span data-ttu-id="14109-104">\[Das **policyinformation** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="14109-104">\[The **PolicyInformation** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="14109-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung zu verarbeiten.\]</span><span class="sxs-lookup"><span data-stu-id="14109-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="14109-106">Das **policyinformation** -Objekt ermöglicht den Zugriff auf die Richtlinien Informationen einer Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="14109-106">The **PolicyInformation** object provides access to the policy information of an extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="14109-107">Verwendung</span><span class="sxs-lookup"><span data-stu-id="14109-107">When to use</span></span>

<span data-ttu-id="14109-108">Das **policyinformation** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="14109-108">The **PolicyInformation** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="14109-109">Rufen Sie die Richtlinie OID ab.</span><span class="sxs-lookup"><span data-stu-id="14109-109">Retrieve the policy OID.</span></span>
-   <span data-ttu-id="14109-110">Ruft eine Auflistung der Qualifizierer der Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="14109-110">Retrieve a collection of the policy's qualifiers.</span></span>

## <a name="members"></a><span data-ttu-id="14109-111">Member</span><span class="sxs-lookup"><span data-stu-id="14109-111">Members</span></span>

<span data-ttu-id="14109-112">Das **policyinformation** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="14109-112">The **PolicyInformation** object has these types of members:</span></span>

-   [<span data-ttu-id="14109-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14109-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14109-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14109-114">Properties</span></span>

<span data-ttu-id="14109-115">Das **policyinformation** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="14109-115">The **PolicyInformation** object has these properties.</span></span>



| <span data-ttu-id="14109-116">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="14109-116">Property</span></span>                                                      | <span data-ttu-id="14109-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14109-117">Description</span></span>                                                                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14109-118">**OID**</span><span class="sxs-lookup"><span data-stu-id="14109-118">**OID**</span></span>](policyinformation-oid.md)<br/>               | <span data-ttu-id="14109-119">Ruft die OID der Richtlinie als [**OID**](oid.md) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="14109-119">Retrieves the policy's OID, as an [**OID**](oid.md) object.</span></span> <span data-ttu-id="14109-120">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="14109-120">This is the default property.</span></span><br/>       |
| [<span data-ttu-id="14109-121">**Qualifikation**</span><span class="sxs-lookup"><span data-stu-id="14109-121">**Qualifiers**</span></span>](policyinformation-qualifiers.md)<br/> | <span data-ttu-id="14109-122">Ruft eine Auflistung der Qualifizierer der Richtlinie als [**qualifiziererobjekt**](qualifiers.md) ab.</span><span class="sxs-lookup"><span data-stu-id="14109-122">Retrieves a collection of the policy's qualifiers, as a [**Qualifiers**](qualifiers.md) object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="14109-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14109-123">Remarks</span></span>

<span data-ttu-id="14109-124">Das **policyinformation** -Objekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="14109-124">The **PolicyInformation** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="14109-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14109-125">Requirements</span></span>



| <span data-ttu-id="14109-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14109-126">Requirement</span></span> | <span data-ttu-id="14109-127">Wert</span><span class="sxs-lookup"><span data-stu-id="14109-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14109-128">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="14109-128">Redistributable</span></span><br/> | <span data-ttu-id="14109-129">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="14109-129">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="14109-130">DLL</span><span class="sxs-lookup"><span data-stu-id="14109-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="14109-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14109-131"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
