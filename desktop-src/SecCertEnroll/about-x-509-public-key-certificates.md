---
description: Die Kryptografie mit öffentlichem Schlüssel basiert auf einem Paar aus öffentlichem und privatem Schlüssel zum Verschlüsseln und Entschlüsseln von Inhalt.
ms.assetid: a85ec2bc-a413-41a6-b3d2-5fa81a9e7bb6
title: X. 509-Zertifikate für öffentliche Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acd602e9b47cb7825f6d75df0fb74399b914db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565760"
---
# <a name="x509-public-key-certificates"></a>X. 509-Zertifikate für öffentliche Schlüssel

Die Kryptografie mit öffentlichem Schlüssel basiert auf einem Paar aus öffentlichem und privatem Schlüssel zum Verschlüsseln und Entschlüsseln von Inhalt. Die Schlüssel sind mathematisch miteinander verknüpft, und Inhalte, die mit einem der Schlüssel verschlüsselt wurden, können nur mit dem anderen entschlüsselt werden. Der private Schlüssel wird geheim gehalten. Der öffentliche Schlüssel ist in der Regel in ein binäres Zertifikat eingebettet, und das Zertifikat wird in einer Datenbank veröffentlicht, die von allen autorisierten Benutzern erreicht werden kann.

Der X. 509-PKI-Standard (Public Key Infrastructure) identifiziert die Anforderungen für robuste Zertifikate für öffentliche Schlüssel. Ein Zertifikat ist eine signierte Datenstruktur, die einen öffentlichen Schlüssel an eine Person, einen Computer oder eine Organisation bindet. Zertifikate werden von [*Zertifizierungs*](/windows/desktop/SecGloss/c-gly) stellen (CAS) ausgestellt. Alle Personen, die die Kommunikation mit einem öffentlichen Schlüssel unterstützen, verlassen sich auf die Zertifizierungsstelle, um die Identitäten der Personen, Systeme oder Entitäten, für die Zertifikate ausgestellt werden, adäquat zu überprüfen. Die Ebene der Überprüfung hängt in der Regel von der Sicherheitsstufe ab, die für die Transaktion erforderlich ist. Wenn die Zertifizierungsstelle die Identität des Anforderers entsprechend überprüfen kann, wird das Zertifikat signiert (verschlüsselt), codiert und ausgestellt.

Ein Zertifikat ist eine signierte Datenstruktur, die einen öffentlichen Schlüssel an eine Entität bindet. Die Syntax für die [*abstrakte Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN. 1) für das [*X. 509*](/windows/desktop/SecGloss/x-gly) -Zertifikat der Version 3 wird im folgenden Beispiel gezeigt.

``` syntax
-- X.509 signed certificate 

SignedContent ::= SEQUENCE 
{
  certificate         CertificateToBeSigned,
  algorithm           Object Identifier,
  signature           BITSTRING
}
 
-- X.509 certificate to be signed

CertificateToBeSigned ::= SEQUENCE 
{
  version                 [0] CertificateVersion DEFAULT v1,
  serialNumber            CertificateSerialNumber,
  signature               AlgorithmIdentifier,
  issuer                  Name
  validity                Validity,
  subject                 Name
  subjectPublicKeyInfo    SubjectPublicKeyInfo,
  issuerUniqueIdentifier  [1] IMPLICIT UniqueIdentifier OPTIONAL,
  subjectUniqueIdentifier [2] IMPLICIT UniqueIdentifier OPTIONAL,
  extensions              [3] Extensions OPTIONAL
}
```

Seit seiner Einführung in 1998 haben sich drei Versionen des öffentlichen X. 509-Zertifikat Standards entwickelt. Wie in der folgenden Abbildung dargestellt, hat jede aufeinander folgende Version der Datenstruktur die Felder, die in den vorherigen Versionen vorhanden waren, aufbewahrt und weitere hinzugefügt.

![x. 509-Zertifikate, Versionen 1, 2 und 3](images/x509certificateversions.png)

In den folgenden Themen werden die verfügbaren Felder ausführlicher erläutert:

-   [Grundlegende Felder](about-basic-fields.md)
-   [Felder der Version 2](about-version-2-fields.md)
-   [Erweiterungen der Version 3](about-version-3-extensions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Public Key-Infrastruktur](public-key-infrastructure.md)
</dt> </dl>

 

 
