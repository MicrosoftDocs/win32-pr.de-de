---
description: Mit dem Zertifikatregistrierungs-SDK können PKCS \# 10-, PKCS \# 7-, CMC-und selbst signierte Zertifikat Anforderungen erstellt werden.
ms.assetid: 218eafb9-c9c8-49ff-8288-3909ed708ffc
title: Zertifikat Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690f3a5117abfa0ae262f0a8fa38f68528abf02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368133"
---
# <a name="certificate-requests"></a>Zertifikat Anforderungen

Mit dem Zertifikatregistrierungs-SDK können PKCS \# 10-, PKCS \# 7-, CMC-und selbst signierte Zertifikat Anforderungen erstellt werden. Jeder Anforderungstyp wird durch eine der in der folgenden Tabelle aufgelisteten Schnittstellen dargestellt. Alle Anforderungs Schnittstellen erben direkt oder indirekt von der [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) -Schnittstelle. 

| Schnittstelle                                                                        | BESCHREIBUNG                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | Stellt eine PKCS \# 10-Anforderung dar. Diese Schnittstelle erbt von [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).                   |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | Stellt eine PKCS \# 7-Anforderung dar. Diese Schnittstelle erbt von [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).                    |
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | Stellt ein selbst signiertes Zertifikat dar. Diese Schnittstelle erbt von [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10). |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | Stellt eine CMC-Anforderung dar. Diese Schnittstelle erbt von [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).               |



 

Die folgende Abbildung zeigt die Vererbungs Struktur der Anforderungs Objekte, die von der Zertifikatregistrierungs-API unterstützt werden. Ein [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) -Objekt dient direkt oder indirekt als Basisklasse für alle verfügbaren Anforderungs Objekte.

![Vererbungs Struktur für die Anforderungs Schnittstellen](images/certificate-request-inheritance.png)

Unabhängig vom Typ enthält eine Zertifikat Anforderung Informationen über den Betreff der Anforderung, den öffentlichen Schlüssel des Antragstellers, eine Gruppe von Attributen, eine Reihe von X. 509 Version 3-Erweiterungen (die als Teil der Attribute übermittelt werden können) und eine Signatur. Diese Probleme werden in den folgenden Themen behandelt:

-   [Antragstellernamen](subject-names.md)
-   [Attribute](attributes.md)
-   [Extensions (Erweiterungen)](extensions.md)

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

 

 



