---
description: Implementiert die Schnittstellen IX509PrivateKey und IX509PublicKey.
ms.assetid: 1358053e-ed4e-4482-b160-5b9b1024c771
title: Funktionen für private und öffentliche Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6f210393ffaeb676e0190d391692225f25e0cfb4bc3acbcd2c3c188bf40a1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774423"
---
# <a name="private-and-public-key-functions"></a>Funktionen für private und öffentliche Schlüssel

CertEnroll.dll implementiert die [**Schnittstellen IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) und [**IX509PublicKey.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) Sie können beispielsweise die [**IX509PrivateKey-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) verwenden, um die folgenden Aktionen für einen privaten [*Schlüssel durchzuführen:*](/windows/desktop/SecGloss/p-gly)

-   Erstellen, Öffnen, Schließen, Importieren, Exportieren und Löschen des Schlüssels.
-   Geben Sie den Algorithmus für den [*öffentlichen Schlüssel an, oder rufen Sie den Algorithmus ab.*](/windows/desktop/SecGloss/p-gly)
-   Geben Sie Informationen zum verfügbaren Kryptografiedienstanbieter (Cryptographic [*Service Provider,*](/windows/desktop/SecGloss/c-gly) CSP) an, der den Algorithmus für öffentliche Schlüssel unterstützt, oder rufen Sie sie ab.
-   Geben Sie das Zertifikat [*an, das dem*](/windows/desktop/SecGloss/c-gly) privaten Schlüssel zugeordnet ist, [*oder rufen Sie es ab.*](/windows/desktop/SecGloss/p-gly)
-   Geben Sie den Namen des Schlüsselcontainers an, oder [*rufen Sie den Namen ab.*](/windows/desktop/SecGloss/k-gly)
-   Geben Sie eine Beschreibung von und einen Anzeigenamen für den Schlüssel an, oder rufen Sie sie ab.
-   Geben Sie die Exporteinschränkungen für einen privaten Schlüssel an, oder rufen Sie sie ab.
-   Geben Sie einen booleschen Wert an, der angibt, ob der Schlüssel vorhanden ist, oder rufen Sie ihn ab.
-   Geben Sie einen Wert an, der angibt, wie der Schlüssel vor der Verwendung geschützt wird, oder rufen Sie diesen ab.
-   Geben Sie einen Wert an, der angibt, ob der Schlüssel zum Signieren, Verschlüsseln oder beides verwendet werden kann, oder rufen Sie einen Wert ab.
-   Geben Sie einen Wert an, der den spezifischen Zweck identifiziert, für den der Schlüssel verwendet werden kann, oder rufen Sie diesen ab.
-   Geben Sie die Länge des Schlüssels an, oder rufen Sie sie ab.
-   Geben Sie einen Wert an, der angibt, ob der Schlüssel im Kontext eines Computers oder Benutzers verwendet oder gespeichert wird, oder rufen Sie ihn ab.
-   Rufen Sie einen booleschen Wert ab, der angibt, ob der Schlüssel geöffnet wurde.
-   Geben Sie eine persönliche ID für den Zugriff auf einen privaten Schlüssel auf einer [*Smartcard an.*](/windows/desktop/SecGloss/s-gly)
-   Geben Sie den Namen des CSP an, der dem Schlüssel zugeordnet ist, oder rufen Sie diesen ab.
-   Geben Sie die Sicherheitsbeschreibung [*für den Schlüssel an, oder*](/windows/desktop/SecGloss/s-gly) rufen Sie sie ab.

In jedem der folgenden Abschnitte wird eine funktion identifiziert, die von einer Xenroll.dll, die zum Verwalten eines kryptografischen Schlüssels [*verwendet werden kann.*](/windows/desktop/SecGloss/c-gly) In jedem Thema wird auch erläutert, wie sie CertEnroll.dll funktion ersetzen, oder gibt an, dass keine Zuordnung zwischen den beiden Bibliotheken vorhanden ist:

-   [ContainerNameWStr](#containernamewstr)
-   [GenKeyFlags](#genkeyflags)
-   [GetKeyLen](#getkeylenex)
-   [GetKeyLenEx](#getkeylenex)
-   [GetSupportedKeySpec](#getsupportedkeyspec)
-   [KeySpec](#getsupportedkeyspec)
-   [LimitExchangeKeyToEncipherment](#limitexchangekeytoencipherment)
-   [PVKFileNameWStr](#pvkfilenamewstr)
-   [ReuseHardwareKeyIfUnableToGenNew](#reusehardwarekeyifunabletogennew)
-   [UseExistingKeySet](#useexistingkeyset)
-   [Zugehörige Themen](#related-topics)

## <a name="containernamewstr"></a>ContainerNameWStr

Die [**ContainerNameWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_containernamewstr) in Xenroll.dll gibt den Namen des Schlüsselcontainers an oder [*ruft den Namen ab.*](/windows/desktop/SecGloss/k-gly)

Wenn Sie CertEnroll.dll, können Sie die folgenden Aktionen ausführen, um den Namen eines Schlüsselcontainers abzurufen:

1.  Rufen Sie [**die Request-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) für ein [**vorhandenes IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) auf.
2.  Rufen Sie [**die GetInnerRequest-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) für die anforderung auf, die aus Schritt 1 zurückgegeben wurde, um die innerste Anforderung abzurufen.
3.  Rufen **Sie QueryInterface** für [**das ix509CertificateRequest-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) auf, das aus Schritt 2 zurückgegeben wurde, um in ein [**IX509CertificateRequestPkcs10-Objekt zu**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) casten.
4.  Rufen Sie die [**PrivateKey-Eigenschaft**](/windows/desktop/SecCrypto/privatekey) in der PKCS \# 10-Anforderung auf.
5.  Rufen Sie [**die ContainerName-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_containername) für das [**IX509PrivateKey-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) auf, das aus Schritt 4 abgerufen wurde.

## <a name="genkeyflags"></a>GenKeyFlags

Die [**genKeyFlags-Funktion,**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags) die in Xenroll.dll definiert ist, gibt Flags an oder ruft diese ab, die zum Generieren eines privaten Schlüssels oder eines Paars aus öffentlichem und [*privatem Schlüssel verwendet werden.*](/windows/desktop/SecGloss/p-gly)

Wenn Sie CertEnroll.dll, können Sie eine Reihe verschiedener Eigenschaften angeben, die bestimmen, wie ein privater Schlüssel erstellt wird. Weitere Informationen finden Sie unter [**Erstellen von**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create).

## <a name="getkeylen"></a>GetKeyLen

Die in Xenroll.dll definierte [**GetKeyLen-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getkeylen) ruft die maximale oder minimale Schlüsselgröße eines Verschlüsselungsschlüssels ab.

Wenn Sie CertEnroll.dll, können Sie die [**Length-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length) für ein [**IX509PrivateKey-**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) oder [**IX509PublicKey-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) aufrufen, um die Schlüsselgröße in Bits abzurufen.

## <a name="getkeylenex"></a>GetKeyLenEx

Die in Xenroll.dll definierte [**GetKeyLenEx-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getkeylenex) ruft die maximale oder minimale Schlüsselgröße oder die Inkrementlänge eines Verschlüsselungsschlüssels ab.

Wenn Sie CertEnroll.dll, können Sie die [**Length-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length) für ein [**IX509PrivateKey-**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) oder [**IX509PublicKey-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) aufrufen, um die Schlüsselgröße in Bits abzurufen. Wenn ein Algorithmus inkrementelle Schlüssellängen unterstützt, können Sie die [**IncrementLength-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_incrementlength) für das [**ICspAlgorithm-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm) aufrufen, um den Inkrementwert abzurufen. Sie können auch die [**Eigenschaften MinLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_minlength) und [**MaxLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_maxlength) aufrufen, um die minimale und maximale Schlüsselgröße abzurufen.

## <a name="getsupportedkeyspec"></a>GetSupportedKeySpec

Die in Xenroll.dll definierte [**GetSupportedKeySpec-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getsupportedkeyspec) ruft einen Wert ab, der angibt, ob ein CSP Austauschschlüssel, Signaturschlüssel oder beides unterstützt.

Wenn Sie CertEnroll.dll, können Sie die [**KeySpec-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) für die [**IX509PrivateKey-**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) oder [**ICspInformation-Objekte**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) aufrufen, um die vom Schlüssel unterstützten Vorgänge abzurufen.

## <a name="keyspec"></a>KeySpec

Die [**keySpec-Funktion,**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_keyspec) die in Xenroll.dll, gibt den Schlüsseltyp an oder ruft diesen ab.

Wenn Sie CertEnroll.dll, können Sie die [**KeySpec-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) für ein [**IX509PrivateKey-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) aufrufen, um die vom Schlüssel unterstützten Vorgänge abzurufen.

## <a name="limitexchangekeytoencipherment"></a>LimitExchangeKeyToEncipherment

Die in Xenroll.dll definierte [**LimitExchangeKeyToEncipherment-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_limitexchangekeytoencipherment) gibt einen booleschen Wert an oder ruft diesen ab, der angibt, ob ein Verschlüsselungsschlüssel nur für Daten- oder Schlüsselverschlüsselung verwendet werden kann.

CertEnroll.dll enthält keine direkte Entsprechung für diese Funktion. Sie können jedoch ein nahezu gleichwertiges Ergebnis erzielen, indem Sie ein [**IX509ExtensionKeyUsage-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage) angeben und es der Zertifikatanforderung hinzufügen.

## <a name="pvkfilenamewstr"></a>PVKFileNameWStr

Die [**in Xenroll.dll PVKFileNameWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_pvkfilenamewstr) gibt den Namen einer Datei an, die exportierte Schlüssel enthält, oder ruft sie ab.

Wenn Sie CertEnroll.dll, können Sie die [**Export-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-export) für ein [**IX509PrivateKey-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) aufrufen, um einen Schlüssel in einen **BSTR zu exportieren.** Sie können die [**ExportPublicKey-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-exportpublickey) aufrufen, um den öffentlichen Schlüsselteil eines asymmetrischen Schlüsselpaars zu exportieren. [](/windows/desktop/SecGloss/p-gly)

## <a name="reusehardwarekeyifunabletogennew"></a>ReuseHardwareKeyIfUnableToGenNew

Die in Xenroll.dll definierte [**ReuseHardwareKeyIfUnableToGenNew-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_reusehardwarekeyifunabletogennew) gibt einen booleschen Wert an oder ruft diesen ab, der angibt, ob ein vorhandener Schlüssel wiederverwendet wird, wenn beim Generieren eines neuen Schlüssels ein Fehler auftritt.

Wenn Sie CertEnroll.dll verwenden, können Sie die [**InitializeFromCertificate-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate) für ein [**IX509CertificateRequestPkcs10-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) aufrufen und einen Wert des [**X509RequestInheritOptions-Enumerationstyps**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions) angeben, um einen vorhandenen privaten Schlüssel wiederzuverwenden.

## <a name="useexistingkeyset"></a>UseExistingKeySet

Die [**useExistingKeySet-Funktion,**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_useexistingkeyset) die in Xenroll.dll definiert ist, gibt einen booleschen Wert an oder ruft diesen ab, der angibt, ob vorhandene Schlüssel verwendet werden.

Bei Verwendung von CertEnroll.dll können Sie die [**InitializeFromCertificate-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate) für ein [**IX509CertificateRequestPkcs10-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) aufrufen und einen Wert des [**X509RequestInheritOptions-Enumerationstyps**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions) angeben, um vorhandene private und öffentliche Schlüssel wiederzuverwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 
