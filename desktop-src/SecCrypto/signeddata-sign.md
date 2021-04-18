---
description: Erstellt eine digitale Signatur für den zu Signier enden Inhalt. Eine digitale Signatur besteht aus einem Hash des zu Signier enden Inhalts, der mit dem privaten Schlüssel des Signatur Gebers verschlüsselt wird.
ms.assetid: ee98a36c-f9a9-4247-ae48-7b1a10b92be4
title: SignedData. Sign-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9f885bb110b51264bc6108ca8c0f881cc48f7710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364819"
---
# <a name="signeddatasign-method"></a><span data-ttu-id="2420d-104">SignedData. Sign-Methode</span><span class="sxs-lookup"><span data-stu-id="2420d-104">SignedData.Sign method</span></span>

<span data-ttu-id="2420d-105">\[Die **Sign** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2420d-105">\[The **Sign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2420d-106">Verwenden Sie stattdessen die [**SignedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="2420d-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="2420d-107">Mit der **Sign** -Methode wird eine [*digitale Signatur*](../secgloss/d-gly.md) für den zu Signier enden Inhalt erstellt.</span><span class="sxs-lookup"><span data-stu-id="2420d-107">The **Sign** method creates a [*digital signature*](../secgloss/d-gly.md) on the content to be signed.</span></span> <span data-ttu-id="2420d-108">Eine digitale Signatur besteht aus einem [*Hash*](../secgloss/h-gly.md) des zu Signier enden Inhalts, der mit dem privaten Schlüssel des Signatur Gebers verschlüsselt wird.</span><span class="sxs-lookup"><span data-stu-id="2420d-108">A digital signature consists of a [*hash*](../secgloss/h-gly.md) of the content to be signed that is encrypted by using the private key of the signer.</span></span> <span data-ttu-id="2420d-109">Diese Methode kann nur verwendet werden, nachdem die [**SignedData. Content**](signeddata-content.md) -Eigenschaft initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2420d-109">This method can only be used after the [**SignedData.Content**](signeddata-content.md) property has been initialized.</span></span> <span data-ttu-id="2420d-110">Wenn die **Sign** -Methode für ein Objekt aufgerufen wird, das bereits über eine Signatur verfügt, wird die alte Signatur ersetzt.</span><span class="sxs-lookup"><span data-stu-id="2420d-110">If the **Sign** method is called on an object that already has a signature, the old signature is replaced.</span></span> <span data-ttu-id="2420d-111">Die Signatur wird mit dem SHA1-Signatur Algorithmus erstellt.</span><span class="sxs-lookup"><span data-stu-id="2420d-111">The signature is created by using the SHA1 signing algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="2420d-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="2420d-112">Syntax</span></span>


```VB
SignedData.Sign( _
  [ ByVal Signer ], _
  [ ByVal bDetached ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2420d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2420d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2420d-114">*Signatur Geber* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2420d-114">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2420d-115">Ein Verweis auf das [**Signatur**](signer.md) Geber Objekt des Signatur Gebers der Daten.</span><span class="sxs-lookup"><span data-stu-id="2420d-115">A reference to the [**Signer**](signer.md) object of the signer of the data.</span></span> <span data-ttu-id="2420d-116">Das **Signatur** Geber Objekt muss Zugriff auf den [*privaten Schlüssel*](../secgloss/p-gly.md) des [*Zertifikats*](../secgloss/c-gly.md) haben, das zum Signieren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2420d-116">The **Signer** object must have access to the [*private key*](../secgloss/p-gly.md) of the [*certificate*](../secgloss/c-gly.md) used to sign.</span></span> <span data-ttu-id="2420d-117">Dieser Parameter kann **null** sein. Weitere Informationen finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="2420d-117">This parameter can be **NULL**; for more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2420d-118">*bgetrennte* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2420d-118">*bDetached* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2420d-119">**True** gibt an, dass die zu Signier enden Daten getrennt sind. Das heißt, der signierte Inhalt ist nicht als Teil des signierten Objekts enthalten.</span><span class="sxs-lookup"><span data-stu-id="2420d-119">If **True**, the data to be signed is detached; that is, the content that is signed is not included as part of the signed object.</span></span> <span data-ttu-id="2420d-120">Zum Überprüfen der Signatur bei getrennter Inhalte muss eine Anwendung über eine Kopie des ursprünglichen Inhalts verfügen.</span><span class="sxs-lookup"><span data-stu-id="2420d-120">To verify the signature on detached content, an application must have a copy of the original content.</span></span> <span data-ttu-id="2420d-121">Getrennter Inhalt wird häufig verwendet, um die Größe eines signierten Objekts zu verringern, das über das Internet gesendet werden soll, wenn der Empfänger der signierten Nachricht über eine ursprüngliche Kopie der signierten Daten verfügt.</span><span class="sxs-lookup"><span data-stu-id="2420d-121">Detached content is often used to decrease the size of a signed object to be sent across the web, if the recipient of the signed message has an original copy of the signed data.</span></span> <span data-ttu-id="2420d-122">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="2420d-122">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="2420d-123">*EncodingType* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2420d-123">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2420d-124">Ein Wert der [CAPICOM- \_ \_ Codierungstyp](capicom-encoding-type.md) -Enumeration, der angibt, wie die signierten Daten codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2420d-124">A value of the [CAPICOM\_ENCODING\_TYPE](capicom-encoding-type.md) enumeration that indicates how the signed data is to be encoded.</span></span> <span data-ttu-id="2420d-125">Der Standardwert ist CAPICOM- \_ Codieren \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="2420d-125">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="2420d-126">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="2420d-126">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="2420d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="2420d-127">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="2420d-128">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2420d-128">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="2420d-129"><dt>**CAPICOM \_ Codieren \_ Any**</dt></span><span class="sxs-lookup"><span data-stu-id="2420d-129"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="2420d-130">Dieser Codierungstyp wird nur verwendet, wenn die Eingabedaten einen unbekannten Codierungstyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2420d-130">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="2420d-131">Wenn dieser Wert verwendet wird, um den Codierungstyp der Ausgabe anzugeben, wird stattdessen der CAPICOM- \_ Code \_ Base64 verwendet.</span><span class="sxs-lookup"><span data-stu-id="2420d-131">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="2420d-132">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="2420d-132">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="2420d-133"><dt>**CAPICOM \_ Codieren \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="2420d-133"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="2420d-134">Daten werden als Base64-codierte Zeichenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2420d-134">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="2420d-135"><dt>**CAPICOM- \_ Codierung ( \_ Binär)**</dt></span><span class="sxs-lookup"><span data-stu-id="2420d-135"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="2420d-136">Daten werden als reine binäre Sequenz gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2420d-136">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2420d-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2420d-137">Return value</span></span>

<span data-ttu-id="2420d-138">Diese Methode gibt eine Zeichenfolge zurück, die die codierten, signierten Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="2420d-138">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="2420d-139">Wenn diese Methode fehlschlägt, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="2420d-139">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="2420d-140">Das **Err** -Objekt enthält zusätzliche Informationen über den Fehler.</span><span class="sxs-lookup"><span data-stu-id="2420d-140">The **Err** object will contain additional information about the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="2420d-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2420d-141">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2420d-142">Wenn diese Methode von einem Webskript aufgerufen wird, muss das Skript den privaten Schlüssel verwenden, um eine digitale Signatur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2420d-142">When this method is called from a web script, the script needs to use your private key to create a digital signature.</span></span> <span data-ttu-id="2420d-143">Es ist ein Sicherheitsrisiko, nicht vertrauenswürdige Websites den privaten Schlüssel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2420d-143">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="2420d-144">Wenn diese Methode erstmals aufgerufen wird, wird ein Dialogfeld angezeigt, in dem Sie gefragt werden, ob die Website den privaten Schlüssel verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="2420d-144">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="2420d-145">Wenn Sie zulassen, dass das Skript den privaten Schlüssel zum Erstellen einer digitalen Signatur verwendet, und wählen Sie "dieses Dialogfeld nicht mehr anzeigen" aus, wird das Dialogfeld nicht mehr für ein Skript in dieser Domäne angezeigt, das den privaten Schlüssel verwendet, um eine digitale Signatur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2420d-145">If you allow the script to use your private key to create a digital signature and select "Do not show this dialog box again," the dialog box will no longer appear for any script within that domain that uses your private key to create a digital signature.</span></span> <span data-ttu-id="2420d-146">Skripts außerhalb dieser Domäne, die versuchen, den privaten Schlüssel zum Erstellen einer digitalen Signatur zu verwenden, führen jedoch weiterhin dazu, dass dieses Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2420d-146">However, scripts outside that domain that attempt to use your private key to create a digital signature will still cause this dialog box to appear.</span></span> <span data-ttu-id="2420d-147">Wenn Sie das Skript nicht für die Verwendung Ihres privaten Schlüssels zulassen und das Kontrollkästchen Dieses Dialogfeld nicht mehr anzeigen aktivieren, wird die Möglichkeit der Verwendung Ihres privaten Schlüssels für die Erstellung digitaler Signaturen automatisch verweigert.</span><span class="sxs-lookup"><span data-stu-id="2420d-147">If you do not allow the script to use your private key and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to use your private key to create digital signatures.</span></span>

 

<span data-ttu-id="2420d-148">Da das Erstellen einer [*digitalen Signatur*](../secgloss/d-gly.md) die Verwendung eines [*privaten Schlüssels*](../secgloss/p-gly.md)erfordert, benötigen webbasierte Anwendungen, die versuchen, diese Methode zu verwenden, Benutzeroberflächen-Eingabe Aufforderungen, die es dem Benutzer ermöglichen, die Verwendung des privaten Schlüssels aus Sicherheitsgründen zu genehmigen.</span><span class="sxs-lookup"><span data-stu-id="2420d-148">Because creating a [*digital signature*](../secgloss/d-gly.md) requires the use of a [*private key*](../secgloss/p-gly.md), web-based applications that attempt to use this method will require user interface prompts that allow the user to approve the use of the private key, for security reasons.</span></span>

<span data-ttu-id="2420d-149">Die folgenden Ergebnisse gelten für den Parameterwert des *Signatur* Gebers:</span><span class="sxs-lookup"><span data-stu-id="2420d-149">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="2420d-150">Wenn der *Signatur* Geber Parameter nicht **null** ist, verwendet diese Methode den privaten Schlüssel, auf den das zugehörige Zertifikat zeigt, um die Signatur zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="2420d-150">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the signature.</span></span> <span data-ttu-id="2420d-151">Wenn der private Schlüssel, auf den vom Zertifikat verwiesen wird, nicht verfügbar ist, schlägt die Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="2420d-151">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="2420d-152">Wenn der *Signatur* Geber Parameter **null** ist und im Speicher des aktuellen Benutzers genau ein Zertifikat vorhanden ist, \_ das auf einen privaten Schlüssel zugreifen kann, wird dieses Zertifikat zum Erstellen der Signatur verwendet.</span><span class="sxs-lookup"><span data-stu-id="2420d-152">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key, that certificate is used to create the signature.</span></span>
-   <span data-ttu-id="2420d-153">Wenn der *Signatur* Geber Parameter den Wert **null** hat, lautet der Wert [**Settings. enablepromptforcertifisineui**](settings-enablepromptforcertificateui.md) Property auf true, und es gibt mehr als ein Zertifikat im aktuellen \_ Benutzer My Store mit einem verfügbaren privaten Schlüssel. Daraufhin wird ein Dialogfeld angezeigt, in dem der Benutzer auswählen kann, welches Zertifikat verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2420d-153">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="2420d-154">Wenn der *Signatur* Geber Parameter den Wert **null** hat und die Eigenschaft [**Settings. enablepromptforcertifigateeui**](settings-enablepromptforcertificateui.md) den Wert false hat, schlägt die Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="2420d-154">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="2420d-155">Wenn der *Signatur* Geber Parameter **null** ist und im aktuellen \_ Benutzer mein Speicher mit einem verfügbaren privaten Schlüssel kein Zertifikat vorhanden ist, schlägt die Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="2420d-155">If the *Signer* parameter is **NULL** and there is no certificate in the CURRENT\_USER MY store with an available private key, the method fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="2420d-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2420d-156">Requirements</span></span>



| <span data-ttu-id="2420d-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2420d-157">Requirement</span></span> | <span data-ttu-id="2420d-158">Wert</span><span class="sxs-lookup"><span data-stu-id="2420d-158">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2420d-159">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="2420d-159">Redistributable</span></span><br/> | <span data-ttu-id="2420d-160">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="2420d-160">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2420d-161">DLL</span><span class="sxs-lookup"><span data-stu-id="2420d-161">DLL</span></span><br/>             | <dl> <span data-ttu-id="2420d-162"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2420d-162"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2420d-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2420d-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2420d-164">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="2420d-164">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="2420d-165">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="2420d-165">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
