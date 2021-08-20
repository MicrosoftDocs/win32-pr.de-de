---
description: Überprüfen der Zertifikatkette
ms.assetid: e0c36f04-1694-40d8-94a1-06ee7de08777
title: Überprüfen der Zertifikatkette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c63aab8cca71453aff456f145e8f04affd85b4b1f80aa770cbf589970874f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072134"
---
# <a name="validating-the-certificate-chain"></a>Überprüfen der Zertifikatkette

In diesem Thema wird beschrieben, wie die Zertifikatkette des Treibers bei Verwendung des Certified Output Protection Protocol (COPP) überprüft wird.

Die Zertifikatkette des Grafiktreibers ist ein XML-Dokument. Die Zertifikatkette enthält drei Zertifikate. Das erste Zertifikat wird als *Blattzertifikat bezeichnet* und ist das COPP-Zertifikat des Treibers. Das nächste Zertifikat ist das Signaturzertifikat des unabhängigen Hardwareanbieters (Independent Hardware Vendor, IHV). Das letzte Zertifikat ist das Signaturzertifikat von Microsoft. Um sicherzustellen, dass der Grafiktreiber ein legitimes COPP-Gerät ist, muss die Anwendung alle drei Zertifikate überprüfen. Ein schädliches Programm kann verhindern, dass COPP funktioniert, wenn eine Anwendung die Zertifikate in der Kette nicht ordnungsgemäß überprüft.

COPP-Zertifikatketten verwenden den UTF-8-Zeichensatz. Binäre Daten in den Zertifikaten, z. B. der öffentliche RSA-Schlüssel, werden base64-codiert und in Big-Endian-Reihenfolge gespeichert. (*Big-Endian* bedeutet, dass das wichtigste Byte am Speicherort des Arbeitsspeichers mit der niedrigsten Adresse gespeichert wird.)

Einige Elemente in einem Zertifikat enthalten boolesche Werte, um zu bezeichnen, dass ein Feature des Zertifikats vorhanden ist. Wenn das Feature vorhanden ist, wird der entsprechende Wert des untergeordneten Elements auf 1 festgelegt. Wenn kein Feature vorhanden ist, ist dieses untergeordnete Element nicht im Zertifikat vorhanden.

### <a name="xml-element-definitions"></a>XML-Elementdefinitionen

Im Folgenden finden Sie Definitionen für Elemente im Zertifikatschema:

-   **CertificateCollection**. Das Stammelement des XML-Dokuments. Sie enthält Certificate-Elemente, eines für jedes Zertifikat in der Kette.
-   **Zertifikat**. Enthält ein Zertifikat. Dieses Element enthält Data- und Signature-Elemente.
-   **Daten**. Enthält Informationen zum Zertifikat. Sie enthält insbesondere den öffentlichen Schlüssel und Typ des Zertifikats. Das Data-Element enthält die folgenden untergeordneten Elemente:
    -   **PublicKey**. Enthält den öffentlichen RSA-Schlüssel des Zertifikats. Das PublicKey-Element enthält ein KeyValue-Element, das ein RSAKeyValue-Element enthält. Das RSAKeyValue-Element verfügt über zwei untergeordnete Elemente, Modulus und Exponent, und diese definieren den öffentlichen Schlüssel. Die Modulus- und Exponentenelemente sind Base64-codiert und in Big-Endian-Reihenfolge gespeichert.
    -   **KeyUsage**. Wenn das Zertifikat das COPP-Zertifikat des Treibers ist, sollte dieses Element ein untergeordnetes Element namens EncryptKey enthalten. Wenn das Zertifikat das Signaturzertifikat der IHV oder das Signaturzertifikat von Microsoft ist, sollte es ein untergeordnetes Element namens SignCertificate enthalten. Beide untergeordneten Elemente enthalten boolesche Werte.
    -   **SecurityLevel**. Dieses Element sollte ignoriert werden.
    -   **ManufacturerData**. Gibt den Hersteller und das Modell des Grafikgeräts an. Dieses Element ist nur informationell.
    -   **Features:** Enthält untergeordnete Elemente, die die Verwendung des Zertifikats angeben. Das einzige für COPP relevante Element ist das COPPCertificate-Element. Andere untergeordnete Elemente sind möglicherweise vorhanden. Wenn dies der Dera ist, sollten sie ignoriert werden. Wenn das COPPCertificate-Element vorhanden ist, ist das Zertifikat ein COPP-Zertifikat. Dieses Element muss im Blattknoten eines gültigen COPP-Zertifikats vorhanden sein. Dieses Element enthält einen booleschen Wert.
-   **Signatur.** Enthält die Signatur für dieses Zertifikat. Sie enthält die folgenden untergeordneten Elemente:
    -   **SignedInfo**. Enthält Informationen zur Signatur. Das wichtige untergeordnete Element dieses Elements ist das DigestValue-Element, das den Base64-codierten Wert des SHA-1-Hashs über das Data-Element enthält. Der Digestwert wird verwendet, wenn das Zertifikat mit der Zertifikatsperrliste (Certificate Revocation List, CRL) überprüft wird.
    -   **SignatureValue**. Dieser Wert wird über das Data-Element berechnet und gemäß dem in Public-Key Cryptography Standards (PKCS) \# 1 (Version 2.1) definierten schema für die digitale RSLASS-PSS-Signatur berechnet. Informationen zu PKCS \# 1 finden Sie unter [https://www.rsa.com/](https://www.rsa.com/) .
    -   **KeyInfo**. Enthält den öffentlichen RSA-Schlüssel des nächsten Zertifikats in der Kette. Mit diesem Element wird überprüft, ob die Daten im Data-Element nicht manipuliert wurden. Dieses Element hat das gleiche Format wie das PublicKey-Element.

### <a name="certificate-validation"></a>Zertifikatüberprüfung

Die Anwendung muss die folgenden Schritte ausführen, um die Zertifikatkette ordnungsgemäß zu überprüfen. Wenn ein Schritt fehlschlägt oder kein Element vorhanden ist, auf das in diesen Prozeduren verwiesen wird, schlägt die Überprüfung fehl.

### <a name="validate-certificate-collection-procedure"></a>Überprüfen der Zertifikatsammlungsprozedur

Führen Sie zum Überprüfen der Zertifikatkette die folgenden Schritte aus:

1.  Vergewissern Sie sich, dass certificateCollection wohlgeformte XML-Daten sind.
2.  Stellen Sie sicher, dass die CertificateCollection im UTF-8-Format codiert ist.
3.  Überprüfen Sie, ob das Versionsattribut im CertificateCollection-Element 2.0 oder höher ist.
4.  Stellen Sie sicher, dass die Zertifikatkette genau drei Certificate-Elemente enthält.
5.  Führen Sie eine Schleife durch jedes Certificate-Element in der Zertifikatkette aus, und führen Sie die unten beschriebene Prozedur Zertifikat überprüfen für jedes Element aus.

### <a name="validate-certificate-procedure"></a>Überprüfen der Zertifikatprozedur

Führen Sie die folgenden Schritte aus, um ein Zertifikat in der Kette zu überprüfen:

1.  Stellen Sie sicher, dass keines der untergeordneten Elemente im Data-Element dupliziert ist. Beispielsweise sollte nur ein PublicKey-Element enthalten sein.
2.  Stellen Sie sicher, dass das Data/PublicKey/KeyValue/RSAKeyValue/Modulus-Element vorhanden ist. Der base64-decodierte Wert muss für alle Zertifikate außer dem Stamm 256 Byte lang sein. Im Stammzertifikat muss dieses Element 128 Bytes lang sein.
3.  Stellen Sie sicher, dass das Data/PublicKey/KeyValue/RSAKeyValue/Exponent-Element vorhanden ist. Der base64-decodierte Wert darf nicht größer als 4 Bytes sein.
4.  Wenn es sich bei diesem Zertifikat um das Blattzertifikat handelt, überprüfen Sie Folgendes:
    -   Das KeyUsage-Element enthält ein EncryptKey-Element mit dem Wert 1.
    -   Das Features-Element enthält ein COPPCertificate-Element mit dem Wert 1.
5.  Wenn dieses Zertifikat nicht das Blattzertifikat ist, überprüfen Sie Folgendes:
    -   Der Modulus und exponent aus dem Data/PublicKey-Element passen genau zum Modulus und Exponenten aus dem Signature/KeyInfo-Element des vorherigen Zertifikats.
    -   Das KeyUsage-Element enthält ein SignCertificate-Element mit dem Wert 1.
6.  Verwenden Sie den SHA-1-Hashalgorithmus, um ein Hash für jedes Byte im Data-Element des Zertifikats zu erstellen. Für jedes Byte vom ersten Zeichen im <Data> Tag bis zum letzten </Data> Zeichen im schließenden Tag sollte ein Hashwert verwendet werden. Der Hashwert wird verwendet, um das Zertifikat mit der Zertifikatsperrliste (Certificate Revocation List, CRL) zu überprüfen, wie unter [Zertifikatsperrlisten beschrieben.](certificate-revocation-lists.md)
7.  Vergleichen Sie den Hashwert aus Schritt 6 mit dem base64-decodierten Wert des Signature/SignedInfo/Reference/DigestValue-Elements. Diese Werte müssen übereinstimmen.
8.  Führen Sie die unten beschriebene Prozedur Zum Überprüfen der Signatur aus.
9.  Wenn dieses Zertifikat nicht das endgültige Zertifikat in der Kette ist, speichern Sie den Wert Signature/KeyInfo/KeyValue/RSAKeyValue für die nächste Iteration der Schleife.
10. Wenn dieses Zertifikat das endgültige Zertifikat in der Kette ist, stellen Sie sicher, dass der Wert von Signature/KeyInfo/KeyValue/RSAKeyValue dem öffentlichen Schlüssel von Microsoft entspricht. Der öffentliche Microsoft-Schlüssel verfügt über die folgenden Base64-codierten Werte:
    -   Modul:

        `pjoeWLSTLDonQG8She6QhkYbYott9fPZ8tHdB128ZETcghn5KHoyin7HkJEcPJ0Eg4UdSv a0KDIYDjA3EXd69R3CN2Wp/QyOo0ZPYWYp3NXpJ700tKPgIplzo5wVd/69g7j+j8M66W7V NmDwaNs9mDc1p2+VVMsDhOsV/Au6E+E=`

    -   Exponent: `AQAB`

### <a name="verify-signature-procedure"></a>Überprüfen der Signaturprozedur

Der Wert des SignatureValue-Elements wird über das Data-Element gemäß dem in PKCS 1 Version 2.1 definierten RSATUR-PSS-Schema \# berechnet (nachfolgend als PKCS bezeichnet). Führen Sie die folgenden Schritte aus, um diese Signatur zu überprüfen:

1.  Decodieren Sie die Werte Modulus und Exponent im Signature/KeyInfo/KeyValue/RSAKeyValue-Element. Diese Werte definieren den öffentlichen RSA-Schlüssel des Signaturzertifikats.
2.  Decodieren Sie das Signature/SignatureValue-Element.
3.  Berechnen Sie den RSIMI-PSS-Verify-Vorgang, der in Abschnitt 8.1.2 von PKCS definiert ist.

Verwenden Sie für den RSBAT-PSS-Verify-Vorgang die folgenden Eingaben:

-   (*n*,*e*) ist der öffentliche Schlüssel aus Schritt 1.
-   *M* umfasst alle Bytes im Data-Element, einschließlich der Tags <Data> und</Data> , die das Element einschließen.
-   *S* ist der decodierte Signaturwert aus Schritt 2.

Für den RSTAXI-PSS-Verify-Vorgang wird der emsa-PSS-ENCODE-Vorgang verwendet, der in Abschnitt 9.1.1 definiert ist. von PKCS. Für diesen Vorgang verwendet COPP die folgenden Optionen:

-   Hash = SHA-1
-   *hLen* = 20
-   MGF (Maskengenerierungsfunktion) = MGF1
-   *sLen* = 0

Die Maskengenerierungsfunktion MGF1 ist in Anhang B.2 von PKCS definiert. Für diese Funktion verwendet COPP die folgenden Optionen:

-   Hash = SHA-1
-   *hLen* = 20

Die Ausgabe des RSATUR-PSS-Verify-Vorgangs gibt an, ob die Signatur gültig oder ungültig ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Certified Output Protection Protocol (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



