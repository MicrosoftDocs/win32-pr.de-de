---
description: 'Empfängerobjekt: Stellt eine Auflistung von Certificate-Objekten dar.'
ms.assetid: 11d294b5-0a8a-4970-be10-a3b22389d96e
title: Empfängerobjekt
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
ms.openlocfilehash: e0f0f6474c6ed8883eb591591eff387fe387f7d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103738"
---
# <a name="recipients-object"></a><span data-ttu-id="98a9c-103">Empfängerobjekt</span><span class="sxs-lookup"><span data-stu-id="98a9c-103">Recipients object</span></span>

<span data-ttu-id="98a9c-104">\[Das **Empfängerobjekt** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="98a9c-104">\[The **Recipients** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="98a9c-105">Verwenden Sie stattdessen die [**CmsRecipientCollection-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography.Pkcs-Namespace.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="98a9c-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="98a9c-106">Das **Recipients-Objekt** stellt eine Auflistung von [**Certificate-Objekten**](certificate.md) dar.</span><span class="sxs-lookup"><span data-stu-id="98a9c-106">The **Recipients** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="98a9c-107">Jedes -Objekt stellt einen beabsichtigten Empfänger der umschlageten Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="98a9c-107">Each object represents an intended recipient of the enveloped message.</span></span> <span data-ttu-id="98a9c-108">Daten in einem [**EnvelopedData-Objekt**](envelopeddata.md) werden mit einem [*symmetrischen*](../secgloss/s-gly.md) Sitzungsschlüssel verschlüsselt, und dieser symmetrische Sitzungsschlüssel wird dann selbst für jeden Empfänger verschlüsselt, indem der öffentliche Schlüssel aus dem Zertifikat des gewünschten Empfängers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="98a9c-108">Data in an [**EnvelopedData**](envelopeddata.md) object is encrypted with a [*symmetric*](../secgloss/s-gly.md) session key, and that symmetric session key is then itself encrypted for each recipient by using the public key from that intended recipient's certificate.</span></span> <span data-ttu-id="98a9c-109">Ein Empfänger mit Zugriff auf den [*privaten Schlüssel,*](../secgloss/p-gly.md) der dem [*öffentlichen Schlüssel*](../secgloss/p-gly.md) eines Zertifikats zugeordnet ist, kann den [*Sitzungsschlüssel*](../secgloss/s-gly.md) entschlüsseln und den entschlüsselten Sitzungsschlüssel verwenden, um die tatsächlichen Daten zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="98a9c-109">A recipient with access to the [*private key*](../secgloss/p-gly.md) associated with a certificate's [*public key*](../secgloss/p-gly.md) can decrypt the [*session key*](../secgloss/s-gly.md) and use the decrypted session key to decrypt the actual data.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="98a9c-110">Verwendung</span><span class="sxs-lookup"><span data-stu-id="98a9c-110">When to use</span></span>

<span data-ttu-id="98a9c-111">Das **Recipients-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="98a9c-111">The **Recipients** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="98a9c-112">Hinzufügen oder Entfernen eines [**Certificate-Objekts**](certificate.md) aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="98a9c-112">Add or remove a [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="98a9c-113">Ruft die Anzahl der Zertifikate in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="98a9c-113">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="98a9c-114">Rufen Sie ein bestimmtes **Empfängerobjekt** aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="98a9c-114">Retrieve a specific **Recipients** object from the collection.</span></span>
-   <span data-ttu-id="98a9c-115">Durchlaufen sie die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="98a9c-115">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="98a9c-116">Member</span><span class="sxs-lookup"><span data-stu-id="98a9c-116">Members</span></span>

<span data-ttu-id="98a9c-117">Das **Recipients-Objekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="98a9c-117">The **Recipients** object has these types of members:</span></span>

-   [<span data-ttu-id="98a9c-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="98a9c-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="98a9c-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="98a9c-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="98a9c-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="98a9c-120">Methods</span></span>

<span data-ttu-id="98a9c-121">Das **Recipients-Objekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="98a9c-121">The **Recipients** object has these methods.</span></span>



| <span data-ttu-id="98a9c-122">Methode</span><span class="sxs-lookup"><span data-stu-id="98a9c-122">Method</span></span>                              | <span data-ttu-id="98a9c-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98a9c-123">Description</span></span>                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="98a9c-124">**Hinzufügen**</span><span class="sxs-lookup"><span data-stu-id="98a9c-124">**Add**</span></span>](recipients-add.md)       | <span data-ttu-id="98a9c-125">Fügt der Auflistung ein [**Certificate-Objekt**](certificate.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="98a9c-125">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/>         |
| [<span data-ttu-id="98a9c-126">**Löschen**</span><span class="sxs-lookup"><span data-stu-id="98a9c-126">**Clear**</span></span>](recipients-clear.md)   | <span data-ttu-id="98a9c-127">Entfernt alle [**Certificate-Objekte**](certificate.md) aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="98a9c-127">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> |
| [<span data-ttu-id="98a9c-128">**Entfernen**</span><span class="sxs-lookup"><span data-stu-id="98a9c-128">**Remove**</span></span>](recipients-remove.md) | <span data-ttu-id="98a9c-129">Entfernt ein [**Certificate-Objekt**](certificate.md) aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="98a9c-129">Removes a [**Certificate**](certificate.md) object from the collection.</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="98a9c-130">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="98a9c-130">Properties</span></span>

<span data-ttu-id="98a9c-131">Das **Recipients-Objekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="98a9c-131">The **Recipients** object has these properties.</span></span>



| <span data-ttu-id="98a9c-132">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="98a9c-132">Property</span></span>                                           | <span data-ttu-id="98a9c-133">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="98a9c-133">Access type</span></span>          | <span data-ttu-id="98a9c-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98a9c-134">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98a9c-135">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="98a9c-135">**\_NewEnum**</span></span>](recipients-newenum.md)<br/> | <span data-ttu-id="98a9c-136">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="98a9c-136">Read-only</span></span><br/> | <span data-ttu-id="98a9c-137">Ruft eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="98a9c-137">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="98a9c-138">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="98a9c-138">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="98a9c-139">**Anzahl**</span><span class="sxs-lookup"><span data-stu-id="98a9c-139">**Count**</span></span>](recipients-count.md)<br/>       |                      | <span data-ttu-id="98a9c-140">Die Anzahl der Objekte in der **Recipients-Auflistung.**</span><span class="sxs-lookup"><span data-stu-id="98a9c-140">The number of objects in the **Recipients** collection.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="98a9c-141">**Element**</span><span class="sxs-lookup"><span data-stu-id="98a9c-141">**Item**</span></span>](recipients-item.md)<br/>         |                      | <span data-ttu-id="98a9c-142">Ein indiziertes Objekt in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="98a9c-142">An indexed object in the collection.</span></span> <span data-ttu-id="98a9c-143">Dies ist die Standardeigenschaft.</span><span class="sxs-lookup"><span data-stu-id="98a9c-143">This is the default property.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="98a9c-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98a9c-144">Remarks</span></span>

<span data-ttu-id="98a9c-145">Das **Recipients-Objekt** kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="98a9c-145">The **Recipients** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="98a9c-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98a9c-146">Requirements</span></span>



| <span data-ttu-id="98a9c-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98a9c-147">Requirement</span></span> | <span data-ttu-id="98a9c-148">Wert</span><span class="sxs-lookup"><span data-stu-id="98a9c-148">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98a9c-149">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="98a9c-149">Redistributable</span></span><br/> | <span data-ttu-id="98a9c-150">CAPICOM 2.0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="98a9c-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="98a9c-151">DLL</span><span class="sxs-lookup"><span data-stu-id="98a9c-151">DLL</span></span><br/>             | <dl> <span data-ttu-id="98a9c-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98a9c-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98a9c-153">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="98a9c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98a9c-154">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="98a9c-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
