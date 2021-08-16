---
description: Initialisiert ein PKCS \# 10-Zertifikatanforderungsobjekt, umschließt es in einem CMC-Anforderungsobjekt, sendet die CMC-Anforderung an eine Unternehmenszertifizierungsstelle und speichert das von der Zertifizierungsstelle zurückgegebene Zertifikat in einer Datei.
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: enrollFromPublicKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0346e2966dc9109ed9413022ead4eda487c37c2ac66ad9da42d2dcee2445032
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780049"
---
# <a name="enrollfrompublickey"></a>enrollFromPublicKey

Das Beispiel enrollFromPublicKey initialisiert ein PKCS \# 10-Zertifikatanforderungsobjekt, umschließt es in einem CMC-Anforderungsobjekt, sendet die CMC-Anforderung an eine Unternehmenszertifizierungsstelle und speichert das von der Zertifizierungsstelle zurückgegebene Zertifikat in einer Datei.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *%ProgramFiles%* \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollFromPublicKey installiert.

## <a name="discussion"></a>Diskussion (Discussion)

Das Beispiel enrollFromPublicKey:

1.  Verarbeitet die folgenden Befehlszeilenargumente:
    -   Der Name einer Zertifikatvorlage.
    -   Der Name einer Datei, in der das installierte Zertifikat als Base64-codiertes Bytearray gespeichert werden soll.
    -   Ein optionaler Name der Signaturzertifikatvorlage. Die Vorlage wird verwendet, um ein Signaturzertifikat zu erstellen, wenn keines im Zertifikatspeicher vorhanden ist.
2.  Erstellt ein privates [**IX509PrivateKey-Schlüsselobjekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) und ruft die [**Create-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) auf, um einen asymmetrischen privaten Schlüssel mithilfe des Standardmäßigen Kryptografieanbieters, der Schlüsselgröße und der [**KeySpec-Werte**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) für den aktuellen Computer zu erstellen.
3.  Ruft den öffentlichen Schlüsselteil des [**IX509PrivateKey-Objekts**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) ab.
4.  Erstellt ein [**IX509CertificateRequestPkcs10-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) und initialisiert es mithilfe der in der Befehlszeile angegebenen Vorlage und des öffentlichen Schlüssels.
5.  Erstellt ein [**IX509CertificateRequestCmc-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) und initialisiert es mithilfe des PKCS \# 10-Anforderungsobjekts.
6.  Ruft ein vorhandenes Signaturzertifikat ab oder erstellt, wenn es nicht gefunden werden kann, eine Zertifikatanforderung aus der in der Befehlszeile angegebenen Vorlage und versucht, es zu registrieren. FindCertByKeyUsage ist in enrollCommon.cpp definiert.
7.  Überprüft die Zertifikatkette.
8.  Erstellt ein [**ISignerCertificate-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) initialisiert es mithilfe des Signaturzertifikats, ruft die [**ISignerCertificates-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) aus dem CMC-Anforderungsobjekt ab und fügt der Auflistung das Signaturzertifikatobjekt hinzu.
9.  Codiert die CMC-Anforderung [*mithilfe*](/windows/desktop/SecGloss/d-gly) von Distinguished Encoding Rules (DER).
10. Erstellt ein [**ICertConfig-Objekt**](/windows/desktop/api/certcli/nn-certcli-icertconfig) und verwendet es, um eine Zeichenfolge abzurufen, die die Zertifizierungsstellenkonfiguration enthält.
11. Erstellt ein [**CryptoAPI-ICertRequest2-Objekt**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) und verwendet es sowie die Zeichenfolgen, die die Zertifizierungsstellenkonfiguration und die Zertifikatanforderung enthalten, um die Anforderung an die Zertifizierungsstelle zu übermitteln.
12. Überprüft den Status des Registrierungsprozesses und speichert das installierte Zertifikat in einer Datei. Die EncodeToFileW-Funktion ist in enrollCommon.cpp definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CMC-Anforderung](cmc-request.md)
</dt> <dt>

[PKCS \# 10-Anforderung](pkcs--10-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 
