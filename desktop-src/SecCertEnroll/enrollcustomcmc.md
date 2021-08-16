---
description: Erstellt eine CMC-Zertifikatanforderung und registriert einen Computer in einer Zertifikathierarchie.
ms.assetid: ef09ef04-8925-4d66-97ad-70b4d7cf78b9
title: enrollCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3799cd70d8f3b70ae32a95b7720a879ddd611fba5e35064d1794d39bdcd7ab9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780059"
---
# <a name="enrollcustomcmc"></a>enrollCustomCMC

Im Beispiel enrollCustomCMC wird eine CMC-Zertifikatanforderung erstellt und ein Computer in einer Zertifikathierarchie registriert.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *%ProgramFiles%* \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollCustomCMC installiert.

## <a name="discussion"></a>Diskussion

Beispiel für enrollCustomCMC:

1.  Verarbeitet die folgenden Befehlszeilenargumente:
    -   Ein benutzerdefiniertes Name-Wert-Paar, das der Zertifikatanforderung hinzugefügt werden soll.
    -   Ein alternativer Betreffname.
    -   Ein Objektbezeichner (OID) für die Erweiterung erweiterte Schlüsselverwendung (Enhanced Key Usage, EKU).
2.  Erstellt ein [**IX509CertificateRequestPkcs10-Anforderungsobjekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) und initialisiert es mithilfe des Computerkontexts.
3.  Verwendet die PKCS \# 10-Anforderung, um ein [**IX509CertificateRequestCmc-Objekt zu**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) initialisieren.
4.  Erstellt ein [**IX509ExtensionEnhancedKeyUsage-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) mithilfe der in der Befehlszeile angegebenen OID und fügt es der Erweiterungsaufforderung für die CMC-Anforderung hinzu.
5.  Erstellt ein [**IAlternativeName-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) unter Verwendung des in der Befehlszeile angegebenen Namens, fügt es der [**IAlternativeNames-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) hinzu, initialisiert mithilfe der Auflistung eine [**IX509ExtensionAlternativeNames-Erweiterung**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) und fügt diese der Erweiterungsaufforderung für die CMC-Anforderung hinzu.
6.  Erstellt ein [**IX509NameValuePair-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) unter Verwendung des in der Befehlszeile angegebenen Namens und Werts und fügt es der [**IX509NameValuePairs-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) in der CMC-Anforderung hinzu.
7.  Erstellt ein [**IX509Enrollment-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) initialisiert es mithilfe des CMC-Anforderungsobjekts und ruft eine Zeichenfolge ab, die eine Base64-codierte Anforderung enthält.
8.  Erstellt ein [**ICertConfig-Objekt**](/windows/desktop/api/certcli/nn-certcli-icertconfig) und verwendet es, um eine Zeichenfolge abzurufen, die die Konfiguration der Zertifizierungsstelle enthält.
9.  Erstellt ein [**CryptoAPI-ICertRequest2-Objekt**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) und verwendet es sowie die Zeichenfolgen, die die Konfiguration der Zertifizierungsstelle und die Zertifikatanforderung enthalten, um die Anforderung an die Zertifizierungsstelle zu übermitteln.
10. Überprüft den Übermittlungsstatus und installiert das Zertifikat bei Erfolg im Zertifikatspeicher.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CMC-Anforderung](cmc-request.md)
</dt> <dt>

[PKCS \# 10-Anforderung](pkcs--10-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 
