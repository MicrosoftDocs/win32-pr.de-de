---
description: Die folgenden Schnittstellen können verwendet werden, um Zertifikat Signaturen sowie öffentliche und private Schlüssel zu verwalten.
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: Zertifikat Signatur und Schlüssel Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35d2f3b1404397b1e6f2e436ef27fb740bbb594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866671"
---
# <a name="certificate-signature-and-key-interfaces"></a>Zertifikat Signatur und Schlüssel Schnittstellen

Die folgenden Schnittstellen können verwendet werden, um Zertifikat Signaturen sowie öffentliche und private Schlüssel zu verwalten.



| Schnittstelle                                                      | BESCHREIBUNG                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**Isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)               | Stellt ein Signaturzertifikat dar, mit dem Sie eine Zertifikat Anforderung signieren können.                  |
| [**Isignerzertifikate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates)             | Verwaltet eine Auflistung von [**isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) -Objekten.                 |
| [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)                     | Stellt einen asymmetrischen privaten Schlüssel dar, der für die Verschlüsselung, Signierung und Schlüssel Übereinstimmung verwendet werden kann. |
| [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)                       | Stellt einen öffentlichen Schlüssel in einem Paar aus öffentlichem und privatem Schlüssel dar.                                             |
| [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) | Stellt Informationen dar, die zum Signieren einer Zertifikat Anforderung verwendet werden.                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CertEnroll-Schnittstellen](certenroll-interfaces.md)
</dt> </dl>

 

 



