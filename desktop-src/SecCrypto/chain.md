---
description: Stellt eine Zertifikats Vertrauenskette dar.
ms.assetid: 45ed686f-4a7f-4df9-8366-98b825c3c657
title: Chain-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5fa3432767ccfdb60a2e3bc0a50ddbbcf565e0aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373712"
---
# <a name="chain-object"></a><span data-ttu-id="7fead-103">Chain-Objekt</span><span class="sxs-lookup"><span data-stu-id="7fead-103">Chain object</span></span>

<span data-ttu-id="7fead-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7fead-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7fead-105">Verwenden Sie stattdessen die [**X509Chain-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="7fead-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7fead-106">Das **Chain** -Objekt stellt eine Zertifikats Vertrauenskette dar.</span><span class="sxs-lookup"><span data-stu-id="7fead-106">The **Chain** object represents a certificate trust chain.</span></span>

<span data-ttu-id="7fead-107">Dieses Objekt stellt Eigenschaften und Methoden zum Erstellen einer Zertifikats Vertrauenskette zum Überprüfen der Gültigkeit von Zertifikaten bereit.</span><span class="sxs-lookup"><span data-stu-id="7fead-107">This object provides properties and methods to build a certificate trust chain to check the validity of certificates.</span></span> <span data-ttu-id="7fead-108">Die Kette wird mit dem Eigenschafts Wert [**CertificateStatus. checkflag**](certificatestatus-checkflag.md) und den Richtlinien Einstellungen eines [**CertificateStatus**](certificatestatus.md) -Objekts erstellt.</span><span class="sxs-lookup"><span data-stu-id="7fead-108">The chain is built using the [**CertificateStatus.CheckFlag**](certificatestatus-checkflag.md) property value and the policy settings of a [**CertificateStatus**](certificatestatus.md) object.</span></span>

<span data-ttu-id="7fead-109">Das **Chain** -Objekt macht die folgenden Schnittstellen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="7fead-109">The **Chain** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="7fead-110">**IChain2**: wurde in CAPICOM 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7fead-110">**IChain2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="7fead-111">**IChain**: wurde in CAPICOM 1,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7fead-111">**IChain**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="7fead-112">Verwendung</span><span class="sxs-lookup"><span data-stu-id="7fead-112">When to use</span></span>

<span data-ttu-id="7fead-113">Das **Chain** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="7fead-113">The **Chain** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="7fead-114">Erstellen Sie eine Zertifikat Vertrauenskette.</span><span class="sxs-lookup"><span data-stu-id="7fead-114">Build a certificate trust chain.</span></span>
-   <span data-ttu-id="7fead-115">Abrufen der OIDs aller Zertifikat-und Anwendungsrichtlinien, die für die Kette gültig sind.</span><span class="sxs-lookup"><span data-stu-id="7fead-115">Obtain the OIDs of all the certificate and application policies valid for the chain.</span></span>
-   <span data-ttu-id="7fead-116">Überprüfen Sie den Status der Zertifikate in der Kette.</span><span class="sxs-lookup"><span data-stu-id="7fead-116">Verify the status of the certificates in the chain.</span></span>
-   <span data-ttu-id="7fead-117">Abrufen erweiterter Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="7fead-117">Obtain extended error information.</span></span>
-   <span data-ttu-id="7fead-118">Ruft die Auflistung der Zertifikate in der Kette ab.</span><span class="sxs-lookup"><span data-stu-id="7fead-118">Retrieve the collection of certificates in the chain.</span></span>

## <a name="members"></a><span data-ttu-id="7fead-119">Member</span><span class="sxs-lookup"><span data-stu-id="7fead-119">Members</span></span>

<span data-ttu-id="7fead-120">Das **Chain** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7fead-120">The **Chain** object has these types of members:</span></span>

-   [<span data-ttu-id="7fead-121">Methoden</span><span class="sxs-lookup"><span data-stu-id="7fead-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="7fead-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7fead-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7fead-123">Methoden</span><span class="sxs-lookup"><span data-stu-id="7fead-123">Methods</span></span>

<span data-ttu-id="7fead-124">Das **Chain** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7fead-124">The **Chain** object has these methods.</span></span>



| <span data-ttu-id="7fead-125">Methode</span><span class="sxs-lookup"><span data-stu-id="7fead-125">Method</span></span>                                                   | <span data-ttu-id="7fead-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7fead-126">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fead-127">**Applicationpolicies**</span><span class="sxs-lookup"><span data-stu-id="7fead-127">**ApplicationPolicies**</span></span>](chain-applicationpolicies.md) | <span data-ttu-id="7fead-128">Gibt eine [**OIDs**](oids.md) -Auflistung zurück, die die Anwendungs Richtlinie für die Kette darstellt.</span><span class="sxs-lookup"><span data-stu-id="7fead-128">Returns an [**OIDs**](oids.md) collection that represents the application policy OIDs valid for the chain.</span></span><br/> <span data-ttu-id="7fead-129">(Geerbt von **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="7fead-129">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                          |
| [<span data-ttu-id="7fead-130">**Entwickeln**</span><span class="sxs-lookup"><span data-stu-id="7fead-130">**Build**</span></span>](chain-build.md)                             | <span data-ttu-id="7fead-131">Erstellt eine Zertifikat Überprüfungs Kette von einem Endzertifikat zum vertrauenswürdigen Stamm [*Zertifikat*](../secgloss/r-gly.md)und gibt einen booleschen Wert zurück, der die Gesamt Gültigkeit der Kette angibt.</span><span class="sxs-lookup"><span data-stu-id="7fead-131">Builds a certificate verification chain from an end certificate to the trusted [*root certificate*](../secgloss/r-gly.md), returning a Boolean value that indicates the overall validity of the chain.</span></span><br/> <span data-ttu-id="7fead-132">(Geerbt von **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="7fead-132">(Inherited from **ChainIChain2IChain**)</span></span> |
| [<span data-ttu-id="7fead-133">**Certificatepolicies**</span><span class="sxs-lookup"><span data-stu-id="7fead-133">**CertificatePolicies**</span></span>](chain-certificatepolicies.md) | <span data-ttu-id="7fead-134">Gibt eine [**OIDs**](oids.md) -Auflistung zurück, die die für die Kette gültigen Zertifikat Richtlinie-OIDs darstellt.</span><span class="sxs-lookup"><span data-stu-id="7fead-134">Returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs valid for the chain.</span></span><br/> <span data-ttu-id="7fead-135">(Geerbt von **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="7fead-135">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                          |
| [<span data-ttu-id="7fead-136">**ExtendedErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="7fead-136">**ExtendedErrorInfo**</span></span>](chain-extendederrorinfo.md)     | <span data-ttu-id="7fead-137">Gibt eine Zeichenfolge zurück, die zusätzliche Fehlerinformationen zum indizierten Eintrag enthält.</span><span class="sxs-lookup"><span data-stu-id="7fead-137">Returns a string that contains additional error information about the indexed entry.</span></span><br/> <span data-ttu-id="7fead-138">(Geerbt von **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="7fead-138">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="7fead-139">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7fead-139">Properties</span></span>

<span data-ttu-id="7fead-140">Das **Chain** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7fead-140">The **Chain** object has these properties.</span></span>



| <span data-ttu-id="7fead-141">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fead-141">Property</span></span>                                              | <span data-ttu-id="7fead-142">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="7fead-142">Access type</span></span>          | <span data-ttu-id="7fead-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7fead-143">Description</span></span>                                                                                                                                                                                 |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fead-144">**Zertifikate**</span><span class="sxs-lookup"><span data-stu-id="7fead-144">**Certificates**</span></span>](chain-certificates.md)<br/> | <span data-ttu-id="7fead-145">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fead-145">Read-only</span></span><br/> | <span data-ttu-id="7fead-146">Ruft eine [**Zertifikat**](certificates.md) Sammlung ab, die die Zertifikate in der Kette darstellt.</span><span class="sxs-lookup"><span data-stu-id="7fead-146">Retrieves a [**Certificates**](certificates.md) collection that represents the certificates in the chain.</span></span> <span data-ttu-id="7fead-147">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7fead-147">This is the default property.</span></span><br/> <span data-ttu-id="7fead-148">(Geerbt von **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="7fead-148">(Inherited from **ChainIChain2IChain**)</span></span> |
| [<span data-ttu-id="7fead-149">**Status**</span><span class="sxs-lookup"><span data-stu-id="7fead-149">**Status**</span></span>](chain-status.md)<br/>             | <span data-ttu-id="7fead-150">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fead-150">Read-only</span></span><br/> | <span data-ttu-id="7fead-151">Ruft den Gültigkeits Status der Kette oder eines bestimmten Zertifikats in der Kette ab.</span><span class="sxs-lookup"><span data-stu-id="7fead-151">Retrieves the validity status of the chain or a specific certificate in the chain.</span></span><br/> <span data-ttu-id="7fead-152">(Geerbt von **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="7fead-152">(Inherited from **ChainIChain2IChain**)</span></span>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="7fead-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7fead-153">Remarks</span></span>

<span data-ttu-id="7fead-154">Das **Ketten** Objekt kann erstellt werden und ist für die Skripterstellung sicher.</span><span class="sxs-lookup"><span data-stu-id="7fead-154">The **Chain** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="7fead-155">Die ProgID für das **Ketten** Objekt ist "CAPICOM". Kette. 2 ".</span><span class="sxs-lookup"><span data-stu-id="7fead-155">The ProgID for the **Chain** object is "CAPICOM.Chain.2".</span></span>

<span data-ttu-id="7fead-156">**CAPICOM 1. *x*:** die ProgID für das **Ketten** Objekt ist CAPICOM. Kette. 1.</span><span class="sxs-lookup"><span data-stu-id="7fead-156">**CAPICOM 1.*x*:** The ProgID for the **Chain** object is CAPICOM.Chain.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fead-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fead-157">Requirements</span></span>



| <span data-ttu-id="7fead-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7fead-158">Requirement</span></span> | <span data-ttu-id="7fead-159">Wert</span><span class="sxs-lookup"><span data-stu-id="7fead-159">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fead-160">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7fead-160">End of client support</span></span><br/> | <span data-ttu-id="7fead-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7fead-161">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7fead-162">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="7fead-162">End of server support</span></span><br/> | <span data-ttu-id="7fead-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fead-163">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7fead-164">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="7fead-164">Redistributable</span></span><br/>       | <span data-ttu-id="7fead-165">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="7fead-165">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7fead-166">DLL</span><span class="sxs-lookup"><span data-stu-id="7fead-166">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7fead-167"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fead-167"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fead-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fead-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fead-169">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="7fead-169">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
