---
description: Die Zertifikatregistrierungs-API unterstützt die folgenden Attribute. Sie können ein einzelnes Attribut erstellen, indem Sie die entsprechende Schnittstelle verwenden, die in den folgenden Abschnitten identifiziert wird.
ms.assetid: e14fd472-1974-4ad2-b35a-3ab58ba0d707
title: Unterstützte Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8c7945113e764d835a685251adaec9149527b2d8f2d535a5dd24f26a5623bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774413"
---
# <a name="supported-attributes"></a>Unterstützte Attribute

Die Zertifikatregistrierungs-API unterstützt die folgenden Attribute. Sie können ein einzelnes Attribut erstellen, indem Sie die entsprechende Schnittstelle verwenden, die in den folgenden Abschnitten identifiziert wird.

## <a name="clientid"></a>ClientId

Die [**IX509AttributeClientId-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) kann verwendet werden, um ein Attribut zu definieren, das Informationen über den Clientcomputer enthält, der die Zertifikatanforderung gesendet hat. Die Informationen können für die Diagnose verwendet werden.

**Gilt für:** PKCS \# 10- oder CMC-Anforderung.

**OID:** XCN \_ OID \_ REQUEST CLIENT INFO \_ \_ (1.3.6.1.4.1.311.21.20)

## <a name="extensions"></a>Erweiterungen

Die [**IX509AttributeExtensions-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) kann verwendet werden, um einen Satz von X.509 Version 3-Zertifikaterweiterungen zu definieren. Die folgenden Erweiterungen werden unterstützt. Weitere Informationen finden Sie im Thema Erweiterungsschnittstellen.



| Durchwahl              | BESCHREIBUNG                                                                                                                                                                                                                      |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlternativeNames       | Enthält eine oder mehrere alternative Namensformen des Ausstellers, der dem Zertifikat zugeordnet ist.                                                                                                                                       |
| AuthorityKeyIdentifier | Enthält einen eindeutigen Schlüsselbezeichner, um zwischen mehreren Zertifikatsignaturschlüsseln der [*Zertifizierungsstelle*](/windows/desktop/SecGloss/c-gly) zu unterscheiden. |
| BasicConstraints       | Gibt an, ob der Antragsteller als Zertifizierungsstelle fungieren kann.                                                                                                                                                                                   |
| CertificatePolicies    | Identifiziert die Richtlinien und optionalen Qualifiziererinformationen, die dem Zertifikat zugeordnet sind.                                                                                                                                      |
| MSApplicationPolicies  | Identifiziert eine oder mehrere Verwendungen für das Zertifikat. Diese Erweiterung ähnelt der Erweiterung EnhancedKeyUsage, ist jedoch von Microsoft definiert.                                                                                           |
| EnhancedKeyUsage       | Identifiziert eine oder mehrere Verwendungen des öffentlichen Schlüssels, der im Zertifikat enthalten ist. Die erweiterte Schlüsselverwendungserweiterung kann zusätzlich zu oder anstelle der Schlüsselverwendungserweiterung verwendet werden.                                                  |
| KeyUsage               | Identifiziert Einschränkungen für die Vorgänge, die vom öffentlichen Schlüssel im Zertifikat ausgeführt werden können.                                                                                                                  |
| SmimeCapabilities      | Meldet die Entschlüsselungsfunktionen eines E-Mail-Empfängers an den E-Mail-Absender, damit der Absender den sichersten symmetrischen Algorithmus auswählen kann, der von beiden Seiten unterstützt wird.                                                      |
| SubjectKeyIdentifier   | Enthält einen eindeutigen Schlüsselbezeichner, der verwendet werden kann, um zwischen mehreren Signaturschlüsseln zu unterscheiden, die dem Zertifikatbesitzer zugeordnet sind.                                                                                          |
| Vorlage               | Identifiziert die Vorlage, die beim Ausstellen oder Erneuern eines Zertifikats verwendet werden soll. Die Erweiterung enthält den Objektbezeichner (OID) der Vorlage.                                                                                       |
| TemplateName           | Identifiziert die Vorlage, die beim Ausstellen oder Erneuern eines Zertifikats verwendet werden soll. Die Erweiterung enthält den Namen der Vorlage.                                                                                                          |



 

**Gilt für:** PKCS \# 10-Anforderung.

**OID:** XCN \_ OID \_ RSA \_ certExtensions (1.2.840.113549.1.9.14)

## <a name="archivekey"></a>ArchiveKey

Die [**IX509AttributeArchiveKey-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) kann verwendet werden, um ein Attribut zu definieren, das einen verschlüsselten privaten Schlüssel enthält, der zur Archivierung an eine Zertifizierungsstelle übermittelt wird.

**Gilt für:** CMC-Anforderung.

**OID:** XCN \_ OID \_ ARCHIVED \_ KEY \_ ATTR (1.3.6.1.4.1.311.21.13)

## <a name="archivekeyhash"></a>ArchiveKeyHash

Die [**IX509AttributeArchiveKeyHash-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) kann verwendet werden, um einen Hash des privaten Schlüssels zu definieren, der im **ArchiveKey-Attribut** enthalten ist.

**Gilt für:** CMC-Anforderung.

**OID:** XCN \_ OID \_ ENCRYPTED KEY HASH \_ \_ (1.3.6.1.4.1.311.21.21)

## <a name="cspprovider"></a>CspProvider

Die [**IX509AttributeCspProvider-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider) kann verwendet werden, um ein Attribut zu definieren, das Informationen über den [*Kryptografiedienstanbieter (Cryptographic Service Provider,*](/windows/desktop/SecGloss/c-gly) CSP) enthält, der vom Anfordernden für kryptografische Vorgänge verwendet wird.

**Gilt für:** PKCS \# 10-Anforderung. Dieses Attribut wird automatisch erstellt, wenn Sie ein [**IX509CertificateRequestPkcs10-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) erstellen.

**OID:** XCN \_ OID \_ ENROLLMENT \_ CSP PROVIDER \_ (1.3.6.1.4.1.311.13.2.2)

## <a name="osversion"></a>OSVersion

Die [**IX509AttributeOSVersion-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) kann verwendet werden, um ein Attribut zu erstellen, das Versionsinformationen zum Clientbetriebssystem enthält. Die Informationen können von der Zertifizierungsstelle verwendet werden, um den Verarbeitungstyp zu bestimmen, der beim Erstellen des Zertifikats angewendet werden soll.

**Gilt für:** PKCS \# 10- oder CMC-Anforderung.

**OID:** XCN \_ OID \_ OS VERSION \_ (1.3.6.1.4.1.311.13.2.3)

## <a name="renewalcertificate"></a>RenewalCertificate

Die [**IX509AttributeRenewalCertificate-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) kann verwendet werden, um ein Attribut zu erstellen, das das zu erneuernde Zertifikat enthält.

**Gilt für:** PKCS \# 10-Anforderung. Dieses Attribut wird automatisch erstellt, wenn Sie eine PKCS \# 10-Anforderung erstellen, indem Sie sie mit dem zu erneuernden Zertifikat initiieren.

**OID:** XCN \_ OID \_ RENEWAL CERTIFICATE \_ (1.3.6.1.4.1.311.13.1)

 

 
