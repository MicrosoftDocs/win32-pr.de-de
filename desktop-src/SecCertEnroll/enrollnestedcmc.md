---
description: Liest eine vorhandene CMC-Zertifikat Anforderung aus einer Datei, umschließt Sie in eine andere CMC-Anforderung, signiert diese äußere Anforderung, sendet Sie an eine Zertifizierungsstelle (Certification Authority, ca) und speichert die Zertifikats Antwort von der Zertifizierungsstelle in einer Datei.
ms.assetid: b1a9161d-1f9a-4c5b-acd2-6058dc65a258
title: registrinetstedcmc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1df25a1bc7f6ce16a67f66ff58dc371a526813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214404"
---
# <a name="enrollnestedcmc"></a>registrinetstedcmc

Das Beispiel "registrinetstedcmc" liest eine vorhandene CMC-Zertifikat Anforderung aus einer Datei, umschließt Sie in eine andere CMC-Anforderung, signiert diese äußere Anforderung, sendet Sie an eine Zertifizierungsstelle (Certification Authority, ca) und speichert die Zertifikats Antwort von der Zertifizierungsstelle in einer Datei.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ X509 Certificate registriment \\ VC \\ registrierungsregistrierungs Ordner installiert.

## <a name="discussion"></a>Diskussion

Das Beispiel "registrinetstedcmc":

1.  Verarbeitet die folgenden Befehlszeilenargumente:
    -   Der Name der Eingabedatei.
    -   Der Name der Ausgabedatei.
    -   Eine optionale Anforderungs Vorlage.
2.  Liest eine vorhandene CMC-Anforderung aus einer Datei als base63-codiertes Bytearray, konvertiert das Bytearray in ein **BSTR**, erstellt ein [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt und verwendet **BSTR** , um das Anforderungs Objekt zu initialisieren. Das initialisierte-Objekt wird zum inneren Request.
3.  Verwendet das interne Anforderungs Objekt, das im vorherigen Schritt erstellt und initialisiert wurde, um eine andere CMC-Anforderung zu initialisieren.
4.  Ruft ein vorhandenes Signaturzertifikat ab. wenn es nicht gefunden werden kann, wird von der in der Befehlszeile angegebenen Vorlage eine Zertifikat Anforderung erstellt, und es wird versucht, Sie zu registrieren. Die Funktionen "findcertbytemplate" und "registricertbytemplate" sind in der Datei "registricommon. cpp" definiert.
5.  Ruft die [**isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) -Auflistung aus der äußeren CMC-Anforderung ab, erstellt ein neues [**isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) -Objekt, initialisiert es mit dem abgerufenen Signaturzertifikat und fügt es der Auflistung hinzu.
6.  Codiert die CMC-Anforderung mithilfe von Distinguished Encoding Rules (der) und ruft die Anforderung als **BSTR** ab.
7.  Erstellt ein [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) -Objekt und verwendet es, um eine Zeichenfolge abzurufen, die die Zertifizierungsstellen Konfiguration enthält.
8.  Erstellt ein CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) -Objekt und verwendet es sowie die Zeichen folgen, die die Zertifizierungsstellen Konfiguration enthalten, und die Zertifikat Anforderung zum übermitteln der Anforderung an die Zertifizierungsstelle.
9.  Hiermit wird der Status des Registrierungsprozesses überprüft und die Zertifikats Antwort der Zertifizierungsstelle in einer Datei gespeichert. Die encodedefilew-Funktion ist in der Datei "registricommon. cpp" definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CMC-Anforderung](cmc-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 
