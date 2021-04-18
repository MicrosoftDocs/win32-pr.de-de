---
description: Stellt einen Objekt Bezeichner (OID) dar, der von mehreren CAPICOM-Eigenschaften verwendet wird.
ms.assetid: d9dc2a9a-920b-41e1-91fb-da1628df577d
title: Oid-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a524bfd8d2eb2edcf3c97919129dd694414d5ace
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364489"
---
# <a name="oid-object"></a><span data-ttu-id="b1ae1-103">Oid-Objekt</span><span class="sxs-lookup"><span data-stu-id="b1ae1-103">OID object</span></span>

<span data-ttu-id="b1ae1-104">\[Das **OID** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b1ae1-104">\[The **OID** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b1ae1-105">Verwenden Sie stattdessen die [**OID-Klasse**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="b1ae1-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="b1ae1-106">Das **OID** -Objekt stellt einen [*Objekt Bezeichner*](../secgloss/o-gly.md) (OID) dar, der von mehreren CAPICOM-Eigenschaften verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b1ae1-106">The **OID** object represents an [*object identifier*](../secgloss/o-gly.md) (OID) that is used by several CAPICOM properties.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b1ae1-107">Verwendung</span><span class="sxs-lookup"><span data-stu-id="b1ae1-107">When to use</span></span>

<span data-ttu-id="b1ae1-108">Das **OID** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="b1ae1-108">The **OID** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="b1ae1-109">Festlegen oder Abrufen eines CAPICOM-namens und eines anzeigen Amens für die OID.</span><span class="sxs-lookup"><span data-stu-id="b1ae1-109">Set or retrieve a CAPICOM name and display name for the OID.</span></span>
-   <span data-ttu-id="b1ae1-110">Festlegen oder Abrufen der gepunkteten Nummer für die OID.</span><span class="sxs-lookup"><span data-stu-id="b1ae1-110">Set or retrieve the dotted number for the OID.</span></span>

## <a name="members"></a><span data-ttu-id="b1ae1-111">Member</span><span class="sxs-lookup"><span data-stu-id="b1ae1-111">Members</span></span>

<span data-ttu-id="b1ae1-112">Das **OID** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b1ae1-112">The **OID** object has these types of members:</span></span>

-   [<span data-ttu-id="b1ae1-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1ae1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1ae1-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1ae1-114">Properties</span></span>

<span data-ttu-id="b1ae1-115">Das **OID** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b1ae1-115">The **OID** object has these properties.</span></span>



| <span data-ttu-id="b1ae1-116">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b1ae1-116">Property</span></span>                                            | <span data-ttu-id="b1ae1-117">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="b1ae1-117">Access type</span></span>           | <span data-ttu-id="b1ae1-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1ae1-118">Description</span></span>                                                                                      |
|:----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1ae1-119">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="b1ae1-119">**FriendlyName**</span></span>](oid-friendlyname.md)<br/> | <span data-ttu-id="b1ae1-120">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b1ae1-120">Read/write</span></span><br/> | <span data-ttu-id="b1ae1-121">Legt den anzeigen Amen für die OID fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="b1ae1-121">Sets or retrieves the display name for the OID.</span></span><br/>                                       |
| [<span data-ttu-id="b1ae1-122">**Name**</span><span class="sxs-lookup"><span data-stu-id="b1ae1-122">**Name**</span></span>](oid-name.md)<br/>                 | <span data-ttu-id="b1ae1-123">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b1ae1-123">Read/write</span></span><br/> | <span data-ttu-id="b1ae1-124">Legt den von CAPICOM definierten Namen für die OID fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="b1ae1-124">Sets or retrieves the CAPICOM-defined name for the OID.</span></span> <span data-ttu-id="b1ae1-125">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b1ae1-125">This is the default property.</span></span><br/> |
| [<span data-ttu-id="b1ae1-126">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b1ae1-126">**Value**</span></span>](oid-value.md)<br/>               | <span data-ttu-id="b1ae1-127">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b1ae1-127">Read/write</span></span><br/> | <span data-ttu-id="b1ae1-128">Legt den Wert der OID-gepunkteten Zahl der OID fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="b1ae1-128">Sets or retrieves the value of the OID dotted number of the OID.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="b1ae1-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1ae1-129">Remarks</span></span>

<span data-ttu-id="b1ae1-130">Das **OID** -Objekt kann erstellt werden und ist für die Skripterstellung sicher.</span><span class="sxs-lookup"><span data-stu-id="b1ae1-130">The **OID** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="b1ae1-131">Die ProgID für das **OID** -Objekt ist CAPICOM. OID. 1.</span><span class="sxs-lookup"><span data-stu-id="b1ae1-131">The ProgID for the **OID** object is CAPICOM.OID.1.</span></span>

<span data-ttu-id="b1ae1-132">Die folgenden CAPICOM-Objekteigenschaften geben ein **OID** -Objekt zurück:</span><span class="sxs-lookup"><span data-stu-id="b1ae1-132">The following CAPICOM object properties return an **OID** object:</span></span>

-   [<span data-ttu-id="b1ae1-133">**Policyinformation. Oid**</span><span class="sxs-lookup"><span data-stu-id="b1ae1-133">**PolicyInformation.OID**</span></span>](policyinformation-oid.md)
-   [<span data-ttu-id="b1ae1-134">**Qualifizierer. Oid**</span><span class="sxs-lookup"><span data-stu-id="b1ae1-134">**Qualifier.OID**</span></span>](qualifier-oid.md)
-   [<span data-ttu-id="b1ae1-135">**Erweiterung. Oid**</span><span class="sxs-lookup"><span data-stu-id="b1ae1-135">**Extension.OID**</span></span>](extension-oid.md)
-   [<span data-ttu-id="b1ae1-136">**Template. Oid**</span><span class="sxs-lookup"><span data-stu-id="b1ae1-136">**Template.OID**</span></span>](template-oid.md)

## <a name="requirements"></a><span data-ttu-id="b1ae1-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1ae1-137">Requirements</span></span>



| <span data-ttu-id="b1ae1-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1ae1-138">Requirement</span></span> | <span data-ttu-id="b1ae1-139">Wert</span><span class="sxs-lookup"><span data-stu-id="b1ae1-139">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1ae1-140">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="b1ae1-140">Redistributable</span></span><br/> | <span data-ttu-id="b1ae1-141">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1ae1-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b1ae1-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b1ae1-142">DLL</span></span><br/>             | <dl> <span data-ttu-id="b1ae1-143"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1ae1-143"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
