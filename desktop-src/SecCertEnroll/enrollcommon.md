---
description: Der Ordner enrollCommon enthält die folgenden Hilfsfunktionen und Makros, die von den Beispielen verwendet werden, die mit dem Certificate Enrollment SDK bereitgestellt werden.
ms.assetid: a9b3532d-9640-4373-a6c6-7828cb6f55c7
title: enrollCommon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ddc05ad1a143de025abbc875c8280a3f419d0e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476016"
---
# <a name="enrollcommon"></a>enrollCommon

Der Ordner enrollCommon enthält die folgenden Hilfsfunktionen und Makros, die von den Beispielen verwendet werden, die mit dem Certificate Enrollment SDK bereitgestellt werden. Sie wird standardmäßig im Ordner *%ProgramFiles%* \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollCommon installiert.




| Funktion | BESCHREIBUNG | 
|----------|-------------|
| _JumpIfError | Makro, das einen <strong>HRESULT-Wert,</strong> eine Bezeichnung und eine Fehlerzeichenfolge akzeptiert, die Zeichenfolge ausgibt und die Programmsteuerung an die erste Anweisung nach der Bezeichnung überträgt. | 
| _JumpError | Entspricht dem _JumpIfError Makro. | 
| _PrintIfError | Derzeit nicht verwendet. | 
| _PrintError | Makro, das eine Fehlermeldung und einen <strong>HRESULT-Wert</strong> aus druckt. | 
| convertWszToSz | Konvertiert eine Breitzeichenfolge mithilfe der <strong>WideCharToMultiByte-Funktion</strong> und des aktuellen ANSI-Codepagebezeichners für das System in eine ASCII-Zeichenfolge. Diese Funktion wird von den funktionen decConvertFromUnicode und findOIDFromTemplateName verwendet, die in enrollCommon.cpp definiert sind. | 
| convertSzToWsz | Konvertiert eine ASCII-Zeichenfolge mithilfe der <strong>MultiByteToWideChar-Funktion</strong> und des aktuellen ANSI-Codepagebezeichners für das System in eine Breitzeichenzeichenfolge. Diese Funktion wird von der findCertByTemplate-Funktion verwendet, die in enrollCommon.cpp definiert ist. | 
| convertSzToBstr | Konvertiert eine ASCII-Zeichenfolge mithilfe der <strong>MultiByteToWideChar-Funktion</strong> in einen <strong>BSTR.</strong> Diese Funktion wird derzeit nicht verwendet. | 
| convertWszToBstr | Konvertiert eine Breitzeichenzeichenfolge in einen <strong>BSTR.</strong> Diese Funktion wird vom InstallResponseFromPFX-Beispiel verwendet. | 
| checkEnrollStatus | Überprüft den Status des Zertifikatregistrierungsprozesses mithilfe der Schnittstellen <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> und <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus.</strong></a> Diese Funktion wird von den Beispielen enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert und enrollSimpleUserCert verwendet. | 
| findCertByKeyUsage | Listet den persönlichen Zertifikatspeicher des aktuellen Benutzers auf, um das erste Zertifikat zu finden, für das die beabsichtigte Verwendung des öffentlichen Schlüssels mit einem angegebenen Wert übereinstimmt. Der angegebene Wert kann eine bitweise Kombination der folgenden Flags sein:<ul><li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li><li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li><li>CERT_KEY_AGREEMENT_KEY_USAGE</li><li>CERT_KEY_CERT_SIGN_KEY_USAGE</li><li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li><li>CERT_NON_REPUDIATION_KEY_USAGE</li><li>CERT_OFFLINE_CRL_SIGN_KEY_USAGE</li></ul>Diese Funktion wird im Beispiel enrollFromPublicKey verwendet.<br /> | 
| findCertByEKU | Listet den persönlichen Zertifikatspeicher des aktuellen Benutzers auf, um das erste Zertifikat zu finden, für das die Erweiterung erweiterte Schlüsselverwendung (Enhanced Key Usage, EKU) mit dem bei der Eingabe angegebenen übereinstimmt. Weitere Informationen zur EKU-Erweiterung finden Sie in der <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage-Schnittstelle.</strong></a> Diese Funktion wird vom beispiel enrollEOBOCMC verwendet. | 
| findCertByTemplate | Listet den persönlichen Zertifikatspeicher des aktuellen Benutzers auf, um das erste Zertifikat zu finden, für das die Vorlage mit dem angegebenen Namen bei der Eingabe übereinstimmt. Diese Funktion wird von den Beispielen enrollPKCS7 und enrollRenewalPKCS7 verwendet. | 
| enrollCertByTemplate | Initialisiert ein <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment-Objekt</strong></a> mithilfe einer Vorlage, versucht, die implizit erstellte Zertifikatanforderung zu registrieren, und überwacht den Status des Registrierungsprozesses. Diese Funktion wird von den Beispielen enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 und enrollRenewalPKCS7 verwendet. | 
| verifyCertContext | Überprüft die Konformität der Zertifikatkette mit der angegebenen (Basis-)Richtlinie und optional mit einer angegebenen Erweiterung für erweiterte Schlüsselverwendung (Enhanced Key Usage, EKU). Weitere Informationen finden Sie unter der <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy-Funktion</strong></a> und den <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA-</strong></a> und <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA-Strukturen.</strong></a> Diese Funktion wird von den Beispielen enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 und enrollRenewalPKCS7 verwendet. | 
| decConvertFromUnicode | Konvertiert eine Zeichenfolge aus Doppel-Byte-Unicode-Zeichen in eine Zeichenfolge von ANSI-Einzel bytezeichen. Diese Funktion wird von der DecodeFileW-Funktion verwendet, die in enrollCommon.cpp definiert ist. | 
| DecodeFileW | Decodiert ein codiertes Zertifikat oder eine Zertifikatanforderungsdatei in ein Bytearray. Diese Funktion wird vom InstallResponseFromPFX-Beispiel verwendet. | 
| EncodeToFileW | Codiert ein Zertifikat oder eine Zertifikatanforderung und speichert es in einer Datei. Diese Funktion wird von den Beispielen createCNGCustomCMC, enrollEOBOCMC und enrollFromPublicKey verwendet. | 
| findOIDFromTemplateName | Ruft den Objektbezeichner für eine durch den Namen angegebene Vorlage ab. Diese Funktion wird von der findCertByTemplate-Funktion verwendet, die in enrollCommon.cpp definiert ist. | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

