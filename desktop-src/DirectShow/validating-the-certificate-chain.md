---
description: Überprüfen der Zertifikat Kette
ms.assetid: e0c36f04-1694-40d8-94a1-06ee7de08777
title: Überprüfen der Zertifikat Kette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13436513ae9199feb7ba5fcba399537da198ba85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216780"
---
# <a name="validating-the-certificate-chain"></a>Überprüfen der Zertifikat Kette

In diesem Thema wird beschrieben, wie die Zertifikat Kette des Treibers bei Verwendung des Certified Output Protection Protocol (COPP) überprüft wird.

Die Zertifikat Kette des Grafik Treibers ist ein XML-Dokument. Die Zertifikatskette enthält drei Zertifikate. Das erste Zertifikat wird als *Blatt Zertifikat* bezeichnet und ist das Kopp-Zertifikat des Treibers. Das nächste Zertifikat ist das Signaturzertifikat des unabhängigen Hardware Herstellers (Independent Hardware Vendor, IHV). Das letzte Zertifikat ist das Signaturzertifikat von Microsoft. Um sicherzustellen, dass der Grafiktreiber ein legitimer COPP-Gerät ist, muss die Anwendung alle drei Zertifikate überprüfen. Ein böswilliges Programm kann verhindern, dass COPP funktioniert, wenn eine Anwendung die Zertifikate in der Kette nicht ordnungsgemäß überprüft.

COPP-Zertifikat Ketten verwenden den UTF-8-Zeichensatz. Binärdaten in den Zertifikaten, z. b. der öffentliche RSA-Schlüssel, sind Base64-codiert und in Big-Endian-Reihenfolge gespeichert. (*Big-Endian* bedeutet, dass das signifikanteste Byte am Speicherort mit der niedrigsten Adresse gespeichert wird.)

Einige Elemente innerhalb eines Zertifikats enthalten boolesche Werte, um anzugeben, dass eine Funktion des Zertifikats vorhanden ist. Wenn das Feature vorhanden ist, wird der entsprechende untergeordnete Elementwert auf 1 festgelegt. Wenn keine Funktion vorhanden ist, ist dieses untergeordnete Element nicht im Zertifikat vorhanden.

### <a name="xml-element-definitions"></a>XML-Element Definitionen

Im folgenden finden Sie Definitionen für Elemente im Zertifikat Schema:

-   **Certifi-ecollection**. Das Stamm Element des XML-Dokuments. Sie enthält Zertifikat Elemente, eine für jedes Zertifikat in der Kette.
-   **Zertifikat**. Enthält ein Zertifikat. Dieses Element enthält Daten und Signatur Elemente.
-   **Daten**. Enthält Informationen zum Zertifikat. Insbesondere enthält Sie den öffentlichen Schlüssel des Zertifikats und den Typ. Das Data-Element enthält die folgenden untergeordneten Elemente:
    -   **PublicKey**. Enthält den öffentlichen RSA-Schlüssel des Zertifikats. Das PublicKey-Element enthält ein KeyValue-Element, das ein RSAKeyValue-Element enthält. Das RSAKeyValue-Element verfügt über zwei untergeordnete Elemente, Modulus und Exponent, die den öffentlichen Schlüssel definieren. Die Modulus-und exponentenelemente sind Base64-codiert und in Big-Endian-Reihenfolge gespeichert.
    -   **KeyUsage**. Wenn das Zertifikat das COPP-Zertifikat des Treibers ist, sollte dieses Element ein untergeordnetes Element mit dem Namen "verschlüsseltkey" enthalten. Handelt es sich bei dem Zertifikat um das Signaturzertifikat des IHV oder um das Signaturzertifikat von Microsoft, sollte es ein untergeordnetes Element mit dem Namen signcertificate enthalten. Beide untergeordneten Elemente enthalten boolesche Werte.
    -   **SecurityLevel**. Dieses Element sollte ignoriert werden.
    -   **Manufacturerdata**. Gibt den Hersteller und das Modell des Grafik Geräts an. Dieses Element dient nur zu Informationszwecken.
    -   **Features:** Enthält untergeordnete Elemente, die die Verwendung des Zertifikats angeben. Der einzige für COPP relevante Wert ist das "coppcertificate"-Element. Möglicherweise sind andere untergeordnete Elemente vorhanden. Wenn dies der Fall ist, sollten Sie ignoriert werden. Wenn das Element "coppcertificate" vorhanden ist, ist das Zertifikat ein COPP-Zertifikat. Dieses Element muss im Blattknoten eines gültigen COPP-Zertifikats vorhanden sein. Dieses Element enthält einen booleschen Wert.
-   **Signatur**. Enthält die Signatur für dieses Zertifikat. Sie enthält die folgenden untergeordneten Elemente:
    -   **Signetzdinfo**. Enthält Informationen über die Signatur. Das wichtige untergeordnete Element dieses Elements ist das DigestValue-Element, das den Base64-codierten Wert des SHA-1-Hashs für das Datenelement enthält. Der Digest-Wert wird verwendet, wenn das Zertifikat mit der Zertifikat Sperr Liste (CRL) überprüft wird.
    -   **SignatureValue**. Dieser Wert wird über das Datenelement berechnet und entsprechend dem digitalen rsassa-PSS-Signatur Schema berechnet, das in Public-Key Cryptography Standards (PKCS) \# 1 (Version 2,1) definiert ist. Weitere Informationen zu PKCS \# 1 finden Sie unter [https://www.rsa.com/](https://www.rsa.com/) .
    -   **KeyInfo**. Enthält den öffentlichen RSA-Schlüssel des nächsten Zertifikats in der Kette. Dieses Element wird verwendet, um zu überprüfen, ob die Daten im Datenelement nicht manipuliert wurden. Dieses Element hat das gleiche Format wie das PublicKey-Element.

### <a name="certificate-validation"></a>Zertifikat Überprüfung

Die Anwendung muss die folgenden Schritte ausführen, um die Zertifikat Kette ordnungsgemäß zu validieren. Wenn ein Schritt fehlschlägt oder ein Element, auf das in diesen Prozeduren verwiesen wird, nicht vorhanden ist, schlägt die Validierung fehl.

### <a name="validate-certificate-collection-procedure"></a>Zertifikat Sammlungs Prozedur überprüfen

Führen Sie die folgenden Schritte aus, um die Zertifikatskette zu überprüfen:

1.  Vergewissern Sie sich, dass Certifi-ecollection wohl geformtes XML ist.
2.  Vergewissern Sie sich, dass Certifi-ecollection im UTF-8-Format codiert ist.
3.  Überprüfen Sie, ob das Versions Attribut im Certifi-ecollection-Element 2,0 oder höher ist.
4.  Vergewissern Sie sich, dass die Zertifikat Kette genau drei Zertifikat Elemente enthält.
5.  Durchlaufen Sie die einzelnen Zertifikat Elemente in der Zertifikat Kette, und führen Sie die nachfolgend beschriebene Prozedur zum Überprüfen des Zertifikats aus.

### <a name="validate-certificate-procedure"></a>Zertifikat Prozedur überprüfen

Führen Sie die folgenden Schritte aus, um ein Zertifikat in der Kette zu überprüfen:

1.  Überprüfen Sie, ob keines der untergeordneten Elemente im Datenelement dupliziert ist. Beispielsweise sollte nur ein PublicKey-Element vorhanden sein.
2.  Stellen Sie sicher, dass das Element Data/PublicKey/KeyValue/RSAKeyValue/Modulus vorhanden ist. Der Base64-decodierte Wert muss für alle Zertifikate mit Ausnahme des Stamms 256 Byte lang sein. Im Stamm Zertifikat muss dieses Element 128 Byte lang sein.
3.  Stellen Sie sicher, dass das Element Data/PublicKey/KeyValue/RSAKeyValue/Exponent vorhanden ist. Der Base64-decodierte Wert darf nicht größer als 4 Byte sein.
4.  Wenn dieses Zertifikat das Blatt Zertifikat ist, überprüfen Sie Folgendes:
    -   Das KeyUsage-Element enthält ein verschlüsseltkey-Element mit dem Wert 1.
    -   Das Features-Element enthält ein coppcertificate-Element mit dem Wert 1.
5.  Wenn dieses Zertifikat nicht das Blatt Zertifikat ist, überprüfen Sie Folgendes:
    -   Der Modulo und der Exponent aus dem Data/PublicKey-Element entsprechen exakt dem Modulo und Exponent aus dem Signature/KeyInfo-Element des vorherigen Zertifikats.
    -   Das KeyUsage-Element enthält ein signcertificate-Element mit dem Wert 1.
6.  Verwenden Sie den SHA-1-Hash Algorithmus, um jedes Byte im Datenelement des Zertifikats zu hashen. Jedes Byte vom ersten Zeichen im <Data> Tag bis zum letzten Zeichen im </Data> Endtag sollte Hashwert sein. Der Hashwert wird verwendet, um das Zertifikat anhand der Zertifikat Sperr Liste (CRL) zu überprüfen, wie in [Zertifikat Sperr Listen](certificate-revocation-lists.md) beschrieben.
7.  Vergleichen Sie den Hashwert aus Schritt 6 mit dem Base64-decodierten Wert des Signature/signetdinfo/Reference/DigestValue-Elements. Diese Werte müssen übereinstimmen.
8.  Führen Sie das unten beschriebene Verfahren zum Überprüfen der Signatur aus.
9.  Wenn dieses Zertifikat nicht das endgültige Zertifikat in der Kette ist, speichern Sie den Wert Signature/KeyInfo/KeyValue/RSAKeyValue für die nächste Iterations Schleife.
10. Wenn dieses Zertifikat das endgültige Zertifikat in der Kette ist, stellen Sie sicher, dass der Wert von Signature/KeyInfo/KeyValue/RSAKeyValue mit dem öffentlichen Schlüssel von Microsoft übereinstimmt. Der öffentliche Schlüssel von Microsoft verfügt über die folgenden Base64-codierten Werte:
    -   Modulo

        `pjoeWLSTLDonQG8She6QhkYbYott9fPZ8tHdB128ZETcghn5KHoyin7HkJEcPJ0Eg4UdSv a0KDIYDjA3EXd69R3CN2Wp/QyOo0ZPYWYp3NXpJ700tKPgIplzo5wVd/69g7j+j8M66W7V NmDwaNs9mDc1p2+VVMsDhOsV/Au6E+E=`

    -   Exponent `AQAB`

### <a name="verify-signature-procedure"></a>Signatur Prozedur überprüfen

Der Wert des SignatureValue-Elements wird basierend auf dem digitalen rsassa-PSS-Signatur Schema, das in PKCS \# 1, Version 2,1 (als PKCS bezeichnet) definiert ist, über dem Datenelement berechnet. Um diese Signatur zu überprüfen, führen Sie die folgenden Schritte aus:

1.  Decodieren Sie die Modulus-und Exponent-Werte im Signature/KeyInfo/KeyValue/RSAKeyValue-Element. Diese Werte definieren den öffentlichen RSA-Schlüssel des Signatur Zertifikats.
2.  Decodieren Sie das Signature/SignatureValue-Element.
3.  Berechnen Sie den rsassa-PSS-Verify-Vorgang, der im Abschnitt 8.1.2 of PKCS definiert ist.

Verwenden Sie für den rsassa-PSS-Verify-Vorgang die folgenden Eingaben:

-   (*n*,*e*) ist der öffentliche Schlüssel aus Schritt 1.
-   *M* ist alle Bytes im Datenelement, einschließlich der <Data> -und-</Data> Tags, die das-Element einschließen.
-   *S* ist der decodierte Signatur Wert aus Schritt 2.

Der rsassa-PSS-Verify-Vorgang verwendet den EMSA-PSS-codevorgang, der im Abschnitt 9.1.1 definiert ist. von PKCS. Für diesen Vorgang verwendet COPP die folgenden Optionen:

-   Hash = SHA-1
-   *hlen* = 20
-   MGF (Masken Generierungs Funktion) = MGF1
-   *slen* = 0

Die Masken Generierungs Funktion MGF1 ist in Anhang B. 2 von PKCS definiert. Für diese Funktion verwendet COPP die folgenden Optionen:

-   Hash = SHA-1
-   *hlen* = 20

Die Ausgabe des rsassa-PSS-Verify-Vorgangs gibt an, ob die Signatur gültig oder ungültig ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Certified Output Protection-Protokolls (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



