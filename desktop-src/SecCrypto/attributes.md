---
description: Stellt eine Auflistung von Attribut Objekten dar.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Attribute-Objekt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2493d4e1bbcbeb2dc7e7b335513beb84c3f28d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364888"
---
# <a name="attributes-object"></a><span data-ttu-id="f925d-103">Attribute-Objekt</span><span class="sxs-lookup"><span data-stu-id="f925d-103">Attributes object</span></span>

<span data-ttu-id="f925d-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f925d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="f925d-105">Verwenden Sie stattdessen die [**cryptographitortributeobjectcollection-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="f925d-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="f925d-106">Das **Attribute** -Objekt stellt eine Auflistung von [**Attribut**](attribute.md) Objekten dar.</span><span class="sxs-lookup"><span data-stu-id="f925d-106">The **Attributes** object represents a collection of [**Attribute**](attribute.md) objects.</span></span> <span data-ttu-id="f925d-107">Jedes [**Attribut**](attribute.md) Objekt stellt ein einzelnes Attribut einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="f925d-107">Each [**Attribute**](attribute.md) object represents a single attribute of a message.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="f925d-108">Verwendung</span><span class="sxs-lookup"><span data-stu-id="f925d-108">When to use</span></span>

<span data-ttu-id="f925d-109">Das **Attribute** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="f925d-109">The **Attributes** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="f925d-110">Fügen Sie ein bestimmtes [**Attribut**](attribute.md) Objekt aus der Auflistung hinzu, oder entfernen Sie es.</span><span class="sxs-lookup"><span data-stu-id="f925d-110">Add or remove a specific [**Attribute**](attribute.md) object from the collection.</span></span>
-   <span data-ttu-id="f925d-111">Löschen Sie die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="f925d-111">Clear the collection.</span></span>
-   <span data-ttu-id="f925d-112">Abrufen der Anzahl von Attributen in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="f925d-112">Retrieve the number of attributes in the collection.</span></span>
-   <span data-ttu-id="f925d-113">Rufen Sie ein bestimmtes [**Attribut**](attribute.md) Objekt aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="f925d-113">Retrieve a specific [**Attribute**](attribute.md) object from the collection.</span></span>
-   <span data-ttu-id="f925d-114">Iterieren Sie die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="f925d-114">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="f925d-115">Member</span><span class="sxs-lookup"><span data-stu-id="f925d-115">Members</span></span>

<span data-ttu-id="f925d-116">Das **Attribute** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f925d-116">The **Attributes** object has these types of members:</span></span>

-   [<span data-ttu-id="f925d-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="f925d-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="f925d-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f925d-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f925d-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="f925d-119">Methods</span></span>

<span data-ttu-id="f925d-120">Das **Attribute** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f925d-120">The **Attributes** object has these methods.</span></span>



| <span data-ttu-id="f925d-121">Methode</span><span class="sxs-lookup"><span data-stu-id="f925d-121">Method</span></span>                              | <span data-ttu-id="f925d-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f925d-122">Description</span></span>                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="f925d-123">**Eren**</span><span class="sxs-lookup"><span data-stu-id="f925d-123">**Add**</span></span>](attributes-add.md)       | <span data-ttu-id="f925d-124">Fügt der Auflistung ein [**Attribut**](attribute.md) Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="f925d-124">Adds an [**Attribute**](attribute.md) object to the collection.</span></span><br/>       |
| [<span data-ttu-id="f925d-125">**Klartext**</span><span class="sxs-lookup"><span data-stu-id="f925d-125">**Clear**</span></span>](attributes-clear.md)   | <span data-ttu-id="f925d-126">Löscht alle [**Attribut**](attribute.md) Objekte aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="f925d-126">Clears all [**Attribute**](attribute.md) objects from the collection.</span></span><br/> |
| [<span data-ttu-id="f925d-127">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="f925d-127">**Remove**</span></span>](attributes-remove.md) | <span data-ttu-id="f925d-128">Entfernt ein [**Attribut**](attribute.md) Objekt aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="f925d-128">Removes an [**Attribute**](attribute.md) object from the collection.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="f925d-129">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f925d-129">Properties</span></span>

<span data-ttu-id="f925d-130">Das **Attribute** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f925d-130">The **Attributes** object has these properties.</span></span>



| <span data-ttu-id="f925d-131">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f925d-131">Property</span></span>                                           | <span data-ttu-id="f925d-132">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="f925d-132">Access type</span></span>          | <span data-ttu-id="f925d-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f925d-133">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f925d-134">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="f925d-134">**\_NewEnum**</span></span>](attributes-newenum.md)<br/> | <span data-ttu-id="f925d-135">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f925d-135">Read-only</span></span><br/> | <span data-ttu-id="f925d-136">Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f925d-136">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="f925d-137">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="f925d-137">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="f925d-138">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="f925d-138">**Count**</span></span>](attributes-count.md)<br/>       | <span data-ttu-id="f925d-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f925d-139">Read-only</span></span><br/> | <span data-ttu-id="f925d-140">Ruft die Anzahl der [**Attribut**](attribute.md) Objekte in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="f925d-140">Retrieves the number of [**Attribute**](attribute.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="f925d-141">**Element**</span><span class="sxs-lookup"><span data-stu-id="f925d-141">**Item**</span></span>](attributes-item.md)<br/>         | <span data-ttu-id="f925d-142">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f925d-142">Read-only</span></span><br/> | <span data-ttu-id="f925d-143">Ruft das [**Attribut**](attribute.md) Objekt ab, das das indizierte Attribut darstellt.</span><span class="sxs-lookup"><span data-stu-id="f925d-143">Retrieves the [**Attribute**](attribute.md) object that represents the indexed attribute.</span></span> <span data-ttu-id="f925d-144">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f925d-144">This is the default property.</span></span><br/>                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="f925d-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f925d-145">Remarks</span></span>

<span data-ttu-id="f925d-146">Das **Attribute** -Objekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f925d-146">The **Attributes** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="f925d-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f925d-147">Requirements</span></span>



| <span data-ttu-id="f925d-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f925d-148">Requirement</span></span> | <span data-ttu-id="f925d-149">Wert</span><span class="sxs-lookup"><span data-stu-id="f925d-149">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f925d-150">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f925d-150">End of client support</span></span><br/> | <span data-ttu-id="f925d-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f925d-151">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f925d-152">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f925d-152">End of server support</span></span><br/> | <span data-ttu-id="f925d-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f925d-153">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f925d-154">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="f925d-154">Redistributable</span></span><br/>       | <span data-ttu-id="f925d-155">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="f925d-155">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f925d-156">DLL</span><span class="sxs-lookup"><span data-stu-id="f925d-156">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f925d-157"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f925d-157"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f925d-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f925d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f925d-159">Kryptografieobjekte</span><span class="sxs-lookup"><span data-stu-id="f925d-159">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
