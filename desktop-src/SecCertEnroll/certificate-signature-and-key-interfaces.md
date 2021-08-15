---
description: Die folgenden Schnittstellen können verwendet werden, um Zertifikatsignaturen sowie öffentliche und private Schlüssel zu verwalten.
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: Zertifikatsignatur und Schlüsselschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdfd4c76b0e73f2954780d797e092e6d8b7570ebaee082ef93319f74abc24e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902306"
---
# <a name="certificate-signature-and-key-interfaces"></a>Zertifikatsignatur und Schlüsselschnittstellen

Die folgenden Schnittstellen können verwendet werden, um Zertifikatsignaturen sowie öffentliche und private Schlüssel zu verwalten.



| Schnittstelle                                                      | BESCHREIBUNG                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)               | Stellt ein Signaturzertifikat dar, mit dem Sie eine Zertifikatanforderung signieren können.                  |
| [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates)             | Verwaltet eine Auflistung von [**ISignerCertificate-Objekten.**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)                 |
| [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)                     | Stellt einen asymmetrischen privaten Schlüssel dar, der für Verschlüsselung, Signatur und Schlüsselvereinbarung verwendet werden kann. |
| [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)                       | Stellt einen öffentlichen Schlüssel in einem Paar aus öffentlichem und privatem Schlüssel dar.                                             |
| [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) | Stellt Informationen dar, die zum Signieren einer Zertifikatanforderung verwendet werden.                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CertEnroll-Schnittstellen](certenroll-interfaces.md)
</dt> </dl>

 

 



