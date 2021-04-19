---
description: Stellt eine Auflistung von Signatur Geber Objekten dar.
ms.assetid: 72e86acd-eb87-4eff-bd4e-327630ebbfc4
title: Signer-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 75eba0ecb2592bf7efc27ecdd63288179e306651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373634"
---
# <a name="signers-object"></a><span data-ttu-id="efb04-103">Signer-Objekt</span><span class="sxs-lookup"><span data-stu-id="efb04-103">Signers object</span></span>

<span data-ttu-id="efb04-104">\[Das **Signatur** Geber Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="efb04-104">\[The **Signers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="efb04-105">Verwenden Sie stattdessen eine Auflistung von CmsSigner-Objekten.</span><span class="sxs-lookup"><span data-stu-id="efb04-105">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="efb04-106">Weitere Informationen finden Sie unter der [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="efb04-106">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="efb04-107">Das **Signatur** Geber-Objekt stellt eine Auflistung von [**Signatur**](signer.md) Geber Objekten dar.</span><span class="sxs-lookup"><span data-stu-id="efb04-107">The **Signers** object represents a collection of [**Signer**](signer.md) objects.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="efb04-108">Verwendung</span><span class="sxs-lookup"><span data-stu-id="efb04-108">When to use</span></span>

<span data-ttu-id="efb04-109">Das **Signatur** Geber-Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="efb04-109">The **Signers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="efb04-110">Ruft die Anzahl der Zertifikate in der Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="efb04-110">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="efb04-111">Ruft ein bestimmtes **Signatur** Geber Objekt aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="efb04-111">Retrieve a specific **Signers** object from the collection.</span></span>
-   <span data-ttu-id="efb04-112">Iterieren Sie die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="efb04-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="efb04-113">Member</span><span class="sxs-lookup"><span data-stu-id="efb04-113">Members</span></span>

<span data-ttu-id="efb04-114">Das **Signatur** Geber-Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="efb04-114">The **Signers** object has these types of members:</span></span>

-   [<span data-ttu-id="efb04-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="efb04-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="efb04-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="efb04-116">Properties</span></span>

<span data-ttu-id="efb04-117">Das **Signatur** Geber-Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="efb04-117">The **Signers** object has these properties.</span></span>



| <span data-ttu-id="efb04-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="efb04-118">Property</span></span>                                        | <span data-ttu-id="efb04-119">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="efb04-119">Access type</span></span>          | <span data-ttu-id="efb04-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="efb04-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efb04-121">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="efb04-121">**\_NewEnum**</span></span>](signers-newenum.md)<br/> | <span data-ttu-id="efb04-122">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="efb04-122">Read-only</span></span><br/> | <span data-ttu-id="efb04-123">Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="efb04-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="efb04-124">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="efb04-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="efb04-125">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="efb04-125">**Count**</span></span>](signers-count.md)<br/>       | <span data-ttu-id="efb04-126">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="efb04-126">Read-only</span></span><br/> | <span data-ttu-id="efb04-127">Anzahl der [**Signatur**](signer.md) Geber Objekte in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="efb04-127">Number of [**Signer**](signer.md) objects in the collection.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="efb04-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="efb04-128">**Item**</span></span>](signers-item.md)<br/>         | <span data-ttu-id="efb04-129">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="efb04-129">Read-only</span></span><br/> | <span data-ttu-id="efb04-130">Ruft das [**Signatur**](signer.md) Geber Objekt ab, das den indizierten Signatur Geber darstellt.</span><span class="sxs-lookup"><span data-stu-id="efb04-130">Retrieves the [**Signer**](signer.md) object that represents the indexed signer.</span></span> <span data-ttu-id="efb04-131">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="efb04-131">This is the default property.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="efb04-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="efb04-132">Remarks</span></span>

<span data-ttu-id="efb04-133">Das **Signatur** Geber Objekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="efb04-133">The **Signers** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="efb04-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="efb04-134">Requirements</span></span>



| <span data-ttu-id="efb04-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="efb04-135">Requirement</span></span> | <span data-ttu-id="efb04-136">Wert</span><span class="sxs-lookup"><span data-stu-id="efb04-136">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="efb04-137">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="efb04-137">Redistributable</span></span><br/> | <span data-ttu-id="efb04-138">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="efb04-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="efb04-139">DLL</span><span class="sxs-lookup"><span data-stu-id="efb04-139">DLL</span></span><br/>             | <dl> <span data-ttu-id="efb04-140"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efb04-140"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efb04-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efb04-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efb04-142">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="efb04-142">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
