---
description: Die folgenden Schnittstellen können zum Erstellen von Zertifikat Attributen verwendet werden.
ms.assetid: 3701f9b2-0857-45f0-b3ed-4f1b3db4d6d8
title: Zertifikat Attribut Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 930f427ae6333084c8a180e5d227e4c24daa5426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368088"
---
# <a name="certificate-attribute-interfaces"></a>Zertifikat Attribut Schnittstellen

Die folgenden Schnittstellen können zum Erstellen von Zertifikat Attributen verwendet werden.



| Schnittstelle                                                                    | BESCHREIBUNG                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Icryptattribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                   | Stellt ein kryptografieattribut in einer Zertifikat Anforderung dar.                                                                              |
| [**Icryptattributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)                                 | Verwaltet eine Auflistung von [**icryptattribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) -Objekten.                                                                 |
| [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                     | Stellt ein Attribut in einer PKCS \# 7-, PKCS \# 10-oder CMC-Zertifikat Anforderung dar.                                                               |
| [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)                     | Stellt ein Attribut dar, das verwendet werden kann, um den Client zu identifizieren, von dem eine Zertifikat Anforderung generiert wurde.                                       |
| [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)                 | Stellt die Zertifikat Erweiterungen in einer Zertifikat Anforderung dar.                                                                             |
| [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)                 | Stellt ein Attribut dar, das einen verschlüsselten privaten Schlüssel enthält, der von einer Zertifizierungsstelle archiviert werden soll.                                 |
| [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)         | Stellt ein Attribut dar, das einen SHA-1-Hash des verschlüsselten privaten Schlüssels enthält, der von einer Zertifizierungsstelle archiviert werden soll.                |
| [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)               | Stellt ein Attribut dar, das den Kryptografieanbieter identifiziert, der von der Entität, die das Zertifikat anfordert                           |
| [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)                   | Stellt ein Attribut dar, das Versionsinformationen über das Client Betriebssystem enthält, für das die Zertifikat Anforderung generiert wurde. |
| [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) | Stellt ein Attribut dar, das das Zertifikat enthält, das erneuert wird.                                                                        |
| [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)                                   | Verwaltet eine Auflistung von [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) -Objekten.                                                                   |
| [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                             | Stellt ein generisches Name-Wert-Paar dar.                                                                                                       |
| [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)                           | Verwaltet eine Auflistung von [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) -Objekten.                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CertEnroll-Schnittstellen](certenroll-interfaces.md)
</dt> </dl>

 

 



