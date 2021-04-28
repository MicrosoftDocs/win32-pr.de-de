---
description: 'Certificates-Objekt: Stellt eine Auflistung von Zertifikatobjekten dar.'
ms.assetid: 82011c49-38fb-4261-8fb3-b76859da8a9e
title: Certificates-Objekt
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
ms.openlocfilehash: 8efb9221f39b8544eabe8f6c00d21f6cfdf20c14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098388"
---
# <a name="certificates-object"></a><span data-ttu-id="6bc7a-103">Certificates-Objekt</span><span class="sxs-lookup"><span data-stu-id="6bc7a-103">Certificates object</span></span>

<span data-ttu-id="6bc7a-104">\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6bc7a-105">Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]</span><span class="sxs-lookup"><span data-stu-id="6bc7a-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6bc7a-106">Das **Certificates-Objekt** stellt eine Auflistung von [**Zertifikatobjekten**](certificate.md) dar.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-106">The **Certificates** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="6bc7a-107">Jedes [**Certificate-Objekt**](certificate.md) stellt ein einzelnes [*digitales Zertifikat dar.*](../secgloss/d-gly.md)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-107">Each [**Certificate**](certificate.md) object represents a single [*digital certificate*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="6bc7a-108">Das **Certificates-Objekt** macht die folgenden Schnittstellen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="6bc7a-108">The **Certificates** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="6bc7a-109">**ICertificates2:** Eingeführt in CAPICOM 2.0.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-109">**ICertificates2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="6bc7a-110">**ICertificates:** Eingeführt in CAPICOM 1.0.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-110">**ICertificates**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="6bc7a-111">Verwendung</span><span class="sxs-lookup"><span data-stu-id="6bc7a-111">When to use</span></span>

<span data-ttu-id="6bc7a-112">Das **Certificates-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="6bc7a-112">The **Certificates** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="6bc7a-113">Hinzufügen oder Entfernen eines [**Certificate-Objekts**](certificate.md) zur oder aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-113">Add or remove a [**Certificate**](certificate.md) object to or from the collection.</span></span>
-   <span data-ttu-id="6bc7a-114">Generieren Sie eine Teilmenge der Sammlung, indem Sie einen Satz von Zertifikaten suchen oder ein Dialogfeld zum Auswählen der Zertifikate anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-114">Generate a subset of the collection by finding a set of certificates or by displaying a dialog box to select the certificates.</span></span>
-   <span data-ttu-id="6bc7a-115">Löschen Sie alle [**Zertifikatobjekte**](certificate.md) aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-115">Clear all the [**Certificate**](certificate.md) objects from the collection.</span></span>
-   <span data-ttu-id="6bc7a-116">Rufen Sie die Anzahl der Zertifikate in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-116">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="6bc7a-117">Rufen Sie ein [**bestimmtes Certificate-Objekt**](certificate.md) aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-117">Retrieve a specific [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="6bc7a-118">Iterieren Sie die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-118">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="6bc7a-119">Member</span><span class="sxs-lookup"><span data-stu-id="6bc7a-119">Members</span></span>

<span data-ttu-id="6bc7a-120">Das **Certificates-Objekt** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="6bc7a-120">The **Certificates** object has these types of members:</span></span>

-   [<span data-ttu-id="6bc7a-121">Methoden</span><span class="sxs-lookup"><span data-stu-id="6bc7a-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="6bc7a-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6bc7a-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6bc7a-123">Methoden</span><span class="sxs-lookup"><span data-stu-id="6bc7a-123">Methods</span></span>

<span data-ttu-id="6bc7a-124">Das **Certificates-Objekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-124">The **Certificates** object has these methods.</span></span>



| <span data-ttu-id="6bc7a-125">Methode</span><span class="sxs-lookup"><span data-stu-id="6bc7a-125">Method</span></span>                                | <span data-ttu-id="6bc7a-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6bc7a-126">Description</span></span>                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6bc7a-127">**Hinzufügen**</span><span class="sxs-lookup"><span data-stu-id="6bc7a-127">**Add**</span></span>](certificates-add.md)       | <span data-ttu-id="6bc7a-128">Fügt der Auflistung ein [**Certificate-Objekt**](certificate.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-128">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/> <span data-ttu-id="6bc7a-129">(Geerbt von **ZertifikatenICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-129">(Inherited from **CertificatesICertificates2**)</span></span>                                        |
| [<span data-ttu-id="6bc7a-130">**Löschen**</span><span class="sxs-lookup"><span data-stu-id="6bc7a-130">**Clear**</span></span>](certificates-clear.md)   | <span data-ttu-id="6bc7a-131">Entfernt alle [**Certificate-Objekte**](certificate.md) aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-131">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> <span data-ttu-id="6bc7a-132">(Geerbt von **ZertifikatenICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-132">(Inherited from **CertificatesICertificates2**)</span></span>                                |
| [<span data-ttu-id="6bc7a-133">**Suchen**</span><span class="sxs-lookup"><span data-stu-id="6bc7a-133">**Find**</span></span>](certificates-find.md)     | <span data-ttu-id="6bc7a-134">Gibt ein **Certificates-Objekt** zurück, das alle Zertifikate enthält, die den angegebenen Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-134">Returns a **Certificates** object that contains all certificates that match the specified search criteria.</span></span><br/> <span data-ttu-id="6bc7a-135">(Geerbt von **ZertifikatenICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-135">(Inherited from **CertificatesICertificates2**)</span></span> |
| [<span data-ttu-id="6bc7a-136">**Entfernen**</span><span class="sxs-lookup"><span data-stu-id="6bc7a-136">**Remove**</span></span>](certificates-remove.md) | <span data-ttu-id="6bc7a-137">Entfernt ein einzelnes [**Certificate-Objekt**](certificate.md) aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-137">Removes a single [**Certificate**](certificate.md) object from the collection.</span></span><br/> <span data-ttu-id="6bc7a-138">(Geerbt von **ZertifikatenICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-138">(Inherited from **CertificatesICertificates2**)</span></span>                            |
| [<span data-ttu-id="6bc7a-139">**Speichern**</span><span class="sxs-lookup"><span data-stu-id="6bc7a-139">**Save**</span></span>](certificates-save.md)     | <span data-ttu-id="6bc7a-140">Speichert die Zertifikate in einer angegebenen Datei.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-140">Saves the certificates to a specified file.</span></span><br/> <span data-ttu-id="6bc7a-141">(Geerbt von **ZertifikatenICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-141">(Inherited from **CertificatesICertificates2**)</span></span>                                                                |
| [<span data-ttu-id="6bc7a-142">**Select**</span><span class="sxs-lookup"><span data-stu-id="6bc7a-142">**Select**</span></span>](certificates-select.md) | <span data-ttu-id="6bc7a-143">Zeigt ein Dialogfeld zum Auswählen von Zertifikaten an und gibt eine Sammlung dieser ausgewählten Zertifikate zurück.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-143">Displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span><br/> <span data-ttu-id="6bc7a-144">(Geerbt von **ZertifikatenICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-144">(Inherited from **CertificatesICertificates2**)</span></span>  |



 

### <a name="properties"></a><span data-ttu-id="6bc7a-145">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6bc7a-145">Properties</span></span>

<span data-ttu-id="6bc7a-146">Das **Certificates-Objekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-146">The **Certificates** object has these properties.</span></span>



| <span data-ttu-id="6bc7a-147">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6bc7a-147">Property</span></span>                                             | <span data-ttu-id="6bc7a-148">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="6bc7a-148">Access type</span></span>          | <span data-ttu-id="6bc7a-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6bc7a-149">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6bc7a-150">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="6bc7a-150">**\_NewEnum**</span></span>](certificates-newenum.md)<br/> | <span data-ttu-id="6bc7a-151">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6bc7a-151">Read-only</span></span><br/> | <span data-ttu-id="6bc7a-152">Ruft eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-152">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="6bc7a-153">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-153">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="6bc7a-154">**Anzahl**</span><span class="sxs-lookup"><span data-stu-id="6bc7a-154">**Count**</span></span>](certificates-count.md)<br/>       | <span data-ttu-id="6bc7a-155">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6bc7a-155">Read-only</span></span><br/> | <span data-ttu-id="6bc7a-156">Ruft die Anzahl der [**Certificate-Objekte**](certificate.md) in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-156">Retrieves the number of [**Certificate**](certificate.md) objects in the collection.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="6bc7a-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="6bc7a-157">**Item**</span></span>](certificates-item.md)<br/>         | <span data-ttu-id="6bc7a-158">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6bc7a-158">Read-only</span></span><br/> | <span data-ttu-id="6bc7a-159">Ruft ein [**Certificate-Objekt**](certificate.md) ab, das das indizierte Zertifikat der Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-159">Retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="6bc7a-160">Dies ist die Standardeigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-160">This is the default property.</span></span><br/> <span data-ttu-id="6bc7a-161">(Geerbt von **ZertifikatenICertificates2ICertificates**)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-161">(Inherited from **CertificatesICertificates2ICertificates**)</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="6bc7a-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6bc7a-162">Remarks</span></span>

<span data-ttu-id="6bc7a-163">Das **Certificates-Objekt** kann erstellt werden und ist sicher für Skripts.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-163">The **Certificates** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="6bc7a-164">Die ProgID für das **Certificates-Objekt** ist "CAPICOM. Certificates.2".</span><span class="sxs-lookup"><span data-stu-id="6bc7a-164">The ProgID for the **Certificates** object is "CAPICOM.Certificates.2".</span></span>

<span data-ttu-id="6bc7a-165">**CAPICOM 1. *x*:** Die ProgID für das **Certificates-Objekt** ist "CAPICOM. Certificates.1".</span><span class="sxs-lookup"><span data-stu-id="6bc7a-165">**CAPICOM 1.*x*:** The ProgID for the **Certificates** object is "CAPICOM.Certificates.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="6bc7a-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bc7a-166">Requirements</span></span>



| <span data-ttu-id="6bc7a-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bc7a-167">Requirement</span></span> | <span data-ttu-id="6bc7a-168">Wert</span><span class="sxs-lookup"><span data-stu-id="6bc7a-168">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bc7a-169">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-169">End of client support</span></span><br/> | <span data-ttu-id="6bc7a-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6bc7a-170">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6bc7a-171">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-171">End of server support</span></span><br/> | <span data-ttu-id="6bc7a-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6bc7a-172">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6bc7a-173">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="6bc7a-173">Redistributable</span></span><br/>       | <span data-ttu-id="6bc7a-174">CAPICOM 2.0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="6bc7a-174">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6bc7a-175">DLL</span><span class="sxs-lookup"><span data-stu-id="6bc7a-175">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6bc7a-176"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bc7a-176"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bc7a-177">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6bc7a-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bc7a-178">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="6bc7a-178">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
