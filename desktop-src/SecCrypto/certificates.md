---
description: Stellt eine Auflistung von Zertifikat Objekten dar.
ms.assetid: 82011c49-38fb-4261-8fb3-b76859da8a9e
title: Zertifikate-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e8c12c16820342c5687720a35ce81aa7b94f180
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357303"
---
# <a name="certificates-object"></a><span data-ttu-id="5a0e3-103">Zertifikate-Objekt</span><span class="sxs-lookup"><span data-stu-id="5a0e3-103">Certificates object</span></span>

<span data-ttu-id="5a0e3-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="5a0e3-105">Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="5a0e3-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="5a0e3-106">Das **Zertifikate** -Objekt stellt eine Sammlung von [**Zertifikat**](certificate.md) Objekten dar.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-106">The **Certificates** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="5a0e3-107">Jedes [**Zertifikat**](certificate.md) Objekt stellt ein einzelnes [*digitales Zertifikat*](../secgloss/d-gly.md)dar.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-107">Each [**Certificate**](certificate.md) object represents a single [*digital certificate*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="5a0e3-108">Das **Zertifikate** -Objekt macht die folgenden Schnittstellen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="5a0e3-108">The **Certificates** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="5a0e3-109">**ICertificates2**: wurde in CAPICOM 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-109">**ICertificates2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="5a0e3-110">**Izertifikate**: eingeführt in CAPICOM 1,0.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-110">**ICertificates**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="5a0e3-111">Verwendung</span><span class="sxs-lookup"><span data-stu-id="5a0e3-111">When to use</span></span>

<span data-ttu-id="5a0e3-112">Das **Zertifikat** Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="5a0e3-112">The **Certificates** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="5a0e3-113">Fügen Sie ein [**Zertifikat**](certificate.md) Objekt zu oder aus der Auflistung hinzu, oder entfernen Sie es.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-113">Add or remove a [**Certificate**](certificate.md) object to or from the collection.</span></span>
-   <span data-ttu-id="5a0e3-114">Generieren Sie eine Teilmenge der Sammlung, indem Sie eine Gruppe von Zertifikaten suchen oder ein Dialogfeld zum Auswählen der Zertifikate anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-114">Generate a subset of the collection by finding a set of certificates or by displaying a dialog box to select the certificates.</span></span>
-   <span data-ttu-id="5a0e3-115">Löschen Sie alle [**Zertifikat**](certificate.md) Objekte aus der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-115">Clear all the [**Certificate**](certificate.md) objects from the collection.</span></span>
-   <span data-ttu-id="5a0e3-116">Ruft die Anzahl der Zertifikate in der Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-116">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="5a0e3-117">Rufen Sie ein bestimmtes [**Zertifikat**](certificate.md) Objekt aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-117">Retrieve a specific [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="5a0e3-118">Iterieren Sie die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-118">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="5a0e3-119">Member</span><span class="sxs-lookup"><span data-stu-id="5a0e3-119">Members</span></span>

<span data-ttu-id="5a0e3-120">Das Objekt " **Zertifikate** " verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5a0e3-120">The **Certificates** object has these types of members:</span></span>

-   [<span data-ttu-id="5a0e3-121">Methoden</span><span class="sxs-lookup"><span data-stu-id="5a0e3-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="5a0e3-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5a0e3-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5a0e3-123">Methoden</span><span class="sxs-lookup"><span data-stu-id="5a0e3-123">Methods</span></span>

<span data-ttu-id="5a0e3-124">Das **Zertifikate** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-124">The **Certificates** object has these methods.</span></span>



| <span data-ttu-id="5a0e3-125">Methode</span><span class="sxs-lookup"><span data-stu-id="5a0e3-125">Method</span></span>                                | <span data-ttu-id="5a0e3-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a0e3-126">Description</span></span>                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a0e3-127">**Eren**</span><span class="sxs-lookup"><span data-stu-id="5a0e3-127">**Add**</span></span>](certificates-add.md)       | <span data-ttu-id="5a0e3-128">Fügt der Auflistung ein [**Zertifikat**](certificate.md) Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-128">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/> <span data-ttu-id="5a0e3-129">(Geerbt von **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="5a0e3-129">(Inherited from **CertificatesICertificates2**)</span></span>                                        |
| [<span data-ttu-id="5a0e3-130">**Klartext**</span><span class="sxs-lookup"><span data-stu-id="5a0e3-130">**Clear**</span></span>](certificates-clear.md)   | <span data-ttu-id="5a0e3-131">Entfernt alle [**Zertifikat**](certificate.md) Objekte aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-131">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> <span data-ttu-id="5a0e3-132">(Geerbt von **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="5a0e3-132">(Inherited from **CertificatesICertificates2**)</span></span>                                |
| [<span data-ttu-id="5a0e3-133">**Sich**</span><span class="sxs-lookup"><span data-stu-id="5a0e3-133">**Find**</span></span>](certificates-find.md)     | <span data-ttu-id="5a0e3-134">Gibt ein **Zertifikate** -Objekt zurück, das alle Zertifikate enthält, die den angegebenen Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-134">Returns a **Certificates** object that contains all certificates that match the specified search criteria.</span></span><br/> <span data-ttu-id="5a0e3-135">(Geerbt von **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="5a0e3-135">(Inherited from **CertificatesICertificates2**)</span></span> |
| [<span data-ttu-id="5a0e3-136">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="5a0e3-136">**Remove**</span></span>](certificates-remove.md) | <span data-ttu-id="5a0e3-137">Entfernt ein einzelnes [**Zertifikat**](certificate.md) Objekt aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-137">Removes a single [**Certificate**](certificate.md) object from the collection.</span></span><br/> <span data-ttu-id="5a0e3-138">(Geerbt von **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="5a0e3-138">(Inherited from **CertificatesICertificates2**)</span></span>                            |
| [<span data-ttu-id="5a0e3-139">**Speichern**</span><span class="sxs-lookup"><span data-stu-id="5a0e3-139">**Save**</span></span>](certificates-save.md)     | <span data-ttu-id="5a0e3-140">Speichert die Zertifikate in einer angegebenen Datei.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-140">Saves the certificates to a specified file.</span></span><br/> <span data-ttu-id="5a0e3-141">(Geerbt von **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="5a0e3-141">(Inherited from **CertificatesICertificates2**)</span></span>                                                                |
| [<span data-ttu-id="5a0e3-142">**Select**</span><span class="sxs-lookup"><span data-stu-id="5a0e3-142">**Select**</span></span>](certificates-select.md) | <span data-ttu-id="5a0e3-143">Zeigt ein Dialogfeld für die Auswahl von Zertifikaten an und gibt eine Sammlung der ausgewählten Zertifikate zurück.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-143">Displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span><br/> <span data-ttu-id="5a0e3-144">(Geerbt von **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="5a0e3-144">(Inherited from **CertificatesICertificates2**)</span></span>  |



 

### <a name="properties"></a><span data-ttu-id="5a0e3-145">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5a0e3-145">Properties</span></span>

<span data-ttu-id="5a0e3-146">Das Objekt " **Zertifikate** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-146">The **Certificates** object has these properties.</span></span>



| <span data-ttu-id="5a0e3-147">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5a0e3-147">Property</span></span>                                             | <span data-ttu-id="5a0e3-148">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="5a0e3-148">Access type</span></span>          | <span data-ttu-id="5a0e3-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a0e3-149">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a0e3-150">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="5a0e3-150">**\_NewEnum**</span></span>](certificates-newenum.md)<br/> | <span data-ttu-id="5a0e3-151">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a0e3-151">Read-only</span></span><br/> | <span data-ttu-id="5a0e3-152">Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-152">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="5a0e3-153">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-153">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="5a0e3-154">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="5a0e3-154">**Count**</span></span>](certificates-count.md)<br/>       | <span data-ttu-id="5a0e3-155">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a0e3-155">Read-only</span></span><br/> | <span data-ttu-id="5a0e3-156">Ruft die Anzahl der [**Zertifikat**](certificate.md) Objekte in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-156">Retrieves the number of [**Certificate**](certificate.md) objects in the collection.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="5a0e3-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a0e3-157">**Item**</span></span>](certificates-item.md)<br/>         | <span data-ttu-id="5a0e3-158">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a0e3-158">Read-only</span></span><br/> | <span data-ttu-id="5a0e3-159">Ruft ein [**Zertifikat**](certificate.md) Objekt ab, das das indizierte Zertifikat der Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-159">Retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="5a0e3-160">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-160">This is the default property.</span></span><br/> <span data-ttu-id="5a0e3-161">(Geerbt von **CertificatesICertificates2ICertificates**)</span><span class="sxs-lookup"><span data-stu-id="5a0e3-161">(Inherited from **CertificatesICertificates2ICertificates**)</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="5a0e3-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a0e3-162">Remarks</span></span>

<span data-ttu-id="5a0e3-163">Das Objekt " **Zertifikate** " kann erstellt und ist für die Skripterstellung sicher.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-163">The **Certificates** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="5a0e3-164">Die ProgID für das **Zertifikat** Objekt ist "CAPICOM". Zertifikate. 2 ".</span><span class="sxs-lookup"><span data-stu-id="5a0e3-164">The ProgID for the **Certificates** object is "CAPICOM.Certificates.2".</span></span>

<span data-ttu-id="5a0e3-165">**CAPICOM 1. *x*:** die ProgID für das **Zertifikat** Objekt ist "CAPICOM". Zertifikate. 1 ".</span><span class="sxs-lookup"><span data-stu-id="5a0e3-165">**CAPICOM 1.*x*:** The ProgID for the **Certificates** object is "CAPICOM.Certificates.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="5a0e3-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a0e3-166">Requirements</span></span>



| <span data-ttu-id="5a0e3-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a0e3-167">Requirement</span></span> | <span data-ttu-id="5a0e3-168">Wert</span><span class="sxs-lookup"><span data-stu-id="5a0e3-168">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a0e3-169">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="5a0e3-169">End of client support</span></span><br/> | <span data-ttu-id="5a0e3-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a0e3-170">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5a0e3-171">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="5a0e3-171">End of server support</span></span><br/> | <span data-ttu-id="5a0e3-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a0e3-172">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5a0e3-173">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="5a0e3-173">Redistributable</span></span><br/>       | <span data-ttu-id="5a0e3-174">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="5a0e3-174">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5a0e3-175">DLL</span><span class="sxs-lookup"><span data-stu-id="5a0e3-175">DLL</span></span><br/>                   | <dl> <span data-ttu-id="5a0e3-176"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a0e3-176"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a0e3-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a0e3-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a0e3-178">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="5a0e3-178">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
