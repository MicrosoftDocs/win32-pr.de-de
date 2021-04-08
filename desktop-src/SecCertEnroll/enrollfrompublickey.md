---
description: Initialisiert ein PKCS \# 10-Zertifikat Anforderungs Objekt, umschließt es in ein Objekt vom Typ "CMC Request", übermittelt die Anforderung "CMC" an eine Unternehmens Zertifizierungsstelle (Certification Authority, ca) und speichert das von der Zertifizierungsstelle zurückgegebene Zertifikat in einer Datei.
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: Registrierungs frompublickey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21b336d04727f4bb4b90674bad6bb6c429465a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752728"
---
# <a name="enrollfrompublickey"></a>Registrierungs frompublickey

Das Registrierungs frompublickey-Beispiel Initialisiert ein PKCS \# 10-Zertifikat Anforderungs Objekt, umschließt es in ein Objekt vom Typ "CMC Request", sendet die Anforderung "CMC" an eine Unternehmens Zertifizierungsstelle (Certification Authority, ca) und speichert das von der Zertifizierungsstelle zurückgegebene Zertifikat in einer Datei.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner " *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Registrierung \\ VC Registrierungs \\ frompublickey" installiert.

## <a name="discussion"></a>Diskussion

Das Beispiel "anmelfrompublickey":

1.  Verarbeitet die folgenden Befehlszeilenargumente:
    -   Der Name einer Zertifikat Vorlage.
    -   Der Name einer Datei, in der das installierte Zertifikat als Base64-codiertes Bytearray gespeichert werden soll.
    -   Ein optionaler Name der Signaturzertifikat Vorlage. Die Vorlage wird verwendet, um ein Signaturzertifikat zu erstellen, wenn keine im Zertifikat Speicher vorhanden ist.
2.  Erstellt ein privates [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Schlüsselobjekt und ruft die [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) -Methode auf, um mithilfe des standardmäßigen Kryptografieanbieters, der Schlüsselgröße und der [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) -Werte für den aktuellen Computer einen asymmetrischen privaten Schlüssel zu erstellen.
3.  Ruft den Teil des öffentlichen Schlüssels des [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Objekts ab.
4.  Erstellt ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt und initialisiert es mit der in der Befehlszeile angegebenen Vorlage und dem öffentlichen Schlüssel.
5.  Erstellt ein [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt und initialisiert es mit dem PKCS \# 10-Anforderungs Objekt.
6.  Ruft ein vorhandenes Signaturzertifikat ab. wenn es nicht gefunden werden kann, wird von der in der Befehlszeile angegebenen Vorlage eine Zertifikat Anforderung erstellt, und es wird versucht, Sie zu registrieren. Findcertbykeyusage ist in der Datei "registricommon. cpp" definiert.
7.  Überprüft die Zertifikat Kette.
8.  Erstellt ein [**isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) -Objekt, initialisiert es mit dem Signaturzertifikat, ruft die [**isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) -Auflistung aus dem Objekt der CMC-Anforderung ab und fügt das Signaturzertifikat Objekt der Auflistung hinzu.
9.  Codiert die CMC-Anforderung mithilfe von [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der).
10. Erstellt ein [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) -Objekt und verwendet es, um eine Zeichenfolge abzurufen, die die Zertifizierungsstellen Konfiguration enthält.
11. Erstellt ein CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) -Objekt und verwendet es sowie die Zeichen folgen, die die Zertifizierungsstellen Konfiguration enthalten, und die Zertifikat Anforderung zum übermitteln der Anforderung an die Zertifizierungsstelle.
12. Hiermit wird der Status des Registrierungsprozesses überprüft und das installierte Zertifikat in einer Datei gespeichert. Die encodedefilew-Funktion ist in der Datei "registricommon. cpp" definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CMC-Anforderung](cmc-request.md)
</dt> <dt>

[PKCS \# 10-Anforderung](pkcs--10-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 
