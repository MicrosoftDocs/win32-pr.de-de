---
description: Die folgenden Schnittstellen können zum Erstellen von Zertifikaterweiterungen verwendet werden.
ms.assetid: 52750a0a-0cd9-40cc-8c23-839e4e20fd77
title: Schnittstellen für Zertifikaterweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d254a413331e1f8bc1da630911258d8e327f000d10003c11b784856cd88e84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902731"
---
# <a name="certificate-extension-interfaces"></a>Schnittstellen für Zertifikaterweiterungen

Die folgenden Schnittstellen können zum Erstellen von Zertifikaterweiterungen verwendet werden.



| Schnittstelle                                                                            | BESCHREIBUNG                                                                                                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename)                                         | Stellt eine Instanz einer **AlternativeNames-Erweiterung** dar.                                                                                   |
| [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames)                                       | Verwaltet eine Auflistung von [**IAlternativeName-Objekten.**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename)                                                                  |
| [**Icertificatepolicy**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy)                                     | Gibt eine Zertifikatrichtlinie an, die den Zweck angibt, für den das Zertifikat verwendet werden kann.                                              |
| [**ICertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicies)                                 | Verwaltet eine Auflistung von [**ICertificatePolicy-Objekten.**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy)                                                              |
| [**IPolicyQualifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier)                                         | Stellt einen Qualifizierer dar, der einer Zertifikatrichtlinie zugeordnet werden kann.                                                                       |
| [**IPolicyQualifiers**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifiers)                                       | Verwaltet eine Auflistung von [**IPolicyQualifier-Objekten.**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier)                                                                  |
| [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)                                             | Definiert eine Erweiterung für eine Zertifikatanforderung.                                                                                                |
| [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)             | Gibt ein oder mehrere alternative Namensformulare für den Subjekt eines Zertifikats an.                                                                 |
| [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier) | Stellt eine **AuthorityKeyIdentifier-Erweiterung** dar.                                                                                            |
| [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)             | Gibt an, ob der Zertifikatssubjekt eine Zertifizierungsstelle und, falls ja, die Tiefe der Kette der untergeordneten Zertifizierungsstellen ist. |
| [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)       | Stellt eine Auflistung von Richtlinieninformationsbegriffen dar.                                                                                           |
| [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)   | Stellt eine Auflistung von Objektbezeichnern dar, die angeben, wie ein Zertifikat von einer Anwendung verwendet werden kann.                                   |
| [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)             | Stellt eine Auflistung von Objektbezeichnern dar, die die beabsichtigte Verwendung des in einem Zertifikat enthaltenen öffentlichen Schlüssels identifizieren.                    |
| [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)                             | Stellt Einschränkungen für die Vorgänge dar, die mit dem im Zertifikat enthaltenen öffentlichen Schlüssel ausgeführt werden können.                                |
| [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)                                           | Verwaltet eine Auflistung von [**IX509Extension-Objekten.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)                                                                      |
| [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)           | Stellt eine Auflistung dar, die die Entschlüsselungsfunktionen eines E-Mail-Empfängers an einen E-Mail-Absender meldet.                                     |
| [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)     | Stellt eine **SubjectKeyIdentifier-Erweiterung** dar, die zum Identifizieren eines Signaturzertifikats verwendet wird.                                                        |
| [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)                             | Stellt eine **CertificateTemplate-Erweiterung** dar, die eine Vorlage der Version 2 enthält.                                                             |
| [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)                     | Stellt eine **CertificateTemplateName-Erweiterung** dar, die eine Vorlage der Version 1 enthält.                                                         |
| [**ISmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapabilities)                                     | Verwaltet eine Auflistung von [**ISmimeCapability-Objekten.**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability)                                                                  |
| [**ISmimeCapability**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability)                                         | Stellt eine **SMIMECapabilities-Erweiterung** dar, die die Entschlüsselungsfunktionen eines E-Mail-Empfängers identifiziert.                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CertEnroll-Schnittstellen](certenroll-interfaces.md)
</dt> </dl>

 

 



