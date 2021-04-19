---
description: Richtet den Signatur Geber eines SignedData-oder signedcode-Objekts ein.
ms.assetid: fca6489c-56cf-472f-ac0f-73ba531fa212
title: Signatur Geber Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 974341eb996f2b5d3701757a5352ef56e2837390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372696"
---
# <a name="signer-object"></a><span data-ttu-id="81dbd-103">Signatur Geber Objekt</span><span class="sxs-lookup"><span data-stu-id="81dbd-103">Signer object</span></span>

<span data-ttu-id="81dbd-104">\[Das **Signatur** Geber Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="81dbd-104">\[The **Signer** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="81dbd-105">Verwenden Sie stattdessen die [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="81dbd-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="81dbd-106">Das **Signatur** Geber Objekt richtet den Signatur Geber eines [**SignedData**](signeddata.md) -oder [**signedcode**](signedcode.md) -Objekts ein.</span><span class="sxs-lookup"><span data-stu-id="81dbd-106">The **Signer** object establishes the signer of a [**SignedData**](signeddata.md) or [**SignedCode**](signedcode.md) object.</span></span> <span data-ttu-id="81dbd-107">Das [**Zertifikat**](certificate.md) des **Signatur** Geber Objekts muss über einen verfügbaren privaten Schlüssel verfügen, der zum Signieren von Daten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="81dbd-107">The [**Certificate**](certificate.md) of the **Signer** object must have an available private key that can be used to sign data.</span></span>

## <a name="members"></a><span data-ttu-id="81dbd-108">Member</span><span class="sxs-lookup"><span data-stu-id="81dbd-108">Members</span></span>

<span data-ttu-id="81dbd-109">Das **Signatur** Geber Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="81dbd-109">The **Signer** object has these types of members:</span></span>

-   [<span data-ttu-id="81dbd-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="81dbd-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="81dbd-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81dbd-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="81dbd-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="81dbd-112">Methods</span></span>

<span data-ttu-id="81dbd-113">Das **Signatur** Geber Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="81dbd-113">The **Signer** object has these methods.</span></span>



| <span data-ttu-id="81dbd-114">Methode</span><span class="sxs-lookup"><span data-stu-id="81dbd-114">Method</span></span>                      | <span data-ttu-id="81dbd-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81dbd-115">Description</span></span>                                                       |
|:----------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="81dbd-116">**Laden**</span><span class="sxs-lookup"><span data-stu-id="81dbd-116">**Load**</span></span>](signer-load.md) | <span data-ttu-id="81dbd-117">Lädt ein Signaturzertifikat aus einer angegebenen PFX-Datei.</span><span class="sxs-lookup"><span data-stu-id="81dbd-117">Loads a signing certificate from a specified PFX file.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="81dbd-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81dbd-118">Properties</span></span>

<span data-ttu-id="81dbd-119">Das **Signatur** Geber Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="81dbd-119">The **Signer** object has these properties.</span></span>



| <span data-ttu-id="81dbd-120">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="81dbd-120">Property</span></span>                                                                     | <span data-ttu-id="81dbd-121">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="81dbd-121">Access type</span></span>           | <span data-ttu-id="81dbd-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81dbd-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81dbd-123">**Authenticatedattributes**</span><span class="sxs-lookup"><span data-stu-id="81dbd-123">**AuthenticatedAttributes**</span></span>](signer-authenticatedattributes.md)<br/> | <span data-ttu-id="81dbd-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81dbd-124">Read-only</span></span><br/>  | <span data-ttu-id="81dbd-125">Die Auflistung von authentifizierten Attributen.</span><span class="sxs-lookup"><span data-stu-id="81dbd-125">The collection of authenticated attributes.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="81dbd-126">**Stellt**</span><span class="sxs-lookup"><span data-stu-id="81dbd-126">**Certificate**</span></span>](signer-certificate.md)<br/>                         | <span data-ttu-id="81dbd-127">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="81dbd-127">Read/write</span></span><br/> | <span data-ttu-id="81dbd-128">Das [**Zertifikat**](certificate.md) Objekt, das das Zertifikat eines Signatur Gebers der Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="81dbd-128">The [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span><br/> <span data-ttu-id="81dbd-129">Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Status*](../secgloss/s-gly.md) des Objekts zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="81dbd-129">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span><br/> <span data-ttu-id="81dbd-130">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="81dbd-130">This is the default property.</span></span><br/> |
| [<span data-ttu-id="81dbd-131">**Ketten**</span><span class="sxs-lookup"><span data-stu-id="81dbd-131">**Chain**</span></span>](signer-chain.md)<br/>                                     | <span data-ttu-id="81dbd-132">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81dbd-132">Read-only</span></span><br/>  | <span data-ttu-id="81dbd-133">Die Kette des Signatur Gebers.</span><span class="sxs-lookup"><span data-stu-id="81dbd-133">The chain of the signer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="81dbd-134">**Optionen**</span><span class="sxs-lookup"><span data-stu-id="81dbd-134">**Options**</span></span>](signer-options.md)<br/>                                 | <span data-ttu-id="81dbd-135">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="81dbd-135">Read/write</span></span><br/> | <span data-ttu-id="81dbd-136">Legt die Zertifikat Option des Signatur Gebers fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="81dbd-136">Sets or retrieves the signer's certificate option.</span></span><br/>                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="81dbd-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81dbd-137">Remarks</span></span>

<span data-ttu-id="81dbd-138">Das **Signatur** Geber Objekt kann erstellt werden und ist für die Skripterstellung sicher.</span><span class="sxs-lookup"><span data-stu-id="81dbd-138">The **Signer** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="81dbd-139">Die ProgID für das **Signatur** Geber Objekt ist CAPICOM. Signatur Geber. 2.</span><span class="sxs-lookup"><span data-stu-id="81dbd-139">The ProgID for the **Signer** object is CAPICOM.Signer.2.</span></span>

<span data-ttu-id="81dbd-140">**CAPICOM 1. *x*:** die ProgID für das **Signatur** Geber Objekt ist CAPICOM. Signer. 1.</span><span class="sxs-lookup"><span data-stu-id="81dbd-140">**CAPICOM 1.*x*:** The ProgID for the **Signer** object is CAPICOM.Signer.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="81dbd-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81dbd-141">Requirements</span></span>



| <span data-ttu-id="81dbd-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81dbd-142">Requirement</span></span> | <span data-ttu-id="81dbd-143">Wert</span><span class="sxs-lookup"><span data-stu-id="81dbd-143">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81dbd-144">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="81dbd-144">Redistributable</span></span><br/> | <span data-ttu-id="81dbd-145">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="81dbd-145">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="81dbd-146">DLL</span><span class="sxs-lookup"><span data-stu-id="81dbd-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="81dbd-147"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81dbd-147"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81dbd-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81dbd-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81dbd-149">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="81dbd-149">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
