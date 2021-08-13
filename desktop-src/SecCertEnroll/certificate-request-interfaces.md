---
description: Die folgenden Schnittstellen können zum Erstellen von Zertifikatanforderungen verwendet werden.
ms.assetid: 6021db79-ac90-4e0c-afbd-0f926abcab78
title: Schnittstellen für Zertifikatanforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba4f16c6aba1be724fcf2639dd64d7988e40b79a5b29a2d500beb3ae66f4ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902559"
---
# <a name="certificate-request-interfaces"></a>Schnittstellen für Zertifikatanforderungen

Die folgenden Schnittstellen können zum Erstellen von Zertifikatanforderungen verwendet werden.



| Schnittstelle                                                                          | BESCHREIBUNG                                                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                         | Stellt die abstrakte Schnittstelle der obersten Ebene für eine Zertifikatanforderung dar.                                                                                        |
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)   | Ermöglicht es Ihnen, Zertifikate direkt zu erstellen, ohne eine Registrierung oder Zertifizierungsstelle zu durchlaufen.                                                  |
| [**IX509CertificateRequestCertificate2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcertificate2) | Erweitert die [**IX509CertificateRequestCertificate-Schnittstelle,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) um die Initialisierung aus einer Vorlage zu ermöglichen.              |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                   | Stellt eine CMC-Anforderung dar.                                                                                                                                     |
| [**IX509CertificateRequestCmc2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcmc2)                 | Erweitert die [**IX509CertificateRequestCmc-Schnittstelle,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) um die Initialisierung aus einer Vorlage zu ermöglichen.                              |
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)             | Stellt eine PKCS \# 10-Anforderung dar.                                                                                                                               |
| [**IX509CertificateRequestPkcs10V2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v2)         | Erweitert die [**IX509CertificateRequestPkcs10-Schnittstelle,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) um die Initialisierung aus einer Vorlage zu ermöglichen.                        |
| [**IX509CertificateRequestPkcs10V3**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3)         | Erweitert die [**IX509CertificateRequestPkcs10-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) und fügt Eigenschaften hinzu, die den TPM-Zertifikatnachweis ermöglichen. |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)               | Stellt eine PKCS \# 7-Anforderung dar.                                                                                                                                |
| [**IX509CertificateRequestPkcs7V2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs7v2)           | Erweitert die [**IX509CertificateRequestPkcs7-Schnittstelle,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) um die Initialisierung aus einer Vorlage zu ermöglichen.                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CertEnroll-Schnittstellen](certenroll-interfaces.md)
</dt> </dl>

 

 



