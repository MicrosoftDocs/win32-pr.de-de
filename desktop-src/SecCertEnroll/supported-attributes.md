---
description: Die Zertifikatregistrierungs-API unterstützt die folgenden Attribute. Sie können ein einzelnes Attribut erstellen, indem Sie die entsprechende Schnittstelle verwenden, die in den folgenden Abschnitten identifiziert ist.
ms.assetid: e14fd472-1974-4ad2-b35a-3ab58ba0d707
title: Unterstützte Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3bfff5785a0b891e98e6d78d59b4688e2d5c11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350468"
---
# <a name="supported-attributes"></a>Unterstützte Attribute

Die Zertifikatregistrierungs-API unterstützt die folgenden Attribute. Sie können ein einzelnes Attribut erstellen, indem Sie die entsprechende Schnittstelle verwenden, die in den folgenden Abschnitten identifiziert ist.

## <a name="clientid"></a>ClientId

Die [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) -Schnittstelle kann verwendet werden, um ein Attribut zu definieren, das Informationen über den Client Computer enthält, der die Zertifikat Anforderung gesendet hat. Die Informationen können für die Diagnose verwendet werden.

**Gilt für:** PKCS \# 10-oder-CMC-Anforderung.

**OID:** XCN \_ OID \_ Request- \_ Client \_ Informationen (1.3.6.1.4.1.311.21.20)

## <a name="extensions"></a>Erweiterungen

Die [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) -Schnittstelle kann verwendet werden, um einen Satz von X. 509 Version 3-Zertifikat Erweiterungen zu definieren. Die folgenden Erweiterungen werden unterstützt. Weitere Informationen finden Sie im Thema Erweiterungs Schnittstellen.



| Durchwahl              | BESCHREIBUNG                                                                                                                                                                                                                      |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Alternativenames       | Enthält mindestens eine Alternative namens Form des Ausstellers, der dem Zertifikat zugeordnet ist.                                                                                                                                       |
| Autoritykeyidentifier | Enthält einen eindeutigen Schlüssel Bezeichner zur Unterscheidung zwischen mehreren Zertifikat Signatur Schlüsseln der Zertifizierungsstelle ( [*Certification Authority*](/windows/desktop/SecGloss/c-gly) , ca). |
| Basiceinschränkungen       | Gibt an, ob der Betreff als Zertifizierungsstelle fungieren kann.                                                                                                                                                                                   |
| Certificatepolicies    | Identifiziert die Richtlinien und optionalen Qualifiziererinformationen, die dem Zertifikat zugeordnet sind.                                                                                                                                      |
| Msapplicationpolicies  | Identifiziert mindestens einen Verwendungs Verwendungs Nachweis für das Zertifikat. Diese Erweiterung ähnelt der Erweiterung EnhancedKeyUsage, ist aber von Microsoft definiert.                                                                                           |
| Felds EnhancedKeyUsage       | Identifiziert mindestens einen Verwendungs Einsatz des öffentlichen Schlüssels, der im Zertifikat enthalten ist. Die Erweiterung für die erweiterte Schlüssel Verwendung kann zusätzlich zu oder anstelle der Schlüssel Verwendungs Erweiterung verwendet werden.                                                  |
| Endeinheits Zertifikaten der               | Identifiziert die Einschränkungen für die Vorgänge, die vom im Zertifikat enthaltenen öffentlichen Schlüssel ausgeführt werden können.                                                                                                                  |
| SMIME-Funktionen      | Meldet die Entschlüsselungs Funktionen eines e-Mail-Empfängers an den e-Mail-Absender, damit der Absender den sichersten symmetrischen Algorithmus auswählen kann, der von beiden Parteien unterstützt wird.                                                      |
| SubjectKeyIdentifier   | Enthält einen eindeutigen Schlüssel Bezeichner, der zur Unterscheidung zwischen mehreren Signatur Schlüsseln verwendet werden kann, die dem Zertifikat Besitzer zugeordnet sind.                                                                                          |
| Vorlage               | Gibt die Vorlage an, die beim ausstellen oder Erneuern eines Zertifikats verwendet werden soll. Die Erweiterung enthält den Objekt Bezeichner (OID) der Vorlage.                                                                                       |
| TemplateName           | Gibt die Vorlage an, die beim ausstellen oder Erneuern eines Zertifikats verwendet werden soll. Die Erweiterung enthält den Namen der Vorlage.                                                                                                          |



 

**Gilt für:** PKCS \# 10-Anforderung.

**OID:** XCN \_ OID \_ RSA \_ certextensions (1.2.840.113549.1.9.14)

## <a name="archivekey"></a>Archivekey

Die [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) -Schnittstelle kann verwendet werden, um ein Attribut zu definieren, das einen verschlüsselten privaten Schlüssel enthält, der zur Archivierung an eine Zertifizierungsstelle gesendet wurde.

**Gilt für:** CMC-Anforderung.

**OID:** Archivierte XCN- \_ OID- \_ \_ Schlüssel \_ attr (1.3.6.1.4.1.311.21.13)

## <a name="archivekeyhash"></a>Archivekeyhash

Die [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) -Schnittstelle kann verwendet werden, um einen Hash des privaten Schlüssels zu definieren, der im **archivekey** -Attribut enthalten ist.

**Gilt für:** CMC-Anforderung.

**OID:** Schlüssel Hash für verschlüsselte XCN- \_ OID \_ \_ \_ (1.3.6.1.4.1.311.21.21)

## <a name="cspprovider"></a>Cspprovider

Die [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider) -Schnittstelle kann verwendet werden, um ein Attribut zu definieren, das Informationen über den [*Kryptografiedienstanbieter (kryptografischen Service Provider*](/windows/desktop/SecGloss/c-gly) , CSP) enthält

**Gilt für:** PKCS \# 10-Anforderung. Dieses Attribut wird automatisch erstellt, wenn Sie ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt erstellen.

**OID:** CSP-Anbieter für die XCN-OID-Registrierung \_ \_ \_ \_ (1.3.6.1.4.1.311.13.2.2)

## <a name="osversion"></a>OSVersion

Die [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) -Schnittstelle kann verwendet werden, um ein Attribut zu erstellen, das Versionsinformationen zum Client Betriebssystem enthält. Die Informationen können von der Zertifizierungsstelle verwendet werden, um die Art der Verarbeitung zu bestimmen, die beim Erstellen des Zertifikats angewendet werden soll.

**Gilt für:** PKCS \# 10-oder-CMC-Anforderung.

**OID:** XCN- \_ OID- \_ Betriebssystem \_ Version (1.3.6.1.4.1.311.13.2.3)

## <a name="renewalcertificate"></a>Erneuerungs Zertifikat

Die [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) -Schnittstelle kann verwendet werden, um ein Attribut zu erstellen, das das Zertifikat enthält, das erneuert wird.

**Gilt für:** PKCS \# 10-Anforderung. Dieses Attribut wird automatisch erstellt, wenn Sie eine PKCS \# 10-Anforderung erstellen, indem Sie es mit dem Zertifikat initialisieren, das erneuert wird.

**OID:** XCN \_ OID- \_ Erneuerungs \_ Zertifikat (1.3.6.1.4.1.311.13.1)

 

 
