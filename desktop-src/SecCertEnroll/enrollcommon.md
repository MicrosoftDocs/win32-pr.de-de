---
description: Der Ordner "registrierungscommon" enthält die folgenden Hilfsfunktionen und Makros, die von den mit dem Zertifikatregistrierungs-SDK bereitgestellten Beispielen verwendet werden.
ms.assetid: a9b3532d-9640-4373-a6c6-7828cb6f55c7
title: gemeinsame Anmeldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384a1f3741fd8bd7762c60da524e2e639c442e41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526999"
---
# <a name="enrollcommon"></a><span data-ttu-id="ff52d-103">gemeinsame Anmeldung</span><span class="sxs-lookup"><span data-stu-id="ff52d-103">enrollCommon</span></span>

<span data-ttu-id="ff52d-104">Der Ordner "registrierungscommon" enthält die folgenden Hilfsfunktionen und Makros, die von den mit dem Zertifikatregistrierungs-SDK bereitgestellten Beispielen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff52d-104">The enrollCommon folder contains the following helper functions and macros used by the samples provided with the Certificate Enrollment SDK.</span></span> <span data-ttu-id="ff52d-105">Sie wird standardmäßig im Ordner *% Program Files%* \\ Microsoft sdcs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Registrierung VC registrierungscommon installiert \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="ff52d-105">It is installed by default in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCommon folder.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff52d-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="ff52d-106">Function</span></span></th>
<th><span data-ttu-id="ff52d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff52d-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff52d-108">_JumpIfError</span><span class="sxs-lookup"><span data-stu-id="ff52d-108">_JumpIfError</span></span></td>
<td><span data-ttu-id="ff52d-109">Ein Makro, das einen <strong>HRESULT</strong> -Wert, eine Bezeichnung und eine Fehler Zeichenfolge akzeptiert, druckt die Zeichenfolge und überträgt die Programmsteuerung an die erste Anweisung, die auf die Bezeichnung folgt.</span><span class="sxs-lookup"><span data-stu-id="ff52d-109">Macro that accepts an <strong>HRESULT</strong> value, a label, and an error string, prints the string, and transfers program control to the first statement following the label.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff52d-110">_JumpError</span><span class="sxs-lookup"><span data-stu-id="ff52d-110">_JumpError</span></span></td>
<td><span data-ttu-id="ff52d-111">Identisch mit dem _JumpIfError-Makro.</span><span class="sxs-lookup"><span data-stu-id="ff52d-111">Same as the _JumpIfError macro.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff52d-112">_PrintIfError</span><span class="sxs-lookup"><span data-stu-id="ff52d-112">_PrintIfError</span></span></td>
<td><span data-ttu-id="ff52d-113">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff52d-113">Not currently used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff52d-114">_PrintError</span><span class="sxs-lookup"><span data-stu-id="ff52d-114">_PrintError</span></span></td>
<td><span data-ttu-id="ff52d-115">Ein Makro, das eine Fehlermeldung und einen <strong>HRESULT</strong> -Wert ausgibt.</span><span class="sxs-lookup"><span data-stu-id="ff52d-115">Macro that prints an error message and an <strong>HRESULT</strong> value.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff52d-116">convertwszumsz</span><span class="sxs-lookup"><span data-stu-id="ff52d-116">convertWszToSz</span></span></td>
<td><span data-ttu-id="ff52d-117">Konvertiert eine Zeichenfolge mit breit Zeichen in eine ASCII-Zeichenfolge mithilfe der <strong>WideCharToMultiByte</strong> -Funktion und des aktuellen ANSI-Code Page Bezeichners für das System.</span><span class="sxs-lookup"><span data-stu-id="ff52d-117">Converts a wide-character string to an ASCII character string by using the <strong>WideCharToMultiByte</strong> function and the current ANSI code-page identifier for the system.</span></span> <span data-ttu-id="ff52d-118">Diese Funktion wird von den Funktionen decconvertfromunicode und findoidfromtemplatename verwendet, die in der Datei "registricommon. cpp" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="ff52d-118">This function is used by the decConvertFromUnicode and findOIDFromTemplateName functions defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff52d-119">converzztowsz</span><span class="sxs-lookup"><span data-stu-id="ff52d-119">convertSzToWsz</span></span></td>
<td><span data-ttu-id="ff52d-120">Konvertiert eine ASCII-Zeichenfolge mithilfe der <strong>multibytedewidechar</strong> -Funktion und des aktuellen ANSI-Code Page Bezeichners für das System in eine Zeichenfolge mit breit Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ff52d-120">Converts an ASCII string to a wide-character string by using the <strong>MultiByteToWideChar</strong> function and the current ANSI code-page identifier for the system.</span></span> <span data-ttu-id="ff52d-121">Diese Funktion wird von der findcertbytemplate-Funktion verwendet, die in der Datei "registricommon. cpp" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ff52d-121">This function is used by the findCertByTemplate function defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff52d-122">converzzumbstr</span><span class="sxs-lookup"><span data-stu-id="ff52d-122">convertSzToBstr</span></span></td>
<td><span data-ttu-id="ff52d-123">Konvertiert eine ASCII-Zeichenfolge mit der <strong>multibytetewidechar</strong> -Funktion in ein <strong>BSTR</strong> .</span><span class="sxs-lookup"><span data-stu-id="ff52d-123">Converts an ASCII string to a <strong>BSTR</strong> by using the <strong>MultiByteToWideChar</strong> function.</span></span> <span data-ttu-id="ff52d-124">Diese Funktion wird zurzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff52d-124">This function is not currently used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff52d-125">convertwszumbstr</span><span class="sxs-lookup"><span data-stu-id="ff52d-125">convertWszToBstr</span></span></td>
<td><span data-ttu-id="ff52d-126">Konvertiert eine Zeichenfolge mit breit Zeichen in ein <strong>BSTR</strong>.</span><span class="sxs-lookup"><span data-stu-id="ff52d-126">Converts a wide-character string to a <strong>BSTR</strong>.</span></span> <span data-ttu-id="ff52d-127">Diese Funktion wird vom InstallResponse-frompfx-Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff52d-127">This function is used by the installResponseFromPFX sample.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff52d-128">checkenrollstatus</span><span class="sxs-lookup"><span data-stu-id="ff52d-128">checkEnrollStatus</span></span></td>
<td><span data-ttu-id="ff52d-129">Überprüft den Status des Zertifikats Registrierungsprozesses mithilfe der <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> -und <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="ff52d-129">Checks the status of the certificate enrollment process by using the <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> and <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> interfaces.</span></span> <span data-ttu-id="ff52d-130">Diese Funktion wird von den Beispielen "anmelleobocmc", "enrollPKCS7", "enrollRenewalPKCS7", "registrisimplemachinecert" und "registrisimpleusercert" verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff52d-130">This function is used by the enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert, and enrollSimpleUserCert samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff52d-131">findcertbykeyusage</span><span class="sxs-lookup"><span data-stu-id="ff52d-131">findCertByKeyUsage</span></span></td>
<td><span data-ttu-id="ff52d-132">Listet den persönlichen Zertifikat Speicher des aktuellen Benutzers auf, um das erste Zertifikat zu finden, für das die beabsichtigte Verwendung des öffentlichen Schlüssels mit einem angegebenen Wert übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="ff52d-132">Enumerates the personal certificate store of the current user to find the first certificate for which the intended use of the public key matches a specified value.</span></span> <span data-ttu-id="ff52d-133">Der angegebene Wert kann eine bitweise Kombination der folgenden Flags sein:</span><span class="sxs-lookup"><span data-stu-id="ff52d-133">The value specified can be a bitwise combination of the following flags:</span></span>
<ul>
<li><span data-ttu-id="ff52d-134">CERT_DATA_ENCIPHERMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="ff52d-134">CERT_DATA_ENCIPHERMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="ff52d-135">CERT_DIGITAL_SIGNATURE_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="ff52d-135">CERT_DIGITAL_SIGNATURE_KEY_USAGE</span></span></li>
<li><span data-ttu-id="ff52d-136">CERT_KEY_AGREEMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="ff52d-136">CERT_KEY_AGREEMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="ff52d-137">CERT_KEY_CERT_SIGN_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="ff52d-137">CERT_KEY_CERT_SIGN_KEY_USAGE</span></span></li>
<li><span data-ttu-id="ff52d-138">CERT_KEY_ENCIPHERMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="ff52d-138">CERT_KEY_ENCIPHERMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="ff52d-139">CERT_NON_REPUDIATION_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="ff52d-139">CERT_NON_REPUDIATION_KEY_USAGE</span></span></li>
<li><span data-ttu-id="ff52d-140">CERT_OFFLINE_CRL_SIGN_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="ff52d-140">CERT_OFFLINE_CRL_SIGN_KEY_USAGE</span></span></li>
</ul>
<span data-ttu-id="ff52d-141">Diese Funktion wird durch das Beispiel "anmelfrompublickey" verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff52d-141">This function is used by the enrollFromPublicKey sample.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff52d-142">findcertbyeku</span><span class="sxs-lookup"><span data-stu-id="ff52d-142">findCertByEKU</span></span></td>
<td><span data-ttu-id="ff52d-143">Listet den persönlichen Zertifikat Speicher des aktuellen Benutzers auf, um das erste Zertifikat zu finden, für das die EKU-Erweiterung (Enhanced Key Usage) mit der in der Eingabe angegebenen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="ff52d-143">Enumerates the personal certificate store of the current user to find the first certificate for which the Enhanced Key Usage (EKU) extension matches that specified on input.</span></span> <span data-ttu-id="ff52d-144">Weitere Informationen zur EKU-Erweiterung finden Sie unter der <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ff52d-144">For more information about the EKU extension, see the <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> interface.</span></span> <span data-ttu-id="ff52d-145">Diese Funktion wird von dem Beispiel "Einschreibung-obocmc" verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff52d-145">This function is used by the enrollEOBOCMC sample.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff52d-146">findcertbytemplate</span><span class="sxs-lookup"><span data-stu-id="ff52d-146">findCertByTemplate</span></span></td>
<td><span data-ttu-id="ff52d-147">Listet den persönlichen Zertifikat Speicher des aktuellen Benutzers auf, um das erste Zertifikat zu finden, für das die Vorlage mit dem angegebenen Namen bei der Eingabe übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="ff52d-147">Enumerates the personal certificate store of the current user to find the first certificate for which the template matches that specified, by name, on input.</span></span> <span data-ttu-id="ff52d-148">Diese Funktion wird von den enrollPKCS7-und enrollRenewalPKCS7-Beispielen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff52d-148">This function is used by the enrollPKCS7 and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff52d-149">"registricertbytemplate"</span><span class="sxs-lookup"><span data-stu-id="ff52d-149">enrollCertByTemplate</span></span></td>
<td><span data-ttu-id="ff52d-150">Initialisiert ein <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> -Objekt mithilfe einer Vorlage, versucht, die implizit erstellte Zertifikat Anforderung zu registrieren, und überwacht den Status des Registrierungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="ff52d-150">Initializes an <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> object by using a template, attempts to enroll the implicitly created certificate request, and monitors the status of the enrollment process.</span></span> <span data-ttu-id="ff52d-151">Diese Funktion wird von den Beispielen "anmelleobocmc", "Einschreibung frompublickey", "enrollPKCS7" und "enrollRenewalPKCS7" verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff52d-151">This function is used by the enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7, and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff52d-152">verifycertcontext</span><span class="sxs-lookup"><span data-stu-id="ff52d-152">verifyCertContext</span></span></td>
<td><span data-ttu-id="ff52d-153">Überprüft die Konformität der Zertifikat Kette mit der angegebenen (Basis-) Richtlinie und optional mit einer angegebenen Erweiterung für erweiterte Schlüssel Verwendung (EKU).</span><span class="sxs-lookup"><span data-stu-id="ff52d-153">Verifies compliance of the certificate chain against the specified (base) policy and, optionally, against a specified Enhanced Key Usage (EKU) extension.</span></span> <span data-ttu-id="ff52d-154">Weitere Informationen finden Sie in der <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> -Funktion und in den <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> -und <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="ff52d-154">For more information, see the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> function and the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> and <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> structures.</span></span> <span data-ttu-id="ff52d-155">Diese Funktion wird von den Beispielen "anmelleobocmc", "Einschreibung frompublickey", "enrollPKCS7" und "enrollRenewalPKCS7" verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff52d-155">This function is used by the enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7, and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff52d-156">decconvertfromunicode</span><span class="sxs-lookup"><span data-stu-id="ff52d-156">decConvertFromUnicode</span></span></td>
<td><span data-ttu-id="ff52d-157">Konvertiert eine Zeichenfolge von Doppelbyte-Unicode-Zeichen in eine Zeichenfolge aus Einzel Byte-ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ff52d-157">Converts a string of double-byte Unicode characters to a string of single-byte ANSI characters.</span></span> <span data-ttu-id="ff52d-158">Diese Funktion wird von der decodefilew-Funktion verwendet, die in "registricommon. cpp" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ff52d-158">This function is used by the DecodeFileW function defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff52d-159">Decodefilew</span><span class="sxs-lookup"><span data-stu-id="ff52d-159">DecodeFileW</span></span></td>
<td><span data-ttu-id="ff52d-160">Decodiert ein codiertes Zertifikat oder eine Zertifikat Anforderungs Datei in ein Bytearray.</span><span class="sxs-lookup"><span data-stu-id="ff52d-160">Decodes an encoded certificate or certificate request file to a byte array.</span></span> <span data-ttu-id="ff52d-161">Diese Funktion wird vom InstallResponse-frompfx-Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff52d-161">This function is used by the installResponseFromPFX sample.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff52d-162">Encode-Filew</span><span class="sxs-lookup"><span data-stu-id="ff52d-162">EncodeToFileW</span></span></td>
<td><span data-ttu-id="ff52d-163">Codiert ein Zertifikat oder eine Zertifikat Anforderung und speichert es in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="ff52d-163">Encodes a certificate or certificate request and saves it to a file.</span></span> <span data-ttu-id="ff52d-164">Diese Funktion wird von den Beispielen "samatecngcustomcmc", "anmelleobocmc" und "Einschreibung frompublickey" verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff52d-164">This function is used by the createCNGCustomCMC, enrollEOBOCMC, and enrollFromPublicKey samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff52d-165">findoidfromtemplatename</span><span class="sxs-lookup"><span data-stu-id="ff52d-165">findOIDFromTemplateName</span></span></td>
<td><span data-ttu-id="ff52d-166">Ruft den Objekt Bezeichner für eine durch den Namen angegebene Vorlage ab.</span><span class="sxs-lookup"><span data-stu-id="ff52d-166">Retrieves the object identifier for a template specified by name.</span></span> <span data-ttu-id="ff52d-167">Diese Funktion wird von der findcertbytemplate-Funktion verwendet, die in der Datei "registricommon. cpp" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ff52d-167">This function is used by the findCertByTemplate function defined in enrollCommon.cpp.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ff52d-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ff52d-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff52d-169">Verwenden der enthaltenen Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff52d-169">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

