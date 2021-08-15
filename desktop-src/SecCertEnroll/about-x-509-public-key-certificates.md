---
description: Die Kryptografie mit öffentlichem Schlüssel basiert auf einem öffentlichen und einem privaten Schlüsselpaar, um Inhalte zu verschlüsseln und zu entschlüsseln.
ms.assetid: a85ec2bc-a413-41a6-b3d2-5fa81a9e7bb6
title: X.509-Zertifikate mit öffentlichem Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1eb40e57114f4509884df3a5ac36e7ae8ea0486817ff300d58f4273d51c123
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903252"
---
# <a name="x509-public-key-certificates"></a>X.509-Zertifikate mit öffentlichem Schlüssel

Die Kryptografie mit öffentlichem Schlüssel basiert auf einem öffentlichen und einem privaten Schlüsselpaar, um Inhalte zu verschlüsseln und zu entschlüsseln. Die Schlüssel sind mathematisch verknüpft, und Inhalte, die mit einem der Schlüssel verschlüsselt werden, können nur mithilfe des anderen entschlüsselt werden. Der private Schlüssel wird geheim gehalten. Der öffentliche Schlüssel ist in der Regel in ein binäres Zertifikat eingebettet, und das Zertifikat wird in einer Datenbank veröffentlicht, die von allen autorisierten Benutzern erreicht werden kann.

Der PKI-Standard (Public Key Infrastructure) von X.509 identifiziert die Anforderungen für stabile Zertifikate mit öffentlichen Schlüsseln. Ein Zertifikat ist eine signierte Datenstruktur, die einen öffentlichen Schlüssel an eine Person, einen Computer oder eine Organisation bindet. Zertifikate werden von Zertifizierungsstellen (Certification [*Authorities,*](/windows/desktop/SecGloss/c-gly) CAs) ausgestellt. Alle Personen, die an einer sicheren Kommunikation beteiligt sind, die einen öffentlichen Schlüssel verwendet, verlassen sich darauf, dass die Zertifizierungsstelle die Identitäten der Personen, Systeme oder Entitäten, denen sie Zertifikate ausstellt, angemessen überprüft. Die Überprüfungsebene hängt in der Regel von der Sicherheitsstufe ab, die für die Transaktion erforderlich ist. Wenn die Zertifizierungsstelle die Identität des Anfordernden entsprechend überprüfen kann, wird das Zertifikat signiert (verschlüsselt), codiert und ausgestellt.

Ein Zertifikat ist eine signierte Datenstruktur, die einen öffentlichen Schlüssel an eine Entität bindet. Die [*Syntax Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) für das [*X.509-Zertifikat*](/windows/desktop/SecGloss/x-gly) der Version 3 wird im folgenden Beispiel gezeigt.

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

Seit der Einführung im Jahr 1998 haben sich drei Versionen des Zertifikatstandards für öffentliche X.509-Schlüssel weiterentwickelt. Wie in der folgenden Abbildung dargestellt, hat jede aufeinanderfolgende Version der Datenstruktur die Felder beibehalten, die in den vorherigen Versionen vorhanden waren, und weitere hinzugefügt.

![x.509-Zertifikate, Versionen 1, 2 und 3](images/x509certificateversions.png)

In den folgenden Themen werden die verfügbaren Felder ausführlicher erläutert:

-   [Grundlegende Felder](about-basic-fields.md)
-   [Felder der Version 2](about-version-2-fields.md)
-   [Erweiterungen der Version 3](about-version-3-extensions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Public Key-Infrastruktur](public-key-infrastructure.md)
</dt> </dl>

 

 
