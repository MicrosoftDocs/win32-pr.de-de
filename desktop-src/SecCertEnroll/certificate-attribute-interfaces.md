---
description: Die folgenden Schnittstellen können zum Erstellen von Zertifikatattributen verwendet werden.
ms.assetid: 3701f9b2-0857-45f0-b3ed-4f1b3db4d6d8
title: Zertifikatattributschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63cbd7b5e80fbb787a0d2aadcfb1617cb7972d7eed200da9184607ad0598031e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902923"
---
# <a name="certificate-attribute-interfaces"></a>Zertifikatattributschnittstellen

Die folgenden Schnittstellen können zum Erstellen von Zertifikatattributen verwendet werden.



| Schnittstelle                                                                    | BESCHREIBUNG                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                   | Stellt ein kryptografisches Attribut in einer Zertifikatanforderung dar.                                                                              |
| [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)                                 | Verwaltet eine Auflistung von [**ICryptAttribute-Objekten.**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                                                 |
| [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                     | Stellt ein Attribut in einer PKCS \# 7-, PKCS \# 10- oder CMC-Zertifikatanforderung dar.                                                               |
| [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)                     | Stellt ein Attribut dar, mit dem der Client identifiziert werden kann, der eine Zertifikatanforderung generiert hat.                                       |
| [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)                 | Stellt die Zertifikaterweiterungen in einer Zertifikatanforderung dar.                                                                             |
| [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)                 | Stellt ein Attribut dar, das einen verschlüsselten privaten Schlüssel enthält, der von einer Zertifizierungsstelle archiviert werden soll.                                 |
| [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)         | Stellt ein Attribut dar, das einen SHA-1-Hash des verschlüsselten privaten Schlüssels enthält, der von einer Zertifizierungsstelle archiviert werden soll.                |
| [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)               | Stellt ein Attribut dar, das den Kryptografieanbieter identifiziert, der von der Entität verwendet wird, die das Zertifikat anfordert.                           |
| [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)                   | Stellt ein Attribut dar, das Versionsinformationen zum Clientbetriebssystem enthält, unter dem die Zertifikatanforderung generiert wurde. |
| [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) | Stellt ein Attribut dar, das das zu erneuernde Zertifikat enthält.                                                                        |
| [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)                                   | Verwaltet eine Auflistung von [**IX509Attribute-Objekten.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                                                   |
| [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                             | Stellt ein generisches Name-Wert-Paar dar.                                                                                                       |
| [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)                           | Verwaltet eine Auflistung von [**IX509NameValuePair-Objekten.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CertEnroll-Schnittstellen](certenroll-interfaces.md)
</dt> </dl>

 

 



