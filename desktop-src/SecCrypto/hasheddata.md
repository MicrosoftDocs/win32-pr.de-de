---
description: Stellt Funktionen für das hashte einer Zeichenfolge bereit.
ms.assetid: 893639c2-57b9-48f6-bf60-a21c3368ffeb
title: HashedData-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b6e54d7d2ca52ceafe500615af4063dfc7310b0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356360"
---
# <a name="hasheddata-object"></a><span data-ttu-id="e552d-103">HashedData-Objekt</span><span class="sxs-lookup"><span data-stu-id="e552d-103">HashedData object</span></span>

<span data-ttu-id="e552d-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e552d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e552d-105">Verwenden Sie stattdessen die [**HashAlgorithm-Klasse**](/previous-versions/windows/) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="e552d-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="e552d-106">Das **hashedData** -Objekt stellt Funktionen zum Hashwert einer Zeichenfolge bereit.</span><span class="sxs-lookup"><span data-stu-id="e552d-106">The **HashedData** object provides functionality for hashing a string.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="e552d-107">Verwendung</span><span class="sxs-lookup"><span data-stu-id="e552d-107">When to use</span></span>

<span data-ttu-id="e552d-108">Das **hashedData** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="e552d-108">The **HashedData** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="e552d-109">Geben Sie die Inhalts Zeichenfolge an, die die zu hashenden Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="e552d-109">Specify the content string that contains the data to be hashed.</span></span>
-   <span data-ttu-id="e552d-110">Wendet einen angegebenen Hash Algorithmus auf die Inhalts Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="e552d-110">Apply a specified hash algorithm to the content string.</span></span>

## <a name="members"></a><span data-ttu-id="e552d-111">Member</span><span class="sxs-lookup"><span data-stu-id="e552d-111">Members</span></span>

<span data-ttu-id="e552d-112">Das **hashedData** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e552d-112">The **HashedData** object has these types of members:</span></span>

-   [<span data-ttu-id="e552d-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="e552d-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="e552d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e552d-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e552d-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="e552d-115">Methods</span></span>

<span data-ttu-id="e552d-116">Das **hashedData** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e552d-116">The **HashedData** object has these methods.</span></span>



| <span data-ttu-id="e552d-117">Methode</span><span class="sxs-lookup"><span data-stu-id="e552d-117">Method</span></span>                          | <span data-ttu-id="e552d-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e552d-118">Description</span></span>                                        |
|:--------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="e552d-119">**Hash**</span><span class="sxs-lookup"><span data-stu-id="e552d-119">**Hash**</span></span>](hasheddata-hash.md) | <span data-ttu-id="e552d-120">Erstellt einen Hash der angegebenen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e552d-120">Creates a hash of the specified string.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e552d-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e552d-121">Properties</span></span>

<span data-ttu-id="e552d-122">Das **hashedData** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e552d-122">The **HashedData** object has these properties.</span></span>



| <span data-ttu-id="e552d-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e552d-123">Property</span></span>                                             | <span data-ttu-id="e552d-124">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="e552d-124">Access type</span></span>           | <span data-ttu-id="e552d-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e552d-125">Description</span></span>                                                                                                                                                                          |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e552d-126">**Algorithmus**</span><span class="sxs-lookup"><span data-stu-id="e552d-126">**Algorithm**</span></span>](hasheddata-algorithm.md)<br/> | <span data-ttu-id="e552d-127">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e552d-127">Read/write</span></span><br/> | <span data-ttu-id="e552d-128">Legt den Typ des verwendeten Hash Algorithmus fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="e552d-128">Sets or retrieves the type of hashing algorithm used.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="e552d-129">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e552d-129">**Value**</span></span>](hasheddata-value.md)<br/>         | <span data-ttu-id="e552d-130">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e552d-130">Read-only</span></span><br/>  | <span data-ttu-id="e552d-131">Ruft die Hash Daten nach erfolgreichen Aufrufen der [**Hash**](hasheddata-hash.md) Methode ab.</span><span class="sxs-lookup"><span data-stu-id="e552d-131">Retrieves the hashed data after successful calls to the [**Hash**](hasheddata-hash.md) method.</span></span> <span data-ttu-id="e552d-132">Der Hash wird im Hexadezimal Format zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e552d-132">The hash is returned in hexadecimal format.</span></span> <span data-ttu-id="e552d-133">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e552d-133">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e552d-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e552d-134">Remarks</span></span>

<span data-ttu-id="e552d-135">Um den Hash einer großen Datenmenge zu erstellen, rufen Sie die [**Hash**](hasheddata-hash.md) Methode für jedes Datenelement auf.</span><span class="sxs-lookup"><span data-stu-id="e552d-135">To create the hash of a large amount of data, call the [**Hash**](hasheddata-hash.md) method for each piece of data.</span></span> <span data-ttu-id="e552d-136">Der Hash der einzelnen Daten Daten wird bis zum Lesen der Eigenschaft mit der [**value**](hasheddata-value.md) -Eigenschaft verkettet.</span><span class="sxs-lookup"><span data-stu-id="e552d-136">The hash of each piece of data is concatenated to the [**Value**](hasheddata-value.md) property until the property is read.</span></span> <span data-ttu-id="e552d-137">Der Inhalt der **value** -Eigenschaft wird zurückgesetzt, wenn die Eigenschaft gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="e552d-137">The contents of the **Value** property are reset when the property is read.</span></span>

<span data-ttu-id="e552d-138">Das **hashedData** -Objekt kann erstellt und ist für die Skripterstellung sicher.</span><span class="sxs-lookup"><span data-stu-id="e552d-138">The **HashedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="e552d-139">Die ProgID für das **hashedData** -Objekt ist "CAPICOM". HashedData. 1 ".</span><span class="sxs-lookup"><span data-stu-id="e552d-139">The ProgID for the **HashedData** object is "CAPICOM.HashedData.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="e552d-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e552d-140">Requirements</span></span>



| <span data-ttu-id="e552d-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e552d-141">Requirement</span></span> | <span data-ttu-id="e552d-142">Wert</span><span class="sxs-lookup"><span data-stu-id="e552d-142">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e552d-143">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e552d-143">End of client support</span></span><br/> | <span data-ttu-id="e552d-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e552d-144">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e552d-145">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="e552d-145">End of server support</span></span><br/> | <span data-ttu-id="e552d-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e552d-146">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e552d-147">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e552d-147">Redistributable</span></span><br/>       | <span data-ttu-id="e552d-148">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="e552d-148">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e552d-149">DLL</span><span class="sxs-lookup"><span data-stu-id="e552d-149">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e552d-150"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e552d-150"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
