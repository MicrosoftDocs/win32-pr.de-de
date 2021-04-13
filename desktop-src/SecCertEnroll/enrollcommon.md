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
# <a name="enrollcommon"></a>gemeinsame Anmeldung

Der Ordner "registrierungscommon" enthält die folgenden Hilfsfunktionen und Makros, die von den mit dem Zertifikatregistrierungs-SDK bereitgestellten Beispielen verwendet werden. Sie wird standardmäßig im Ordner *% Program Files%* \\ Microsoft sdcs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Registrierung VC registrierungscommon installiert \\ \\ .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>_JumpIfError</td>
<td>Ein Makro, das einen <strong>HRESULT</strong> -Wert, eine Bezeichnung und eine Fehler Zeichenfolge akzeptiert, druckt die Zeichenfolge und überträgt die Programmsteuerung an die erste Anweisung, die auf die Bezeichnung folgt.</td>
</tr>
<tr class="even">
<td>_JumpError</td>
<td>Identisch mit dem _JumpIfError-Makro.</td>
</tr>
<tr class="odd">
<td>_PrintIfError</td>
<td>Derzeit nicht verwendet.</td>
</tr>
<tr class="even">
<td>_PrintError</td>
<td>Ein Makro, das eine Fehlermeldung und einen <strong>HRESULT</strong> -Wert ausgibt.</td>
</tr>
<tr class="odd">
<td>convertwszumsz</td>
<td>Konvertiert eine Zeichenfolge mit breit Zeichen in eine ASCII-Zeichenfolge mithilfe der <strong>WideCharToMultiByte</strong> -Funktion und des aktuellen ANSI-Code Page Bezeichners für das System. Diese Funktion wird von den Funktionen decconvertfromunicode und findoidfromtemplatename verwendet, die in der Datei "registricommon. cpp" definiert sind.</td>
</tr>
<tr class="even">
<td>converzztowsz</td>
<td>Konvertiert eine ASCII-Zeichenfolge mithilfe der <strong>multibytedewidechar</strong> -Funktion und des aktuellen ANSI-Code Page Bezeichners für das System in eine Zeichenfolge mit breit Zeichen. Diese Funktion wird von der findcertbytemplate-Funktion verwendet, die in der Datei "registricommon. cpp" definiert ist.</td>
</tr>
<tr class="odd">
<td>converzzumbstr</td>
<td>Konvertiert eine ASCII-Zeichenfolge mit der <strong>multibytetewidechar</strong> -Funktion in ein <strong>BSTR</strong> . Diese Funktion wird zurzeit nicht verwendet.</td>
</tr>
<tr class="even">
<td>convertwszumbstr</td>
<td>Konvertiert eine Zeichenfolge mit breit Zeichen in ein <strong>BSTR</strong>. Diese Funktion wird vom InstallResponse-frompfx-Beispiel verwendet.</td>
</tr>
<tr class="odd">
<td>checkenrollstatus</td>
<td>Überprüft den Status des Zertifikats Registrierungsprozesses mithilfe der <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> -und <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> -Schnittstellen. Diese Funktion wird von den Beispielen "anmelleobocmc", "enrollPKCS7", "enrollRenewalPKCS7", "registrisimplemachinecert" und "registrisimpleusercert" verwendet.</td>
</tr>
<tr class="even">
<td>findcertbykeyusage</td>
<td>Listet den persönlichen Zertifikat Speicher des aktuellen Benutzers auf, um das erste Zertifikat zu finden, für das die beabsichtigte Verwendung des öffentlichen Schlüssels mit einem angegebenen Wert übereinstimmt. Der angegebene Wert kann eine bitweise Kombination der folgenden Flags sein:
<ul>
<li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li>
<li>CERT_KEY_AGREEMENT_KEY_USAGE</li>
<li>CERT_KEY_CERT_SIGN_KEY_USAGE</li>
<li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_NON_REPUDIATION_KEY_USAGE</li>
<li>CERT_OFFLINE_CRL_SIGN_KEY_USAGE</li>
</ul>
Diese Funktion wird durch das Beispiel "anmelfrompublickey" verwendet.<br/></td>
</tr>
<tr class="odd">
<td>findcertbyeku</td>
<td>Listet den persönlichen Zertifikat Speicher des aktuellen Benutzers auf, um das erste Zertifikat zu finden, für das die EKU-Erweiterung (Enhanced Key Usage) mit der in der Eingabe angegebenen übereinstimmt. Weitere Informationen zur EKU-Erweiterung finden Sie unter der <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> -Schnittstelle. Diese Funktion wird von dem Beispiel "Einschreibung-obocmc" verwendet.</td>
</tr>
<tr class="even">
<td>findcertbytemplate</td>
<td>Listet den persönlichen Zertifikat Speicher des aktuellen Benutzers auf, um das erste Zertifikat zu finden, für das die Vorlage mit dem angegebenen Namen bei der Eingabe übereinstimmt. Diese Funktion wird von den enrollPKCS7-und enrollRenewalPKCS7-Beispielen verwendet.</td>
</tr>
<tr class="odd">
<td>"registricertbytemplate"</td>
<td>Initialisiert ein <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> -Objekt mithilfe einer Vorlage, versucht, die implizit erstellte Zertifikat Anforderung zu registrieren, und überwacht den Status des Registrierungsprozesses. Diese Funktion wird von den Beispielen "anmelleobocmc", "Einschreibung frompublickey", "enrollPKCS7" und "enrollRenewalPKCS7" verwendet.</td>
</tr>
<tr class="even">
<td>verifycertcontext</td>
<td>Überprüft die Konformität der Zertifikat Kette mit der angegebenen (Basis-) Richtlinie und optional mit einer angegebenen Erweiterung für erweiterte Schlüssel Verwendung (EKU). Weitere Informationen finden Sie in der <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> -Funktion und in den <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> -und <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> -Strukturen. Diese Funktion wird von den Beispielen "anmelleobocmc", "Einschreibung frompublickey", "enrollPKCS7" und "enrollRenewalPKCS7" verwendet.</td>
</tr>
<tr class="odd">
<td>decconvertfromunicode</td>
<td>Konvertiert eine Zeichenfolge von Doppelbyte-Unicode-Zeichen in eine Zeichenfolge aus Einzel Byte-ANSI-Zeichen. Diese Funktion wird von der decodefilew-Funktion verwendet, die in "registricommon. cpp" definiert ist.</td>
</tr>
<tr class="even">
<td>Decodefilew</td>
<td>Decodiert ein codiertes Zertifikat oder eine Zertifikat Anforderungs Datei in ein Bytearray. Diese Funktion wird vom InstallResponse-frompfx-Beispiel verwendet.</td>
</tr>
<tr class="odd">
<td>Encode-Filew</td>
<td>Codiert ein Zertifikat oder eine Zertifikat Anforderung und speichert es in einer Datei. Diese Funktion wird von den Beispielen "samatecngcustomcmc", "anmelleobocmc" und "Einschreibung frompublickey" verwendet.</td>
</tr>
<tr class="even">
<td>findoidfromtemplatename</td>
<td>Ruft den Objekt Bezeichner für eine durch den Namen angegebene Vorlage ab. Diese Funktion wird von der findcertbytemplate-Funktion verwendet, die in der Datei "registricommon. cpp" definiert ist.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

