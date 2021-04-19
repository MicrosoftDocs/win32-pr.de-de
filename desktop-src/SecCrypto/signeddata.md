---
description: Stellt Eigenschaften und Methoden bereit, um den Inhalt zu erstellen, der mit einer digitalen Signatur signiert werden soll, um Daten digital zu signieren oder cosignieren, und um die digitale Signatur der signierten Daten zu überprüfen. Die signierte Nachricht weist das PKCS \# 7-Format auf.
ms.assetid: 500437e8-a637-4e89-9ac9-aa3ea20d437f
title: SignedData-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d0424826f7dc5d041b877ced1cd7f50490d7801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360305"
---
# <a name="signeddata-object"></a><span data-ttu-id="ac2bc-104">SignedData-Objekt</span><span class="sxs-lookup"><span data-stu-id="ac2bc-104">SignedData object</span></span>

<span data-ttu-id="ac2bc-105">\[Das **SignedData** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="ac2bc-105">\[The **SignedData** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ac2bc-106">Verwenden Sie stattdessen die [**SignedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="ac2bc-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="ac2bc-107">Das **SignedData** -Objekt stellt Eigenschaften und Methoden bereit, um den Inhalt zu erstellen, der mit einer [*digitalen Signatur*](../secgloss/d-gly.md)signiert werden soll, um Daten digital zu signieren oder cosignieren, und um die digitale Signatur der signierten Daten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="ac2bc-107">The **SignedData** object provides properties and methods to establish the content to be signed with a [*digital signature*](../secgloss/d-gly.md), to sign or cosign data digitally, and to verify the digital signature of signed data.</span></span> <span data-ttu-id="ac2bc-108">Die signierte Nachricht weist das PKCS \# 7-Format auf.</span><span class="sxs-lookup"><span data-stu-id="ac2bc-108">The signed message is in PKCS \#7 format.</span></span>

<span data-ttu-id="ac2bc-109">Wenn eine Daten Signatur überprüft wird, wird die Zuordnung zwischen einem Signatur Geber und Daten bestätigt, und es wird angezeigt, dass die Daten nach der Erstellung der Signatur nicht geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="ac2bc-109">A data signature, if verified, proves the association between a signer and data and shows that the data was not changed in any way after the signature was created.</span></span>

## <a name="members"></a><span data-ttu-id="ac2bc-110">Member</span><span class="sxs-lookup"><span data-stu-id="ac2bc-110">Members</span></span>

<span data-ttu-id="ac2bc-111">Das **SignedData** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ac2bc-111">The **SignedData** object has these types of members:</span></span>

-   [<span data-ttu-id="ac2bc-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="ac2bc-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="ac2bc-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac2bc-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ac2bc-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="ac2bc-114">Methods</span></span>

<span data-ttu-id="ac2bc-115">Das **SignedData** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ac2bc-115">The **SignedData** object has these methods.</span></span>



| <span data-ttu-id="ac2bc-116">Methode</span><span class="sxs-lookup"><span data-stu-id="ac2bc-116">Method</span></span>                              | <span data-ttu-id="ac2bc-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac2bc-117">Description</span></span>                                                         |
|:------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="ac2bc-118">**Cosign**</span><span class="sxs-lookup"><span data-stu-id="ac2bc-118">**CoSign**</span></span>](signeddata-cosign.md) | <span data-ttu-id="ac2bc-119">Signiert eine bereits signierte Nachricht mit einem Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="ac2bc-119">Cosigns an already signed message.</span></span><br/>                       |
| [<span data-ttu-id="ac2bc-120">**Gebärden**</span><span class="sxs-lookup"><span data-stu-id="ac2bc-120">**Sign**</span></span>](signeddata-sign.md)     | <span data-ttu-id="ac2bc-121">Erstellt eine digitale Signatur für den zu Signier enden Inhalt.</span><span class="sxs-lookup"><span data-stu-id="ac2bc-121">Creates a digital signature on the content to be signed.</span></span><br/> |
| [<span data-ttu-id="ac2bc-122">**Weisen**</span><span class="sxs-lookup"><span data-stu-id="ac2bc-122">**Verify**</span></span>](signeddata-verify.md) | <span data-ttu-id="ac2bc-123">Bestimmt die Gültigkeit einer Signatur oder von Signaturen.</span><span class="sxs-lookup"><span data-stu-id="ac2bc-123">Determines the validity of a signature or signatures.</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="ac2bc-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac2bc-124">Properties</span></span>

<span data-ttu-id="ac2bc-125">Das **SignedData** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ac2bc-125">The **SignedData** object has these properties.</span></span>



| <span data-ttu-id="ac2bc-126">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ac2bc-126">Property</span></span>                                                   | <span data-ttu-id="ac2bc-127">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="ac2bc-127">Access type</span></span>           | <span data-ttu-id="ac2bc-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac2bc-128">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac2bc-129">**Zertifikate**</span><span class="sxs-lookup"><span data-stu-id="ac2bc-129">**Certificates**</span></span>](signeddata-certificates.md)<br/> | <span data-ttu-id="ac2bc-130">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ac2bc-130">Read-only</span></span><br/>  | <span data-ttu-id="ac2bc-131">Ruft die [**Zertifikats**](certificates.md) Sammlung der signierten Daten ab.</span><span class="sxs-lookup"><span data-stu-id="ac2bc-131">Retrieves the [**Certificates**](certificates.md) collection of the signed data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="ac2bc-132">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="ac2bc-132">**Content**</span></span>](signeddata-content.md)<br/>           | <span data-ttu-id="ac2bc-133">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ac2bc-133">Read/write</span></span><br/> | <span data-ttu-id="ac2bc-134">Zu Signier Ende Daten.</span><span class="sxs-lookup"><span data-stu-id="ac2bc-134">Data to be signed.</span></span> <span data-ttu-id="ac2bc-135">Diese Eigenschaft muss initialisiert werden, bevor die [**Sign**](signeddata-sign.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ac2bc-135">This property must be initialized before the [**Sign**](signeddata-sign.md) method is called.</span></span><br/> <span data-ttu-id="ac2bc-136">Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Status*](../secgloss/s-gly.md) des Objekts zurückgesetzt, und alle Signaturen, die dem-Objekt zugeordnet waren, bevor die-Eigenschaft geändert wurde, gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="ac2bc-136">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any signature that was associated with the object before the property was changed is lost.</span></span><br/> <span data-ttu-id="ac2bc-137">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ac2bc-137">This is the default property.</span></span><br/> |
| [<span data-ttu-id="ac2bc-138">**Signatur Geber**</span><span class="sxs-lookup"><span data-stu-id="ac2bc-138">**Signers**</span></span>](signeddata-signers.md)<br/>           | <span data-ttu-id="ac2bc-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ac2bc-139">Read-only</span></span><br/>  | <span data-ttu-id="ac2bc-140">Ruft die Signatur Geber Auflistung ab [**, die die**](signers.md) Signatur Ersteller der Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="ac2bc-140">Retrieves the [**Signers**](signers.md) collection that represents the signature creators of the data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="ac2bc-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac2bc-141">Remarks</span></span>

<span data-ttu-id="ac2bc-142">Das **SignedData** -Objekt kann erstellt und ist für die Skripterstellung sicher.</span><span class="sxs-lookup"><span data-stu-id="ac2bc-142">The **SignedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="ac2bc-143">Die ProgID für das **SignedData** -Objekt ist CAPICOM. SignedData. 1.</span><span class="sxs-lookup"><span data-stu-id="ac2bc-143">The ProgID for the **SignedData** object is CAPICOM.SignedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac2bc-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac2bc-144">Requirements</span></span>



| <span data-ttu-id="ac2bc-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac2bc-145">Requirement</span></span> | <span data-ttu-id="ac2bc-146">Wert</span><span class="sxs-lookup"><span data-stu-id="ac2bc-146">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac2bc-147">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ac2bc-147">Redistributable</span></span><br/> | <span data-ttu-id="ac2bc-148">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="ac2bc-148">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ac2bc-149">DLL</span><span class="sxs-lookup"><span data-stu-id="ac2bc-149">DLL</span></span><br/>             | <dl> <span data-ttu-id="ac2bc-150"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac2bc-150"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac2bc-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac2bc-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac2bc-152">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="ac2bc-152">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
