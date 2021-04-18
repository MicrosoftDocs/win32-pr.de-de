---
description: Bestimmt, ob die Signaturen für signierte Daten im SignedData-Objekt gültig sind.
ms.assetid: 920ac235-0c1a-4b15-9cdd-c7e0c3ea6107
title: SignedData. Verify-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3cb48943a826296c13df80130171442fc29435f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364817"
---
# <a name="signeddataverify-method"></a><span data-ttu-id="44426-103">SignedData. Verify-Methode</span><span class="sxs-lookup"><span data-stu-id="44426-103">SignedData.Verify method</span></span>

<span data-ttu-id="44426-104">\[Die **Verifizierungs** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="44426-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="44426-105">Verwenden Sie stattdessen die [**SignedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="44426-105">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="44426-106">Die **Verify** -Methode bestimmt, ob die [*Signaturen*](../secgloss/d-gly.md) für signierte Daten im [**SignedData**](signeddata.md) -Objekt gültig sind.</span><span class="sxs-lookup"><span data-stu-id="44426-106">The **Verify** method determines whether the [*signatures*](../secgloss/d-gly.md) on signed data in the [**SignedData**](signeddata.md) object are valid.</span></span> <span data-ttu-id="44426-107">Um eine Signatur zu überprüfen, wird der verschlüsselte [*Hash*](../secgloss/h-gly.md) der Inhalte mithilfe des öffentlichen Schlüssels des Signatur Gebers aus dem Zertifikat des Signatur Gebers entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="44426-107">To verify a signature, the encrypted [*hash*](../secgloss/h-gly.md) of the contents is decrypted by using the signer's public key from the signer's certificate.</span></span> <span data-ttu-id="44426-108">Der entschlüsselte Hash wird mit einem neuen Hash des Daten Inhalts verglichen.</span><span class="sxs-lookup"><span data-stu-id="44426-108">The decrypted hash is compared to a new hash of the data content.</span></span> <span data-ttu-id="44426-109">Eine Signatur ist gültig, wenn die Hashwerte entsprechen.</span><span class="sxs-lookup"><span data-stu-id="44426-109">A signature is valid if the hashes match.</span></span> <span data-ttu-id="44426-110">Außerdem wird mit dieser Methode auch eine Zertifikat Kette erstellt, um die Gültigkeit des Zertifikats zu bestimmen, das den [*öffentlichen Schlüssel*](../secgloss/p-gly.md) zum Entschlüsseln des Hashs bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="44426-110">In addition, this method also builds a certificate chain to determine the validity of the certificate that provides the [*public key*](../secgloss/p-gly.md) used to decrypt the hash.</span></span>

## <a name="syntax"></a><span data-ttu-id="44426-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="44426-111">Syntax</span></span>


```VB
SignedData.Verify( _
  ByVal SignedMessage, _
  [ ByVal bDetached ], _
  [ ByVal VerifyFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="44426-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="44426-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44426-113">*Signedmessage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44426-113">*SignedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44426-114">Eine Zeichenfolge, die die signierte Meldung enthält, die überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="44426-114">A string that contains the signed message to be verified.</span></span>

</dd> <dt>

<span data-ttu-id="44426-115">*bgetrennte* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="44426-115">*bDetached* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44426-116">**True** gibt an, dass die zu Signier enden Daten getrennt sind. Das heißt, der signierte Inhalt ist nicht als Teil des signierten Objekts enthalten.</span><span class="sxs-lookup"><span data-stu-id="44426-116">If **True**, the data to be signed is detached; that is, the content that is signed is not included as part of the signed object.</span></span> <span data-ttu-id="44426-117">Zum Überprüfen der Signatur bei getrennter Inhalte muss eine Anwendung über eine Kopie des ursprünglichen Inhalts verfügen.</span><span class="sxs-lookup"><span data-stu-id="44426-117">To verify the signature on detached content, an application must have a copy of the original content.</span></span> <span data-ttu-id="44426-118">Getrennter Inhalt wird häufig verwendet, um die Größe eines signierten Objekts zu verringern, das über das Internet gesendet werden soll, wenn der Empfänger der signierten Nachricht über eine ursprüngliche Kopie der signierten Daten verfügt.</span><span class="sxs-lookup"><span data-stu-id="44426-118">Detached content is often used to decrease the size of a signed object to be sent across the web, if the recipient of the signed message has an original copy of the signed data.</span></span> <span data-ttu-id="44426-119">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="44426-119">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="44426-120">*Verifyflag* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="44426-120">*VerifyFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44426-121">Ein Wert der [CAPICOM- \_ \_ \_ \_ Flag für signierte Daten](capicom-signed-data-verify-flag.md) Überprüfung, der die Überprüfungs Richtlinie angibt.</span><span class="sxs-lookup"><span data-stu-id="44426-121">A value of the [CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG](capicom-signed-data-verify-flag.md) enumeration that indicates the verification policy.</span></span> <span data-ttu-id="44426-122">Der Standardwert ist CAPICOM \_ Verify \_ Signature \_ und \_ Certificate.</span><span class="sxs-lookup"><span data-stu-id="44426-122">The default value is CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE.</span></span> <span data-ttu-id="44426-123">Wenn Sie diesen Wert verwenden, werden sowohl die Gültigkeit des Zertifikats als auch die Gültigkeit der Signatur überprüft.</span><span class="sxs-lookup"><span data-stu-id="44426-123">Using this value, both the validity of the certificate and the validity of the signature are checked.</span></span> <span data-ttu-id="44426-124">Dieser Parameter kann festgelegt werden, um die Signatur und nicht das Zertifikat zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="44426-124">This parameter may be set to verify the signature and not the certificate.</span></span> <span data-ttu-id="44426-125">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="44426-125">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="44426-126">Wert</span><span class="sxs-lookup"><span data-stu-id="44426-126">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="44426-127">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="44426-127">Meaning</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_VERIFY_SIGNATURE_ONLY"></span><span id="capicom_verify_signature_only"></span><dl> <span data-ttu-id="44426-128"><dt>**nur CAPICOM- \_ Signatur überprüfen \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="44426-128"><dt>**CAPICOM\_VERIFY\_SIGNATURE\_ONLY**</dt></span></span> </dl>                                   | <span data-ttu-id="44426-129">Nur die Signatur wird geprüft.</span><span class="sxs-lookup"><span data-stu-id="44426-129">Only the signature is checked.</span></span><br/>                                                                   |
| <span id="CAPICOM_VERIFY_SIGNATURE_AND_CERTIFICATE"></span><span id="capicom_verify_signature_and_certificate"></span><dl> <span data-ttu-id="44426-130"><dt>**CAPICOM \_ \_ -Signatur \_ und \_ Zertifikat überprüfen**</dt></span><span class="sxs-lookup"><span data-stu-id="44426-130"><dt>**CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE**</dt></span></span> </dl> | <span data-ttu-id="44426-131">Sowohl die Signatur als auch die Gültigkeit des Zertifikats, das zum Erstellen der Signatur verwendet wird, werden überprüft.</span><span class="sxs-lookup"><span data-stu-id="44426-131">Both the signature and the validity of the certificate used to create the signature are checked.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44426-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44426-132">Return value</span></span>

<span data-ttu-id="44426-133">Diese Methode gibt eine Zeichenfolge zurück, die die codierten, signierten Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="44426-133">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="44426-134">Wenn diese Methode fehlschlägt, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="44426-134">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="44426-135">Das **Err** -Objekt enthält zusätzliche Informationen über den Fehler.</span><span class="sxs-lookup"><span data-stu-id="44426-135">The **Err** object will contain additional information about the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="44426-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44426-136">Requirements</span></span>



| <span data-ttu-id="44426-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44426-137">Requirement</span></span> | <span data-ttu-id="44426-138">Wert</span><span class="sxs-lookup"><span data-stu-id="44426-138">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44426-139">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="44426-139">Redistributable</span></span><br/> | <span data-ttu-id="44426-140">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="44426-140">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="44426-141">DLL</span><span class="sxs-lookup"><span data-stu-id="44426-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="44426-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44426-142"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44426-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44426-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44426-144">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="44426-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="44426-145">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="44426-145">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
