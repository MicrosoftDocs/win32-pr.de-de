---
description: Stellt eine von Microsoft erweiterte Eigenschaft dar.
ms.assetid: 91375fd5-b3af-4ed4-961d-5cc1db1a14e3
title: ExtendedProperty-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ec61da301dc1819c899a7da23da9a10efd81ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364758"
---
# <a name="extendedproperty-object"></a><span data-ttu-id="8cfe3-103">ExtendedProperty-Objekt</span><span class="sxs-lookup"><span data-stu-id="8cfe3-103">ExtendedProperty object</span></span>

<span data-ttu-id="8cfe3-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8cfe3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="8cfe3-105">Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktion [**certgetcertifierecontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) aufzurufen und die Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8cfe3-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="8cfe3-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="8cfe3-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="8cfe3-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="8cfe3-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="8cfe3-108">Das **ExtendedProperty** -Objekt stellt eine von Microsoft erweiterte Eigenschaft dar.</span><span class="sxs-lookup"><span data-stu-id="8cfe3-108">The **ExtendedProperty** object represents a Microsoft-extended property.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="8cfe3-109">Verwendung</span><span class="sxs-lookup"><span data-stu-id="8cfe3-109">When to use</span></span>

<span data-ttu-id="8cfe3-110">Das **ExtendedProperty** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="8cfe3-110">The **ExtendedProperty** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="8cfe3-111">Legen Sie den Typ der erweiterten Eigenschaft fest, oder rufen Sie ihn ab.</span><span class="sxs-lookup"><span data-stu-id="8cfe3-111">Set or retrieve the type of the extended property.</span></span>
-   <span data-ttu-id="8cfe3-112">Legt den Codierungstyp fest, der zum Codieren der erweiterten Eigenschaft verwendet wird, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="8cfe3-112">Set or retrieve the type of encoding used to encode the extended property.</span></span>

## <a name="members"></a><span data-ttu-id="8cfe3-113">Member</span><span class="sxs-lookup"><span data-stu-id="8cfe3-113">Members</span></span>

<span data-ttu-id="8cfe3-114">Das **ExtendedProperty** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8cfe3-114">The **ExtendedProperty** object has these types of members:</span></span>

-   [<span data-ttu-id="8cfe3-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8cfe3-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8cfe3-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8cfe3-116">Properties</span></span>

<span data-ttu-id="8cfe3-117">Das **ExtendedProperty** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8cfe3-117">The **ExtendedProperty** object has these properties.</span></span>



| <span data-ttu-id="8cfe3-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8cfe3-118">Property</span></span>                                             | <span data-ttu-id="8cfe3-119">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="8cfe3-119">Access type</span></span>           | <span data-ttu-id="8cfe3-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8cfe3-120">Description</span></span>                                                                                                                                                                    |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8cfe3-121">**PROPID**</span><span class="sxs-lookup"><span data-stu-id="8cfe3-121">**PropID**</span></span>](extendedproperty-propid.md)<br/> | <span data-ttu-id="8cfe3-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8cfe3-122">Read/write</span></span><br/> | <span data-ttu-id="8cfe3-123">Ein Wert der [**CAPICOM \_ PROPID**](capicom-propid.md) -Enumeration, der den Typ der erweiterten Eigenschaft festlegt oder abruft.</span><span class="sxs-lookup"><span data-stu-id="8cfe3-123">A value of the [**CAPICOM\_PROPID**](capicom-propid.md) enumeration that sets or retrieves the type of extended property.</span></span><br/> <span data-ttu-id="8cfe3-124">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8cfe3-124">This is the default property.</span></span><br/> |
| [<span data-ttu-id="8cfe3-125">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8cfe3-125">**Value**</span></span>](extendedproperty-value.md)<br/>   | <span data-ttu-id="8cfe3-126">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8cfe3-126">Read/write</span></span><br/> | <span data-ttu-id="8cfe3-127">Ein Wert der [**CAPICOM- \_ \_ Codierungstyp**](capicom-encoding-type.md) -Enumeration, die die erweiterten Eigenschaften Daten festlegt oder abruft.</span><span class="sxs-lookup"><span data-stu-id="8cfe3-127">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that sets or retrieves the extended property data.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="8cfe3-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cfe3-128">Remarks</span></span>

<span data-ttu-id="8cfe3-129">Das **ExtendedProperty** -Objekt wird von der [**ExtendedProperties**](extendedproperties.md) -Auflistung verwendet.</span><span class="sxs-lookup"><span data-stu-id="8cfe3-129">The **ExtendedProperty** object is used by the [**ExtendedProperties**](extendedproperties.md) collection.</span></span>

<span data-ttu-id="8cfe3-130">Das **ExtendedProperty** -Objekt kann erstellt werden und ist für die Skripterstellung nicht sicher.</span><span class="sxs-lookup"><span data-stu-id="8cfe3-130">The **ExtendedProperty** object can be created, and it is not safe for scripting.</span></span> <span data-ttu-id="8cfe3-131">Die ProgID für das **ExtendedProperty** -Objekt ist CAPICOM. ExtendedProperty. 1.</span><span class="sxs-lookup"><span data-stu-id="8cfe3-131">The ProgID for the **ExtendedProperty** object is CAPICOM.ExtendedProperty.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cfe3-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cfe3-132">Requirements</span></span>



| <span data-ttu-id="8cfe3-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cfe3-133">Requirement</span></span> | <span data-ttu-id="8cfe3-134">Wert</span><span class="sxs-lookup"><span data-stu-id="8cfe3-134">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cfe3-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="8cfe3-135">End of client support</span></span><br/> | <span data-ttu-id="8cfe3-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8cfe3-136">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8cfe3-137">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="8cfe3-137">End of server support</span></span><br/> | <span data-ttu-id="8cfe3-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cfe3-138">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8cfe3-139">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="8cfe3-139">Redistributable</span></span><br/>       | <span data-ttu-id="8cfe3-140">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="8cfe3-140">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8cfe3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8cfe3-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8cfe3-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cfe3-142"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
