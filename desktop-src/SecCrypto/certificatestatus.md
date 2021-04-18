---
description: Enthält Informationen zum Erstellen einer Zertifikats Vertrauenskette.
ms.assetid: 120cd79e-7c9b-45f3-8596-091b674e73d8
title: CertificateStatus-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e9a6cb31a00f4d2943e68670930e6cbc4436b6b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371044"
---
# <a name="certificatestatus-object"></a><span data-ttu-id="41d7d-103">CertificateStatus-Objekt</span><span class="sxs-lookup"><span data-stu-id="41d7d-103">CertificateStatus object</span></span>

<span data-ttu-id="41d7d-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="41d7d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="41d7d-105">Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="41d7d-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="41d7d-106">Das **CertificateStatus** -Objekt enthält Informationen zum Erstellen einer Zertifikats Vertrauenskette.</span><span class="sxs-lookup"><span data-stu-id="41d7d-106">The **CertificateStatus** object contains information about how to construct a certificate trust chain.</span></span>

## <a name="members"></a><span data-ttu-id="41d7d-107">Member</span><span class="sxs-lookup"><span data-stu-id="41d7d-107">Members</span></span>

<span data-ttu-id="41d7d-108">Das **CertificateStatus** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="41d7d-108">The **CertificateStatus** object has these types of members:</span></span>

-   [<span data-ttu-id="41d7d-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="41d7d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="41d7d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41d7d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="41d7d-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="41d7d-111">Methods</span></span>

<span data-ttu-id="41d7d-112">Das **CertificateStatus** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="41d7d-112">The **CertificateStatus** object has these methods.</span></span>



| <span data-ttu-id="41d7d-113">Methode</span><span class="sxs-lookup"><span data-stu-id="41d7d-113">Method</span></span>                                                               | <span data-ttu-id="41d7d-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41d7d-114">Description</span></span>                                                                                                                                  |
|:---------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41d7d-115">**Applicationpolicies**</span><span class="sxs-lookup"><span data-stu-id="41d7d-115">**ApplicationPolicies**</span></span>](certificatestatus-applicationpolicies.md) | <span data-ttu-id="41d7d-116">Gibt eine [**OIDs**](oids.md) -Auflistung zurück, die die OIDs der Anwendungs Richtlinie darstellt.</span><span class="sxs-lookup"><span data-stu-id="41d7d-116">Returns an [**OIDs**](oids.md) collection that represents the application policy OIDs.</span></span><br/>                                           |
| [<span data-ttu-id="41d7d-117">**Certificatepolicies**</span><span class="sxs-lookup"><span data-stu-id="41d7d-117">**CertificatePolicies**</span></span>](certificatestatus-certificatepolicies.md) | <span data-ttu-id="41d7d-118">Gibt eine [**OIDs**](oids.md) -Auflistung zurück, die die während der Ketten Bildung verwendeten Zertifikat Richtlinien-OIDs darstellt.</span><span class="sxs-lookup"><span data-stu-id="41d7d-118">Returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs used during chain building.</span></span><br/>                |
| [<span data-ttu-id="41d7d-119">**EKU**</span><span class="sxs-lookup"><span data-stu-id="41d7d-119">**EKU**</span></span>](certificatestatus-eku.md)                                 | <span data-ttu-id="41d7d-120">Gibt das [**EKU**](eku.md) -Objekt zurück, mit dem die EKU-Elemente festgelegt werden, die beim Einrichten des Gültigkeits Status eines Zertifikats überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="41d7d-120">Returns the [**EKU**](eku.md) object used to set the EKU elements to be checked in establishing a certificate's validity status.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="41d7d-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41d7d-121">Properties</span></span>

<span data-ttu-id="41d7d-122">Das **CertificateStatus** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="41d7d-122">The **CertificateStatus** object has these properties.</span></span>



| <span data-ttu-id="41d7d-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="41d7d-123">Property</span></span>                                                                        | <span data-ttu-id="41d7d-124">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="41d7d-124">Access type</span></span>           | <span data-ttu-id="41d7d-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41d7d-125">Description</span></span>                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41d7d-126">**Zertifikate**</span><span class="sxs-lookup"><span data-stu-id="41d7d-126">**Certificates**</span></span>](certificatestatus-certificates.md)<br/>               | <span data-ttu-id="41d7d-127">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41d7d-127">Read/write</span></span><br/> | <span data-ttu-id="41d7d-128">Legt die Auflistung der Zertifikate fest, die zum Erstellen der Zertifikat Kette verwendet werden können, oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="41d7d-128">Sets or retrieves the collection of certificates that can be used to build the certificate chain.</span></span><br/> <span data-ttu-id="41d7d-129">**CAPICOM 2.0.0.3 und früher:** Die Eigenschaft [**Zertifikate**](certificatestatus-certificates.md) wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="41d7d-129">**CAPICOM 2.0.0.3 and earlier:** The [**Certificates**](certificatestatus-certificates.md) property is not supported.</span></span><br/>                    |
| [<span data-ttu-id="41d7d-130">**Checkflag**</span><span class="sxs-lookup"><span data-stu-id="41d7d-130">**CheckFlag**</span></span>](certificatestatus-checkflag.md)<br/>                     | <span data-ttu-id="41d7d-131">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41d7d-131">Read/write</span></span><br/> | <span data-ttu-id="41d7d-132">Flag zum Überprüfen der Gültigkeit.</span><span class="sxs-lookup"><span data-stu-id="41d7d-132">Validity check flag.</span></span> <span data-ttu-id="41d7d-133">Werte können mithilfe eines logischen **or** -Operators verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="41d7d-133">Values can be joined by using a logical **OR** operator.</span></span> <span data-ttu-id="41d7d-134">Das Standardflag für die Überprüfung lautet [**CAPICOM \_ \_ Online \_ alle überprüfen**](capicom-check-flag.md).</span><span class="sxs-lookup"><span data-stu-id="41d7d-134">The default check flag is [**CAPICOM\_CHECK\_ONLINE\_ALL**](capicom-check-flag.md).</span></span><br/>                                                                                     |
| [<span data-ttu-id="41d7d-135">**Dadurch**</span><span class="sxs-lookup"><span data-stu-id="41d7d-135">**Result**</span></span>](certificatestatus-result.md)<br/>                           | <span data-ttu-id="41d7d-136">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41d7d-136">Read-only</span></span><br/>  | <span data-ttu-id="41d7d-137">Gibt an, ob das Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="41d7d-137">Indicates whether the certificate is valid.</span></span> <span data-ttu-id="41d7d-138">Die Gültigkeit des Zertifikats wird mithilfe der aktuellen Einstellung der Eigenschaft [**checkflag**](certificatestatus-checkflag.md) und den Richtlinien Einstellungen des Zertifikats überprüft.</span><span class="sxs-lookup"><span data-stu-id="41d7d-138">The certificate's validity is checked using the current setting of the [**CheckFlag**](certificatestatus-checkflag.md) property and the policy settings of the certificate.</span></span> <span data-ttu-id="41d7d-139">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="41d7d-139">This is the default property.</span></span><br/> |
| [<span data-ttu-id="41d7d-140">**UrlRetrievalTimeout**</span><span class="sxs-lookup"><span data-stu-id="41d7d-140">**UrlRetrievalTimeout**</span></span>](certificatestatus-urlretrievaltimeout.md)<br/> | <span data-ttu-id="41d7d-141">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41d7d-141">Read/write</span></span><br/> | <span data-ttu-id="41d7d-142">Legt die Zeitspanne fest, nach der eine URL als nicht erreichbar festgelegt wird, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="41d7d-142">Sets or retrieves the length of time before a URL is determined to be unreachable.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="41d7d-143">**VerificationTime**</span><span class="sxs-lookup"><span data-stu-id="41d7d-143">**VerificationTime**</span></span>](certificatestatus-verificationtime.md)<br/>       | <span data-ttu-id="41d7d-144">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41d7d-144">Read/write</span></span><br/> | <span data-ttu-id="41d7d-145">Legt die Uhrzeit fest, zu der das Zertifikat überprüft wurde, oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="41d7d-145">Sets or retrieves the time that the certificate was verified.</span></span><br/>                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="41d7d-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41d7d-146">Remarks</span></span>

<span data-ttu-id="41d7d-147">Das **CertificateStatus** -Objekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="41d7d-147">The **CertificateStatus** object cannot be created.</span></span>

<span data-ttu-id="41d7d-148">Das **CertificateStatus** -Objekt wird von der [**Certificate. IsValid**](certificate-isvalid.md) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="41d7d-148">The **CertificateStatus** object is returned by the [**Certificate.IsValid**](certificate-isvalid.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="41d7d-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41d7d-149">Requirements</span></span>



| <span data-ttu-id="41d7d-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41d7d-150">Requirement</span></span> | <span data-ttu-id="41d7d-151">Wert</span><span class="sxs-lookup"><span data-stu-id="41d7d-151">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41d7d-152">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="41d7d-152">End of client support</span></span><br/> | <span data-ttu-id="41d7d-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41d7d-153">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="41d7d-154">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="41d7d-154">End of server support</span></span><br/> | <span data-ttu-id="41d7d-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41d7d-155">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="41d7d-156">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="41d7d-156">Redistributable</span></span><br/>       | <span data-ttu-id="41d7d-157">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="41d7d-157">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="41d7d-158">DLL</span><span class="sxs-lookup"><span data-stu-id="41d7d-158">DLL</span></span><br/>                   | <dl> <span data-ttu-id="41d7d-159"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41d7d-159"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41d7d-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41d7d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41d7d-161">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="41d7d-161">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="41d7d-162">**Ketten**</span><span class="sxs-lookup"><span data-stu-id="41d7d-162">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
