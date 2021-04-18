---
description: Leitet einen Sitzungsschlüssel aus dem geheimen Schlüssel ab und verschlüsselt den Content-Eigenschafts Wert mit diesem Schlüssel. Der verschlüsselte Inhalt wird als codierte Zeichenfolge zurückgegeben.
ms.assetid: aa6f6e6a-208b-4e9c-b530-08673ab9d794
title: Verschlüsselteddata. Verschlüsseln-Methode (InfoCard. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 04d7bf8a337c1bcfa0a024b84304fe50c035f9dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368296"
---
# <a name="encrypteddataencrypt-method"></a><span data-ttu-id="63888-104">Verschlüsselteddata. Verschlüsseln-Methode</span><span class="sxs-lookup"><span data-stu-id="63888-104">EncryptedData.Encrypt method</span></span>

<span data-ttu-id="63888-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="63888-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="63888-106">Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktionen [**cryptencryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) und [**cryptdecryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) aufzurufen, um Nachrichten zu verschlüsseln und zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="63888-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="63888-107">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="63888-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="63888-108">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="63888-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="63888-109">Die Methode **verschlüsseln** leitet einen Sitzungsschlüssel aus dem geheimen Schlüssel ab und verschlüsselt den Eigenschafts Wert [**Content**](encrypteddata-content.md) mit diesem Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="63888-109">The **Encrypt** method derives a session key from the secret and encrypts the [**Content**](encrypteddata-content.md) property value using that key.</span></span> <span data-ttu-id="63888-110">Der verschlüsselte Inhalt wird als codierte Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="63888-110">It returns the encrypted content as an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="63888-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="63888-111">Syntax</span></span>


```VB
EncryptedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="63888-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="63888-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63888-113">*EncodingType* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="63888-113">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="63888-114">Ein Wert der [**CAPICOM- \_ \_ Codierungstyp**](capicom-encoding-type.md) -Enumeration, der den Codierungstyp angibt, der zum Codieren der verschlüsselten Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63888-114">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the encoding type used to encode the encrypted data.</span></span> <span data-ttu-id="63888-115">Der Standardwert ist CAPICOM- \_ Codieren \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="63888-115">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="63888-116">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="63888-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="63888-117">Wert</span><span class="sxs-lookup"><span data-stu-id="63888-117">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="63888-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="63888-118">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="63888-119"><dt>**CAPICOM \_ Codieren \_ Any**</dt></span><span class="sxs-lookup"><span data-stu-id="63888-119"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="63888-120">Dieser Codierungstyp wird nur verwendet, wenn die Eingabedaten einen unbekannten Codierungstyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="63888-120">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="63888-121">Wenn dieser Wert verwendet wird, um den Codierungstyp der Ausgabe anzugeben, wird stattdessen der CAPICOM- \_ Code \_ Base64 verwendet.</span><span class="sxs-lookup"><span data-stu-id="63888-121">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="63888-122">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="63888-122">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="63888-123"><dt>**CAPICOM \_ Codieren \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="63888-123"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="63888-124">Daten werden als Base64-codierte Zeichenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="63888-124">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="63888-125"><dt>**CAPICOM- \_ Codierung ( \_ Binär)**</dt></span><span class="sxs-lookup"><span data-stu-id="63888-125"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="63888-126">Daten werden als reine binäre Sequenz gespeichert.</span><span class="sxs-lookup"><span data-stu-id="63888-126">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63888-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63888-127">Return value</span></span>

<span data-ttu-id="63888-128">Eine Zeichenfolge, die verschlüsselte, codierte Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="63888-128">A string that contains the encrypted, encoded data.</span></span>

## <a name="remarks"></a><span data-ttu-id="63888-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63888-129">Remarks</span></span>

<span data-ttu-id="63888-130">Legen Sie vor dem Aufrufen der **Verschlüsselungs** Methode die [**Content**](encrypteddata-content.md) -Eigenschaft fest, und rufen Sie die [**setsecret**](encrypteddata-setsecret.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="63888-130">Before calling the **Encrypt** method, set the [**Content**](encrypteddata-content.md) property and call the [**SetSecret**](encrypteddata-setsecret.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="63888-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63888-131">Requirements</span></span>



| <span data-ttu-id="63888-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63888-132">Requirement</span></span> | <span data-ttu-id="63888-133">Wert</span><span class="sxs-lookup"><span data-stu-id="63888-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63888-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="63888-134">End of client support</span></span><br/> | <span data-ttu-id="63888-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63888-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="63888-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="63888-136">End of server support</span></span><br/> | <span data-ttu-id="63888-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63888-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="63888-138">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="63888-138">Redistributable</span></span><br/>       | <span data-ttu-id="63888-139">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="63888-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="63888-140">Header</span><span class="sxs-lookup"><span data-stu-id="63888-140">Header</span></span><br/>                | <dl> <span data-ttu-id="63888-141"><dt>InfoCard. h</dt></span><span class="sxs-lookup"><span data-stu-id="63888-141"><dt>Infocard.h</dt></span></span> </dl>  |
| <span data-ttu-id="63888-142">DLL</span><span class="sxs-lookup"><span data-stu-id="63888-142">DLL</span></span><br/>                   | <dl> <span data-ttu-id="63888-143"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63888-143"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63888-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63888-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63888-145">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="63888-145">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="63888-146">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="63888-146">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
