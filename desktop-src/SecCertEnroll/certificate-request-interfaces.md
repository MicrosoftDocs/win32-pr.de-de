---
description: Die folgenden Schnittstellen können verwendet werden, um Zertifikat Anforderungen zu erstellen.
ms.assetid: 6021db79-ac90-4e0c-afbd-0f926abcab78
title: Schnittstellen für Zertifikat Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e18a4f8e1ce60348ffdf52afe210247f6d20a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129892"
---
# <a name="certificate-request-interfaces"></a>Schnittstellen für Zertifikat Anforderungen

Die folgenden Schnittstellen können verwendet werden, um Zertifikat Anforderungen zu erstellen.



| Schnittstelle                                                                          | BESCHREIBUNG                                                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                         | Stellt die abstrakte Oberfläche der obersten Ebene für eine Zertifikat Anforderung dar.                                                                                        |
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)   | Ermöglicht das direkte Erstellen von Zertifikaten, ohne eine Registrierung oder Zertifizierungsstelle durchlaufen zu müssen.                                                  |
| [**IX509CertificateRequestCertificate2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcertificate2) | Erweitert die [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) -Schnittstelle, um die Initialisierung aus einer Vorlage zu ermöglichen.              |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                   | Stellt eine CMC-Anforderung dar.                                                                                                                                     |
| [**IX509CertificateRequestCmc2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcmc2)                 | Erweitert die [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Schnittstelle, um die Initialisierung aus einer Vorlage zu ermöglichen.                              |
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)             | Stellt eine PKCS \# 10-Anforderung dar.                                                                                                                               |
| [**IX509CertificateRequestPkcs10V2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v2)         | Erweitert die [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Schnittstelle, um die Initialisierung aus einer Vorlage zu ermöglichen.                        |
| [**IX509CertificateRequestPkcs10V3**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3)         | Erweitert die [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Schnittstelle und fügt Eigenschaften hinzu, die den TPM-Zertifikat Nachweis aktivieren. |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)               | Stellt eine PKCS \# 7-Anforderung dar.                                                                                                                                |
| [**IX509CertificateRequestPkcs7V2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs7v2)           | Erweitert die [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) -Schnittstelle, um die Initialisierung aus einer Vorlage zu ermöglichen.                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CertEnroll-Schnittstellen](certenroll-interfaces.md)
</dt> </dl>

 

 



