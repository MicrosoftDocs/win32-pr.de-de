---
description: Liest eine vorhandene CMC-Zertifikatanforderung aus einer Datei, umschließt sie in einer anderen CMC-Anforderung, signiert diese äußere Anforderung, übermittelt sie an eine Zertifizierungsstelle und speichert die Zertifikatantwort von der Zertifizierungsstelle in einer Datei.
ms.assetid: b1a9161d-1f9a-4c5b-acd2-6058dc65a258
title: enrollNestedCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b55c2957fc04e8bd9a088d3a07ed10c639c29d27dd1262b34709a9215c6c8b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882940"
---
# <a name="enrollnestedcmc"></a>enrollNestedCMC

Das Beispiel enrollNestedCMC liest eine vorhandene CMC-Zertifikatanforderung aus einer Datei, umschließt sie in einer anderen CMC-Anforderung, signiert diese äußere Anforderung, übermittelt sie an eine Zertifizierungsstelle und speichert die Zertifikatantwort von der Zertifizierungsstelle in einer Datei.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *%ProgramFiles%* \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples \\ X509 Certificate Enrollment \\ VC \\ enrollNestedCMC installiert.

## <a name="discussion"></a>Diskussion (Discussion)

Beispiel für enrollNestedCMC:

1.  Verarbeitet die folgenden Befehlszeilenargumente:
    -   Der Name der Eingabedatei.
    -   Der Name der Ausgabedatei.
    -   Eine optionale Anforderungsvorlage.
2.  Liest eine vorhandene CMC-Anforderung aus einer Datei als Base63-codiertes Bytearray, konvertiert das Bytearray in einen **BSTR,** erstellt ein [**IX509CertificateRequestCmc-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) und initialisiert das Anforderungsobjekt mit **dem BSTR.** Das initialisierte Objekt wird zur inneren Anforderung.
3.  Verwendet das innere Anforderungsobjekt, das im vorherigen Schritt erstellt und initialisiert wurde, um eine weitere CMC-Anforderung zu initialisieren.
4.  Ruft ein vorhandenes Signaturzertifikat ab oder erstellt, wenn es nicht gefunden werden kann, eine Zertifikatanforderung aus der in der Befehlszeile angegebenen Vorlage und versucht, es zu registrieren. Die Funktionen findCertByTemplate und enrollCertByTemplate sind in enrollCommon.cpp definiert.
5.  Ruft die [**ISignerCertificates-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) aus der äußeren CMC-Anforderung ab, erstellt ein neues [**ISignerCertificate-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) initialisiert es mithilfe des abgerufenen Signaturzertifikats und fügt es der Auflistung hinzu.
6.  Codiert die CMC-Anforderung mit Distinguished Encoding Rules (DER) und ruft die Anforderung als **BSTR ab.**
7.  Erstellt ein [**ICertConfig-Objekt**](/windows/desktop/api/certcli/nn-certcli-icertconfig) und verwendet es, um eine Zeichenfolge abzurufen, die die Konfiguration der Zertifizierungsstelle enthält.
8.  Erstellt ein [**CryptoAPI-ICertRequest2-Objekt**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) und verwendet es sowie die Zeichenfolgen, die die Konfiguration der Zertifizierungsstelle und die Zertifikatanforderung enthalten, um die Anforderung an die Zertifizierungsstelle zu übermitteln.
9.  Überprüft den Status des Registrierungsprozesses und speichert die Zertifikatantwort der Zertifizierungsstelle in einer Datei. Die EncodeToFileW-Funktion ist in enrollCommon.cpp definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CMC-Anforderung](cmc-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 
