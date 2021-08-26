---
description: Sie können die IX509Extension-Schnittstelle verwenden, um eine beliebige Erweiterung zu definieren.
ms.assetid: 025447f4-98d0-4cb8-b546-4797b7e60722
title: Unterstützte Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0362bc289e8f0631520a7d9d56ff4bed1af2c698c721db703b27b0ecee5a1629
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101109"
---
# <a name="supported-extensions"></a>Unterstützte Erweiterungen

Sie können die [**IX509Extension-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) verwenden, um eine beliebige Erweiterung zu definieren. Die Zertifikatregistrierungs-API stellt auch Schnittstellen bereit, die von **IX509Extension** abgeleitet wurden, damit Sie problemlos eine der am häufigsten verwendeten Erweiterungen erstellen können. In der folgenden Liste sind die allgemeinen Erweiterungen aufgeführt, die von Microsoft-Zertifizierungsstellen unterstützt werden, sowie die Objektbezeichner und Schnittstellen, mit denen Sie sie erstellen können.

## <a name="alternativenames"></a>AlternativeNames

Die Erweiterung für alternative Namen kann verwendet werden, um ein oder mehrere alternative Namensformulare für den Betreff der Zertifikatanforderung zu definieren. Beispiele für alternative Namen sind E-Mail-Adressen, DNS-Namen, IP-Adressen und URIs.

**Schnittstelle:** [ **IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)

**OID:** XCN \_ OID \_ SUBJECT ALT \_ \_ NAME2 (2.5.29.17)

## <a name="authorityinformationaccess"></a>AuthorityInformationAccess

Die Erweiterung für den Zugriff auf Autoritätsinformationen identifiziert den Zugriff auf Informationen und Dienste der Zertifizierungsstelle. Der Erweiterungswert enthält eine Sequenz von URIs.

**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ AUTHORITY INFO ACCESS \_ \_ (1.3.6.1.5.5.7.1.1)

## <a name="authoritykeyidentifier"></a>AuthorityKeyIdentifier

Die Erweiterung des Zertifizierungsstellenschlüssels ermöglicht die Identifizierung des öffentlichen Schlüssels der Zertifizierungsstelle, der dem privaten Zertifizierungsstellenschlüssel entspricht, der ein ausgestelltes Zertifikat signiert hat. Sie wird vom Zertifikatpfad verwendet, der Software auf einem Windows Server erstellt, um das Zertifizierungsstellenzertifikat zu finden. Wenn eine Zertifizierungsstelle ein Zertifikat aushing, wird der Erweiterungswert auf die **SubjectKeyIdentifier-Erweiterung** im Signaturzertifikat der Zertifizierungsstelle festgelegt. Der Wert ist in der Regel ein SHA-1-Hash des öffentlichen Schlüssels.

**Schnittstelle:** [ **IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)

**OID:** \_SCHLÜSSELBEZEICHNER DER XCN-OID-AUTORITÄT2 \_ \_ \_ (2.5.29.35)

## <a name="basicconstraints"></a>BasicConstraints

Die Erweiterung für grundlegende Einschränkungen kann verwendet werden, um zu bestimmen, ob die Entität als Zertifizierungsstelle (Ca) verwendet werden kann, und, falls ja, die Anzahl der untergeordneten Zertifizierungsstellen, die darunter in der Zertifikatkette vorhanden sein können.

**Schnittstelle:** [ **IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)

**OID:** GRUNDLEGENDE EINSCHRÄNKUNGEN \_ FÜR XCN-OID2 \_ \_ (2.5.29.19)

## <a name="certificatepolicies"></a>CertificatePolicies

Die Zertifikatrichtlinienerweiterung kann verwendet werden, um die Richtlinien zu identifizieren, unter denen das Zertifikat ausgestellt wurde, und die Zwecke, zu denen es verwendet werden kann. Diese werden durch eine Auflistung von Objektbezeichnern (OIDs) identifiziert. Richtlinien werden an die Anforderungen einer Organisation angepasst.

**Schnittstelle:** [ **IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)

**OID:** \_ \_ XCN-OID-ZERTIFIKATRICHTLINIEN \_ (2.5.29.32)

## <a name="crldistributionpoints"></a>CrlDistributionPoints

Die Erweiterung für Zertifikatsperrlisten-Verteilungspunkte enthält den URI der Basiszertifikatsperrliste (CRL).

**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** \_ \_ XCN-OID-CRL-DIST-PUNKTE \_ \_ (2.5.29.31)

## <a name="enhancedkeyusage"></a>EnhancedKeyUsage

Die Erweiterte Schlüsselverwendungserweiterung kann verwendet werden, um eine oder mehrere Verwendungen des öffentlichen Schlüssels zu definieren, der im Zertifikat enthalten ist.

**Schnittstelle:** [ **IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)

**OID:** ERWEITERTE SCHLÜSSELVERWENDUNG \_ DER XCN-OID \_ \_ \_ (2.5.29.37)

## <a name="freshestcrl"></a>FreshestCRL

Die neueste CRL-Erweiterung enthält den URI der Delta-Zertifikatsperrliste. Für diese Erweiterung und die **Erweiterung CrlDistributionPoints** wird die gleiche ASN.1-Syntax verwendet.

**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** \_XCN-OID \_ \_ FRESHEST-ZERTIFIKATSPERRLISTE (2.5.29.46)

## <a name="keyusage"></a>KeyUsage

Die Schlüsselverwendungserweiterung kann verwendet werden, um Einschränkungen für die Vorgänge zu definieren, die mit dem im Zertifikat enthaltenen öffentlichen Schlüssel ausgeführt werden können. Beispielsweise können Sie angeben, dass der öffentliche Schlüssel nur zum Erstellen einer digitalen Signatur, Signieren einer Zertifikatsperrliste (Certificate Revocation List, CRL) oder Verschlüsseln eines anderen Schlüssels verwendet werden soll.

**Schnittstelle:** [ **IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)

**OID:** VERWENDUNG DES \_ XCN-OID-SCHLÜSSELS \_ \_ (2.5.29.15)

## <a name="msapplicationpolicies"></a>MSApplicationPolicies

Die Microsoft-Anwendungsrichtlinienerweiterung kann von einer Anwendung verwendet werden, um Zertifikate auf der Grundlage der zulässigen Verwendung zu filtern. Zulässige Verwendungen werden durch OIDs identifiziert. Diese Erweiterung ähnelt der **Erweiterung EnhancedKeyUsage,** jedoch mit einer strengeren Semantik, die auf die übergeordnete Zertifizierungsstelle angewendet wird. Die Erweiterung ist microsoftspezifisch.

**Schnittstelle:** [ **IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)

**OID:** \_ \_ \_ XCN-OID-ANWENDUNGSZERTIFIKATRICHTLINIEN \_ (1.3.6.1.4.1.311.21.10)

## <a name="nameconstraints"></a>NameConstraints

Die Erweiterung für Namenseinschränkungen wird verwendet, um den Namespace zu identifizieren, in dem sich alle Betreffnamen von Zertifikaten in einer Zertifikathierarchie befinden müssen. Die Erweiterung wird lediglich in einem Zertifizierungsstellenzertifikat verwendet.

**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** \_XCN-OID-NAMENSEINSCHRÄNKUNGEN \_ \_ (2.5.29.30)

## <a name="policyconstraints"></a>PolicyConstraints

Die Erweiterung für Richtlinieneinschränkungen wird Zertifizierungsstellenzertifikaten hinzugefügt, um die Pfadvalidierung zu beschränken, indem die Richtlinienzuordnung verhindert oder verlangt wird, dass jedes Zertifikat in der Hierarchie einen zulässigen Richtlinienbezeichner enthält.

**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** \_XCN-OID-RICHTLINIENEINSCHRÄNKUNGEN \_ \_ (2.5.29.36)

## <a name="policymappings"></a>PolicyMappings

Die Erweiterung für Richtlinienzuordnungen wird verwendet, um die Richtlinien in einer untergeordneten Zertifizierungsstelle zu identifizieren, die Richtlinien in der ausstellenden Zertifizierungsstelle entsprechen. Der Erweiterungswert enthält eine Sequenz ausstellenden Richtlinienzuordnungen der Zertifizierungsstelle und der untergeordneten Zertifizierungsstelle, die durch Objektbezeichner dargestellt werden.

**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** \_XCN-OID-RICHTLINIENZUORDNUNGEN \_ \_ (2.5.29.33)

## <a name="privatekeyusageperiod"></a>PrivateKeyUsagePeriod

Die Nutzungsdauererweiterung für private Schlüssel wird verwendet, um eine andere Gültigkeitsdauer für den privaten Schlüssel als für das Zertifikat anzugeben, dem der Schlüssel zugeordnet ist.

**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** NUTZUNGSZEITRAUM \_ DES XCN-OID-PRIVATEKEY \_ \_ \_ (2.5.29.16)

## <a name="smimecapabilities"></a>SmimeCapabilities

Die S/MIME-Funktionenerweiterung (Secure/Multipurpose Internet Mail Extensions) kann verwendet werden, um die Entschlüsselungsfunktionen eines E-Mail-Empfängers an den Absender der E-Mail-Nachricht zu melden, damit der Absender den sichersten Verschlüsselungsalgorithmus auswählen kann, der von beiden Parteien unterstützt wird. Der Erweiterungswert enthält eine Sammlung symmetrischer Verschlüsselungsalgorithmus-OIDs und eine optionale Verschlüsselungsstärke für jede.

**Schnittstelle:** [ **IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)

**OID:** XCN \_ OID \_ RSA \_ SMIMECapabilities (1.2.840.113549.1.9.15)

## <a name="subjectdirectoryattributes"></a>SubjectDirectoryAttributes

Die Erweiterung "Subject Directory Attributes" kann verwendet werden, um Identifikationsattribute zu vermitteln, z. B. das Subjekt des Zertifikatssubjekts. Der Erweiterungswert ist eine Folge von OID-Wertepaaren.

**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ SUBJECT DIR \_ \_ ATTRS (2.5.29.9)

## <a name="subjectkeyidentifier"></a>SubjectKeyIdentifier

Die Erweiterung für den Schlüsselbezeichner des Betreffs kann verwendet werden, um zwischen mehreren öffentlichen Schlüsseln zu unterscheiden, die vom Zertifikatsubjekt gehalten werden. Der Erweiterungswert ist normalerweise ein SHA-1-Hash des Schlüssels.

**Schnittstelle:** [ **IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)

**OID:** BEZEICHNER DES \_ XCN-OID-SUBJEKTSCHLÜSSELS \_ \_ \_ (2.5.29.14)

## <a name="template"></a>Vorlage

Die Vorlagenerweiterung kann verwendet werden, um die Vorlage der Version 2 zu identifizieren, die beim Ausstellen oder Erneuern eines Zertifikats verwendet werden soll. Der Erweiterungswert enthält die Vorlagen-OID und optionale Versionsinformationen. Die Erweiterung ist microsoftspezifisch.

**Schnittstelle:** [ **IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)

**OID:** \_XCN-OID-ZERTIFIKATVORLAGE \_ \_ (1.3.6.1.4.1.311.21.7)

## <a name="templatename"></a>TemplateName

Die Vorlagennamenerweiterung kann verwendet werden, um die Vorlage der Version 1 zu identifizieren, die beim Ausstellen oder Erneuern eines Zertifikats verwendet werden soll. Der Erweiterungswert enthält den Namen der Vorlage. Die Erweiterung ist microsoftspezifisch.

**Schnittstelle:** [ **IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)

**OID:** XCN \_ OID \_ ENROLL \_ CERTTYPE \_ EXTENSION (1.3.6.1.4.1.311.20.2)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterungen](extensions.md)
</dt> </dl>

 

 



