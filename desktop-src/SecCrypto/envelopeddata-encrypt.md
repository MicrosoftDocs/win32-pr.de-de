---
description: Generiert einen Sitzungsschlüssel und verschlüsselt und umschließt Daten.
ms.assetid: 7ae0c908-207b-4a74-a195-d12e9e7dec76
title: EnvelopedData. Verschlüsseln-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ecdb665a8e70ff329f25398eb855ff3e82c96cfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373725"
---
# <a name="envelopeddataencrypt-method"></a><span data-ttu-id="26f22-103">EnvelopedData. Verschlüsseln-Methode</span><span class="sxs-lookup"><span data-stu-id="26f22-103">EnvelopedData.Encrypt method</span></span>

<span data-ttu-id="26f22-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="26f22-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="26f22-105">Verwenden Sie stattdessen die [**EnvelopedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="26f22-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="26f22-106">Die Methode " **verschlüsseln** " generiert einen Sitzungsschlüssel, verwendet diesen Schlüssel zum Verschlüsseln des Inhalts, gibt den verschlüsselten Inhalt für jeden Empfänger ein, indem er den Sitzungsschlüssel mit dem öffentlichen Schlüssel jedes Empfängers verschlüsselt und dann das [*BLOB*](../secgloss/b-gly.md) zurückgibt, das den verschlüsselten Inhalt und die verschlüsselten Sitzungsschlüssel als codierte Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="26f22-106">The **Encrypt** method generates a session key, uses that key to encrypt the contents, envelops the encrypted content for each recipient by encrypting the session key with each recipient's public key, and then returns the [*BLOB*](../secgloss/b-gly.md) that contains the encrypted contents and the encrypted session keys as an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f22-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="26f22-107">Syntax</span></span>


```VB
EnvelopedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="26f22-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="26f22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f22-109">*EncodingType* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="26f22-109">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26f22-110">Ein Wert der [**CAPICOM- \_ \_ Codierungstyp**](capicom-encoding-type.md) -Enumeration, der den Codierungstyp angibt, der zum Codieren der eingeschlossenen Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="26f22-110">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the encoding type used to encode the enveloped data.</span></span> <span data-ttu-id="26f22-111">Der Standard Codierungs Wert ist CAPICOM- \_ Codieren \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="26f22-111">The default encoding value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="26f22-112">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="26f22-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="26f22-113">Wert</span><span class="sxs-lookup"><span data-stu-id="26f22-113">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="26f22-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="26f22-114">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="26f22-115"><dt>**CAPICOM \_ Codieren \_ Any**</dt></span><span class="sxs-lookup"><span data-stu-id="26f22-115"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="26f22-116">Dieser Codierungstyp wird nur verwendet, wenn die Eingabedaten einen unbekannten Codierungstyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="26f22-116">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="26f22-117">Wenn dieser Wert verwendet wird, um den Codierungstyp der Ausgabe anzugeben, wird stattdessen der CAPICOM- \_ Code \_ Base64 verwendet.</span><span class="sxs-lookup"><span data-stu-id="26f22-117">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="26f22-118">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="26f22-118">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="26f22-119"><dt>**CAPICOM \_ Codieren \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="26f22-119"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="26f22-120">Daten werden als Base64-codierte Zeichenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="26f22-120">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="26f22-121"><dt>**CAPICOM- \_ Codierung ( \_ Binär)**</dt></span><span class="sxs-lookup"><span data-stu-id="26f22-121"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="26f22-122">Daten werden als reine binäre Sequenz gespeichert.</span><span class="sxs-lookup"><span data-stu-id="26f22-122">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26f22-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26f22-123">Return value</span></span>

<span data-ttu-id="26f22-124">Diese Methode gibt ein BLOB zurück, das die eingeschlossenen Daten in einer codierten Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="26f22-124">This method returns a BLOB that contains the enveloped data in an encoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="26f22-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26f22-125">Remarks</span></span>

<span data-ttu-id="26f22-126">Das zurückgegebene BLOB enthält den verschlüsselten Inhalt und einen verschlüsselten Sitzungsschlüssel für jeden vorgesehenen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="26f22-126">The returned BLOB contains the encrypted content and an encrypted session key for each intended recipient.</span></span> <span data-ttu-id="26f22-127">Diese Sitzungsschlüssel werden mit dem öffentlichen Schlüssel der einzelnen Empfänger verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="26f22-127">These session keys are encrypted using the public key of each recipient.</span></span> <span data-ttu-id="26f22-128">Die verschlüsselten Sitzungsschlüssel können nur mit dem privaten Schlüssel eines Empfängers entschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="26f22-128">The encrypted session keys can be decrypted only with a recipient's private key.</span></span>

<span data-ttu-id="26f22-129">Wenn die Eigenschaft " [**Empfänger**](envelopeddata-recipients.md) " keine Informationen enthält, durchsucht diese Methode den addressbook-Zertifikat Speicher des aktuellen Benutzers nach möglichen Empfängern.</span><span class="sxs-lookup"><span data-stu-id="26f22-129">If the [**Recipients**](envelopeddata-recipients.md) property does not contain any information, this method searches the current user's AddressBook certificate store for potential recipients.</span></span> <span data-ttu-id="26f22-130">Wenn mehr als ein potenzieller Empfänger gefunden wird, wird der Benutzer aufgefordert, im Dialogfeld Auswahl einen Empfänger auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="26f22-130">If more than one potential recipient is found, the user is prompted to select a recipient from a selection dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="26f22-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26f22-131">Requirements</span></span>



| <span data-ttu-id="26f22-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26f22-132">Requirement</span></span> | <span data-ttu-id="26f22-133">Wert</span><span class="sxs-lookup"><span data-stu-id="26f22-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26f22-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="26f22-134">End of client support</span></span><br/> | <span data-ttu-id="26f22-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26f22-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="26f22-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="26f22-136">End of server support</span></span><br/> | <span data-ttu-id="26f22-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26f22-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="26f22-138">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="26f22-138">Redistributable</span></span><br/>       | <span data-ttu-id="26f22-139">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="26f22-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="26f22-140">DLL</span><span class="sxs-lookup"><span data-stu-id="26f22-140">DLL</span></span><br/>                   | <dl> <span data-ttu-id="26f22-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26f22-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26f22-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26f22-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f22-143">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="26f22-143">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="26f22-144">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="26f22-144">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
