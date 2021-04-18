---
description: Das PublicKey-Objekt stellt einen öffentlichen Schlüssel in einem Zertifikat Objekt dar.
title: PublicKey-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 12ab8fcf61d30b47fc809fb05e1ffa524bb2488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352149"
---
# <a name="publickey-object"></a><span data-ttu-id="27109-103">PublicKey-Objekt</span><span class="sxs-lookup"><span data-stu-id="27109-103">PublicKey object</span></span>

<span data-ttu-id="27109-104">\[Das **PublicKey** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="27109-104">\[The **PublicKey** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="27109-105">Verwenden Sie stattdessen die [**X509Certificate2. PublicKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="27109-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="27109-106">Das **PublicKey** -Objekt stellt einen öffentlichen Schlüssel in einem [**Zertifikat**](certificate.md) Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="27109-106">The **PublicKey** object represents a public key in a [**Certificate**](certificate.md) object.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="27109-107">Verwendung</span><span class="sxs-lookup"><span data-stu-id="27109-107">When to use</span></span>

<span data-ttu-id="27109-108">Das **PublicKey** -Objekt wird verwendet, um Daten zum öffentlichen Schlüssel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="27109-108">The **PublicKey** object is used to retrieve data about the public key.</span></span>

## <a name="members"></a><span data-ttu-id="27109-109">Member</span><span class="sxs-lookup"><span data-stu-id="27109-109">Members</span></span>

<span data-ttu-id="27109-110">Das **PublicKey** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="27109-110">The **PublicKey** object has these types of members:</span></span>

-   [<span data-ttu-id="27109-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27109-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="27109-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27109-112">Properties</span></span>

<span data-ttu-id="27109-113">Das **PublicKey** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="27109-113">The **PublicKey** object has these properties.</span></span>



| <span data-ttu-id="27109-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="27109-114">Property</span></span>                                                            | <span data-ttu-id="27109-115">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="27109-115">Access type</span></span>          | <span data-ttu-id="27109-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27109-116">Description</span></span>                                                                                                                            |
|:--------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27109-117">**Algorithmus**</span><span class="sxs-lookup"><span data-stu-id="27109-117">**Algorithm**</span></span>](publickey-algorithm.md)<br/>                 | <span data-ttu-id="27109-118">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27109-118">Read-only</span></span><br/> | <span data-ttu-id="27109-119">Ruft das [**OID**](oid.md) -Objekt ab, das den vom öffentlichen Schlüssel verwendeten Algorithmus identifiziert.</span><span class="sxs-lookup"><span data-stu-id="27109-119">Retrieves the [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span> <span data-ttu-id="27109-120">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="27109-120">This is the default property.</span></span><br/> |
| [<span data-ttu-id="27109-121">**Encodkey**</span><span class="sxs-lookup"><span data-stu-id="27109-121">**EncodedKey**</span></span>](publickey-encodedkey.md)<br/>               | <span data-ttu-id="27109-122">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27109-122">Read-only</span></span><br/> | <span data-ttu-id="27109-123">Ruft ein [**encoddata**](encodeddata.md) -Objekt ab, das Zugriff auf den Wert des öffentlichen Schlüssels bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="27109-123">Retrieves an [**EncodedData**](encodeddata.md) object that provides access to the value of the public key.</span></span><br/>                 |
| [<span data-ttu-id="27109-124">**EncodedParameters**</span><span class="sxs-lookup"><span data-stu-id="27109-124">**EncodedParameters**</span></span>](publickey-encodedparameters.md)<br/> | <span data-ttu-id="27109-125">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27109-125">Read-only</span></span><br/> | <span data-ttu-id="27109-126">Ruft ein [**encodeddata**](encodeddata.md) -Objekt ab, das Zugriff auf die Parameter des Algorithmus des öffentlichen Schlüssels bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="27109-126">Retrieves an [**EncodedData**](encodeddata.md) object that provides access to the parameters of the public key algorithm.</span></span><br/>  |
| [<span data-ttu-id="27109-127">**Länge**</span><span class="sxs-lookup"><span data-stu-id="27109-127">**Length**</span></span>](publickey-length.md)<br/>                       | <span data-ttu-id="27109-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27109-128">Read-only</span></span><br/> | <span data-ttu-id="27109-129">Ruft die Länge des öffentlichen Schlüssels in Bits ab.</span><span class="sxs-lookup"><span data-stu-id="27109-129">Retrieves the length of the public key in bits.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="27109-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27109-130">Remarks</span></span>

<span data-ttu-id="27109-131">Das **PublicKey** -Objekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="27109-131">The **PublicKey** object cannot be created.</span></span>

<span data-ttu-id="27109-132">Das **PublicKey** -Objekt wird von der [**Certificate. PublicKey**](certificate-publickey.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="27109-132">The **PublicKey** object is used by the [**Certificate.PublicKey**](certificate-publickey.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="27109-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27109-133">Requirements</span></span>



| <span data-ttu-id="27109-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27109-134">Requirement</span></span> | <span data-ttu-id="27109-135">Wert</span><span class="sxs-lookup"><span data-stu-id="27109-135">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27109-136">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="27109-136">Redistributable</span></span><br/> | <span data-ttu-id="27109-137">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="27109-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="27109-138">DLL</span><span class="sxs-lookup"><span data-stu-id="27109-138">DLL</span></span><br/>             | <dl> <span data-ttu-id="27109-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27109-139"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
