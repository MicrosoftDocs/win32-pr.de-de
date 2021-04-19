---
description: Stellt eine Auflistung von Zertifikat Objekten dar.
ms.assetid: 11d294b5-0a8a-4970-be10-a3b22389d96e
title: Empfänger Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c68ca0217631970f35680160b71841f758b13fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355269"
---
# <a name="recipients-object"></a><span data-ttu-id="cd46e-103">Empfänger Objekt</span><span class="sxs-lookup"><span data-stu-id="cd46e-103">Recipients object</span></span>

<span data-ttu-id="cd46e-104">\[Das Objekt " **Empfänger** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="cd46e-104">\[The **Recipients** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cd46e-105">Verwenden Sie stattdessen die [**cmsrecepentcollection-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="cd46e-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="cd46e-106">Das **Empfängers** -Objekt stellt eine Auflistung von [**Zertifikat**](certificate.md) Objekten dar.</span><span class="sxs-lookup"><span data-stu-id="cd46e-106">The **Recipients** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="cd46e-107">Jedes-Objekt stellt einen beabsichtigten Empfänger der eingeschlossenen Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="cd46e-107">Each object represents an intended recipient of the enveloped message.</span></span> <span data-ttu-id="cd46e-108">Daten in einem [**EnvelopedData**](envelopeddata.md) -Objekt werden mit einem [*symmetrischen*](../secgloss/s-gly.md) Sitzungsschlüssel verschlüsselt, und dieser symmetrische Sitzungsschlüssel wird dann selbst für jeden Empfänger verschlüsselt, indem der öffentliche Schlüssel aus dem Zertifikat dieses gewünschten Empfängers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cd46e-108">Data in an [**EnvelopedData**](envelopeddata.md) object is encrypted with a [*symmetric*](../secgloss/s-gly.md) session key, and that symmetric session key is then itself encrypted for each recipient by using the public key from that intended recipient's certificate.</span></span> <span data-ttu-id="cd46e-109">Ein Empfänger mit Zugriff auf den [*privaten Schlüssel*](../secgloss/p-gly.md) , der dem [*öffentlichen Schlüssel*](../secgloss/p-gly.md) eines Zertifikats zugeordnet ist, kann den [*Sitzungsschlüssel*](../secgloss/s-gly.md) entschlüsseln und den entschlüsselten Sitzungsschlüssel verwenden, um die eigentlichen Daten zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="cd46e-109">A recipient with access to the [*private key*](../secgloss/p-gly.md) associated with a certificate's [*public key*](../secgloss/p-gly.md) can decrypt the [*session key*](../secgloss/s-gly.md) and use the decrypted session key to decrypt the actual data.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="cd46e-110">Verwendung</span><span class="sxs-lookup"><span data-stu-id="cd46e-110">When to use</span></span>

<span data-ttu-id="cd46e-111">Das Objekt " **Empfänger** " wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="cd46e-111">The **Recipients** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="cd46e-112">Fügen Sie ein [**Zertifikat**](certificate.md) Objekt der Auflistung hinzu, oder entfernen Sie es.</span><span class="sxs-lookup"><span data-stu-id="cd46e-112">Add or remove a [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="cd46e-113">Ruft die Anzahl der Zertifikate in der Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="cd46e-113">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="cd46e-114">Rufen Sie ein bestimmtes **Empfänger** Objekt aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="cd46e-114">Retrieve a specific **Recipients** object from the collection.</span></span>
-   <span data-ttu-id="cd46e-115">Iterieren Sie die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="cd46e-115">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="cd46e-116">Member</span><span class="sxs-lookup"><span data-stu-id="cd46e-116">Members</span></span>

<span data-ttu-id="cd46e-117">Das **Empfänger** Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cd46e-117">The **Recipients** object has these types of members:</span></span>

-   [<span data-ttu-id="cd46e-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="cd46e-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="cd46e-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd46e-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cd46e-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="cd46e-120">Methods</span></span>

<span data-ttu-id="cd46e-121">Das **Empfänger** Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="cd46e-121">The **Recipients** object has these methods.</span></span>



| <span data-ttu-id="cd46e-122">Methode</span><span class="sxs-lookup"><span data-stu-id="cd46e-122">Method</span></span>                              | <span data-ttu-id="cd46e-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd46e-123">Description</span></span>                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd46e-124">**Eren**</span><span class="sxs-lookup"><span data-stu-id="cd46e-124">**Add**</span></span>](recipients-add.md)       | <span data-ttu-id="cd46e-125">Fügt der Auflistung ein [**Zertifikat**](certificate.md) Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="cd46e-125">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/>         |
| [<span data-ttu-id="cd46e-126">**Klartext**</span><span class="sxs-lookup"><span data-stu-id="cd46e-126">**Clear**</span></span>](recipients-clear.md)   | <span data-ttu-id="cd46e-127">Entfernt alle [**Zertifikat**](certificate.md) Objekte aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="cd46e-127">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> |
| [<span data-ttu-id="cd46e-128">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="cd46e-128">**Remove**</span></span>](recipients-remove.md) | <span data-ttu-id="cd46e-129">Entfernt ein [**Zertifikat**](certificate.md) Objekt aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="cd46e-129">Removes a [**Certificate**](certificate.md) object from the collection.</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="cd46e-130">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd46e-130">Properties</span></span>

<span data-ttu-id="cd46e-131">Das **Empfänger** Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cd46e-131">The **Recipients** object has these properties.</span></span>



| <span data-ttu-id="cd46e-132">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cd46e-132">Property</span></span>                                           | <span data-ttu-id="cd46e-133">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="cd46e-133">Access type</span></span>          | <span data-ttu-id="cd46e-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd46e-134">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd46e-135">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="cd46e-135">**\_NewEnum**</span></span>](recipients-newenum.md)<br/> | <span data-ttu-id="cd46e-136">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd46e-136">Read-only</span></span><br/> | <span data-ttu-id="cd46e-137">Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="cd46e-137">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="cd46e-138">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="cd46e-138">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="cd46e-139">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="cd46e-139">**Count**</span></span>](recipients-count.md)<br/>       |                      | <span data-ttu-id="cd46e-140">Die Anzahl der-Objekte in der **Empfänger** Auflistung.</span><span class="sxs-lookup"><span data-stu-id="cd46e-140">The number of objects in the **Recipients** collection.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="cd46e-141">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd46e-141">**Item**</span></span>](recipients-item.md)<br/>         |                      | <span data-ttu-id="cd46e-142">Ein indiziertes Objekt in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="cd46e-142">An indexed object in the collection.</span></span> <span data-ttu-id="cd46e-143">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cd46e-143">This is the default property.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="cd46e-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd46e-144">Remarks</span></span>

<span data-ttu-id="cd46e-145">Das **Empfänger** Objekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cd46e-145">The **Recipients** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd46e-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd46e-146">Requirements</span></span>



| <span data-ttu-id="cd46e-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd46e-147">Requirement</span></span> | <span data-ttu-id="cd46e-148">Wert</span><span class="sxs-lookup"><span data-stu-id="cd46e-148">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd46e-149">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="cd46e-149">Redistributable</span></span><br/> | <span data-ttu-id="cd46e-150">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="cd46e-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cd46e-151">DLL</span><span class="sxs-lookup"><span data-stu-id="cd46e-151">DLL</span></span><br/>             | <dl> <span data-ttu-id="cd46e-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd46e-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd46e-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd46e-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd46e-154">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="cd46e-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
