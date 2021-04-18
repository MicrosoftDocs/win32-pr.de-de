---
description: Die folgenden Schnittstellen können zum Erstellen von Zertifikat Erweiterungen verwendet werden.
ms.assetid: 52750a0a-0cd9-40cc-8c23-839e4e20fd77
title: Zertifikat Erweiterungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c192ff7bc661c36ded8611628a1cd82dddca1697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526333"
---
# <a name="certificate-extension-interfaces"></a>Zertifikat Erweiterungs Schnittstellen

Die folgenden Schnittstellen können zum Erstellen von Zertifikat Erweiterungen verwendet werden.



| Schnittstelle                                                                            | BESCHREIBUNG                                                                                                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ialternativename**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename)                                         | Stellt eine Instanz einer **alternativenames** -Erweiterung dar.                                                                                   |
| [**Ialternativenames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames)                                       | Verwaltet eine Auflistung von [**ialternativename**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) -Objekten.                                                                  |
| [**ICertificatePolicy**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy)                                     | Gibt eine Zertifikat Richtlinie an, die den Zweck identifiziert, für den das Zertifikat verwendet werden kann.                                              |
| [**Icertificatepolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicies)                                 | Verwaltet eine Auflistung von [**ICertificatePolicy**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy) -Objekten.                                                              |
| [**Ipolicyqualifizierer**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier)                                         | Stellt einen Qualifizierer dar, der einer Zertifikat Richtlinie zugeordnet werden kann.                                                                       |
| [**Ipolicyqualifizierer**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifiers)                                       | Verwaltet eine Auflistung von [**ipolicyqualifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier) -Objekten.                                                                  |
| [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)                                             | Definiert eine Erweiterung für eine Zertifikat Anforderung.                                                                                                |
| [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)             | Gibt mindestens ein alternatives namens Formular für den Betreff eines Zertifikats an.                                                                 |
| [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier) | Stellt eine **autoritykeyidentifier** -Erweiterung dar.                                                                                            |
| [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)             | Gibt an, ob der Zertifikat Antragsteller eine Zertifizierungsstelle ist, und wenn dies der Fall ist, die Tiefe der untergeordneten Zertifizierungsstellen Kette. |
| [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)       | Stellt eine Sammlung von Richtlinien Informations Begriffen dar.                                                                                           |
| [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)   | Stellt eine Auflistung von Objekt bezeichatoren dar, die angeben, wie ein Zertifikat von einer Anwendung verwendet werden kann.                                   |
| [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)             | Stellt eine Auflistung von Objekt Bezeichnerobjekten dar, die die beabsichtigte Verwendung des in einem Zertifikat enthaltenen öffentlichen Schlüssels identifizieren.                    |
| [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)                             | Stellt Einschränkungen für die Vorgänge dar, die von dem im Zertifikat enthaltenen öffentlichen Schlüssel ausgeführt werden können.                                |
| [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)                                           | Verwaltet eine Auflistung von [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) -Objekten.                                                                      |
| [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)           | Stellt eine Auflistung dar, die die Entschlüsselungs Funktionen eines e-Mail Empfängers an einen e-Mail-Absender meldet.                                     |
| [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)     | Stellt eine " **subjetkeyidentifier** "-Erweiterung dar, mit der ein Signaturzertifikat identifiziert wird.                                                        |
| [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)                             | Stellt eine **certificatetemplate** -Erweiterung dar, die eine Vorlage der Version 2 enthält.                                                             |
| [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)                     | Stellt eine **certificatetemplatename** -Erweiterung dar, die eine Vorlage der Version 1 enthält.                                                         |
| [**Ismime-Funktionen**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapabilities)                                     | Verwaltet eine Auflistung von [**ismimecapability**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability) -Objekten.                                                                  |
| [**Ismimecapability**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability)                                         | Stellt eine **SMIME-** Funktionserweiterung dar, die die Entschlüsselungs Funktionen eines e-Mail-Empfängers angibt.                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CertEnroll-Schnittstellen](certenroll-interfaces.md)
</dt> </dl>

 

 



