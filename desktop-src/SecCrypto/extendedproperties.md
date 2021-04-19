---
description: Stellt eine Auflistung von ExtendedProperty-Objekten dar.
ms.assetid: 9de25994-9f0b-47a0-b4c8-781aec782f88
title: ExtendedProperties-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 512c29e43b9099d9ef577cce61bbcc3a38d68ac6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361968"
---
# <a name="extendedproperties-object"></a><span data-ttu-id="d2a6f-103">ExtendedProperties-Objekt</span><span class="sxs-lookup"><span data-stu-id="d2a6f-103">ExtendedProperties object</span></span>

<span data-ttu-id="d2a6f-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d2a6f-105">Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktion [**certgetcertifierecontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) aufzurufen und die Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="d2a6f-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="d2a6f-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="d2a6f-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="d2a6f-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="d2a6f-108">Das **ExtendedProperties** -Objekt stellt eine Auflistung von [**ExtendedProperty**](extendedproperty.md) -Objekten dar.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-108">The **ExtendedProperties** object represents a collection of [**ExtendedProperty**](extendedproperty.md) objects.</span></span> <span data-ttu-id="d2a6f-109">Jedes-Objekt stellt eine einzelne erweiterte Eigenschaft dar.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-109">Each object represents a single extended property.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="d2a6f-110">Verwendung</span><span class="sxs-lookup"><span data-stu-id="d2a6f-110">When to use</span></span>

<span data-ttu-id="d2a6f-111">Das **ExtendedProperties** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="d2a6f-111">The **ExtendedProperties** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="d2a6f-112">Fügen Sie ein [**ExtendedProperty**](extendedproperty.md) -Objekt aus der Auflistung hinzu, oder entfernen Sie es.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-112">Add or remove an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span>
-   <span data-ttu-id="d2a6f-113">Ruft die Anzahl der erweiterten Eigenschaften in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-113">Retrieve the number of extended properties in the collection.</span></span>
-   <span data-ttu-id="d2a6f-114">Rufen Sie ein bestimmtes [**ExtendedProperty**](extendedproperty.md) -Objekt aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-114">Retrieve a specific [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span>
-   <span data-ttu-id="d2a6f-115">Iterieren Sie die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-115">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="d2a6f-116">Member</span><span class="sxs-lookup"><span data-stu-id="d2a6f-116">Members</span></span>

<span data-ttu-id="d2a6f-117">Das **ExtendedProperties** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d2a6f-117">The **ExtendedProperties** object has these types of members:</span></span>

-   [<span data-ttu-id="d2a6f-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="d2a6f-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="d2a6f-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d2a6f-119">Properties</span></span>](#extendedproperties-object)

### <a name="methods"></a><span data-ttu-id="d2a6f-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="d2a6f-120">Methods</span></span>

<span data-ttu-id="d2a6f-121">Das **ExtendedProperties** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-121">The **ExtendedProperties** object has these methods.</span></span>



| <span data-ttu-id="d2a6f-122">Methode</span><span class="sxs-lookup"><span data-stu-id="d2a6f-122">Method</span></span>                                      | <span data-ttu-id="d2a6f-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2a6f-123">Description</span></span>                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2a6f-124">**Eren**</span><span class="sxs-lookup"><span data-stu-id="d2a6f-124">**Add**</span></span>](extendedproperties-add.md)       | <span data-ttu-id="d2a6f-125">Fügt der Auflistung ein [**ExtendedProperty**](extendedproperty.md) -Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-125">Adds an [**ExtendedProperty**](extendedproperty.md) object to the collection.</span></span><br/>      |
| [<span data-ttu-id="d2a6f-126">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="d2a6f-126">**Remove**</span></span>](extendedproperties-remove.md) | <span data-ttu-id="d2a6f-127">Entfernt ein [**ExtendedProperty**](extendedproperty.md) -Objekt aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-127">Removes an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d2a6f-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d2a6f-128">Properties</span></span>

<span data-ttu-id="d2a6f-129">Das **ExtendedProperties** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-129">The **ExtendedProperties** object has these properties.</span></span>



| <span data-ttu-id="d2a6f-130">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d2a6f-130">Property</span></span>                                                   | <span data-ttu-id="d2a6f-131">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="d2a6f-131">Access type</span></span>          | <span data-ttu-id="d2a6f-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2a6f-132">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2a6f-133">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="d2a6f-133">**\_NewEnum**</span></span>](extendedproperties-newenum.md)<br/> | <span data-ttu-id="d2a6f-134">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a6f-134">Read-only</span></span><br/> | <span data-ttu-id="d2a6f-135">Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-135">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="d2a6f-136">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-136">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="d2a6f-137">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="d2a6f-137">**Count**</span></span>](extendedproperties-count.md)<br/>       | <span data-ttu-id="d2a6f-138">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a6f-138">Read-only</span></span><br/> | <span data-ttu-id="d2a6f-139">Ruft die Anzahl von [**ExtendedProperty**](extendedproperty.md) -Objekten in der-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-139">Retrieves the number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="d2a6f-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="d2a6f-140">**Item**</span></span>](extendedproperties-item.md)<br/>         | <span data-ttu-id="d2a6f-141">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a6f-141">Read-only</span></span><br/> | <span data-ttu-id="d2a6f-142">Ruft ein [**ExtendedProperty**](extendedproperty.md) -Objekt ab, das die indizierte erweiterte Eigenschaft der Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-142">Retrieves an [**ExtendedProperty**](extendedproperty.md) object that represents the indexed extended property of the collection.</span></span> <span data-ttu-id="d2a6f-143">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-143">This is the default property.</span></span><br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="d2a6f-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2a6f-144">Remarks</span></span>

<span data-ttu-id="d2a6f-145">Das **ExtendedProperties** -Objekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d2a6f-145">The **ExtendedProperties** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2a6f-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2a6f-146">Requirements</span></span>



| <span data-ttu-id="d2a6f-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2a6f-147">Requirement</span></span> | <span data-ttu-id="d2a6f-148">Wert</span><span class="sxs-lookup"><span data-stu-id="d2a6f-148">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a6f-149">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d2a6f-149">End of client support</span></span><br/> | <span data-ttu-id="d2a6f-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2a6f-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d2a6f-151">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="d2a6f-151">End of server support</span></span><br/> | <span data-ttu-id="d2a6f-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2a6f-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d2a6f-153">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d2a6f-153">Redistributable</span></span><br/>       | <span data-ttu-id="d2a6f-154">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="d2a6f-154">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d2a6f-155">DLL</span><span class="sxs-lookup"><span data-stu-id="d2a6f-155">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d2a6f-156"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2a6f-156"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
