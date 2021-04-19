---
description: Entschlüsselt eine verschlüsselte und codierte Daten Zeichenfolge.
ms.assetid: 7601083d-0adb-48e1-98a7-804a49f71206
title: Verschlüsselteddata. entschlpt-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aa702a5cefc46f6d0cbe5d7e0fba17ff03596b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370558"
---
# <a name="encrypteddatadecrypt-method"></a><span data-ttu-id="356ad-103">Verschlüsselteddata. entschlpt-Methode</span><span class="sxs-lookup"><span data-stu-id="356ad-103">EncryptedData.Decrypt method</span></span>

<span data-ttu-id="356ad-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="356ad-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="356ad-105">Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktionen [**cryptencryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) und [**cryptdecryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) aufzurufen, um Nachrichten zu verschlüsseln und zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="356ad-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="356ad-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="356ad-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="356ad-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="356ad-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="356ad-108">Die **Entschlüsselungsmethode** entschlüsselt eine verschlüsselte und codierte Daten Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="356ad-108">The **Decrypt** method decrypts an encrypted and encoded data string.</span></span> <span data-ttu-id="356ad-109">Die sich daraus ergebenden Klartext-Daten werden zur [**Content**](encrypteddata-content.md) -Eigenschaft des [**verschlüsselteddata**](encrypteddata.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="356ad-109">The resulting plaintext data becomes the [**Content**](encrypteddata-content.md) property of the [**EncryptedData**](encrypteddata.md) object.</span></span> <span data-ttu-id="356ad-110">Das Entschlüsseln des Inhalts schlägt fehl, es sei denn, der geheime Schlüssel, der von der [**setsecret**](encrypteddata-setsecret.md) -Methode festgelegt wird, ist identisch mit dem geheimen Schlüssel, der zum Ableiten des Schlüssels verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="356ad-110">Decryption of the content fails unless the secret, set by the [**SetSecret**](encrypteddata-setsecret.md) method, is exactly the same as the secret used to derive the key used to encrypt the content.</span></span>

## <a name="syntax"></a><span data-ttu-id="356ad-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="356ad-111">Syntax</span></span>


```VB
EncryptedData.Decrypt( _
  ByVal EncryptedMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="356ad-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="356ad-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="356ad-113">" *Verschlüsseltedmessage* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="356ad-113">*EncryptedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="356ad-114">Eine Zeichenfolge, die die verschlüsselten, verschlüsselten Daten enthält, die entschlüsselt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="356ad-114">String that contains the encoded, encrypted data to be decrypted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="356ad-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="356ad-115">Return value</span></span>

<span data-ttu-id="356ad-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="356ad-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="356ad-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="356ad-117">Remarks</span></span>

<span data-ttu-id="356ad-118">Der vom aktuellen geheimen Schlüssel abgeleitete Sitzungsschlüssel wird für die Entschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="356ad-118">The session key derived from the current secret is used for the decryption.</span></span> <span data-ttu-id="356ad-119">Diese Methode erzeugt nicht den richtigen Klartext, es sei denn, das aktuelle Geheimnis stimmt genau mit dem geheimen Schlüssel überein, der zum Verschlüsseln der Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="356ad-119">This method will not produce the correct plaintext unless the current secret exactly matches the secret used to encrypt the message.</span></span>

## <a name="requirements"></a><span data-ttu-id="356ad-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="356ad-120">Requirements</span></span>



| <span data-ttu-id="356ad-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="356ad-121">Requirement</span></span> | <span data-ttu-id="356ad-122">Wert</span><span class="sxs-lookup"><span data-stu-id="356ad-122">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="356ad-123">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="356ad-123">End of client support</span></span><br/> | <span data-ttu-id="356ad-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="356ad-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="356ad-125">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="356ad-125">End of server support</span></span><br/> | <span data-ttu-id="356ad-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="356ad-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="356ad-127">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="356ad-127">Redistributable</span></span><br/>       | <span data-ttu-id="356ad-128">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="356ad-128">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="356ad-129">DLL</span><span class="sxs-lookup"><span data-stu-id="356ad-129">DLL</span></span><br/>                   | <dl> <span data-ttu-id="356ad-130"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="356ad-130"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="356ad-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="356ad-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="356ad-132">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="356ad-132">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="356ad-133">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="356ad-133">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
