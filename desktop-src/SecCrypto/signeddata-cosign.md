---
description: Erstellt eine digitale Signatur für zuvor signierten Inhalt.
ms.assetid: c0a3de75-afba-45ba-b701-2729f4495eda
title: SignedData. cosign-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.CoSign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1ab2a24a20fd65fad9622b775bedc59cfa28301a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352125"
---
# <a name="signeddatacosign-method"></a><span data-ttu-id="ec1af-103">SignedData. cosign-Methode</span><span class="sxs-lookup"><span data-stu-id="ec1af-103">SignedData.CoSign method</span></span>

<span data-ttu-id="ec1af-104">\[Die Methode " **cosign** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="ec1af-104">\[The **CoSign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ec1af-105">Verwenden Sie stattdessen die [**SignedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="ec1af-105">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="ec1af-106">Die Methode " **cosign** " erstellt eine [*digitale Signatur*](../secgloss/d-gly.md) für zuvor signierten Inhalt.</span><span class="sxs-lookup"><span data-stu-id="ec1af-106">The **CoSign** method creates a [*digital signature*](../secgloss/d-gly.md) on previously signed content.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec1af-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec1af-107">Syntax</span></span>


```VB
SignedData.CoSign( _
  [ ByVal Signer ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ec1af-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec1af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec1af-109">*Signatur Geber* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ec1af-109">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec1af-110">Ein Verweis auf das [**Signatur**](signer.md) Geber Objekt des Signatur Gebers der Daten.</span><span class="sxs-lookup"><span data-stu-id="ec1af-110">A reference to the [**Signer**](signer.md) object of the signer of the data.</span></span> <span data-ttu-id="ec1af-111">Das **Signatur** Geber Objekt muss Zugriff auf den privaten Schlüssel des Zertifikats haben, das zum Signieren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ec1af-111">The **Signer** object must have access to the private key of the certificate used to sign.</span></span> <span data-ttu-id="ec1af-112">Dieser Parameter kann **null** sein. Weitere Informationen finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="ec1af-112">This parameter can be **NULL**; for more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ec1af-113">*EncodingType* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ec1af-113">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec1af-114">Ein Wert der [**CAPICOM- \_ \_ Codierungstyp**](capicom-encoding-type.md) -Enumeration, der angibt, wie die signierten Daten codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ec1af-114">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates how the signed data is to be encoded.</span></span> <span data-ttu-id="ec1af-115">Der Standardwert ist CAPICOM- \_ Codieren \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="ec1af-115">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="ec1af-116">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="ec1af-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="ec1af-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ec1af-117">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="ec1af-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ec1af-118">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="ec1af-119"><dt>**CAPICOM \_ Codieren \_ Any**</dt></span><span class="sxs-lookup"><span data-stu-id="ec1af-119"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="ec1af-120">Dieser Codierungstyp wird nur verwendet, wenn die Eingabedaten einen unbekannten Codierungstyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ec1af-120">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="ec1af-121">Wenn dieser Wert verwendet wird, um den Codierungstyp der Ausgabe anzugeben, wird stattdessen der CAPICOM- \_ Code \_ Base64 verwendet.</span><span class="sxs-lookup"><span data-stu-id="ec1af-121">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="ec1af-122">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="ec1af-122">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="ec1af-123"><dt>**CAPICOM \_ Codieren \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="ec1af-123"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="ec1af-124">Daten werden als Base64-codierte Zeichenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ec1af-124">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="ec1af-125"><dt>**CAPICOM- \_ Codierung ( \_ Binär)**</dt></span><span class="sxs-lookup"><span data-stu-id="ec1af-125"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="ec1af-126">Daten werden als reine binäre Sequenz gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ec1af-126">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec1af-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec1af-127">Return value</span></span>

<span data-ttu-id="ec1af-128">Diese Methode gibt eine Zeichenfolge zurück, die die codierten, signierten Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="ec1af-128">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="ec1af-129">Wenn diese Methode fehlschlägt, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ec1af-129">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="ec1af-130">Das **Err** -Objekt enthält zusätzliche Informationen über den Fehler.</span><span class="sxs-lookup"><span data-stu-id="ec1af-130">The **Err** object will contain additional information about the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec1af-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec1af-131">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec1af-132">Wenn diese Methode von einem Webskript aufgerufen wird, muss das Skript den [*privaten Schlüssel*](../secgloss/p-gly.md) verwenden, um eine digitale Signatur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec1af-132">When this method is called from a web script, the script needs to use your [*private key*](../secgloss/p-gly.md) to create a digital signature.</span></span> <span data-ttu-id="ec1af-133">Es ist ein Sicherheitsrisiko, nicht vertrauenswürdige Websites den privaten Schlüssel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec1af-133">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="ec1af-134">Wenn diese Methode erstmals aufgerufen wird, wird ein Dialogfeld angezeigt, in dem Sie gefragt werden, ob die Website den privaten Schlüssel verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="ec1af-134">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="ec1af-135">Wenn Sie zulassen, dass das Skript den privaten Schlüssel zum Erstellen einer digitalen Signatur verwendet, und wählen Sie "dieses Dialogfeld nicht mehr anzeigen" aus, wird das Dialogfeld nicht mehr für ein Skript in dieser Domäne angezeigt, das den privaten Schlüssel verwendet, um eine digitale Signatur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec1af-135">If you allow the script to use your private key to create a digital signature and select "Do not show this dialog box again," the dialog box will no longer appear for any script within that domain that uses your private key to create a digital signature.</span></span> <span data-ttu-id="ec1af-136">Skripts außerhalb dieser Domäne, die versuchen, den privaten Schlüssel zum Erstellen einer digitalen Signatur zu verwenden, führen jedoch weiterhin dazu, dass dieses Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ec1af-136">However, scripts outside that domain that attempt to use your private key to create a digital signature will still cause this dialog box to appear.</span></span> <span data-ttu-id="ec1af-137">Wenn Sie das Skript nicht für die Verwendung Ihres privaten Schlüssels zulassen und das Kontrollkästchen Dieses Dialogfeld nicht mehr anzeigen aktivieren, wird die Möglichkeit der Verwendung Ihres privaten Schlüssels für die Erstellung digitaler Signaturen automatisch verweigert.</span><span class="sxs-lookup"><span data-stu-id="ec1af-137">If you do not allow the script to use your private key and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to use your private key to create digital signatures.</span></span>

 

<span data-ttu-id="ec1af-138">Es ist nicht gewährleistet, dass die cosigner in einer bestimmten Reihenfolge vorliegen.</span><span class="sxs-lookup"><span data-stu-id="ec1af-138">Cosigners are not guaranteed to be in any particular order.</span></span>

<span data-ttu-id="ec1af-139">Die folgenden Ergebnisse gelten für den Parameterwert des *Signatur* Gebers:</span><span class="sxs-lookup"><span data-stu-id="ec1af-139">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="ec1af-140">Wenn der *Signatur* Geber Parameter nicht **null** ist, verwendet diese Methode den privaten Schlüssel, auf den das zugehörige Zertifikat zeigt, um die cosignatur zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="ec1af-140">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the cosignature.</span></span> <span data-ttu-id="ec1af-141">Wenn der private Schlüssel, auf den vom Zertifikat verwiesen wird, nicht verfügbar ist, schlägt die Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="ec1af-141">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="ec1af-142">Wenn der *Signatur* Geber Parameter **null** ist und im Speicher des aktuellen Benutzers genau ein Zertifikat vorhanden ist, \_ das Zugriff auf einen privaten Schlüssel hat, wird dieses Zertifikat verwendet, um die cosignatur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec1af-142">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key, that certificate is used to create the cosignature.</span></span>
-   <span data-ttu-id="ec1af-143">Wenn der *Signatur* Geber Parameter den Wert **null** hat, lautet der Wert [**Settings. enablepromptforcertifisineui**](settings-enablepromptforcertificateui.md) Property auf true, und es gibt mehr als ein Zertifikat im aktuellen \_ Benutzer My Store mit einem verfügbaren privaten Schlüssel. Daraufhin wird ein Dialogfeld angezeigt, in dem der Benutzer auswählen kann, welches Zertifikat verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ec1af-143">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="ec1af-144">Wenn der *Signatur* Geber Parameter den Wert **null** hat und die Eigenschaft [**Settings. enablepromptforcertifigateeui**](settings-enablepromptforcertificateui.md) den Wert false hat, schlägt die Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="ec1af-144">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="ec1af-145">Wenn der *Signatur* Geber Parameter **null** ist und im aktuellen \_ Benutzer mein Speicher mit einem verfügbaren privaten Schlüssel kein Zertifikat vorhanden ist, schlägt die Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="ec1af-145">If the *Signer* parameter is **NULL** and there is no certificate in the CURRENT\_USER MY store with an available private key, the method fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec1af-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec1af-146">Requirements</span></span>



| <span data-ttu-id="ec1af-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec1af-147">Requirement</span></span> | <span data-ttu-id="ec1af-148">Wert</span><span class="sxs-lookup"><span data-stu-id="ec1af-148">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec1af-149">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ec1af-149">Redistributable</span></span><br/> | <span data-ttu-id="ec1af-150">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="ec1af-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ec1af-151">DLL</span><span class="sxs-lookup"><span data-stu-id="ec1af-151">DLL</span></span><br/>             | <dl> <span data-ttu-id="ec1af-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec1af-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec1af-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec1af-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec1af-154">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="ec1af-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="ec1af-155">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="ec1af-155">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
