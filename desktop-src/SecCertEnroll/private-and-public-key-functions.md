---
description: Implementiert die IX509PrivateKey-und IX509PublicKey-Schnittstellen.
ms.assetid: 1358053e-ed4e-4482-b160-5b9b1024c771
title: Funktionen für private und öffentliche Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c1d8ec481c87337e7d7e56cffee47f1f483b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353575"
---
# <a name="private-and-public-key-functions"></a>Funktionen für private und öffentliche Schlüssel

CertEnroll.dll implementiert die [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -und [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) -Schnittstellen. Beispielsweise können Sie die [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Schnittstelle verwenden, um die folgenden Aktionen für einen [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly)auszuführen:

-   Erstellen, öffnen, schließen, importieren, exportieren und Löschen des Schlüssels.
-   Gibt den Algorithmus für [*öffentliche Schlüssel*](/windows/desktop/SecGloss/p-gly)an oder ruft ihn ab.
-   Geben Sie Informationen zum verfügbaren [*Kryptografiedienstanbieter*](/windows/desktop/SecGloss/c-gly) (CSP) an, der den Algorithmus für öffentliche Schlüssel unterstützt, oder rufen Sie
-   Hiermit wird das dem [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly)zugeordnete [*Zertifikat*](/windows/desktop/SecGloss/c-gly) angegeben oder abgerufen.
-   Geben Sie den Namen des [*Schlüssel Containers*](/windows/desktop/SecGloss/k-gly)an, oder rufen Sie ihn ab.
-   Geben Sie eine Beschreibung von und einen anzeigen Amen für den Schlüssel an, oder rufen Sie diese ab.
-   Geben Sie die Export Einschränkungen für einen privaten Schlüssel an, oder rufen Sie diese ab.
-   Gibt einen booleschen Wert an, der angibt, ob der Schlüssel vorhanden ist, oder ruft ihn ab.
-   Geben Sie einen Wert an, der angibt, wie der Schlüssel vor der Verwendung geschützt wird
-   Geben Sie einen Wert an, der angibt, ob der Schlüssel für Signierung, Verschlüsselung oder beides verwendet werden kann, oder rufen Sie ihn ab.
-   Geben Sie einen Wert an, der den spezifischen Zweck für die Verwendung des Schlüssels angibt, oder rufen Sie ihn ab.
-   Geben Sie die Länge des Schlüssels an, oder rufen Sie diese ab.
-   Geben Sie einen Wert an, der angibt, ob der Schlüssel im Kontext eines Computers oder Benutzers verwendet oder gespeichert wird, oder rufen Sie ihn ab.
-   Ruft einen booleschen Wert ab, der angibt, ob der Schlüssel geöffnet wurde.
-   Geben Sie eine persönliche Identifikationsnummer an, um auf einen privaten Schlüssel auf einer [*Smartcard*](/windows/desktop/SecGloss/s-gly)zuzugreifen.
-   Geben Sie den Namen des dem Schlüssel zugeordneten CSP an, oder rufen Sie ihn ab.
-   Geben Sie die [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) für den Schlüssel an, oder rufen Sie Sie ab.

Jeder der folgenden Abschnitte gibt eine Funktion an, die von Xenroll.dll exportiert und zum Verwalten eines [*Kryptografieschlüssels*](/windows/desktop/SecGloss/c-gly)verwendet werden kann. Jedes Thema erläutert auch, wie CertEnroll.dll verwendet wird, um die Funktion zu ersetzen, oder gibt an, dass keine Zuordnung zwischen den beiden Bibliotheken vorhanden ist:

-   [Containernamewstr](#containernamewstr)
-   [Genkeyflags](#genkeyflags)
-   [Getkeylen](#getkeylenex)
-   [Getkeylenex](#getkeylenex)
-   [Getsupportedkeyspec](#getsupportedkeyspec)
-   [KeySpec](#getsupportedkeyspec)
-   [Limitexchangekeyumcipherment](#limitexchangekeytoencipherment)
-   [Pvkdateinamewstr](#pvkfilenamewstr)
-   [Reusehardwarekeyifunableumgennew](#reusehardwarekeyifunabletogennew)
-   [Useexistingkeyset](#useexistingkeyset)
-   [Zugehörige Themen](#related-topics)

## <a name="containernamewstr"></a>Containernamewstr

Die [**containernamewstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_containernamewstr) -Funktion in Xenroll.dll gibt den Namen des [*Schlüssel Containers*](/windows/desktop/SecGloss/k-gly)an oder ruft ihn ab.

Wenn Sie CertEnroll.dll verwenden, können Sie die folgenden Aktionen ausführen, um den Namen eines Schlüssel Containers abzurufen:

1.  Ruft die [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) -Eigenschaft für ein vorhandenes [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt auf.
2.  Rufen Sie die [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) -Methode für die Anforderung auf, die in Schritt 1 zurückgegeben wurde, um die innerste Anforderung abzurufen.
3.  Ruft **QueryInterface** für das [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) -Objekt auf, das von Schritt 2 zum Umwandeln in ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt zurückgegeben wird.
4.  Aufrufen der [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) -Eigenschaft für die PKCS \# 10-Anforderung.
5.  Nennen Sie die [**Containername**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_containername) -Eigenschaft für das [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Objekt, das aus Schritt 4 abgerufen wurde.

## <a name="genkeyflags"></a>Genkeyflags

Die in Xenroll.dll definierte [**genkeyflags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags) -Funktion gibt Flags an oder ruft Sie ab, mit denen ein privates Schlüsselpaar oder ein [*öffentliches/privates Schlüsselpaar*](/windows/desktop/SecGloss/p-gly)generiert wird.

Wenn Sie CertEnroll.dll verwenden, können Sie eine Reihe von verschiedenen Eigenschaften angeben, die bestimmen, wie ein privater Schlüssel erstellt wird. Weitere Informationen finden Sie unter [**Erstellen**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create)von.

## <a name="getkeylen"></a>Getkeylen

Die in Xenroll.dll definierte [**getkeylen**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getkeylen) -Funktion Ruft die maximale oder minimale Schlüsselgröße eines Verschlüsselungsschlüssels ab.

Wenn Sie CertEnroll.dll verwenden, können Sie die [**length**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length) -Eigenschaft für ein [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -oder [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) -Objekt aufrufen, um die Schlüsselgröße in Bits abzurufen.

## <a name="getkeylenex"></a>Getkeylenex

Die in Xenroll.dll definierte [**getkeylenex**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getkeylenex) -Funktion Ruft die maximale oder minimale Schlüsselgröße oder die Inkrement-Länge eines Verschlüsselungsschlüssels ab.

Wenn Sie CertEnroll.dll verwenden, können Sie die [**length**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length) -Eigenschaft für ein [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -oder [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) -Objekt aufrufen, um die Schlüsselgröße in Bits abzurufen. Wenn ein Algorithmus inkrementelle Schlüssellängen unterstützt, können Sie die [**incrementlength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_incrementlength) -Eigenschaft für das [**icspalgorithmusobjekt**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm) aufrufen, um den Inkrementwert abzurufen. Sie können auch die Eigenschaften [**minLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_minlength) und [**MaxLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_maxlength) aufrufen, um die minimale und maximale Schlüsselgröße abzurufen.

## <a name="getsupportedkeyspec"></a>Getsupportedkeyspec

Die in Xenroll.dll definierte Funktion [**getsupportedkeyspec**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getsupportedkeyspec) Ruft einen Wert ab, der angibt, ob ein CSP Exchange-Schlüssel, Signatur Schlüssel oder beides unterstützt.

Wenn Sie CertEnroll.dll verwenden, können Sie die [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) -Eigenschaft für das [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -oder [**icspinformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) -Objekt aufrufen, um die vom Schlüssel unterstützten Vorgänge abzurufen.

## <a name="keyspec"></a>KeySpec

Die in Xenroll.dll definierte [**KeySpec**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_keyspec) -Funktion gibt den Schlüsseltyp an oder ruft ihn ab.

Wenn Sie CertEnroll.dll verwenden, können Sie die [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) -Eigenschaft für ein [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Objekt aufrufen, um die vom Schlüssel unterstützten Vorgänge abzurufen.

## <a name="limitexchangekeytoencipherment"></a>Limitexchangekeyumcipherment

Die in Xenroll.dll definierte [**limitexchangekeytoencipherment**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_limitexchangekeytoencipherment) -Funktion gibt einen booleschen Wert an oder ruft ihn ab, der angibt, ob ein Verschlüsselungsschlüssel nur für Daten oder Schlüssel Chiffrierung verwendet werden kann.

CertEnroll.dll enthält keine direkte Entsprechung für diese Funktion. Sie können jedoch ein annähernd gleichwertiges Ergebnis erzielen, indem Sie ein [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage) -Objekt angeben und es der Zertifikat Anforderung hinzufügen.

## <a name="pvkfilenamewstr"></a>Pvkdateinamewstr

Die in Xenroll.dll definierte [**pvkfileamewstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_pvkfilenamewstr) -Funktion gibt den Namen einer Datei an, die exportierte Schlüssel enthält, oder ruft ihn ab.

Wenn Sie CertEnroll.dll verwenden, können Sie die [**Export**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-export) -Methode für ein [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Objekt zum Exportieren eines Schlüssels in ein **BSTR**-Objekt aufzurufen. Sie können die [**exportpublickey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-exportpublickey) -Methode zum Exportieren des [*öffentlichen Schlüssel*](/windows/desktop/SecGloss/p-gly) Teils eines asymmetrischen Schlüssel Paars abrufen.

## <a name="reusehardwarekeyifunabletogennew"></a>Reusehardwarekeyifunableumgennew

Die in Xenroll.dll definierte [**reusehardwarekeyifunabletogennew**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_reusehardwarekeyifunabletogennew) -Funktion gibt einen booleschen Wert an, der angibt, ob ein vorhandener Schlüssel wieder verwendet wird, wenn beim Generieren eines neuen Schlüssels ein Fehler aufgetreten ist, oder ruft ihn ab.

Wenn Sie CertEnroll.dll verwenden, können Sie die [**initializefromcertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate) -Methode für ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt aufzurufen und einen Wert des [**X509RequestInheritOptions**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions) -Enumerationstyps angeben, um einen vorhandenen privaten Schlüssel wiederzuverwenden.

## <a name="useexistingkeyset"></a>Useexistingkeyset

Die in Xenroll.dll definierte [**useexistingkeyset**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_useexistingkeyset) -Funktion gibt einen booleschen Wert an, der angibt, ob vorhandene Schlüssel verwendet werden sollen, oder ruft ihn ab.

Wenn Sie CertEnroll.dll verwenden, können Sie die [**initializefromcertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate) -Methode für ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt aufzurufen und einen Wert des [**X509RequestInheritOptions**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions) -Enumerationstyps angeben, um vorhandene private und öffentliche Schlüssel wiederzuverwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnung von Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 
