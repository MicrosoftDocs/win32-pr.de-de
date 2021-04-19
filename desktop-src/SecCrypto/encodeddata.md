---
description: Stellt einen Block von ASN. 1-codierten Daten dar.
ms.assetid: af7acc5f-da0a-4235-8496-05db94664ea5
title: Encoddata-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d05fce31ad4ef08bf9f573c0158a683bdbeba739
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367130"
---
# <a name="encodeddata-object"></a><span data-ttu-id="31a19-103">Encoddata-Objekt</span><span class="sxs-lookup"><span data-stu-id="31a19-103">EncodedData object</span></span>

<span data-ttu-id="31a19-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="31a19-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="31a19-105">Verwenden Sie stattdessen die [**AsnEncodedData-Klasse**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="31a19-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="31a19-106">Das **encoddata** -Objekt stellt einen Block von ASN. 1-codierten Daten dar.</span><span class="sxs-lookup"><span data-stu-id="31a19-106">The **EncodedData** object represents a block of ASN.1 encoded data.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="31a19-107">Verwendung</span><span class="sxs-lookup"><span data-stu-id="31a19-107">When to use</span></span>

<span data-ttu-id="31a19-108">Das **encoddata** -Objekt wird von mehreren CAPICOM-Objekteigenschaften zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="31a19-108">The **EncodedData** object is returned by several CAPICOM object properties.</span></span> <span data-ttu-id="31a19-109">Wenn Sie zurückgegeben wird, wird dieses Objekt verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="31a19-109">When returned, this object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="31a19-110">Eine Zeichen folgen Darstellung der codierten Daten abrufen.</span><span class="sxs-lookup"><span data-stu-id="31a19-110">Obtain a string representation of the encoded data.</span></span>
-   <span data-ttu-id="31a19-111">Rufen Sie ggf. das Decoder-Objekt ab, das den codierten Daten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="31a19-111">Obtain the decoder object, if it exists, that is associated with the encoded data.</span></span>
-   <span data-ttu-id="31a19-112">Bestimmen Sie den Typ der codierten Daten.</span><span class="sxs-lookup"><span data-stu-id="31a19-112">Determine the type of encoded data.</span></span>

## <a name="members"></a><span data-ttu-id="31a19-113">Member</span><span class="sxs-lookup"><span data-stu-id="31a19-113">Members</span></span>

<span data-ttu-id="31a19-114">Das **encoddata** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="31a19-114">The **EncodedData** object has these types of members:</span></span>

-   [<span data-ttu-id="31a19-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="31a19-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="31a19-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="31a19-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="31a19-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="31a19-117">Methods</span></span>

<span data-ttu-id="31a19-118">Das **encodeddata** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="31a19-118">The **EncodedData** object has these methods.</span></span>



| <span data-ttu-id="31a19-119">Methode</span><span class="sxs-lookup"><span data-stu-id="31a19-119">Method</span></span>                                 | <span data-ttu-id="31a19-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31a19-120">Description</span></span>                                                     |
|:---------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="31a19-121">**Decoder**</span><span class="sxs-lookup"><span data-stu-id="31a19-121">**Decoder**</span></span>](encodeddata-decoder.md) | <span data-ttu-id="31a19-122">Ruft ein Decoder-Objekt ab, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="31a19-122">Obtains a decoder object, if one exists.</span></span><br/>             |
| [<span data-ttu-id="31a19-123">**Ges**</span><span class="sxs-lookup"><span data-stu-id="31a19-123">**Format**</span></span>](encodeddata-format.md)   | <span data-ttu-id="31a19-124">Gibt eine Zeichen folgen Darstellung der codierten Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="31a19-124">Returns a string representation of the encoded data.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="31a19-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="31a19-125">Properties</span></span>

<span data-ttu-id="31a19-126">Das **encoddata** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="31a19-126">The **EncodedData** object has these properties.</span></span>



| <span data-ttu-id="31a19-127">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="31a19-127">Property</span></span>                                      | <span data-ttu-id="31a19-128">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="31a19-128">Access type</span></span>          | <span data-ttu-id="31a19-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31a19-129">Description</span></span>                                                          |
|:----------------------------------------------|:---------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="31a19-130">**Wert**</span><span class="sxs-lookup"><span data-stu-id="31a19-130">**Value**</span></span>](encodeddata-value.md)<br/> | <span data-ttu-id="31a19-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31a19-131">Read-only</span></span><br/> | <span data-ttu-id="31a19-132">Ruft die codierten Daten ab.</span><span class="sxs-lookup"><span data-stu-id="31a19-132">Retrieves the encoded data.</span></span> <span data-ttu-id="31a19-133">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="31a19-133">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="31a19-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31a19-134">Remarks</span></span>

<span data-ttu-id="31a19-135">Der einzige unterstützte Typ von codierten Daten ist [**certificatepolicies**](certificatepolicies.md).</span><span class="sxs-lookup"><span data-stu-id="31a19-135">The only supported type of encoded data is [**CertificatePolicies**](certificatepolicies.md).</span></span>

<span data-ttu-id="31a19-136">Das **encoddata** -Objekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="31a19-136">The **EncodedData** object cannot be created.</span></span>

<span data-ttu-id="31a19-137">Die folgenden CAPICOM-Objekteigenschaften geben ein **encoddata** -Objekt zurück:</span><span class="sxs-lookup"><span data-stu-id="31a19-137">The following CAPICOM object properties return an **EncodedData** object:</span></span>

-   <span data-ttu-id="31a19-138">**PublicKey. encodecodkey**</span><span class="sxs-lookup"><span data-stu-id="31a19-138">**PublicKey.EncodedKey**</span></span>
-   <span data-ttu-id="31a19-139">**PublicKey. EncodedParameters**</span><span class="sxs-lookup"><span data-stu-id="31a19-139">**PublicKey.EncodedParameters**</span></span>
-   <span data-ttu-id="31a19-140">**Erweiterung. encodeddata**</span><span class="sxs-lookup"><span data-stu-id="31a19-140">**Extension.EncodedData**</span></span>
-   <span data-ttu-id="31a19-141">**Policy. encoddata**</span><span class="sxs-lookup"><span data-stu-id="31a19-141">**Policy.EncodedData**</span></span>

## <a name="requirements"></a><span data-ttu-id="31a19-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31a19-142">Requirements</span></span>



| <span data-ttu-id="31a19-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31a19-143">Requirement</span></span> | <span data-ttu-id="31a19-144">Wert</span><span class="sxs-lookup"><span data-stu-id="31a19-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31a19-145">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="31a19-145">End of client support</span></span><br/> | <span data-ttu-id="31a19-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31a19-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="31a19-147">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="31a19-147">End of server support</span></span><br/> | <span data-ttu-id="31a19-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31a19-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="31a19-149">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="31a19-149">Redistributable</span></span><br/>       | <span data-ttu-id="31a19-150">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="31a19-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="31a19-151">DLL</span><span class="sxs-lookup"><span data-stu-id="31a19-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="31a19-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31a19-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
