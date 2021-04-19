---
description: Gibt den Algorithmus an, der zum Signieren, umbrechen und Verschlüsseln von Vorgängen verwendet wird.
ms.assetid: 9a3071a3-e62d-43d3-acd7-0685592c78b4
title: Algorithmusobjekt (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f564efe9df3122951969a45443d58ace60e9db30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369548"
---
# <a name="algorithm-object"></a><span data-ttu-id="e3869-103">Algorithmusobjekt</span><span class="sxs-lookup"><span data-stu-id="e3869-103">Algorithm object</span></span>

<span data-ttu-id="e3869-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e3869-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="e3869-105">Verwenden Sie stattdessen die [**AlgorithmIdentifier-Klasse**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="e3869-105">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="e3869-106">Das **Algorithmusobjekt** gibt den Algorithmus an, der zum Signieren, umbrechen und Verschlüsseln von Vorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3869-106">The **Algorithm** object specifies the algorithm used for signing, enveloping, and encrypting operations.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="e3869-107">Verwendung</span><span class="sxs-lookup"><span data-stu-id="e3869-107">When to use</span></span>

<span data-ttu-id="e3869-108">Das **Algorithmusobjekt** wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="e3869-108">The **Algorithm** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="e3869-109">Legen Sie den zu verwendenden Algorithmus fest oder rufen Sie ihn ab.</span><span class="sxs-lookup"><span data-stu-id="e3869-109">Set or retrieve the algorithm to be used.</span></span>
-   <span data-ttu-id="e3869-110">Festlegen oder Abrufen der Schlüssellänge.</span><span class="sxs-lookup"><span data-stu-id="e3869-110">Set or retrieve the key length.</span></span>

> [!Note]  
> <span data-ttu-id="e3869-111">CAPICOM versucht, den standardmäßigen Kryptografiedienstanbieter (CSP) des Systems zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e3869-111">CAPICOM attempts to use the system default cryptographic service provider (CSP).</span></span> <span data-ttu-id="e3869-112">Wenn dieser CSP den angeforderten Algorithmus oder die Schlüssellänge nicht bereitstellen kann, sucht CAPICOM nach einem verfügbaren von Microsoft bereitgestellten CSP, der den angeforderten Algorithmus und die Schlüssellänge in dieser Verfügbarkeits Reihenfolge verarbeiten kann: Microsoft Enhanced Cryptographic Provider, Microsoft Strong Cryptographic Provider, Microsoft Base Cryptographic Provider.</span><span class="sxs-lookup"><span data-stu-id="e3869-112">If that CSP cannot provide the requested algorithm or key length, CAPICOM searches for an available Microsoft-provided CSP that can handle the requested algorithm and key length, in this order of availability: Microsoft Enhanced Cryptographic Provider, Microsoft Strong Cryptographic Provider, Microsoft Base Cryptographic Provider.</span></span>

 

## <a name="members"></a><span data-ttu-id="e3869-113">Member</span><span class="sxs-lookup"><span data-stu-id="e3869-113">Members</span></span>

<span data-ttu-id="e3869-114">Das  Algorithmusobjekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e3869-114">The **Algorithm** object has these types of members:</span></span>

-   [<span data-ttu-id="e3869-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3869-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3869-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3869-116">Properties</span></span>

<span data-ttu-id="e3869-117">Das  Algorithmusobjekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e3869-117">The **Algorithm** object has these properties.</span></span>



| <span data-ttu-id="e3869-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e3869-118">Property</span></span>                                            | <span data-ttu-id="e3869-119">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="e3869-119">Access type</span></span>           | <span data-ttu-id="e3869-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3869-120">Description</span></span>                                                                                                                       |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3869-121">**KeyLength**</span><span class="sxs-lookup"><span data-stu-id="e3869-121">**KeyLength**</span></span>](algorithm-keylength.md)<br/> | <span data-ttu-id="e3869-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e3869-122">Read/write</span></span><br/> | <span data-ttu-id="e3869-123">Legt die Länge des Schlüssels fest oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="e3869-123">Sets or retrieves the length of the key.</span></span><br/>                                                                               |
| [<span data-ttu-id="e3869-124">**Name**</span><span class="sxs-lookup"><span data-stu-id="e3869-124">**Name**</span></span>](algorithm-name.md)<br/>           | <span data-ttu-id="e3869-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e3869-125">Read/write</span></span><br/> | <span data-ttu-id="e3869-126">Legt den Algorithmus fest, der zum Signieren, umbrechen und Verschlüsseln von Vorgängen verwendet wird, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="e3869-126">Sets or retrieves the algorithm used for signing, enveloping, and encrypting operations.</span></span> <span data-ttu-id="e3869-127">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e3869-127">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e3869-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3869-128">Remarks</span></span>

<span data-ttu-id="e3869-129">Das  Algorithmusobjekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e3869-129">The **Algorithm** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3869-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3869-130">Requirements</span></span>



| <span data-ttu-id="e3869-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3869-131">Requirement</span></span> | <span data-ttu-id="e3869-132">Wert</span><span class="sxs-lookup"><span data-stu-id="e3869-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3869-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e3869-133">End of client support</span></span><br/> | <span data-ttu-id="e3869-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3869-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e3869-135">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="e3869-135">End of server support</span></span><br/> | <span data-ttu-id="e3869-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3869-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e3869-137">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e3869-137">Redistributable</span></span><br/>       | <span data-ttu-id="e3869-138">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="e3869-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e3869-139">Header</span><span class="sxs-lookup"><span data-stu-id="e3869-139">Header</span></span><br/>                | <dl> <span data-ttu-id="e3869-140"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3869-140"><dt>Capicom.h</dt></span></span> </dl>   |
| <span data-ttu-id="e3869-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e3869-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e3869-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3869-142"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3869-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3869-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3869-144">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="e3869-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
