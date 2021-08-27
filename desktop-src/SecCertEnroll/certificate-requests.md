---
description: Das Zertifikatregistrierungs-SDK kann verwendet werden, um PKCS \# 10-, PKCS \# 7-, CMC- und selbstsignierte Zertifikatanforderungen zu erstellen.
ms.assetid: 218eafb9-c9c8-49ff-8288-3909ed708ffc
title: Zertifikatanforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39125774584d127e40b16dbb2adca563d8c341b79454235163be30edc865b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902414"
---
# <a name="certificate-requests"></a>Zertifikatanforderungen

Das Zertifikatregistrierungs-SDK kann verwendet werden, um PKCS \# 10-, PKCS \# 7-, CMC- und selbstsignierte Zertifikatanforderungen zu erstellen. Jeder Anforderungstyp wird durch eine der in der folgenden Tabelle aufgeführten Schnittstellen dargestellt. Alle Anforderungsschnittstellen erben direkt oder indirekt von der [**IX509CertificateRequest-Schnittstelle.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) 

| Schnittstelle                                                                        | BESCHREIBUNG                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | Stellt eine PKCS \# 10-Anforderung dar. Diese Schnittstelle erbt [**von IX509CertificateRequest.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                   |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | Stellt eine PKCS \# 7-Anforderung dar. Diese Schnittstelle erbt [**von IX509CertificateRequest.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                    |
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | Stellt ein selbstsigniertes Zertifikat dar. Diese Schnittstelle erbt von [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10). |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | Stellt eine CMC-Anforderung dar. Diese Schnittstelle erbt von [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).               |



 

Die folgende Abbildung zeigt die Vererbungsstruktur der Anforderungsobjekte, die von der Zertifikatregistrierungs-API unterstützt werden. Ein [**IX509CertificateRequest-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) dient direkt oder indirekt als Basisklasse für alle verfügbaren Anforderungsobjekte.

![Vererbungsstruktur für die Anforderungsschnittstellen](images/certificate-request-inheritance.png)

Unabhängig vom Typ enthält eine Zertifikatanforderung Informationen über den Betreff, der die Anforderung stellt, den öffentlichen Schlüssel des Subjekts, einen Satz von Attributen, einen Satz von X.509 Version 3-Erweiterungen (die als Teil der Attribute übermittelt werden können) und eine Signatur. Diese Probleme werden in den folgenden Themen behandelt:

-   [Antragstellernamen](subject-names.md)
-   [Attribute](attributes.md)
-   [Erweiterungen](extensions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> </dl>

 

 



