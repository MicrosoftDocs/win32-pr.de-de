---
description: Legt den Wert des Geheimnisses fest, der zum Ableiten des kryptografiesitzungsschlüssels verwendet wird, der zum Verschlüsseln und Entschlüsseln von Daten verwendet wird.
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: Verschlüsselteddata. setsecret-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.SetSecret
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c8d30355b022a593ca17519e3ccfa876a5b07b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352847"
---
# <a name="encrypteddatasetsecret-method"></a><span data-ttu-id="08420-103">Verschlüsselteddata. setsecret-Methode</span><span class="sxs-lookup"><span data-stu-id="08420-103">EncryptedData.SetSecret method</span></span>

<span data-ttu-id="08420-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="08420-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="08420-105">Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktionen [**cryptencryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) und [**cryptdecryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) aufzurufen, um Nachrichten zu verschlüsseln und zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="08420-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="08420-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="08420-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="08420-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="08420-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="08420-108">Die **setsecret** -Methode legt den Wert des Geheimnisses fest, der zum Ableiten des [*kryptografiesitzungsschlüssels*](../secgloss/s-gly.md) verwendet wird, der zum Verschlüsseln und Entschlüsseln von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08420-108">The **SetSecret** method sets the value of the secret used to derive the cryptographic [*session key*](../secgloss/s-gly.md) used to encrypt and decrypt data.</span></span>

## <a name="syntax"></a><span data-ttu-id="08420-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="08420-109">Syntax</span></span>


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="08420-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="08420-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08420-111">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08420-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08420-112">Eine Zeichenfolge, die ein Geheimnis enthält, das zum Erstellen eines Sitzungs Kryptografieschlüssels verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="08420-112">A string that contains a secret used to create a session cryptographic key.</span></span>

</dd> <dt>

<span data-ttu-id="08420-113">*Secrettype* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="08420-113">*SecretType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08420-114">Ein Wert der [**CAPICOM \_ Secret \_ Type**](capicom-secret-type.md) -Enumeration, die die Art des Geheimnisses angibt, das zum Generieren des Sitzungsschlüssels verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="08420-114">A value of the [**CAPICOM\_SECRET\_TYPE**](capicom-secret-type.md) enumeration that indicates the kind of secret used to generate the session key.</span></span> <span data-ttu-id="08420-115">Der Standardwert ist CAPICOM \_ Secret \_ Password.</span><span class="sxs-lookup"><span data-stu-id="08420-115">The default value is CAPICOM\_SECRET\_PASSWORD.</span></span> <span data-ttu-id="08420-116">Dieser Parameter kann den folgenden Wert aufweisen:</span><span class="sxs-lookup"><span data-stu-id="08420-116">This parameter can be the following value.</span></span>



| <span data-ttu-id="08420-117">Wert</span><span class="sxs-lookup"><span data-stu-id="08420-117">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="08420-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="08420-118">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <span data-ttu-id="08420-119"><dt>**geheimer CAPICOM- \_ \_ Kennwort**</dt></span><span class="sxs-lookup"><span data-stu-id="08420-119"><dt>**CAPICOM\_SECRET\_PASSWORD**</dt></span></span> </dl> | <span data-ttu-id="08420-120">Der Verschlüsselungsschlüssel muss von einem Kennwort abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="08420-120">The encryption key is to be derived from a password.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08420-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08420-121">Return value</span></span>

<span data-ttu-id="08420-122">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="08420-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="08420-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08420-123">Remarks</span></span>

<span data-ttu-id="08420-124">Der geheime Schlüssel wird zum Erstellen des Sitzungsschlüssels für die Verschlüsselung oder Entschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="08420-124">The secret is used to create the session key for encryption or decryption.</span></span> <span data-ttu-id="08420-125">Für beide Vorgänge muss das gleiche Geheimnis verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08420-125">The same secret must be used for both operations.</span></span> <span data-ttu-id="08420-126">Wenn der geheime Schlüssel für die Datenverschlüsselung verloren geht, können die verschlüsselten Daten nicht entschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="08420-126">If the secret used to encrypt data is lost, the encrypted data cannot be decrypted.</span></span>

<span data-ttu-id="08420-127">Verwenden Sie ggf. " [**cryptprotectmemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) " oder " [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) ", um den geheimen Schlüssel vor und nach der Verwendung zu schützen.</span><span class="sxs-lookup"><span data-stu-id="08420-127">If appropriate for your application, consider using [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) or [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) to protect the secret before and after use.</span></span> <span data-ttu-id="08420-128">Löschen Sie den Arbeitsspeicher, der dem geheimen Schlüssel zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="08420-128">Clear the memory associated with the secret when done.</span></span>

## <a name="requirements"></a><span data-ttu-id="08420-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08420-129">Requirements</span></span>



| <span data-ttu-id="08420-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08420-130">Requirement</span></span> | <span data-ttu-id="08420-131">Wert</span><span class="sxs-lookup"><span data-stu-id="08420-131">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08420-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="08420-132">End of client support</span></span><br/> | <span data-ttu-id="08420-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08420-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="08420-134">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="08420-134">End of server support</span></span><br/> | <span data-ttu-id="08420-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08420-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="08420-136">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="08420-136">Redistributable</span></span><br/>       | <span data-ttu-id="08420-137">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="08420-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="08420-138">DLL</span><span class="sxs-lookup"><span data-stu-id="08420-138">DLL</span></span><br/>                   | <dl> <span data-ttu-id="08420-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08420-139"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08420-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08420-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08420-141">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="08420-141">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="08420-142">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="08420-142">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
