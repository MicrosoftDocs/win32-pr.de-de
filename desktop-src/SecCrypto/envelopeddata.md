---
description: Das EnvelopedData-Objekt stellt Eigenschaften und Methoden bereit, um Daten mithilfe der Verschlüsselung für den Datenschutz zu umhüllen.
ms.assetid: 7c5f3e3d-6a70-455d-8921-20495eec4b3e
title: EnvelopedData-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5309061c6ab315a089a1e1d8b9488556cae9f31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364910"
---
# <a name="envelopeddata-object"></a><span data-ttu-id="b4b9e-103">EnvelopedData-Objekt</span><span class="sxs-lookup"><span data-stu-id="b4b9e-103">EnvelopedData object</span></span>

<span data-ttu-id="b4b9e-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b4b9e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b4b9e-105">Verwenden Sie stattdessen die [**EnvelopedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="b4b9e-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="b4b9e-106">Das **EnvelopedData** -Objekt stellt Eigenschaften und Methoden bereit, um Daten mithilfe der Verschlüsselung für den Datenschutz zu umhüllen.</span><span class="sxs-lookup"><span data-stu-id="b4b9e-106">The **EnvelopedData** object provides properties and methods to envelop data for privacy by encryption.</span></span> <span data-ttu-id="b4b9e-107">Zum Umhüllen von Daten wird ein Sitzungs kryptografischer Schlüssel generiert.</span><span class="sxs-lookup"><span data-stu-id="b4b9e-107">To envelop data, a session cryptographic key is generated.</span></span> <span data-ttu-id="b4b9e-108">Dieser [*Sitzungsschlüssel*](../secgloss/s-gly.md) wird dann für jeden vorgesehenen Empfänger mit dem [*öffentlichen Schlüssel*](../secgloss/p-gly.md) des Zertifikats des Empfängers verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="b4b9e-108">That [*session key*](../secgloss/s-gly.md) is then encrypted for each intended recipient using the [*public key*](../secgloss/p-gly.md) of that intended recipient from the recipient's certificate.</span></span> <span data-ttu-id="b4b9e-109">Die verschlüsselten Daten und der Satz Verschlüsselter Sitzungsschlüssel können an alle gewünschten Empfänger gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4b9e-109">The encrypted data and the set of encrypted session keys can be sent to all intended recipients.</span></span> <span data-ttu-id="b4b9e-110">Die generierte Nachricht weist das PKCS \# 7-Format auf.</span><span class="sxs-lookup"><span data-stu-id="b4b9e-110">The message generated is in PKCS \#7 format.</span></span>

## <a name="members"></a><span data-ttu-id="b4b9e-111">Member</span><span class="sxs-lookup"><span data-stu-id="b4b9e-111">Members</span></span>

<span data-ttu-id="b4b9e-112">Das **EnvelopedData** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b4b9e-112">The **EnvelopedData** object has these types of members:</span></span>

-   [<span data-ttu-id="b4b9e-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="b4b9e-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="b4b9e-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b4b9e-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b4b9e-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="b4b9e-115">Methods</span></span>

<span data-ttu-id="b4b9e-116">Das **EnvelopedData** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b4b9e-116">The **EnvelopedData** object has these methods.</span></span>



| <span data-ttu-id="b4b9e-117">Methode</span><span class="sxs-lookup"><span data-stu-id="b4b9e-117">Method</span></span>                                   | <span data-ttu-id="b4b9e-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4b9e-118">Description</span></span>                                                                                                 |
|:-----------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4b9e-119">**Entschlüsseln**</span><span class="sxs-lookup"><span data-stu-id="b4b9e-119">**Decrypt**</span></span>](envelopeddata-decrypt.md) | <span data-ttu-id="b4b9e-120">Entschlüsselt den eingeschlossenen Inhalt.</span><span class="sxs-lookup"><span data-stu-id="b4b9e-120">Decrypts enveloped content.</span></span><br/>                                                                      |
| [<span data-ttu-id="b4b9e-121">**Verschlüsseln**</span><span class="sxs-lookup"><span data-stu-id="b4b9e-121">**Encrypt**</span></span>](envelopeddata-encrypt.md) | <span data-ttu-id="b4b9e-122">Verschlüsselt den Inhalt, verschlüsselt einen Sitzungsschlüssel für jeden Empfänger und gibt das verschlüsselte BLOB zurück.</span><span class="sxs-lookup"><span data-stu-id="b4b9e-122">Encrypts the content, encrypts a session key for each recipient, and returns the encrypted BLOB.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b4b9e-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b4b9e-123">Properties</span></span>

<span data-ttu-id="b4b9e-124">Das **EnvelopedData** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b4b9e-124">The **EnvelopedData** object has these properties.</span></span>



| <span data-ttu-id="b4b9e-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b4b9e-125">Property</span></span>                                                  | <span data-ttu-id="b4b9e-126">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="b4b9e-126">Access type</span></span>           | <span data-ttu-id="b4b9e-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4b9e-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4b9e-128">**Algorithmus**</span><span class="sxs-lookup"><span data-stu-id="b4b9e-128">**Algorithm**</span></span>](envelopeddata-algorithm.md)<br/>   | <span data-ttu-id="b4b9e-129">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b4b9e-129">Read/write</span></span><br/> | <span data-ttu-id="b4b9e-130">Verschlüsselungsalgorithmus und [*Schlüssellänge*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b4b9e-130">Encryption algorithm and [*key length*](../secgloss/k-gly.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="b4b9e-131">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="b4b9e-131">**Content**</span></span>](envelopeddata-content.md)<br/>       | <span data-ttu-id="b4b9e-132">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b4b9e-132">Read/write</span></span><br/> | <span data-ttu-id="b4b9e-133">Der Klartext-Inhalt einer zu umzurufenden Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b4b9e-133">The plaintext content of a message to be enveloped.</span></span> <span data-ttu-id="b4b9e-134">Das Festlegen dieser Eigenschaft muss erfolgen, bevor die [**Verschlüsselungs**](envelopeddata-encrypt.md) Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b4b9e-134">Setting this property must be done before the [**Encrypt**](envelopeddata-encrypt.md) method is called.</span></span><br/> <span data-ttu-id="b4b9e-135">Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Status*](../secgloss/s-gly.md) des Objekts zurückgesetzt, und alle verschlüsselten Inhalte im Objekt gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="b4b9e-135">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span><br/> <span data-ttu-id="b4b9e-136">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b4b9e-136">This is the default property.</span></span><br/> |
| [<span data-ttu-id="b4b9e-137">**Empfänger**</span><span class="sxs-lookup"><span data-stu-id="b4b9e-137">**Recipients**</span></span>](envelopeddata-recipients.md)<br/> | <span data-ttu-id="b4b9e-138">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b4b9e-138">Read-only</span></span><br/>  | <span data-ttu-id="b4b9e-139">Sammlung von [**Zertifikat**](certificate.md) Objekten, die die eingehüllte Nachricht empfangen.</span><span class="sxs-lookup"><span data-stu-id="b4b9e-139">Collection of [**Certificate**](certificate.md) objects to receive the enveloped message.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="b4b9e-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4b9e-140">Remarks</span></span>

<span data-ttu-id="b4b9e-141">Das **EnvelopedData** -Objekt kann erstellt und ist für die Skripterstellung sicher.</span><span class="sxs-lookup"><span data-stu-id="b4b9e-141">The **EnvelopedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="b4b9e-142">Die ProgID für das **EnvelopedData** -Objekt ist CAPICOM. EnvelopedData. 1.</span><span class="sxs-lookup"><span data-stu-id="b4b9e-142">The ProgID for the **EnvelopedData** object is CAPICOM.EnvelopedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4b9e-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4b9e-143">Requirements</span></span>



| <span data-ttu-id="b4b9e-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4b9e-144">Requirement</span></span> | <span data-ttu-id="b4b9e-145">Wert</span><span class="sxs-lookup"><span data-stu-id="b4b9e-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b9e-146">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b4b9e-146">End of client support</span></span><br/> | <span data-ttu-id="b4b9e-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4b9e-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b4b9e-148">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="b4b9e-148">End of server support</span></span><br/> | <span data-ttu-id="b4b9e-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4b9e-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b4b9e-150">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="b4b9e-150">Redistributable</span></span><br/>       | <span data-ttu-id="b4b9e-151">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="b4b9e-151">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b4b9e-152">DLL</span><span class="sxs-lookup"><span data-stu-id="b4b9e-152">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b4b9e-153"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4b9e-153"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4b9e-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4b9e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4b9e-155">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="b4b9e-155">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
