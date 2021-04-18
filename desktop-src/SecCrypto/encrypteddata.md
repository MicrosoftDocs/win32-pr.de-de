---
description: Stellt Eigenschaften und Methoden zum Verschlüsseln und Entschlüsseln von Daten mit einem Sitzungsschlüssel bereit, der von einem geheimen Schlüssel abgeleitet ist.
ms.assetid: 3b9bd0a2-6e15-4d58-a682-588a93895799
title: Verschlüsselteddata-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 123e0973343e4990dd2d49cfb321d739085358f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364442"
---
# <a name="encrypteddata-object"></a><span data-ttu-id="47008-103">Verschlüsselteddata-Objekt</span><span class="sxs-lookup"><span data-stu-id="47008-103">EncryptedData object</span></span>

<span data-ttu-id="47008-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="47008-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="47008-105">Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktionen [**cryptencryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) und [**cryptdecryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) aufzurufen, um Nachrichten zu verschlüsseln und zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="47008-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="47008-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="47008-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="47008-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="47008-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="47008-108">Das **verschlüsselteddata** -Objekt stellt Eigenschaften und Methoden zum Verschlüsseln und Entschlüsseln von Daten mit einem [*Sitzungsschlüssel*](../secgloss/s-gly.md) bereit, der von einem geheimen Schlüssel abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="47008-108">The **EncryptedData** object provides properties and methods to encrypt and decrypt data using a [*session key*](../secgloss/s-gly.md) derived from a secret.</span></span>

> [!Note]  
> <span data-ttu-id="47008-109">CAPICOM unterstützt den PKCS \# 7-Inhaltstyp "verschlüsselteddata" nicht, sondern verwendet eine nicht dem Standard entsprechende ASN-Struktur für " **verschlüsselteddata**".</span><span class="sxs-lookup"><span data-stu-id="47008-109">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a nonstandard ASN structure for **EncryptedData**.</span></span> <span data-ttu-id="47008-110">Daher kann nur CAPICOM ein CAPICOM-Objekt " **verschlüsselteddata** " entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="47008-110">Therefore, only CAPICOM can decrypt a CAPICOM **EncryptedData** object.</span></span>

 

## <a name="members"></a><span data-ttu-id="47008-111">Member</span><span class="sxs-lookup"><span data-stu-id="47008-111">Members</span></span>

<span data-ttu-id="47008-112">Das **verschlüsselteddata** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="47008-112">The **EncryptedData** object has these types of members:</span></span>

-   [<span data-ttu-id="47008-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="47008-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="47008-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47008-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="47008-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="47008-115">Methods</span></span>

<span data-ttu-id="47008-116">Das **verschlüsselteddata** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="47008-116">The **EncryptedData** object has these methods.</span></span>



| <span data-ttu-id="47008-117">Methode</span><span class="sxs-lookup"><span data-stu-id="47008-117">Method</span></span>                                       | <span data-ttu-id="47008-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47008-118">Description</span></span>                                                                             |
|:---------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="47008-119">**Entschlüsseln**</span><span class="sxs-lookup"><span data-stu-id="47008-119">**Decrypt**</span></span>](encrypteddata-decrypt.md)     | <span data-ttu-id="47008-120">Entschlüsselt verschlüsselte Inhalte mit dem geheimen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="47008-120">Decrypts encrypted content using the secret.</span></span><br/>                                 |
| [<span data-ttu-id="47008-121">**Verschlüsseln**</span><span class="sxs-lookup"><span data-stu-id="47008-121">**Encrypt**</span></span>](encrypteddata-encrypt.md)     | <span data-ttu-id="47008-122">Verschlüsselt den Inhalt mit dem aktuellen geheimen Schlüssel und Verschlüsselungsalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="47008-122">Encrypts the content using the current secret and encryption algorithm.</span></span><br/>      |
| [<span data-ttu-id="47008-123">**Setsecret**</span><span class="sxs-lookup"><span data-stu-id="47008-123">**SetSecret**</span></span>](encrypteddata-setsecret.md) | <span data-ttu-id="47008-124">Legt den geheimen Schlüssel fest, von dem der Verschlüsselungs-/Entschlüsselungs Sitzungsschlüssel abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="47008-124">Sets the secret from which the encryption/decryption session key is derived.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="47008-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47008-125">Properties</span></span>

<span data-ttu-id="47008-126">Das **verschlüsselteddata** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="47008-126">The **EncryptedData** object has these properties.</span></span>



| <span data-ttu-id="47008-127">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="47008-127">Property</span></span>                                                | <span data-ttu-id="47008-128">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="47008-128">Access type</span></span>           | <span data-ttu-id="47008-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47008-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47008-130">**Algorithmus**</span><span class="sxs-lookup"><span data-stu-id="47008-130">**Algorithm**</span></span>](encrypteddata-algorithm.md)<br/> | <span data-ttu-id="47008-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47008-131">Read-only</span></span><br/>  | <span data-ttu-id="47008-132">Der Algorithmus, der für die Verschlüsselung/Entschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="47008-132">Algorithm used for encryption/decryption.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="47008-133">**Inhalt**</span><span class="sxs-lookup"><span data-stu-id="47008-133">**Content**</span></span>](encrypteddata-content.md)<br/>     | <span data-ttu-id="47008-134">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47008-134">Read/write</span></span><br/> | <span data-ttu-id="47008-135">Der Inhalt, der verschlüsselt oder entschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="47008-135">The content to be encrypted or decrypted.</span></span> <span data-ttu-id="47008-136">Das Festlegen dieser Eigenschaft muss erfolgen, bevor die [**Verschlüsselungs**](encrypteddata-encrypt.md) Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="47008-136">Setting this property must be done before the [**Encrypt**](encrypteddata-encrypt.md) method is called.</span></span> <br/> <span data-ttu-id="47008-137">Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Status*](../secgloss/s-gly.md) des Objekts zurückgesetzt, und alle verschlüsselten Inhalte im Objekt gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="47008-137">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span><br/> <span data-ttu-id="47008-138">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="47008-138">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="47008-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47008-139">Remarks</span></span>

<span data-ttu-id="47008-140">Das Objekt " **verschlüsselteddata** " kann erstellt werden und ist für die Skripterstellung sicher.</span><span class="sxs-lookup"><span data-stu-id="47008-140">The **EncryptedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="47008-141">Die ProgID für das " **verschlüsselteddata** "-Objekt ist "CAPICOM". "Verschlüsselteddata. 1".</span><span class="sxs-lookup"><span data-stu-id="47008-141">The ProgID for the **EncryptedData** object is CAPICOM.EncryptedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="47008-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47008-142">Requirements</span></span>



| <span data-ttu-id="47008-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47008-143">Requirement</span></span> | <span data-ttu-id="47008-144">Wert</span><span class="sxs-lookup"><span data-stu-id="47008-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47008-145">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="47008-145">End of client support</span></span><br/> | <span data-ttu-id="47008-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47008-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="47008-147">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="47008-147">End of server support</span></span><br/> | <span data-ttu-id="47008-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47008-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="47008-149">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="47008-149">Redistributable</span></span><br/>       | <span data-ttu-id="47008-150">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="47008-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="47008-151">DLL</span><span class="sxs-lookup"><span data-stu-id="47008-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="47008-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47008-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47008-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47008-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47008-154">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="47008-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
