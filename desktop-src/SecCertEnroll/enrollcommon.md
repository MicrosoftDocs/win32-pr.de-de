---
description: Der Ordner enrollCommon enthält die folgenden Hilfsfunktionen und Makros, die von den Beispielen im Zertifikatregistrierungs-SDK verwendet werden.
ms.assetid: a9b3532d-9640-4373-a6c6-7828cb6f55c7
title: enrollCommon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d087ce1aeced0ef68f5b33a06546897d09687ae5ccbd096f1bb34552d0a4a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780069"
---
# <a name="enrollcommon"></a>enrollCommon

Der Ordner enrollCommon enthält die folgenden Hilfsfunktionen und Makros, die von den Beispielen im Zertifikatregistrierungs-SDK verwendet werden. Sie wird standardmäßig im Ordner *%ProgramFiles%* \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollCommon installiert.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>_JumpIfError</td>
<td>Makro, das einen <strong>HRESULT-Wert,</strong> eine Bezeichnung und eine Fehlerzeichenfolge akzeptiert, die Zeichenfolge ausgibt und die Programmsteuerung an die erste Anweisung nach der Bezeichnung überträgt.</td>
</tr>
<tr class="even">
<td>_JumpError</td>
<td>Identisch mit dem _JumpIfError Makro.</td>
</tr>
<tr class="odd">
<td>_PrintIfError</td>
<td>Derzeit nicht verwendet.</td>
</tr>
<tr class="even">
<td>_PrintError</td>
<td>Makro, das eine Fehlermeldung und einen <strong>HRESULT-Wert</strong> ausgibt.</td>
</tr>
<tr class="odd">
<td>convertWszToSz</td>
<td>Konvertiert eine Breitzeichenfolge mithilfe der <strong>WideCharToMultiByte-Funktion</strong> und des aktuellen ANSI-Codepagebezeichners für das System in eine ASCII-Zeichenfolge. Diese Funktion wird von den funktionen decConvertFromUnicode und findOIDFromTemplateName verwendet, die in enrollCommon.cpp definiert sind.</td>
</tr>
<tr class="even">
<td>convertSzToWsz</td>
<td>Konvertiert eine ASCII-Zeichenfolge mithilfe der <strong>MultiByteToWideChar-Funktion</strong> und des aktuellen ANSI-Codepagebezeichners für das System in eine Breitzeichenfolge. Diese Funktion wird von der findCertByTemplate-Funktion verwendet, die in enrollCommon.cpp definiert ist.</td>
</tr>
<tr class="odd">
<td>convertSzToBstr</td>
<td>Konvertiert eine ASCII-Zeichenfolge mithilfe der <strong>MultiByteToWideChar-Funktion in</strong> einen <strong>BSTR.</strong> Diese Funktion wird derzeit nicht verwendet.</td>
</tr>
<tr class="even">
<td>convertWszToBstr</td>
<td>Konvertiert eine Breitzeichenzeichenfolge in einen <strong>BSTR.</strong> Diese Funktion wird vom InstallResponseFromPFX-Beispiel verwendet.</td>
</tr>
<tr class="odd">
<td>checkEnrollStatus</td>
<td>Überprüft den Status des Zertifikatregistrierungsprozesses mithilfe der <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>Schnittstellen IX509Enrollment</strong></a> und <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus.</strong></a> Diese Funktion wird von den Beispielen enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert und enrollSimpleUserCert verwendet.</td>
</tr>
<tr class="even">
<td>findCertByKeyUsage</td>
<td>Enumeriert den persönlichen Zertifikatspeicher des aktuellen Benutzers, um das erste Zertifikat zu finden, für das die beabsichtigte Verwendung des öffentlichen Schlüssels einem angegebenen Wert entspricht. Der angegebene Wert kann eine bitweise Kombination der folgenden Flags sein:
<ul>
<li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li>
<li>CERT_KEY_AGREEMENT_KEY_USAGE</li>
<li>CERT_KEY_CERT_SIGN_KEY_USAGE</li>
<li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_NON_REPUDIATION_KEY_USAGE</li>
<li>CERT_OFFLINE_CRL_SIGN_KEY_USAGE</li>
</ul>
Diese Funktion wird vom Beispiel enrollFromPublicKey verwendet.<br/></td>
</tr>
<tr class="odd">
<td>findCertByEKU</td>
<td>Enumeriert den persönlichen Zertifikatspeicher des aktuellen Benutzers, um das erste Zertifikat zu finden, für das die Erweiterung erweiterte Schlüsselverwendung (Enhanced Key Usage, EKU) mit dem in der Eingabe angegebenen Zertifikat ab stimmt. Weitere Informationen zur EKU-Erweiterung finden Sie unter der <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage-Schnittstelle.</strong></a> Diese Funktion wird vom beispiel enrollEOBOCMC verwendet.</td>
</tr>
<tr class="even">
<td>findCertByTemplate</td>
<td>Enumeriert den persönlichen Zertifikatspeicher des aktuellen Benutzers, um bei der Eingabe das erste Zertifikat zu finden, für das die Vorlage dem angegebenen entspricht. Diese Funktion wird von den Beispielen enrollPKCS7 und enrollRenewalPKCS7 verwendet.</td>
</tr>
<tr class="odd">
<td>enrollCertByTemplate</td>
<td>Initialisiert ein <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment-Objekt</strong></a> mithilfe einer Vorlage, versucht, die implizit erstellte Zertifikatanforderung zu registrieren, und überwacht den Status des Registrierungsprozesses. Diese Funktion wird von den Beispielen enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 und enrollRenewalPKCS7 verwendet.</td>
</tr>
<tr class="even">
<td>verifyCertContext</td>
<td>Überprüft die Konformität der Zertifikatkette mit der angegebenen (Basisrichtlinie) und optional mit einer angegebenen Erweiterten Schlüsselverwendungserweiterung (Enhanced Key Usage, EKU). Weitere Informationen finden Sie unter der <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy-Funktion</strong></a> und den CERT_CHAIN_POLICY_PARA <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>und</strong></a> <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> Strukturen. Diese Funktion wird von den Beispielen enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 und enrollRenewalPKCS7 verwendet.</td>
</tr>
<tr class="odd">
<td>decConvertFromUnicode</td>
<td>Konvertiert eine Zeichenfolge aus Doppel-Byte-Unicode-Zeichen in eine Zeichenfolge mit ANSI-Einzel bytezeichen. Diese Funktion wird von der In enrollCommon.cpp definierten DecodeFileW-Funktion verwendet.</td>
</tr>
<tr class="even">
<td>DecodeFileW</td>
<td>Decodiert ein codiertes Zertifikat oder eine Zertifikatanforderungsdatei in ein Bytearray. Diese Funktion wird vom InstallResponseFromPFX-Beispiel verwendet.</td>
</tr>
<tr class="odd">
<td>EncodeToFileW</td>
<td>Codiert ein Zertifikat oder eine Zertifikatanforderung und speichert es in einer Datei. Diese Funktion wird von den Beispielen createCNGCustomCMC, enrollEOBOCMC und enrollFromPublicKey verwendet.</td>
</tr>
<tr class="even">
<td>findOIDFromTemplateName</td>
<td>Ruft den Objektbezeichner für eine vorlage ab, die durch den Namen angegeben wird. Diese Funktion wird von der findCertByTemplate-Funktion verwendet, die in enrollCommon.cpp definiert ist.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

