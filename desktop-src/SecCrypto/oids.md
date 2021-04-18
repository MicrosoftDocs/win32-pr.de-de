---
description: Stellt eine Auflistung von Oid-Objekten dar.
ms.assetid: 2c4ff87a-58e1-46aa-9680-29062b05308c
title: OIDs-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 894689c214d8b7d352a2453d2d62c847866b9bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365941"
---
# <a name="oids-object"></a><span data-ttu-id="03159-103">OIDs-Objekt</span><span class="sxs-lookup"><span data-stu-id="03159-103">OIDs object</span></span>

<span data-ttu-id="03159-104">\[Das **OIDs** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="03159-104">\[The **OIDs** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="03159-105">Verwenden Sie stattdessen die [**OidCollection-Klasse**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="03159-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="03159-106">Das **OIDs** -Objekt stellt eine Auflistung von [**OID**](oid.md) -Objekten dar.</span><span class="sxs-lookup"><span data-stu-id="03159-106">The **OIDs** object represents a collection of [**OID**](oid.md) objects.</span></span> <span data-ttu-id="03159-107">Jedes [**OID**](oid.md) -Objekt stellt einen einzelnen Objekt Bezeichner dar.</span><span class="sxs-lookup"><span data-stu-id="03159-107">Each [**OID**](oid.md) object represents a single object identifier.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="03159-108">Verwendung</span><span class="sxs-lookup"><span data-stu-id="03159-108">When to use</span></span>

<span data-ttu-id="03159-109">Das **OIDs** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="03159-109">The **OIDs** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="03159-110">Fügen Sie der Auflistung ein [**OID**](oid.md) -Objekt hinzu, oder entfernen Sie es.</span><span class="sxs-lookup"><span data-stu-id="03159-110">Add or remove an [**OID**](oid.md) object from the collection.</span></span>
-   <span data-ttu-id="03159-111">Löschen Sie alle [**OID**](oid.md) -Objekte aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="03159-111">Clear all the [**OID**](oid.md) objects from the collection.</span></span>
-   <span data-ttu-id="03159-112">Ruft die Anzahl der Objekt Bezeichner in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="03159-112">Retrieve the number of object identifiers in the collection.</span></span>
-   <span data-ttu-id="03159-113">Ruft ein bestimmtes [**OID**](oid.md) -Objekt aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="03159-113">Retrieve a specific [**OID**](oid.md) object from the collection.</span></span>
-   <span data-ttu-id="03159-114">Iterieren Sie die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="03159-114">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="03159-115">Member</span><span class="sxs-lookup"><span data-stu-id="03159-115">Members</span></span>

<span data-ttu-id="03159-116">Das **OIDs** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="03159-116">The **OIDs** object has these types of members:</span></span>

-   [<span data-ttu-id="03159-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="03159-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="03159-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03159-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="03159-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="03159-119">Methods</span></span>

<span data-ttu-id="03159-120">Das **OIDs** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="03159-120">The **OIDs** object has these methods.</span></span>



| <span data-ttu-id="03159-121">Methode</span><span class="sxs-lookup"><span data-stu-id="03159-121">Method</span></span>                        | <span data-ttu-id="03159-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03159-122">Description</span></span>                                                                  |
|:------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="03159-123">**Eren**</span><span class="sxs-lookup"><span data-stu-id="03159-123">**Add**</span></span>](oids-add.md)       | <span data-ttu-id="03159-124">Fügt der Auflistung ein [**OID**](oid.md) -Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="03159-124">Adds an [**OID**](oid.md) object to the collection.</span></span><br/>              |
| [<span data-ttu-id="03159-125">**Klartext**</span><span class="sxs-lookup"><span data-stu-id="03159-125">**Clear**</span></span>](oids-clear.md)   | <span data-ttu-id="03159-126">Löscht alle [**OID**](oid.md) -Objekte aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="03159-126">Clears all [**OID**](oid.md) objects from the collection.</span></span><br/>        |
| [<span data-ttu-id="03159-127">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="03159-127">**Remove**</span></span>](oids-remove.md) | <span data-ttu-id="03159-128">Entfernt ein indiziertes [**OID**](oid.md) -Objekt aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="03159-128">Removes an indexed [**OID**](oid.md) object from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="03159-129">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03159-129">Properties</span></span>

<span data-ttu-id="03159-130">Das **OIDs** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="03159-130">The **OIDs** object has these properties.</span></span>



| <span data-ttu-id="03159-131">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="03159-131">Property</span></span>                                     | <span data-ttu-id="03159-132">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="03159-132">Access type</span></span>          | <span data-ttu-id="03159-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03159-133">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03159-134">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="03159-134">**\_NewEnum**</span></span>](oids-newenum.md)<br/> | <span data-ttu-id="03159-135">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="03159-135">Read-only</span></span><br/> | <span data-ttu-id="03159-136">Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="03159-136">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="03159-137">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="03159-137">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="03159-138">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="03159-138">**Count**</span></span>](oids-count.md)<br/>       | <span data-ttu-id="03159-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="03159-139">Read-only</span></span><br/> | <span data-ttu-id="03159-140">Ruft die Anzahl von [**OID**](oid.md) -Objekten in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="03159-140">Retrieves the number of [**OID**](oid.md) objects in the collection.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="03159-141">**Element**</span><span class="sxs-lookup"><span data-stu-id="03159-141">**Item**</span></span>](oids-item.md)<br/>         | <span data-ttu-id="03159-142">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="03159-142">Read-only</span></span><br/> | <span data-ttu-id="03159-143">Ruft ein indiziertes [**OID**](oid.md) -Objekt aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="03159-143">Retrieves an indexed [**OID**](oid.md) object from the collection.</span></span> <span data-ttu-id="03159-144">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="03159-144">This is the default property.</span></span><br/>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="03159-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03159-145">Remarks</span></span>

<span data-ttu-id="03159-146">Das **OIDs** -Objekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="03159-146">The **OIDs** object cannot be created.</span></span>

<span data-ttu-id="03159-147">Das **OIDs** -Objekt wird von den folgenden Eigenschaften verwendet:</span><span class="sxs-lookup"><span data-stu-id="03159-147">The **OIDs** object is used by the following properties:</span></span>

-   [<span data-ttu-id="03159-148">**CertificateStatus. applicationpolicies**</span><span class="sxs-lookup"><span data-stu-id="03159-148">**CertificateStatus.ApplicationPolicies**</span></span>](certificatestatus-applicationpolicies.md)
-   [<span data-ttu-id="03159-149">**CertificateStatus. certificatepolicies**</span><span class="sxs-lookup"><span data-stu-id="03159-149">**CertificateStatus.CertificatePolicies**</span></span>](certificatestatus-certificatepolicies.md)

## <a name="requirements"></a><span data-ttu-id="03159-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03159-150">Requirements</span></span>



| <span data-ttu-id="03159-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03159-151">Requirement</span></span> | <span data-ttu-id="03159-152">Wert</span><span class="sxs-lookup"><span data-stu-id="03159-152">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03159-153">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="03159-153">Redistributable</span></span><br/> | <span data-ttu-id="03159-154">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="03159-154">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="03159-155">DLL</span><span class="sxs-lookup"><span data-stu-id="03159-155">DLL</span></span><br/>             | <dl> <span data-ttu-id="03159-156"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03159-156"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
