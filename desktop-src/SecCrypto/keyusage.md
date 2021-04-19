---
description: Bietet schreibgeschützten Zugriff auf Schlüssel Verwendungs Eigenschaften eines Zertifikats.
ms.assetid: 8b8e9076-1a4f-4383-ac4b-1322d52949f0
title: KeyUsage-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d2324b4e1e06650f2eed7b63337f2bd48520498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357300"
---
# <a name="keyusage-object"></a><span data-ttu-id="a6953-103">KeyUsage-Objekt</span><span class="sxs-lookup"><span data-stu-id="a6953-103">KeyUsage object</span></span>

<span data-ttu-id="a6953-104">\[Das **KeyUsage** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a6953-104">\[The **KeyUsage** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a6953-105">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="a6953-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a6953-106">Das **KeyUsage** -Objekt bietet schreibgeschützten Zugriff auf Schlüssel Verwendungs Eigenschaften eines Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="a6953-106">The **KeyUsage** object provides read-only access to key usage properties of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="a6953-107">Member</span><span class="sxs-lookup"><span data-stu-id="a6953-107">Members</span></span>

<span data-ttu-id="a6953-108">Das **KeyUsage** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a6953-108">The **KeyUsage** object has these types of members:</span></span>

-   [<span data-ttu-id="a6953-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a6953-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a6953-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a6953-110">Properties</span></span>

<span data-ttu-id="a6953-111">Das **KeyUsage** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a6953-111">The **KeyUsage** object has these properties.</span></span>



| <span data-ttu-id="a6953-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a6953-112">Property</span></span>                                                                           | <span data-ttu-id="a6953-113">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="a6953-113">Access type</span></span>          | <span data-ttu-id="a6953-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6953-114">Description</span></span>                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6953-115">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="a6953-115">**IsCritical**</span></span>](keyusage-iscritical.md)<br/>                               | <span data-ttu-id="a6953-116">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a6953-116">Read-only</span></span><br/> | <span data-ttu-id="a6953-117">Ruft einen booleschen Wert ab, der angibt, ob die **KeyUsage** -Erweiterung als kritisch markiert ist.</span><span class="sxs-lookup"><span data-stu-id="a6953-117">Retrieves a Boolean value that indicates whether the **KeyUsage** extension is marked critical.</span></span><br/>                                  |
| [<span data-ttu-id="a6953-118">**Iscrlsignenabled**</span><span class="sxs-lookup"><span data-stu-id="a6953-118">**IsCRLSignEnabled**</span></span>](keyusage-iscrlsignenabled.md)<br/>                   | <span data-ttu-id="a6953-119">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a6953-119">Read-only</span></span><br/> | <span data-ttu-id="a6953-120">Ruft einen booleschen Wert ab, der angibt, ob das crlsign-Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6953-120">Retrieves a Boolean value that indicates whether the CRLSign bit is set.</span></span><br/>                                                         |
| [<span data-ttu-id="a6953-121">**Isdataenciphermentaktivierte**</span><span class="sxs-lookup"><span data-stu-id="a6953-121">**IsDataEnciphermentEnabled**</span></span>](keyusage-isdataenciphermentenabled.md)<br/> | <span data-ttu-id="a6953-122">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a6953-122">Read-only</span></span><br/> | <span data-ttu-id="a6953-123">Ruft einen booleschen Wert ab, der angibt, ob das DataEncipherment-Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6953-123">Retrieves a Boolean value that indicates whether the dataEncipherment bit is set.</span></span><br/>                                                |
| [<span data-ttu-id="a6953-124">**Isdecocipheronlyaktivierte**</span><span class="sxs-lookup"><span data-stu-id="a6953-124">**IsDecipherOnlyEnabled**</span></span>](keyusage-isdecipheronlyenabled.md)<br/>         | <span data-ttu-id="a6953-125">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a6953-125">Read-only</span></span><br/> | <span data-ttu-id="a6953-126">Ruft einen booleschen Wert ab, der angibt, ob das decodische Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6953-126">Retrieves a Boolean value that indicates whether the decipherOnly bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="a6953-127">**Isdigitalsignatureaktivierte**</span><span class="sxs-lookup"><span data-stu-id="a6953-127">**IsDigitalSignatureEnabled**</span></span>](keyusage-isdigitalsignatureenabled.md)<br/> | <span data-ttu-id="a6953-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a6953-128">Read-only</span></span><br/> | <span data-ttu-id="a6953-129">Ruft einen booleschen Wert ab, der angibt, ob das DigitalSignature-Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6953-129">Retrieves a Boolean value that indicates whether the digitalSignature bit is set.</span></span><br/>                                                |
| [<span data-ttu-id="a6953-130">**"Isencipheronlyaktiviert"**</span><span class="sxs-lookup"><span data-stu-id="a6953-130">**IsEncipherOnlyEnabled**</span></span>](keyusage-isencipheronlyenabled.md)<br/>         | <span data-ttu-id="a6953-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a6953-131">Read-only</span></span><br/> | <span data-ttu-id="a6953-132">Ruft einen booleschen Wert ab, der angibt, ob das encipheronly-Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6953-132">Retrieves a Boolean value that indicates whether the encipherOnly bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="a6953-133">**Iskeyagreementaktivierte**</span><span class="sxs-lookup"><span data-stu-id="a6953-133">**IsKeyAgreementEnabled**</span></span>](keyusage-iskeyagreementenabled.md)<br/>         | <span data-ttu-id="a6953-134">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a6953-134">Read-only</span></span><br/> | <span data-ttu-id="a6953-135">Ruft einen booleschen Wert ab, der angibt, ob das KeyAgreement-Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6953-135">Retrieves a Boolean value that indicates whether the keyAgreement bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="a6953-136">**Iskeycertsignenabled**</span><span class="sxs-lookup"><span data-stu-id="a6953-136">**IsKeyCertSignEnabled**</span></span>](keyusage-iskeycertsignenabled.md)<br/>           | <span data-ttu-id="a6953-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a6953-137">Read-only</span></span><br/> | <span data-ttu-id="a6953-138">Ruft einen booleschen Wert ab, der angibt, ob das keyCertSign-Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6953-138">Retrieves a Boolean value that indicates whether the keyCertSign bit is set.</span></span><br/>                                                     |
| [<span data-ttu-id="a6953-139">**Iskeykociphermentaktivierte**</span><span class="sxs-lookup"><span data-stu-id="a6953-139">**IsKeyEnciphermentEnabled**</span></span>](keyusage-iskeyenciphermentenabled.md)<br/>   | <span data-ttu-id="a6953-140">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a6953-140">Read-only</span></span><br/> | <span data-ttu-id="a6953-141">Ruft einen booleschen Wert ab, der angibt, ob das KeyEncipherment-Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6953-141">Retrieves a Boolean value that indicates whether the keyEncipherment bit is set.</span></span><br/>                                                 |
| [<span data-ttu-id="a6953-142">**Isnonablehnt ationaktivierte**</span><span class="sxs-lookup"><span data-stu-id="a6953-142">**IsNonRepudiationEnabled**</span></span>](keyusage-isnonrepudiationenabled.md)<br/>     | <span data-ttu-id="a6953-143">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a6953-143">Read-only</span></span><br/> | <span data-ttu-id="a6953-144">Ruft einen booleschen Wert ab, der angibt, ob das nonablehnationaktivierte Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6953-144">Retrieves a Boolean value that indicates whether the nonRepudiationEnabled bit is set.</span></span><br/>                                           |
| [<span data-ttu-id="a6953-145">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="a6953-145">**IsPresent**</span></span>](keyusage-ispresent.md)<br/>                                 | <span data-ttu-id="a6953-146">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a6953-146">Read-only</span></span><br/> | <span data-ttu-id="a6953-147">Ruft einen booleschen Wert ab, der angibt, ob die **KeyUsage** -Erweiterung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a6953-147">Retrieves a Boolean value that indicates whether the **KeyUsage** extension is present.</span></span><br/> <span data-ttu-id="a6953-148">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a6953-148">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a6953-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6953-149">Remarks</span></span>

<span data-ttu-id="a6953-150">Das **KeyUsage** -Objekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a6953-150">The **KeyUsage** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6953-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6953-151">Requirements</span></span>



| <span data-ttu-id="a6953-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6953-152">Requirement</span></span> | <span data-ttu-id="a6953-153">Wert</span><span class="sxs-lookup"><span data-stu-id="a6953-153">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6953-154">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="a6953-154">Redistributable</span></span><br/> | <span data-ttu-id="a6953-155">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="a6953-155">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a6953-156">DLL</span><span class="sxs-lookup"><span data-stu-id="a6953-156">DLL</span></span><br/>             | <dl> <span data-ttu-id="a6953-157"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6953-157"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6953-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6953-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6953-159">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="a6953-159">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
