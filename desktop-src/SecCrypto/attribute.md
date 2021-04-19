---
description: Stellt ein einzelnes authentifiziertes Attribut dar.
ms.assetid: 71c4543b-683f-4ffa-8301-c40c46c490b3
title: Attribute-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34c0800874dc9380b8c9034df2867fc3d1fb578d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370818"
---
# <a name="attribute-object"></a><span data-ttu-id="d6f9a-103">Attribute-Objekt</span><span class="sxs-lookup"><span data-stu-id="d6f9a-103">Attribute object</span></span>

<span data-ttu-id="d6f9a-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6f9a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="d6f9a-105">Verwenden Sie stattdessen die [**cryptographiertributeobject-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography**](/previous-versions/windows/) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="d6f9a-105">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="d6f9a-106">Das **Attribut** Objekt stellt ein einzelnes authentifiziertes Attribut dar.</span><span class="sxs-lookup"><span data-stu-id="d6f9a-106">The **Attribute** object represents a single authenticated attribute.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="d6f9a-107">Verwendung</span><span class="sxs-lookup"><span data-stu-id="d6f9a-107">When to use</span></span>

<span data-ttu-id="d6f9a-108">Das **Attribut** Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="d6f9a-108">The **Attribute** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="d6f9a-109">Festlegen oder Abrufen des CAPICOM-namens des Attributs.</span><span class="sxs-lookup"><span data-stu-id="d6f9a-109">Set or retrieve the CAPICOM name of the attribute.</span></span>
-   <span data-ttu-id="d6f9a-110">Legen Sie den Wert des Attributs fest, oder rufen Sie ihn ab, wie z. b. die Signatur Zeit, den Namen des signierten Dokuments oder eine Beschreibung des signierten Dokuments.</span><span class="sxs-lookup"><span data-stu-id="d6f9a-110">Set or retrieve the value of the attribute, such as signing time, the name of the document signed, or a description of the document signed.</span></span>

## <a name="members"></a><span data-ttu-id="d6f9a-111">Member</span><span class="sxs-lookup"><span data-stu-id="d6f9a-111">Members</span></span>

<span data-ttu-id="d6f9a-112">Das **Attribut** Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d6f9a-112">The **Attribute** object has these types of members:</span></span>

-   [<span data-ttu-id="d6f9a-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d6f9a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d6f9a-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d6f9a-114">Properties</span></span>

<span data-ttu-id="d6f9a-115">Das **Attribut** Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d6f9a-115">The **Attribute** object has these properties.</span></span>



| <span data-ttu-id="d6f9a-116">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d6f9a-116">Property</span></span>                                    | <span data-ttu-id="d6f9a-117">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="d6f9a-117">Access type</span></span>           | <span data-ttu-id="d6f9a-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6f9a-118">Description</span></span>                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6f9a-119">**Name**</span><span class="sxs-lookup"><span data-stu-id="d6f9a-119">**Name**</span></span>](attribute-name.md)<br/>   | <span data-ttu-id="d6f9a-120">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d6f9a-120">Read/write</span></span><br/> | <span data-ttu-id="d6f9a-121">Legt den CAPICOM-Namen des Attributs fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="d6f9a-121">Sets or retrieves the CAPICOM name of the attribute.</span></span> <span data-ttu-id="d6f9a-122">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d6f9a-122">This is the default property.</span></span><br/> |
| [<span data-ttu-id="d6f9a-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d6f9a-123">**Value**</span></span>](attribute-value.md)<br/> | <span data-ttu-id="d6f9a-124">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d6f9a-124">Read/write</span></span><br/> | <span data-ttu-id="d6f9a-125">Legt den Wert des Attributs fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="d6f9a-125">Sets or retrieves the value of the attribute.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="d6f9a-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6f9a-126">Remarks</span></span>

<span data-ttu-id="d6f9a-127">Das **Attribut** Objekt kann erstellt werden und ist für die Skripterstellung sicher.</span><span class="sxs-lookup"><span data-stu-id="d6f9a-127">The **Attribute** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="d6f9a-128">Die ProgID für das **Attribut** Objekt ist "CAPICOM". Attribut. 1.</span><span class="sxs-lookup"><span data-stu-id="d6f9a-128">The ProgID for the **Attribute** object is CAPICOM.Attribute.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6f9a-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6f9a-129">Requirements</span></span>



| <span data-ttu-id="d6f9a-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6f9a-130">Requirement</span></span> | <span data-ttu-id="d6f9a-131">Wert</span><span class="sxs-lookup"><span data-stu-id="d6f9a-131">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f9a-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d6f9a-132">End of client support</span></span><br/> | <span data-ttu-id="d6f9a-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6f9a-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d6f9a-134">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="d6f9a-134">End of server support</span></span><br/> | <span data-ttu-id="d6f9a-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6f9a-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d6f9a-136">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d6f9a-136">Redistributable</span></span><br/>       | <span data-ttu-id="d6f9a-137">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="d6f9a-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d6f9a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d6f9a-138">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d6f9a-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6f9a-139"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6f9a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6f9a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6f9a-141">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="d6f9a-141">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
