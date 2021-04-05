---
description: Sie können die IX509Extension-Schnittstelle verwenden, um eine beliebige Erweiterung zu definieren.
ms.assetid: 025447f4-98d0-4cb8-b546-4797b7e60722
title: Unterstützte Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd55886b03cdea5783f918182c84382910510918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752161"
---
# <a name="supported-extensions"></a>Unterstützte Erweiterungen

Sie können die [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) -Schnittstelle verwenden, um eine beliebige Erweiterung zu definieren. Die Zertifikatregistrierungs-API bietet auch Schnittstellen, die von **IX509Extension** abgeleitet werden, damit Sie problemlos eine der gängigsten Erweiterungen erstellen können. Die folgende Liste enthält die allgemeinen Erweiterungen, die von Microsoft-Zertifizierungsstellen unterstützt werden, sowie die Objekt Bezeichner und Schnittstellen, die Sie verwenden können, um Sie zu erstellen.

## <a name="alternativenames"></a>Alternativenames

Die Alternative Namen Erweiterung kann verwendet werden, um mindestens ein alternatives namens Formular für den Betreff der Zertifikat Anforderung zu definieren. Beispiele für alternative Namen sind E-Mail-Adressen, DNS-Namen, IP-Adressen und URIs.

**Schnittstelle:** [ **IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)

**OID:** XCN- \_ OID- \_ Betreff \_ alt \_ name2 (2.5.29.17)

## <a name="authorityinformationaccess"></a>Autorityinformationaccess

Die Erweiterung Authority Information Access gibt Aufschluss über den Zugriff auf Zertifizierungsstellen Informationen und-Dienste. Der Erweiterungs Wert enthält eine Sequenz von URIs.

**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** Informationen zum Zugriff auf die XCN- \_ OID- \_ Autorität \_ \_ (1.3.6.1.5.5.7.1.1)

## <a name="authoritykeyidentifier"></a>Autoritykeyidentifier

Die Zertifizierungsstellen-schlüsselbezeichnererweiterung ermöglicht die Identifizierung des öffentlichen Zertifizierungsstellen Schlüssels, der dem privaten Schlüssel der Zertifizierungsstelle entspricht, der ein ausgestelltes Zertifikat signiert hat Sie wird von einem Zertifikat Pfad zum Entwickeln von Software auf einem Windows-Server verwendet, um das Zertifizierungsstellen Zertifikat zu finden. Wenn eine Zertifizierungsstelle ein Zertifikat ausgibt, wird der Erweiterungs Wert auf die Erweiterung " **subjetkeyidentifier** " im Signaturzertifikat der Zertifizierungsstelle festgelegt. Der Wert ist in der Regel ein SHA-1-Hash des öffentlichen Schlüssels.

**Schnittstelle:** [ **IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)

**OID:** XCN \_ OID \_ Authority \_ Key \_ Bezeichner2 (2.5.29.35)

## <a name="basicconstraints"></a>Basiceinschränkungen

Mithilfe der Basis Einschränkungs Erweiterung können Sie feststellen, ob die Entität als Zertifizierungsstelle (Certification Authority, ca) verwendet werden kann. wenn dies der Fall ist, wird die Anzahl der untergeordneten Zertifizierungsstellen in der Zertifikat Kette verwendet.

**Schnittstelle:** [ **IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)

**OID:** XCN \_ OID \_ Basic \_ CONSTRAINTS2 (2.5.29.19)

## <a name="certificatepolicies"></a>Certificatepolicies

Die Zertifikat Richtlinien Erweiterung kann verwendet werden, um die Richtlinien zu identifizieren, unter denen das Zertifikat ausgestellt wurde, und die Zwecke dafür können verwendet werden. Diese werden durch eine Auflistung von Objekt Bezeichner (OIDs) identifiziert. Die Richtlinien sind an die Anforderungen einer Organisation angepasst.

**Schnittstelle:** [ **IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)

**OID:** XCN- \_ OID- \_ Zertifikat \_ Richtlinien (2.5.29.32)

## <a name="crldistributionpoints"></a>Crldistributionpoints

Die Erweiterung für die Zertifikat Sperr Listen-Verteilungs Punkte enthält den URI der Basiszertifikat Sperr Liste (CRL).

**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ CRL- \_ dist- \_ Punkte (2.5.29.31)

## <a name="enhancedkeyusage"></a>Felds EnhancedKeyUsage

Die erweiterte Schlüssel Verwendungs Erweiterung kann verwendet werden, um eine oder mehrere Verwendungen des im Zertifikat enthaltenen öffentlichen Schlüssels zu definieren.

**Schnittstelle:** [ **IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)

**OID:** Erweiterte XCN- \_ OID- \_ \_ Schlüssel \_ Verwendung (2.5.29.37)

## <a name="freshestcrl"></a>Freshestcrl

Die neueste CRL-Erweiterung enthält den URI der Delta-CRL. Dieselbe ASN. 1-Syntax wird für diese Erweiterung und die **crldistributionpoints** -Erweiterung verwendet.

**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ Freshest \_ CRL (2.5.29.46)

## <a name="keyusage"></a>Endeinheits Zertifikaten der

Die Schlüssel Verwendungs Erweiterung kann verwendet werden, um Einschränkungen für die Vorgänge zu definieren, die von dem im Zertifikat enthaltenen öffentlichen Schlüssel ausgeführt werden können. Sie können z. b. angeben, dass der öffentliche Schlüssel nur zum Erstellen einer digitalen Signatur verwendet werden soll, eine Zertifikat Sperr Liste signiert oder einen anderen Schlüssel verschlüsselt.

**Schnittstelle:** [ **IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)

**OID:** Verwendung von XCN \_ OID \_ Key \_ (2.5.29.15)

## <a name="msapplicationpolicies"></a>Msapplicationpolicies

Die Microsoft-Anwendungsrichtlinien Erweiterung kann von einer Anwendung verwendet werden, um Zertifikate auf der Grundlage der zulässigen Verwendung zu filtern. Zulässige Verwendungen werden durch OIDs identifiziert. Diese Erweiterung ähnelt der Erweiterung **EnhancedKeyUsage** , aber mit einer strengeren Semantik, die auf die übergeordnete Zertifizierungsstelle angewendet wird. Die Erweiterung ist Microsoft-spezifisch.

**Schnittstelle:** [ **IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)

**OID:** Richtlinien für die XCN- \_ OID- \_ Anwendungs \_ Zertifikat \_ (1.3.6.1.4.1.311.21.10)

## <a name="nameconstraints"></a>Nameconstraints

Die Erweiterung namens Einschränkungen dient zum Identifizieren des Namespace, in dem alle Antragsteller Namen von Zertifikaten in einer Zertifikat Hierarchie gefunden werden müssen. Die Erweiterung wird lediglich in einem Zertifizierungsstellenzertifikat verwendet.

**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** Einschränkungen für den XCN- \_ OID- \_ Namen \_ (2.5.29.30)

## <a name="policyconstraints"></a>Policyeinschränkungen

Die richtlinieneinschränkungs-Erweiterung wird Zertifizierungsstellen Zertifikaten hinzugefügt, um die Pfad Validierung einzuschränken, indem die Richtlinien Zuordnung untersagt wird oder dass jedes Zertifikat in der Hierarchie eine akzeptable Richtlinien Kennung enthält.

**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** Einschränkungen für XCN- \_ OID- \_ Richtlinien \_ (2.5.29.36)

## <a name="policymappings"></a>Policymappings

Die Erweiterung Richtlinien Zuordnungen dient zum Identifizieren der Richtlinien in einer untergeordneten Zertifizierungsstelle, die den Richtlinien in der ausstellenden Zertifizierungsstelle entsprechen. Der Erweiterungs Wert enthält eine Sequenz von Richtlinien Zuordnungen für ausstellende Zertifizierungsstellen und untergeordnete Zertifizierungsstellen, die von Objekt Bezeichnern dargestellt werden

**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** Zuordnungen von XCN- \_ OID- \_ Richtlinien \_ (2.5.29.33)

## <a name="privatekeyusageperiod"></a>Privatekeyusageperiod

Die Erweiterung für den privaten Schlüssel Verwendungs Zeitraum wird verwendet, um eine andere Gültigkeitsdauer für den privaten Schlüssel anzugeben, als für das Zertifikat, dem der Schlüssel zugeordnet ist.

**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** Verwendungs Zeitraum für XCN \_ OID \_ PrivateKey \_ \_ (2.5.29.16)

## <a name="smimecapabilities"></a>SMIME-Funktionen

Die Secure/Multipurpose Internet Mail Extensions (S/MIME)-Funktionserweiterung kann verwendet werden, um die Entschlüsselungs Funktionen eines e-Mail-Empfängers an den Absender der e-Mail-Nachricht zu melden, damit der Absender den sichersten Verschlüsselungsalgorithmus auswählen kann, der von beiden Parteien unterstützt wird. Der Erweiterungs Wert enthält eine Sammlung von symmetrischen Verschlüsselungsalgorithmus-OIDs und eine optionale Verschlüsselungsstärke.

**Schnittstelle:** [ **IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)

**OID:** XCN \_ OID \_ RSA \_ SMIME-Funktionen (1.2.840.113549.1.9.15)

## <a name="subjectdirectoryattributes"></a>Subjetdirectoriyattribute

Die Erweiterung "Subject Directory-Attribute" kann verwendet werden, um Identifikations Attribute wie die Nationalität des Zertifikat Antragstellers zu übermitteln. Der Erweiterungswert ist eine Folge von OID-Wertepaaren.

**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ Subject \_ dir \_ attrs (2.5.29.9)

## <a name="subjectkeyidentifier"></a>SubjectKeyIdentifier

Mithilfe der Erweiterung "Subject Key Identifier" können Sie zwischen mehreren öffentlichen Schlüsseln unterscheiden, die vom Zertifikat Antragsteller aufbewahrt werden. Der Erweiterungswert ist normalerweise ein SHA-1-Hash des Schlüssels.

**Schnittstelle:** [ **IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)

**OID:** Schlüssel Bezeichner für den XCN- \_ OID- \_ Betreff \_ \_ (2.5.29.14)

## <a name="template"></a>Vorlage

Mithilfe der Vorlagen Erweiterung kann die Vorlage Version 2 identifiziert werden, die beim ausstellen oder Erneuern eines Zertifikats verwendet werden soll. Der Erweiterungs Wert enthält die Vorlagen-OID und optionale Versionsinformationen. Die Erweiterung ist Microsoft-spezifisch.

**Schnittstelle:** [ **IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)

**OID:** XCN \_ OID- \_ Zertifikat \_ Vorlage (1.3.6.1.4.1.311.21.7)

## <a name="templatename"></a>TemplateName

Mithilfe der Vorlagen Namen Erweiterung kann die Vorlage Version 1 identifiziert werden, die beim ausstellen oder Erneuern eines Zertifikats verwendet werden soll. Der Erweiterungs Wert enthält den Namen der Vorlage. Die Erweiterung ist Microsoft-spezifisch.

**Schnittstelle:** [ **IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)

**OID:** XCN \_ OID \_ ENROLL \_ certtype- \_ Erweiterung (1.3.6.1.4.1.311.20.2)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Extensions (Erweiterungen)](extensions.md)
</dt> </dl>

 

 



